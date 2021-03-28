---
title: FURUCOMBO - REKT
date: 2021年3月1日
tags:
  - Furucombo
  - rekt
excerpt: 最好耐心等待而不是摇摆和错失。rekt和Limzero及Kurt Barry一道调查furucombo1400万美元黑客事件。“无限授权”从来都不安全。
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-header.png
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-header.png)

**最好耐心等待而不是摇摆和错失。**

我们听说[Furucombo](https://twitter.com/furucombo/status/1365743632460910593?s=20)的消息但是我们人手紧张-小型团队并不能总是准时交付，尤其当黑客数以周计的干活时。如果你是一个愿意分享技巧的DeFi侦探，那么联系并告知我们你的经验-在rekt.news有您的一席之地。

一名黑客回击，攻破Furucombo并从不同钱包中盗取1400万美元，这些钱包授予该app“无限的授权”。

无限授权意味着无限信任—我们知道在DeFi中不应该这么做。

**“别信任，去检验”，但是每次交易时谁有时间或者gas金钱来授权设置许可的数额？**

使用Furucombo的人不得不授予一些额度，不过看起来授予得太多了，作为回报他们上了一堂残酷的课。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-linebreak.png)

在一个如今被人所知的“恶意合约”漏洞中，[攻击者](https://etherscan.io/address/0xb624E2b10b84a41687caeC94BDd484E48d76B212)让[Furucombo]代理合约(https://etherscan.io/address/0x17e8Ca1b4798B97602895f63206afCd1Fc90Ca5f)以为Aave V2有一个[新实现版本](https://etherscan.io/address/0x86765dde9304bea32f65330d266155c4fa0c4f04)。 

当然，新得实现是恶意的，并且拥有转移所有授权过的代币到攻击者控制的地址的能力，因为用户已经授权Furucombo合约代表他们使用他们的代币。

**[Kurt Barry](https://twitter.com/Kurt_M_Barry/status/1365876788757471234?s=20)提供如下分析：**

其中一笔[资金盗窃交易](https://etherscan.io/tx/0x5af11a27e98a167b61b01fea093cf612d5ec76c20fd2032f2d1aa49c8b1ee529)被发往Furucombo代理，指定AAVE v2借款池代理作为第一个以及唯一一个行动的处理者。

如[ethtx.info](https://ethtx.info/)所示，你可以从下图查看执行轨迹。注意聚簇的委托调用。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx1.png)

需要在注册里授权处理者；在这笔交易发生的时候（而不是现在）该代理是一个有效的处理者。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx2.png)

FC代理委托调用AAVE v2代理，然后从一个特殊的存储卡槽读取实现地址，不过因为这是一个委托调用，它从FC代理存储中读取，而且提取的地址是黑客的漏洞合约。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx3.png)

如果我们观察黑客[之前的交易](https://etherscan.io/tx/0x6a14869266a1dcf3f51b102f44b7af7d0a56f1766e5b1908ac80a6a23dbaf449#statechange%E2%80%A6)：

我们看到黑客使用他们的恶意合约使得FC代理委托调用AAVE v2代理，调用初始化函数，设置实施卡槽。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx4.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx5.png)

一旦委托调用在FC代理上下文中执行黑客的代码，就完了。受害者已经授权FC代理动用他们的stETH，漏洞代码把币全部发送给黑客。

剩下的如法炮制。

总结：

· FC代理对信任的处理者执行调用方特定的委托调用，让它的存储被修改

· 一个处理者对从存储中读取的一个地址进行调用方特定的委托调用。

· 处理者暴露一个设置那个地址的函数。

我们学到的内容：

· 一个“信任列表”是有用的但并不是保证。

· 开发者应该审计被委托调用函数如何影响调用者的存储。

· 考虑限制被调用者的参数或者功能

· 小心用户提供的输入参数

**并不单单是个人受损，甚至Cream金融也遭受损失，因为攻击者直接从他们的财政库“借钱”。**

[Igor Igamberdiev](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-cream.png)给出一份被盗资产的列表。

· 3900 stETH

· 240万 USDC

· 64.9万 USDT

· 25.7万 DAI

· 26 aWBTC

· 270 aWETH

· 296 aETH

· 2300 aAAVE

· 4 WBTC

· 9万 CRV

· 4.3万 LINK

· 7300 cETH

· 1720万 cUSDC

· 69 cWBTC

· 1.422亿 BAO

· 3.86万 PERP

· 3.04万 COMBO

· 7500 PAID

· 22.5万 UNIDX

· 342 GRO

· 1.9万 NDX

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-ropebreak.png)

在发现DeFi发烧友Limzero ([@pleyuh](https://twitter.com/pleyuh/status/1365998455638876161?s=20))是受影响最惨的人中一员后，我们与他谈了谈。

**rekt：**

_这事对你啥影响？_

_你如何意识到Furucombo遭到攻击以及你何时采取行动？_

Limzero:

我正在跟一些朋友在我家放松。我用手机打开电报去看看啥情况，从[Darren](https://twitter.com/Darrenlautf)的"[猩猩日报](https://t.me/thedailyape)"频道看到有一个与Furucombo相关的漏洞。

我查验曾经用过furucombo的一个地址，注意到我的aAAVE和一些aETH发生了转移。

我很害怕因为我有一些活跃的借款，不想让我的抵押品被清算。我发现我的健康因子已经降到1.15，因此我迅速偿付贷款。

我注意到攻击者榨干我的全部aAAVE但是仅拿走三分之一aETH。我猜测低健康因子阻挡他们移走更多的资金。我真的幸运拥有一些活跃的借贷。

偿付贷款保护抵押品后，我收回曾经授予那个地址的所有代币授权。

那是一个我延迟几周的行动（为了等费用变得更低）。显然这是一次花费不菲的拖延。

我注意到黑客转移我的自己在黑客发生90分钟之后。

**rekt：**

_对你来说是一个巨大损失吗？_

_心理上感觉如何，这次攻击之后你对使用DeFi感觉更谨慎还是更没信心？_

**Limzero：**

以绝对数字来看是一个巨大的损失不过在我的组合中微乎其微。

我害怕了好几分钟因为我担心所有aToken都会被清算，当我看到我的健康因子在1.1之上我感觉一阵轻松。

我把整个经历当作一堂重要的课—从我的角度来看对一个拥有巨大数额的地址授予无限的许可是一个非常愚蠢的错误。考虑所有的情况，那是我不得不付的[智商税](https://rekt.eth.link/ape-tax/)。这是在这个行业这么多年来影响到我的首个智能合约黑客/漏洞。我对更严重的情形没有发生在我身上感到庆幸。

实际上是在COVER漏洞之后的第一场漏洞，不过我忘了那件:P

我倒没有对使用DeFi感到缺少信心。这类风险众所周知。

不过我已经采取措施增加安全

**rekt：**

_关于这些举措能跟我们讲讲吗？_

**Limzero：**

很抱歉不能。

这正是我采用的措施的一部分。

**rekt：**

_你会向我们的读者推荐哪些步骤来提升他们的安全性呢？_
 
**Limzero：**

1. 使用硬件钱包

2. 避免用windows操作系统

3. 合约交互时用专门的web3机器

4. 单独的密码或者密码管理器+VPN

5. 较少的社交媒体画像

6. 使用多地址来分散风险

7. 新挖矿用新地址

8. 对频繁使用的地址收回授权
 
我并不是一个安全专家。这些是在加密领域懂得更多的的人的标准指引。

9. 读REKT

**rekt：**

_对我们读者最后要说的？_

**Limzero：**

"求求大哥别再黑我"

此外，除非你对自己的安全性特别自信，考虑把一小部分持仓放到像Kraken, Coinbase, Gemini, Binance等头部CEX，以防个人钱包被黑。

这就是所有我想说的。

**rekt：**

_感谢与我们交谈。_

**Limzero：**

谢谢你。希望咱们再也不会交流。

**一场简单的攻击只需简单的修复**—不要使用“无限授权”除非你无限信任。分开授权花费不小，但是当涉及到安全时不要缩减开支。

诸如[Debank](https://debank.com/)或者[Etherscan](https://etherscan.io/tokenapprovalchecker)之类的网站让你监控以及撤回钱包授权，而且正如Limzero所言这并不是直到再发生一次后才应该拖延的任务。

不要丢掉你的防卫，黑客总是在寻找一个缺口，这些攻击可能比你预期的还要频繁发生。

**本文并没有推荐费；你对自己的安全负责，不过一旦你学会此法，奖励的钱值得冒此风险。**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-conc.png)
