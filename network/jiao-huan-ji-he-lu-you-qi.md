---
description: 交换机Switch，路由器Router
---

# 交换机和路由器

## 交换机

{% embed url="https://www.youtube.com/watch?v=uP1DK-pJcpI&ab\_channel=Jing%E7%BB%B4" %}

![](../.gitbook/assets/image%20%2837%29.png)

不用交换机，而用那种多口Hub（比如三通线~）的话，数据是以”广播“形式发送的，比如n点虽然只是想给k点发一个，但这个信息包实际上是发给了所有人，也就是m，k，l都能收到。这就造成了带宽和网卡的浪费。所以这里Switch就可以派上用场。

![](../.gitbook/assets/image%20%2836%29.png)

简单说就是在发送数据的时候，也特意说明目标的MAC地址。比如A想发给C，A就把C的MAC地址也特意附带上。然后等交换机（Switch）收到的时候，就自动”开关“，放行A-&gt;C这条路

![](../.gitbook/assets/image%20%2835%29.png)

加入路由器来看看。上面是”局域网“，下面是”广域网“，这时候A点要是想访问广域网的话，A就可以把数据包的目的地址设为路由器的地址，于是交换机就会把数据发给路由器，然后路由器解析，再发给下一个目的地。

普通的家用”路由器“其实已经包含了路由器和交换机的功能

## 路由器

![](../.gitbook/assets/image%20%2834%29.png)

![](../.gitbook/assets/image%20%2832%29.png)

在这里路由器起到的是网关的作用，指示这个路线从内网走向外网。

> 首先‘网关’一个大概念，不具体特指一类产品，只要连接两个不同的网络的设备都可以叫网关；而‘路由器’么一般特指能够实现路由寻找和转发的特定类产品，路由器很显然能够实现网关的功能。当然电信行业说的‘路由器’又和家用的‘路由器’两个概念，这个暂且不表。默认网关事实上不是一个产品而是一个网络层的概念，PC本身不具备路由寻址能力，所以PC要把所有的IP包发送到一个默认的中转地址上面进行转发，也就是默认网关。这个网关可以在路由器上，可以在三层交换机上，可以在防火墙上，可以在服务器上，所以和物理的设备无关。



