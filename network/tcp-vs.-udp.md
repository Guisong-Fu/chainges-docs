# TCP vs. UDP

简单说，TCP通过三次握手建立连接（session），并且通过发送序号确保接收端接受到了完整的数据包。但UDP不需建立连接，一直发送数据包就可以，可能丢包，数据包到达顺序也可能不一样

{% embed url="https://www.youtube.com/watch?v=uwoD5YsGACg&ab\_channel=PowerCertAnimatedVideos" %}

{% embed url="https://www.youtube.com/watch?v=Vdc8TCESIg8&ab\_channel=PieterExplainsTech" %}

![](../.gitbook/assets/image%20%2848%29.png)

![](../.gitbook/assets/image%20%2853%29.png)

UDP -&gt; Fire and Forget Protocol

因为UDP不用建立连接等等，所以UDP is faster than TCP

![](../.gitbook/assets/image%20%2855%29.png)

![](../.gitbook/assets/image%20%2854%29.png)

 

![](../.gitbook/assets/image%20%2851%29.png)

![](../.gitbook/assets/image%20%2842%29.png)

![](../.gitbook/assets/image%20%2845%29.png)

![](../.gitbook/assets/image%20%2840%29.png)

![](../.gitbook/assets/image%20%2847%29.png)

当需要确保信息完整的时候，要用TCP，比如发信息啊，下载文件等等。但当需要更快的速度的时候，可以用UDP，比如在线看电影（本机会做一部分的cache，排序等等），网络电话等等







