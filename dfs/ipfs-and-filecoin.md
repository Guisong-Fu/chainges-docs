# IPFS & FileCoin

## What is the connection between IPFS and Filecoin?

[https://docs.ipfs.io/concepts/faq/\#contributing-to-ipfs](https://docs.ipfs.io/concepts/faq/#contributing-to-ipfs)

Filecoin and IPFS are two separate, complementary protocols, both created by Protocol Labs. IPFS allows peers to store, request, and transfer verifiable data with each other, while Filecoin is designed to provide a system of persistent data storage. Under Filecoin's incentive structure, clients pay to store data at specific levels of redundancy and availability, and miners earn payments and rewards by continuously storing data and cryptographically proving it.

In short: IPFS addresses and moves content, while Filecoin is an incentive layer to persist data.

These components are separable - **you can use one without the other**, and IPFS already supports more self-organized or altruistic forms of data persistence via tools like [IPFS Cluster \(opens new window\)](https://cluster.ipfs.io/). Compatibility between IPFS and Filecoin is intended to be as seamless as possible, but we expect it to evolve over time. You can view the [draft spec for IPFS-Filecoin Interoperability \(opens new window\)](https://github.com/filecoin-project/specs/issues/143)and [ideas for future improvements \(opens new window\)](https://github.com/filecoin-project/specs/issues/144)to learn more.



## 我的理解：

IPFS和FileCoin可以单独使用。

单独用IPFS的话，自己本机就相当于一个host，自己发布文件到自己的这个host上面，别人也可以通过hash 下载你的文件，但如果你的ipfs不运行了，或者你把这个文件从本机上删掉了，并且这个文件并没有被别人下载的话，这个文件就相当于“丢失了”。所有要是想让文件更加persistant的话，可以设置ipfs cluster。也可以支付一笔费用也就是filecoin，请别人（filecoin矿工）存储这个数据，并且将来fetch这个数据的时候也要收费。

也可以单独用FileCoin，也就是filecoin矿工，存储别人愿意付费存储数据，给别人付费提供数据。FileCoin存储数据的费用是通过和买家协商来的。另外比如说将来有一个“爆款文件”，很多人都想付费下载，其他矿工也可以下载这个文件到自己的矿机里面，自己挣了钱，也同时提供了其他人对这个文件的下载速度。

{% embed url="https://github.com/filecoin-project/specs/issues/1191" %}

The upper post explains many things. Read it thoroughly!

> IPFS is \(at this point\) detached from Filecoin.

> > Is it possible to use filecoin to make sure a file persists on IPFS
>
> Nope, if you use Filecoin, then the file will persist on the Filecoin network, not the IPFS network. At this point, these are two different networks.



