# Source/Destination Port

IP地址能够确认和哪个主机进行交流，Port（destination port）能决定主机上的哪个服务进行处理，是web还是ssh等等。

但我们也需要源端口号，比如我们的浏览器中有多个页面，有个要访问google，有的要访问youtube，所以每个请求不仅会有destination port，也要有source port，这样当数据返回的时候，我们才能知道该把这个数据包返回给谁。



