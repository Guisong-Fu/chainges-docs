# Uniswap & Sushiswap

{% embed url="https://uniswap.org/" %}

{% embed url="https://sushiswap.fi/" %}

{% embed url="https://zhuanlan.zhihu.com/p/226085593" %}



{% embed url="https://www.mycryptopedia.com/what-is-uniswap-a-detailed-beginners-guide/" %}

中文译版：

{% embed url="https://zhuanlan.zhihu.com/p/158422988" %}

> Sushiswap协议是今年8月底才从Uniswap分叉而来，它基本延续Uniswap的核心设计，没有构建全新的模式，同样也是采用兑换池+自动做市商（AMM）的模式。另外，Sushiswap的代币池和前端页面设计与Uniswap也基本相同。

## 我的理解：

代币交易平台（交易所）有中心化的账簿式的，比如火币，币安这种。”账簿式“的意思是，买卖双方标出各自目标标的的价钱，然后互相交易，就像现在的股票交易所一样（富途，Avanza这些）。Uniswap代表的是另一种”去中心化“”自动化“的交易平台，自动计算”汇率“。

{% hint style="info" %}
DEX: Decentralized Exchange 分布式交易所

AMM: Automated Market Maker 自动化做市商

LP： Liquidity Provider 流动性提供者
{% endhint %}

tokenA 池 \* tokenB 池 = 恒定乘积值  
可以用一个例子简单解释Uniswap是如何运行的：

> Bob想要发起交易来用自己的1个ETH兑换成ERC20代币BAT，Bob将使用 Uniswap上已经存在的BAT交易合约来实现此兑换操作。此时，流动性提供者已经将一定量的ETH和BAT存在了交易合约中。我们这里举例，流动性提供者一共存了10ETH和500BAT。因此，基础的恒定乘积值为：
>
> ETH 池 \* BAT 池 = 恒定乘积值
>
> ETH 池 = 10
>
> BAT 池 = 500
>
> 恒定乘积值 = 500 \* 10 = 5000
>
> Bob将通过向交易合约的ETH池发送1ETH来启动这笔交易，此时，交易金额的0.3%也就是0.003ETH将被扣除作为给流动性提供者的报酬。剩余的0.997ETH则被添加到了ETH池里面。然后，恒定乘积值除ETH池中新的ETH数量，来得到BAT池中应该有的数量。那么多出来的BAT，就可以分给Bob了。具体如下：
>
> Bob发送了 1 ETH
>
> 费用 = 0.003 ETH
>
> ETH 池 = 10 + \(1 – 0.003\) = 10.997
>
> BAT 池 = 5000/10.997 = 454.67
>
> Bob 将兑换得到 : 500 – 454.67 = 45.33 BAT

![](../.gitbook/assets/image%20%283%29.png)

当”滑点“向一方移动太多的话，就会有人发现有利可图，然后朝着相反的方向买入。Uniswap通过这种方式将”汇率“维持在一个市场认可的位置。

> ### Uniswap的经济激励机制
>
> Uniswap给流动性提供者的奖励就是交易所的手续费。流动性提供者可以得到所在流动性池中代币交易的手续费作为奖励，手续费率为0.3%，流动性提供者之间依据存入资金的份额按比例分配。
>
> 根据上文截图中的数据计算，一天的成交额是40.85亿CNY，一天的手续费就有122万元，经过一段时间的积累，流动性提供者（LP）得到的手续费奖励金额就非常可观了。Uniswap会根据流动性提供者存入资金的数额发给他们一定数量的LP token，我们可以理解为存款奖状或者收据，它是LP获得交易所手续费奖励的凭证。
>
> 注意：LP token不是Uniswap的项目代币或者说平台币，对于每一种代币交易对有不同的LP token。
>
> 举个例子具体说明：假设这个交易对是ETH--DAI，目前兑换比例是1ETH--400DAI。我向资金池充了1ETH和400DAI，这个资金池发给我1个LP token，代表我有1份（ETH--DAI）的流动性贡献。这个资金池所产生的手续费进入一个pool，经过一段时间后，pool中共有积累的手续费A个ETH和B个DAI，当我把我的1个LP token交还给Uniswap时，我有权利从pool拿走它按比例对应的手续费。假设此时整个资金池共发出了X个LP token，我的流动性贡献占比就是1/X，我就可以获得A/X个ETH和B/X个DAI，然后再赎回我的1ETH和400DAI。
>
> Uniswap通过AMM模式和为流动性提供者奖励手续费的模式，极大地调动了LP的积极性。由于任何人都可以提供流动性并且从中获利，人们有动力为Uniswap提供流动性；交易所获得充足的交易流动性，交易滑点就小，用户体验也好。交易所的运行完全基于市场的需求进行。人工的运维成本大幅降低。

 简单说，Uniswap的良好运行需要token池里的token量越多越好（以此保证滑点不会大幅度偏差）。而Uniswap收的手续费就是给这些流动性提供者LP的激励措施。  
所以，当交易量越多，LP的收益就越好。LP如果不取出的话，会自动放到token池里继续跑。良性循环。



> ### Sushiswap的经济激励机制
>
> Sushiswap在Uniswap的激励机制基础上做出了一些改变，这是它们二者最大的区别。Sushiswap增加了代币经济激励，也就是将其交易费用的一部分分配给Sushiswap代币SUSHI的持有人。
>
> Uniswap没有发行平台币，它每笔交易收0.3%的手续费，再通过LP token的形式把交易费按比例分配给LP（流动性提供者）。
>
> Sushiswap发行了平台币SUSHI，它的交易手续费也是0.3%。它将这0.3%的手续费分成2个部分，其中0.25%提供给LP，方法和Uniswap一样；剩下的0.05%将用于回购SUSHI代币，即用这部分钱购买SUSHI代币持有者手里的SUSHI代币。这意味着，SUSHI的价值与Sushiswap平台交易量是挂钩的。在Sushiswap上，交易量越大，SUSHI捕获的价值就越高。SUSHI代币和COMP、LEND、YFI一样，也可以在二级市场交易。此外，为了保证研发和运营的持续，有10%SUSHI代币会用于开发和未来的迭代、审计等。
>
> Sushiswap的经济激励机制在Uniswap的基础上做了改进，它保证了早期参与者的长期利益。
>
> Sushiswap每个区块将释放100枚SUSHI代币，会均分给所有支持的代币池，LP们还是根据流动性贡献来按比例获得SUSHI。和Uniswap用LP token的形式来分配手续费不同，LP token只有在存入代币对时才发给用户，而SUSHI是每个区块都产生一次，根据用户现在的资金比例分配。这样即使未来有大资金进入Sushiswap，早期参与者的资金份额被摊薄，但是他们之前已经获得的SUSHI代币不会减少，这就相当于是挖到了“头矿”。更何况在最初的100,000个区块，SUSHI产量更高，每个区块释放1,000枚SUSHI。在Sushiswap交易额增长起来后，SUSHI代币的价格也水涨船高，早期参与者凭借着早期相对较高资金份额占比而积累下的SUSHI代币可以享受到Sushiswap长期发展带来的福利。此外，前文提及，Uniswap的LP在赎回了当初存入的代币对之后，就不能再获得交易所的手续费分成了，而Sushiswap的LP即使赎回了资金，也还能够凭借着持有的SUSHI代币获得币价上涨带来的利益。

简单说，Sushiswap也有LP，LP除了能拿到和Uniswap一样的交易费奖励之外，还能获得一些SUSHI代币。并且Sushiswap会用一部分的交易费回购SUSHI。相当于参与Sushiswap的LP有两类收入。（感觉有点像股票分红~） 并且SUSHI还能放到二级市场进行交易。

