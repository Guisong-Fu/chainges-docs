---
description: Open Systems Interconnection Model
---

# OSI Model

![](../.gitbook/assets/image%20%2844%29.png)

![](../.gitbook/assets/image%20%2843%29.png)

![](../.gitbook/assets/image%20%2846%29.png)

我们重点关注其中的5层：

![](../.gitbook/assets/image%20%2850%29.png)

为什么需要这么多层？

网线传输的是一段由0和1组成的电信号，它如何知道这段信号是有效信号而不是噪声，如果是有效信号，它如何确认这段信号应该发给这台主机还是由这台主机转发给其他主机，并且是该由这台主机上的哪个服务来处理呢，是SSH，还是web服务呢，还有，如何确认这段信号是没有丢失，完整无缺的呢，又如何确认这段信号是json的字符串还是gRPC的二进制字节流呢。等确认了这么信息之后，最后还是真正的商务逻辑的事情。所以我们需要这么多层的协议去处理上面这些问题。

举例：物理层来保障这段0-1信号是有效信号，不是噪声；当信号到达链路层的时候，链路层来确认这段信号是发给当前主机的当前网卡的，也就是说当到达链路层的时候，主机知道自己是可以接收并处理这段信号的；当信号来到网络层的时候，通过网络层的协议来确认这段信号是由本机进行处理还是应该进行路由转发，也就说当信号到达传输层的时候，本机就已经可以确认这段信号是发给本机的，并且可以由本级上的某个服务进行处理；当信号来到传输层，通过传输层的协议就可以确认处理这段信号的服务是谁，并且能进行一些其他操作，比如通过TCP可以确认信号是否完整，比如它拿到的是http请求的一个网络包，那TCP协议可以拿到所有的这一个请求的网络包并把信号复原之后交给应用层进行处理。

![](../.gitbook/assets/image%20%2852%29.png)

所以每一层都有特殊的header的












