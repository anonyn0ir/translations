---
title: Coinbase和预言机
date: 2020年11月26日
tags:
  - Coinbase
  - 预言机
  - 清算
excerpt: 最近的攻击事件中，黑客将数百万美元归还给受害者，或者干脆将钱留在桌上，而他们本可以拿走更多。在最近发生的黑客事件中，各种方法已被用来盗取资金，但有一个人物却在整个过程中扮演了一个角色...
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/MV5BMjQ1NDAwMzI4Nl5BMl5BanBnXkFtZTgwMDkwMTEyMjI@._V1_.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/MV5BMjQ1NDAwMzI4Nl5BMl5BanBnXkFtZTgwMDkwMTEyMjI@._V1_.jpg)

**我们永远看不透那些我们不理解的选择。**

最近的攻击事件中，黑客将数百万美元归还给受害者，或者干脆将钱留在桌上， 
而他们本可以拿走更多。

在最近发生的[黑客事件](https://www.rekt.news/hack-epidemic/)中，各种方法已被用来盗取资金，但有一个人物却
在整个过程中扮演了一个角色...

根据莫斐斯的说法，预言机"自始至终"都在为秘密抵抗组织服务。她
是一个有意识的程序，协助人类抵抗，
将人类从机器的压迫下解放出来。

最近，预言机不断受到匿名特工的攻击，他们的目的是操纵她对现实的认知， 
以达到利益最大化。

> [NEO](https://youtu.be/CsigSyTME9E?t=87)：我想最明显的问题是，我怎么能相信你？

> 预言机：_这是一个_[黄瓜](https://www.rekt.news/pickle-finance-rekt/)，毫无疑问。

信任问题是价格预言机的共同特点，它可以是链上的，也可以是链下的。

就像samczsun[写的那样](https://samczsun.com/so-you-want-to-use-a-price-oracle/)：

> 其中一种方法是，你可以直接从价格API或交易所中获取现有的链下价格数据，然后将其
> 带到链上。另一方面，你可以通过咨询链上去中心化交易所
> 来计算即时价格。

这两种方案都有各自的优势和劣势。

Uniswap、Kyber或Balancer等链上价格预言机不需要任何特权访问，并且
始终保持最新状态，然而，这意味着它们很容易被攻击者操纵。

链下预言机**如Coinbase**通常对波动性的反应较慢，而且它们还需要

**_"特权用户将数据推送到链上，所以你要相信他们不会变成邪恶，不能
被胁迫推送不良更新"。_**

今天的大规模清算是由于Coinbase预言机出现失误，或者说是操纵。

**我们在Compound Finance上看到了超过1.1亿的贷款清算，因为他们依赖Coinbase这个单一的
预言机。**

![](https://lh6.googleusercontent.com/sR9XX4BQ3SiHSNM2iZzUh8msdZQ45UDfTkhhChTlKD55pzU3rNQU8hPyHUJndLeW7jXvbW0CWRErqePHbQQNnZ-KlR8HWbGNz2ImvumqAKO2sDaQozoq5pHTVyB7kmOhc6ZWj9P5)

热门的收益耕作使得DAI/USDC脱锚，导致DAI的价格飙升至1.3美元，造成大规模
清算，并为那些等待清算这些仓位的匿名代理带来了巨大利润。

> [Sam Priestley](https://twitter.com/arbingsam/status/1331922588193484800?s=20)解释了清算是如何发生的，以及人们如何从中获利。
>
> "今天有人在compound上被清算了4900万美元。清算人仅仅因为调用了一个方法就获得了370万美元。

> 受害者是一个杠杆式的复合耕作者。他们借出DAI和USDC，也借入DAI和
> USDC。当DAI价格发生变化时，就把他们的账户推向了清算。如果他们保持DAI和
> USDC在不同的钱包里，这就不会发生。

> 当你的账户被清算时，清算人可以选择用你的任何抵押品
> 用于偿还你的债务。所以清算人拿了DAI。向Uniswap借DAI。偿还DAI债务。获得更多
> 清算中的DAI。偿还Uniswap。盈利

> 大鳄可能认为他们是安全的，
> 因为他们从来没有调用USDC的"进入市场"功能。但是，通过借入 USDC，他们激活了USDC作为DAI债务的抵押品。"

![](https://lh4.googleusercontent.com/4s6zvtJuvM2gvebHTrXn_Nn5yf2wCtpMGMgQYkWmRFNgmyyT4vcfw1BpOKTNaZQkwMJ2dBo9ObVKOapaqOwykDqfT8f_Dx7dTBATRTD7egKq6y0il5mGetT2Jz6etsB97j0Cm4dC)

感谢[@arbingsam](https://twitter.com/arbingsam/status/1331922588193484800?s=20)作出的分析。

下图显示了DAI价格飙升的情况--对于一个本应稳定的代币来说，这是一个巨大的波动。

![](https://lh4.googleusercontent.com/CWugWH8TcpdzKzgTzseevvzKjHuVzZGZ7XbUD1k6w5JT4v9Sqx2e0u4WsFoND5rFrb7cPehLXQhpNhwKNrtVOnlc7V51HSHaXMm0zvN9rELvuuTDzvFESAxTCo0SJPsQwnlt_K0k)

当Coinbase[推出](https://blog.coinbase.com/introducing-the-coinbase-price-oracle-6d1ee22c7068)他们的预言机时，他们就意识到了依赖链下预言机
所带来的问题。

> "使用链下数据，需要相信发布者会发布正确价格，
> 并妥善保管签名私钥"

然而，他们并没有试图减少对信任的需求，只是向读者保证他们
是值得信任的。

> Coinbase是加密领域最值得信赖的公司之一，我们的主要任务之一就是
> 发展加密经济。一个锚定在Coinbase安全基础设施中的高度可靠的价格馈送
> 可以帮助使去中心化金融生态系统更加安全，降低系统性风险，并开启下一波增长和
> 采纳。

> 看来罗伯特·莱什纳（Robert Leshner）相信他们，正如他当时所说；

> "Coinbase的价格预言机将提高Compound价格馈送的安全性和去中心化，这对协议和建立在Compound之上的
> 应用生态系统来说是至关重要的任务。我们并不孤立—去中心化金融的其他成员将
> 因更快的开发速度、一致的数据和共享标准
> 而受益。"
> 
> - Compound首席执行官罗伯特·莱什纳（Robert Leshner）

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/image.png)


**那么到底是哪里出了问题呢？**

如果*"链下预言机需要特权用户才能将数据推送到链上"，*怎么会出现
这种情况？

Coinbase[状态页面](https://status.coinbase.com/)目前显示如下：

![](https://lh6.googleusercontent.com/WQdMK6Voz-KX1DowA36GhZf8G3xrLN91xG6hFjHpevjVeA8VUL-2b3YPb-QYqyUBb9EjOoRG4c_M-gHNuoaMkmlze58fQUvpkim6SA-GtjkDt9KBh8gjFbMHwcjmk5QCZpt-LNVp)

Coinbase 的预言机过去也曾出现过"问题"，似乎总能给某些行为者
带来高额利润。

这到底是操纵还是技术问题尚不清楚，但我们知道
没有使用过闪电贷。要想把Coinbase的订单簿操纵到这种状态，就必须
花上10万DAI，因为订单簿有30万的深度，锚定价格达到1.3美元。

这是恶意的，粗心的，还是过期的技术？无论哪种情况，那些清算机器人都从
这次事件中获利。

使用任何单一的去中心化数据源作为价格预言机都并非明智之举，而Coinbase
的情况特别糟糕，尤其是当你能用10万美元把订单簿抹掉。

> "有些程序在各个地方运行。那些做着自己的工作，
> 做着自己该做的事情的人，是无形的。你甚至不知道他们在这里。但其他人；
> 嗯，我们经常听到他们的消息。"

![](https://lh6.googleusercontent.com/7H_rZ46PnRaGA2vlOfTOgp5Lz0wtz7M4nNyuqEnLDDEx8fd2U5j5kOsfyw7MOWSo406JcW5btz4BYFBKT6KwZeAZDsMZayIuWC_K_0HB4zfRwkP03AweiMCJkwT6TX7w3krY1Nfs)

别担心花瓶的事
