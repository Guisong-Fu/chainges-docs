# Cadence Study

> Questions: How to implement "function" in Cadence? By function, I mean, like random number and etc.

What should be in "init" in contract?

Transaction: what is AuthAccount? → Is this like "authenticating the current account"?

And what should be in "Prepare" in Transaction?

> Transactions are divided into two main phases, prepare and execute. The prepare phase is the only place that has access to the signing accounts' private AuthAccount object. AuthAccount has special methods that allow saving to and loading from /storage/, and creating /private/ and /public/ links to the objects in /storage/. \(called capabilities, will be covered later\) The execute phase does not have access to AuthAccount and thus can only modify the objects that were removed in the prepare phase and call functions on external contracts and objects.
>
> Transactions have access to the /storage/ and /private/ domains of the accounts that signed the transaction and can read and write to those domains, as well as read and call functions in public contracts and the public domains in other users\` accounts.
>
> The prepare phase is the only place that has access to the signing accounts' private AuthAccount object. AuthAccount has special methods that allow saving to and loading from /storage/, and creating /private/ and /public/ links to the objects in /storage/. \(called capabilities, will be covered later\)

```swift
let helloResouce <- acct.load<@HelloWorld.HelloAsset>(from: /storage/hello)

    log(helloResouce?.hello())

    acct.save(<-helloResouce, to: /storage/hello)
```

The above code can only run ONCE?

I thought, it could always run. Because I thought, it's like "take out hello from /storage/hello and put it "back"", but next time, when I run it, there will be an error:

→ Puzzle solved, I shall call ←helloResource! → there is an exclamation point

**Error**

failed to save object: path /storage/hello in account 0x1 already stores an object

Q: so I cannot use the same "path" twice?

Q: and I always have to "save" it somewhere? i cannot just read it? → I guess it's because I was using load? Maybe it will work if I use "borrow" ?

Q: and if I use the other accounts, it also works? But it returns "nil" ? I thought it will fail and throw "no access" error?

> I think the Storage is the biggest thing. I have to understand this better! !!! And the path name\(domain\) matters ??!!

Q: Can I add Transaction to Contract? For example, this linkage things

Q: so inside a resource, something also has to be inited?

```swift
pub resource Vault: Provider, Receiver {

    // Balance of a user's Vault
    // we use unsigned integers for balances because they do not require the
    // concept of a negative number
    pub var balance: UFix64

    init(balance: UFix64) {
        self.balance = balance
    }

    pub fun withdraw(amount: UFix64): @Vault {
        self.balance = self.balance - amount
        return <-create Vault(balance: amount)
    }

    pub fun deposit(from: @Vault) {
        self.balance = self.balance + from.balance
        destroy from
    }
}
```

Q: forgot, what is the point of having **interfaces** in Contract?

Q: what's the point of having these interfaces? For example, if I remove balance interface, nothing seems to be changed?

Q: so you cannot call "Resource" from the contracts that are in the others account? You can only call functions? → I mean, like, I cannot use another account to call "Vault/Mint Resource" in another account?

Q: Another question. What if Account2 deploys the same contract as Account1? Then would the token minted by Account2 be different from Account1? Or, I mean, generally, how are different tokens distinguished between each other?

→ I'll try to explain myself first.

```swift
import FT from 0x03
```

In transactions, we will need to import Contract\(which creates such tokens\) from a certain account, so even if there is another account that has deployed the exact same contract, with exact same name, they will not be the same.

Q: there is another question. so in Flow, only one account or several accounts who has access to that resource\(/private/Mint something\) can mint new tokens, does it mean that Flow cannot work like ethereum where everyone is free to join and mint tokens as they wish by using PoW or something? And how to mint other tokens on etherum other than ETH? → I guess this is more like a consensus question, right? Probably I can find the answer from Flow WhitePaper?

Q: link,borrow,load, what's the difference, and what is the usage?

Q: double check again, in transaction, only in Prepare phase where we have access to the storage.

Q: note, one needs getCapability, while the other does not need.

```swift
self.minterRef = acct.borrow<&FT.VaultMinter>(from: /storage/MainMinter) ?? panic("Cannot do Minter")
self.receiverRef = getAccount(0x02).getCapability(/public/MainReceiver).borrow<&FT.Vault>() ?? panic("Cannot do Vault")
```

[Untitled](https://www.notion.so/80c0b4e31ffd4aa5a99fa388456b0365)

