---
description: 'Distributed Ledger Technology vs. Blockchain, 分布式账本对比区块链'
---

# DLT vs. Blockchain

## TL; DR

Blockchain是DLT的一种实现形式。

## R3 的这篇解释我觉得是最简单明了的

{% embed url="https://www.r3.com/blockchain-101/" %}

> DLT is a decentralized database managed by multiple participants, across multiple nodes. 
>
> Blockchain is a type of DLT where transactions are recorded with an immutable cryptographic signature called a hash. The transactions are then grouped in blocks and each new block includes a hash of the previous one, chaining them together, hence why distributed ledgers are often called blockchains.
>
> ### Is Corda a blockchain?
>
> Transactions on Corda are cryptographically linked or chained to the transactions it depends upon. So, by definition, Corda is a blockchain—with one _key_ differentiator.
>
> Corda does _not_ periodically batch up transactions needing confirmation — into a _block —_ and confirm them in one go. Instead, Corda confirms each transaction in real-time. With Corda, there is no need to wait for other transactions to come along or a “block interval”. Transactions are confirmed immediately. This means that your transaction is not dependent on any others, increasing both privacy and scalability.
>
> So, Corda is both a blockchain and not a blockchain.

我的解释：

比特币，以太坊这些的数据结构是一个一个的块（Block），每一个块包含一组交易数据，把这些块”链“起来，就成了区块链。区块链是DLT的一种形式，区块链实现了分布式的账本，分布式的数据库，但分布式账本（DLT）不一定非要用”块“这种形式，比如R3就是real-time的，不需要一波一波（batch）的处理，所以从这个意义上讲，R3不是区块链。但是呢，虽然R3没有一块一块的处理，但R3也把transaction链起来了，所以从这个角度上讲R3也是区块链。

下面还有几篇文章”详细“讲解区块链和分布式账本的区别，但窃以为”废话偏多，大多扯淡“：  
比如，有的post把区块链特指成了公链，把DLT特指成了私链，所以一个是permissionless，一个就是permissioned。有点扯。比如哪怕是比特币我也可以照搬中本聪的代码，在自己的服务器里面跑啊，我加一层权限不就是私链了吗。同样的，我也可以把DLT做成公链。所以他们把这些公链私链，permissionless/permissioned， DLT，Blockchain都混为一谈了。

{% embed url="https://serokell.io/blog/blockchain-vs-dlt" %}

{% embed url="https://cointelegraph.com/news/what-is-the-difference-between-blockchain-and-dlt" %}

{% embed url="https://xueqiu.com/2190319249/132091490" %}

{% embed url="https://www.bitorb.com/zh/campus/dlt-technology-blockchains-vs-dags-vs-tempo/" %}

{% embed url="https://www.bbva.com/en/difference-dlt-blockchain/" %}





