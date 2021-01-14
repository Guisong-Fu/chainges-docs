# BSN提供IPFS专网服务

存储文件，文件上链，发送/共享文件应该是很多应用场景的需求。就我目前的知识和理解，IPFS应该是最适合的解决方案。

但使用IPFS时，我们仍有很多需要考虑的地方。主要是文件的保密需求。

比如：

* 是用public ipfs还是private IPFS? 如果是public的话，文件的保密性如何确保，先加密再上传可以是一个解决方案，但另外一个问题就是如何保证文件一直在哪里，这个确实比如用pinning service来做。如果是用的private话，server的设置，网络设置，维护，成本都需要考虑。
* 目前如果我需要自己搭建IPFS的话，我可能会倾向于搭建一个中心化的private IPFS cluster，然后我的用户可以把数据先加密，再上传到我这里。就相当于我自己搭建了pinning service，不过我可以至少“把我这个cluster”里的文件删掉。

BSN推出了IPFS的专网服务，这个相当值得一试！ 如果BSN完美应用了IPFS，或者解决了大文件存储的问题的话，那BSN提供的确实就是“一站式”服务了。

{% embed url="https://www.chainnews.com/articles/901025418543.htm" %}



