# 边缘计算 Edge Computing

{% embed url="https://www.youtube.com/watch?v=0idvaOCnF9E&ab\_channel=ExplainingComputers" %}

我觉得上面这个讲的是最直观的。

{% embed url="https://www.youtube.com/watch?v=mCDXnls6pQk&ab\_channel=TheLinuxFoundation" %}

{% embed url="https://www.youtube.com/watch?v=DDvMkgEoHxQ&ab\_channel=GoldmanSachs" %}

{% embed url="https://www.youtube.com/watch?v=cEOUeItHDdo&ab\_channel=IBMCloud" %}

## 我对边缘计算的理解：

过去的十几年发展趋势是“云计算”，人们把数据传到云上，然后由云计算处理后返回结果。

随着“能产生数据的设备”数量的激增，2020年已经有500亿部设备能产生数据，而在将来这个数字还会增长的更快。要这么设备都把数据传到云上，然后由云集中处理几乎是不可能的，因为数据量太大，纵使有了5G的加持，现有的带宽也不能承担这么庞大的数据量，所以势必会造成更长的延迟。但比如自动驾驶汽车，要求延迟越低越好。因此也就有了边缘计算，Process data close to where the data is generated 

我的理解，边缘计算某种意义上是“逆云计算”的一种方向。

但边缘计算也有很challenge。比如，如何更好的操控这么庞大数量级的设备，在上面Intel的那个演讲中，提到了他们的解决方案，cotainerize，（还有些别的解决方案，将来可以再仔细看看那个视频）。

另外，比如现在的监控摄像头，现在的监控摄像头不做任何计算，把数据全部传到云上，然后由云计算做比如人脸识别等等，这会有延迟。所以对应的方案可以是，给这个摄像头也增加计算能力，然后云计算生成machine learning model，传给这个摄像头使用，这个摄像头本身就能通过自己的计算进行人脸识别，提高效率。

Intel 推出的那个 Neural Compute Stick挺有意思的，甚至可以插（USB）在Raspberry Pi上面，让Raspberry Pi也能运行Tensorflow， Caffe这些framework。

