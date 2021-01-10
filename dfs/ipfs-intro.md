# IPFS Intro

## IPFS Concepts

{% embed url="https://docs.ipfs.io/concepts/" %}



## IPFS Gateway

An IPFS Gateway acts as a bridge between traditional web browsers and IPFS. Through the gateway, users can browse files and websites stored in IPFS as if they were stored in a traditional web server.

By default, go-ipfs nodes run a gateway at `http://127.0.0.1:8080/`.

We also provide a public gateway at `https://ipfs.io`. If you've ever seen a link in the form `https://ipfs.io/ipfs/Qm...`, that's being served from _our_ gateway.

{% embed url="https://stackoverflow.com/questions/60936369/do-i-need-to-have-a-running-ipfs-node-to-be-able-to-store-and-retrieve-files" %}

> You can use an IPFS [Gateway](https://github.com/ipfs/go-ipfs/blob/master/docs/gateway.md) to access files without running your own node.
>
> When you pin an IPFS file to your own node and shut it down, your files will not be accessible anymore by yourself or others unless another node pins them as well and stays online.
>
> You can pay IPFS file hosters to pin your file on their nodes, [Cloudflare](https://www.cloudflare.com/distributed-web-gateway/) and [Eternum](https://www.eternum.io/) are two of them.
>
> Here is a list of more: [https://www.reddit.com/r/ipfs/comments/9pb5pf/are\_there\_any\_ipfs\_file\_hosting\_services/](https://www.reddit.com/r/ipfs/comments/9pb5pf/are_there_any_ipfs_file_hosting_services/)



## BitSwap:

{% embed url="https://docs.ipfs.io/concepts/bitswap/" %}



## Where can I see IPFS in action today?

[Awesome IPFS \(opens new window\)](https://awesome.ipfs.io/)is a good starting point to see the wide variety of projects that are using IPFS today. If you've got your own awesome IPFS project, please add it to the [Awesome IPFS repo \(opens new window\)](https://github.com/ipfs/awesome-ipfs), so the rest of the world can see it!



## 我目前的理解

命令行 ipfs add 只会把文件通过本机发布到ipfs里面，只有等别人fetch通过这个文件hash fetch文件的时候，这个文件才算duplicate了。

ipfs pin相当于是设置“这个文件不要删”



Check this post:

{% embed url="https://github.com/ipfs/go-ipfs/issues/4083" %}

> Currently Bitswap does not download any content that is not requested by the node operator/user.
>
> If that resolves this issue, please close it.
>
> We are building higher layer solution that might help you [https://github.com/ipfs/ipfs-cluster/](https://github.com/ipfs/ipfs-cluster/)

