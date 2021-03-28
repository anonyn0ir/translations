---
title: ALPHA FINANCE - REKT
date: 2021年2月13日
tags:
  - Alpha Finance
  - Cronje
  - rekt
excerpt: DeFi的黑暗艺术仍然是最赚钱的。在一个虚假的魔术传奇中3750万美元不翼而飞，伴随困惑和指责。受害者单挑袭击者。
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/header-alpha-homora.png
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/header-alpha-homora.png)

**DeFi的黑暗艺术仍然是最赚钱的。**

接下来是我们至今最具戏剧性的故事之一。

**一个虚假的魔术传奇，伴随困惑和指责，导致了迄今为止最大的DeFi黑客入侵。**

在一场复杂的DeFi欺骗中，约有3750万美元被盗，这是因为使用了多笔交易攻击来突袭Alpha Finance的金库，而许多人则认为钢铁银行受到了影响。

这场谋杀案发生在[镜子大厅](https://youtu.be/F-BqDWG72iM)里。DeFi协议越来越相互交织的本质，再加上攻击的复杂性，使社区对于谁是真正的受害者以及谁负责赔偿感到困惑。

攻击者的合约使Homora代码“相信”他们的恶意合约是他们自身的一个合约，以便操纵系统中的内部债务数量。

**这是协议和攻击者之间的一场私下战斗。**被利用的合约尚未公布，也未提供给用户，这意味着他们没有受到直接影响。我们还没有看到如此夸张的内部操作，Alpha Finance很快指出他们有一个“[主要嫌疑犯](https://twitter.com/AlphaFinanceLab/status/1360623172433760256?s=20)”。

如果合约尚未准备好，为什么会上主网？我们问了Alpha Finance，它告诉我们；

> _“我们在合约层面而不是UI层面上线了多个资金池，例如sUSD，因为我们准备在下周推出包括sUSD在内的新资金池。”_

**在混乱中，大型玩家迅速采取行动以保留其资本。**SBF从Cream Finance取出价值[4亿美元](https://twitter.com/_wilbur4ce_/status/1360636958595305474?s=20)的FTT，[三箭资本](https://etherscan.io/address/0x5cfd0cddf989959a6a6c3ad985ce324460d46dfd)向Binance转去超过[300万美元](https://twitter.com/Raez_x/status/1360542616849375233?s=20)的ALPHA，唯一的目的可能是出售。

与攻击相关的所有代币的价值均下降。

Alpha Homora治理代币[ALPHA](https://www.coingecko.com/en/coins/alpha-finance)从2.25美元跌至1.78美元。

钢铁银行治理代币[CREAM](https://www.coingecko.com/en/coins/cream)从288.32美元跌至193.51美元。AAVE(https://www.coingecko.com/en/coins/aave)，是有争议的闪电贷的故乡，它使如此多的此类攻击得以实施，从当天的518美元跌至492美元的低点。

**但是，代币价格不是这个故事中最有趣的部分……**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/linebreak-shanghai2.png)

Alpha Finance团队进行了出色的[事后调查](https://blog.alphafinance.io/alpha-homora-v2-post-mortem/)，他们的发现令人震惊。我们联合调查的结果表明，腐败的深度比预期的要严重得多。

Alpha Finance是否会因其指控而走进公众的视野还有待观察，但他们最初有主要嫌疑人的陈述表明反响正在赶来。

**从官方时候调查报告中可以看出，攻击者必须了解以下信息才能进行攻击：**

· **HomoraBankv2有一个在合约级别的sUSD池，以为即将发布的版本做准备，而既不能通过UI访问和也没有公开宣布。**

· **sUSD借贷池中没有流动性，**因此攻击者可以完全操纵和通胀债务总量和债务总份额。

· **借款函数计算中存在舍入计算错误，**仅在攻击者是唯一借款人时才会造成影响。

· **resolveReserve函数可以在不增加totalDebtShare的情况下增加totalDebt**，这个意在把收入收集到储备池的函数，可以被任何人调用。

· HomoraBankv2接受任何自定义咒语，只要常量检查抵押品>借款（咒语类似于Yearn中的策略）。

在如此众多的用户注视下，劫掠者留下了清晰的线索，而在罕见的反攻行动中，受害者将攻击者挑了出来。

以上要求证明，进行此攻击需要内幕信息。但是，由于所涉及的协议和审计公司范围广泛，内鬼可能来自多个不同的角度。

rekt不再从事指责业务，但我们期待看到Alpha Finance如何处理这种情况。

根据[Alpha Finance报告](https://blog.alphafinance.io/alpha-homora-v2-post-mortem/)：它是这样发生的

1.攻击者创建一个恶意的咒语（相当于Yearn的策略）。[https://etherscan.io/tx/0x2b419173c1f116e94e43afed15a46e3b3a109e118aba166fcca0ba583f686d23](https://etherscan.io/tx/0x2b419173c1f116e94e43afed15a46e3b3a109e118aba166fcca0ba583f686d23)

2.攻击者兑换ETH-> UNI，并将ETH + UNI提供给Uniswap池（获取ETH/UNI LP代币）。在同一笔交易中，在Uniswap上兑换ETH-> sUSD，然后将sUSD存入Cream的钢铁银行（获取cysUSD） [https://etherscan.io/tx/0x4441eefe434fbef9d9b3acb169e35eb7b3958763b74c5617b39034decd4dd3ad](https://etherscan.io/tx/0x4441eefe434fbef9d9b3acb169e35eb7b3958763b74c5617b39034decd4dd3ad)

3.使用恶意咒语(创建883仓位)调用HomoraBank的执行函数，执行：借入1000e18 sUSD将UNI-WETH LP存入WERC20，并用作抵押品（绕过抵押品>借款检验）。在此过程中，攻击者拥有1000e18 sUSD的债务份额（因为攻击者是首位借款人） [httpshttps://etherscan.io/tx/0xcc57ac77dc3953de7832162ea4cd925970e064ead3f6861ee40076aca8e7e571](httpshttps://etherscan.io/tx/0xcc57ac77dc3953de7832162ea4cd925970e064ead3f6861ee40076aca8e7e571)

4. 再次使用恶意咒语调用HomoraBankV2的执行函数（到仓位883），执行：偿还1000000098548938710983sUSD（附带应计利息的实际债务是1000000098548938710984sUSD），导致偿还的份额比总份额少1。结果，攻击者现在拥有1个minisUSD债务和1个债务份额。 [https://etherscan.io/tx/0xf31ee9d9e83db3592601b854fe4f8b872cecd0ea2a3247c475eea8062a20dd41](https://etherscan.io/tx/0xf31ee9d9e83db3592601b854fe4f8b872cecd0ea2a3247c475eea8062a20dd41)
 
5. 调用sUSD上的resolveReserve函数，累积19709787742196债务，而totalShare保持1.当前状态：totalDebt = 19709787742197，而totalShare = 1 [https://etherscan.io/tx/0x98f623af655f1e27e1c04ffe0bc8c9bbdb35d39999913bedfe712d4058c67c0e](https://etherscan.io/tx/0x98f623af655f1e27e1c04ffe0bc8c9bbdb35d39999913bedfe712d4058c67c0e)
 
6. 再次使用恶意咒语调用HomoraBankV2的执行函数，执行（重复16次，每次将借入金额加倍）：借入19709787742196 minisUSD并转给攻击者（每次增加一倍，因为每次借贷成功后totalDebt都会翻倍）。每次借贷都比totalDebt值小1，导致相应的借贷份额= 0，因此协议将其视为没有借贷。在交易结束时，攻击者将19.54sUSD存入Cream的钢铁银行。 [https://etherscan.io/tx/0x2e387620bb31c067efc878346742637d650843210596e770d4e2d601de5409e3](https://etherscan.io/tx/0x2e387620bb31c067efc878346742637d650843210596e770d4e2d601de5409e3)
 
7.继续此过程：再次使用恶意咒语调用HomoraBankV2的执行函数，执行（重复10次，每次借入金额翻倍）。在交易结束时，攻击者将1321sUSD存入Cream的钢铁银行。 [https://etherscan.io/tx/0x64de824a7aa339ff41b1487194ca634a9ce35a32c65f4e78eb3893cc183532a4](https://etherscan.io/tx/0x64de824a7aa339ff41b1487194ca634a9ce35a32c65f4e78eb3893cc183532a4)

8.使用Aave的闪电贷（借入1800000USDC）将1800000USDC兑换成1770757.56254472419047906sUSD，将其质押到Cream来为攻击者使用定制的咒语借款提供足够的流动性。从1322.7sUSD到677223.15sUSD来持续倍增借入的sUSD（共10倍）。在Curve上将135312359SUSD兑换为1374960.72USDC。从Cream借426659.27USDC（因为攻击者已经在步骤b质押sUSD。）[https://etherscan.io/tx/0x7eb2436eedd39c8865fcc1e51ae4a245e89765f4c64a13200c623f676b3912f9](https://etherscan.io/tx/0x7eb2436eedd39c8865fcc1e51ae4a245e89765f4c64a13200c623f676b3912f9)

9. 重复步骤8，但是用大约1千万USDC（最后并没有USDC借款）[https://etherscan.io/tx/0xd7a91172c3fd09acb75a9447189e1178ae70517698f249b84062681f43f0e26e](https://etherscan.io/tx/0xd7a91172c3fd09acb75a9447189e1178ae70517698f249b84062681f43f0e26e)

10. 用1千万USDC重复操作（（最后并没有USDC借款）[https://etherscan.io/tx/0xacec6ddb7db4baa66c0fb6289c25a833d93d2d9eb4fbe9a8d8495e5bfa24ba57](https://etherscan.io/tx/0xacec6ddb7db4baa66c0fb6289c25a833d93d2d9eb4fbe9a8d8495e5bfa24ba57)

11.	借入13244.63 WETH + 360万USDC + 560万USDT + 426万DAI。向Aave提供稳定币（以获取aToken，因此无法冻结USDC和USDT）向Curve的a3Crv池提供aDAI，aUSDT，aUSDC [https://etherscan.io/tx/0x745ddedf268f60ea4a038991d46b33b7a1d4e5a9ff2767cdba2d3af69f43eb1b](https://etherscan.io/tx/0x745ddedf268f60ea4a038991d46b33b7a1d4e5a9ff2767cdba2d3af69f43eb1b)

12. 向Curve的流动性添加a3Crv LP代币 [https://etherscan.io/tx/0xc60bc6ab561af2a19ebc9e57b44b21774e489bb07f75cb367d69841b372fe896](https://etherscan.io/tx/0xc60bc6ab561af2a19ebc9e57b44b21774e489bb07f75cb367d69841b372fe896)

13.剩余的交易提供到Tornado Cash，GitCoin资助。1千ETH被发送到Cream和Alpha的每个部署者地址。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/linebreak-shanghai.png)

**这个故事是独一无二的。**

我们一直期望在白帽/黑帽活动方面有些模棱两可和角色互换，但是我们很少看到来自受害者如此清晰地指责。

Andre Cronje，几周前Yearn和Alpha Homora[达成合作](https://twitter.com/AndreCronjeTech/status/1347194324237176832?s=20)，今天[记下这次攻击](https://twitter.com/AndreCronjeTech/status/1360674224797483010?s=20)：

> _花时间研究漏洞。9笔交易。4种不同的操作。包括精确的债务计算的一笔交易。这需要花费大量的研究人员几个小时才能弄清楚。 Alpha立即采取了措施以减轻该漏洞。在最初发现的几分钟内解决了该问题。_

[Banteg的回复](https://twitter.com/bantg/status/1360678595551707139?s=20)：

> _操作绝对疯狂。随便看看合约的人不可能发现这个漏洞，尤其是那些未宣布的东西。_

**也许这将导致Yearn的另一次收购；事后报告中曾四次提到Cronje的名字，而且[这种模式看起来很熟悉……](https://rekt.eth.link/decentralised-monopoly/)**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/alpha-finance-conclusion.png)

**对于匿名黑客来说，这个时代还能持续多久？**

由于可能的犯罪嫌疑人列表非常小，因此排除并追踪潜在的攻击者变得更加容易，在这种情况下，此列表甚至比平时要小。

在使用代码时，“别信任，验证”是一个极好的口号，但它并不能阻止在去中心化金融高层必须增加的越来越多的社会偏执狂。我们正经历着加密货币和DeFi前所未有的增长期，其中不能正常运转的成本非常高。DeFi开发人员的精神负担日渐变得越来越重。

帝国是建立在代码行之上的，金融的未来是在我们眼前构建的。

**开发人员陷入太空竞赛，而腐败的内部人员则帮助黑客在地下工作，在他们的基础上挖洞。**

当一座塔倾倒时，其他人就会继续学习。在还没有尘埃落定之前，人群就继续前进，不计其数的队伍重返赛场，以寻求重建更强的应用。

**在不可避免的错误导致他们的匿名斗篷掉下之前，他们能还能维持这种强度多久？**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/af-gif.gif)
