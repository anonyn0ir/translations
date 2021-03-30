---
title: COVER - REKT
date: 2020年12月29日
tags:
  - cover
  - Rekt
excerpt: 下次，自己的事情自己解决。无限铸造，但它不是威利旺卡，这是一部好莱坞经典的保险主题黑色电影。保险单的黑白结果很适合好莱坞的故事情节。
banner: https://lh4.googleusercontent.com/IgAdM7JctrErxRd1kLmyJz4CEUbBDH1xZdsE4h7YZ_6NTRmWbF3p7rNREX-4BcKiTRH9FygNeZXSOzLCe2PqmVZ2NrWz5fb6ZKpPREHc4x3zsCoF8RcQvhj9Sx5XlBDiM04p1Xnh
---

![](https://lh4.googleusercontent.com/IgAdM7JctrErxRd1kLmyJz4CEUbBDH1xZdsE4h7YZ_6NTRmWbF3p7rNREX-4BcKiTRH9FygNeZXSOzLCe2PqmVZ2NrWz5fb6ZKpPREHc4x3zsCoF8RcQvhj9Sx5XlBDiM04p1Xnh)

**下次，自己的事情自己解决。**

无限铸造，但它不是威利旺卡，这是一部好莱坞经典的保险主题黑色电影。

保险单的黑白结果很适合好莱坞的故事情节。

**在电影[双重赔偿](https://www.youtube.com/watch?v=yKrrAa2o9Eg)（1944年）里，保险是善与恶的动力。**

这部电影的名字源于一个人寿保险条款，该条款指出，如果投保人意外死亡，则可获得双倍赔付。

这导致了一个曲折的剧情，一个保险推销员被他的情人卷入了一个谋杀计划中，情人希望他谋杀她的丈夫，并将其诬陷为意外事故，以便从赔款中获利。

**千万不要信以为真。**去中心化金融的剧情线很少是直白的。匿名性和可组合性是阴谋的完美温床；一个人有多种方式可以从单一事件中获利，这意味着聪明的玩家并不总是拿出最明显的报酬。

**被取走940万美元，追回320万美元，损失620万美元。**

COVER（前称SAFE）下跌~[90%](https://www.coingecko.com/en/coins/cover-protocol)时，一个无限铸造的漏洞被发现并被利用，导致代币的总供应量增加了40万亿，从84,477个增加到40,796,131,214,802,600,000个。

在这个漏洞被关闭之前，有六个不同的地址通过这个漏洞铸造了COVER。**有的人留着钱，有的人却没有。**

在这6个利用该漏洞的地址中，之前[尚未出名的Grap Finance](https://etherscan.io/token/0xC8D2AB2a6FdEbC25432E54941cb85b55b9f152dB)备受关注，因为他们借机以"白帽"黑客的身份出现，将铸造的COVER兑换成ETH，并自信地返还。

**法典即法律，但漏洞依然存在**--我们可以依靠攻击者的优势，但我们知道，事事情并不像表面上看起来那么简单。

谁在他们的$COVER上被掩护？我们秘密行事了解情况。 

![](https://lh3.googleusercontent.com/StXzSYZ9O3fWgBSfhG1AUgJwfNlHvh20UIr03MSxmDW94rKhJfr9VJnyjxUyRAhgxAmGY7yeVnqokpMW3rk6ZzpZOB0bQuDCTxMzRAlParXEr6lNlN_WkI_xHSo6hxk5ul1n9D5y)

**Rekt OPSEC**

最初的攻击有[四个步骤](https://twitter.com/vasa_develop/status/1343571127331737600?s=20)和一个攻击者，但一旦漏洞[公之于众](https://twitter.com/Luciano_vPEPO/status/1343509612583145472?s=20)，其他钱包复制了这个过程，故事就变得错综复杂。

以下时间线取自官方Cover Post-Mortem(https://coverprotocol.medium.com/12-28-post-mortem-34c5f9f718d4)，如要了解更详细的分析，请见[@vasa_dev](https://twitter.com/vasa_develop)的逐步指南(https://www.notion.so/Cover-Infinite-Mint-Exploit-0a234cc279484982ae559bb5ab54532a#6359c6970a1b414499b76241a7e7b967)。

**攻击者1的时间线**

2020年12月28日 04:09:27 AM +UTC

  •	团队使用多签签署一笔[交易](https://etherscan.io/tx/0xe5173fffaed3342b53d41319dc538e7923e287e962df2d27f5e425c633db45d4),为新的承保到期**增加一个[Balancer池](https://etherscan.io/address/0x59686e01aa841f622a43688153062c2f24f8fded)到铁匠合约。**

2020年12月28日08:08:12 AM +UTC

  •	**攻击者[执行](https://etherscan.io/tx/0xd721b0ef2886f14b75548b70d2d1fd82bea085ca24f5de29b833a64cfd8f7a50)铁匠合同的第一笔存款**，存入1,326,880个BPT代币。

2020年12月28日 08:11:16 AM +UTC

  •	**随后，同一攻击者[调用](https://etherscan.io/tx/0xadf27f5dd052482d46fdf69a5208a27cc7352522c7c19bbde5aee18f6ea4373b)withdraw()**，利用合约换取约703.64$COVER，并提取了1,326,878.99 BPT。

2020年12月28日08:47:15 AM +UTC

  •	**第一次卖出被利用的$COVER代币可在[此处](https://etherscan.io/tx/0x66128a1685605b1798c852e14db0b0232a56e3bebf7f3f35b168642801754beb)找到**。在此期间，有多个账户滥用该漏洞，并在市场上出售他们的$COVER。

2020年12月28日09:18:28 AM +UTC

  •	攻击者乘着攻击因子依然存在[继续造币](https://etherscan.io/tx/0xf81fb72ee096e0d7afe4b99a55b723110604fb26ec82846043cfc396e1fa79da)。

攻击者总共盗取了约440万美元的用户资金，并将其转移到[这个地址](https://etherscan.io/address/0x85abf036ca922e56fed670f4d3ce53fc4ea52b95#tokentxns)。

看来这个漏洞一开始是意外发现的，因为攻击者的OPSEC很差，是一个正常的钱包，由交易所出资，有KYC，交易期为3年。有人声称知道这个利用者的身份，[建议](https://twitter.com/0xRevert/status/1343743516544028672?s=20)他们返还资金。
________________________________________

**在经典的去中心化金融剧情转折中，与抓住机会扮演"白帽"的Grap Finance相比，原攻击者鲜为人知。**

**Grap Finance的时间线**

2020年12月28日11:54:47 AM +UTC

  •	[Grap Finance：部署者](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd) （外部拥有的账户）[存入](https://etherscan.io/tx/0x77490baee41a9b35a6e87d49453c7329c7517c10ce6ce26b4c142692a2877e65)15255.552810089260015362 BPT（DAI/Basis池）进入铁匠挖矿合约。 

2020年12月28日11:58:04 AM +UTC

  •	[Grap Finance：部署者提取](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd)他们的15255.552810089260015361 BPT（DAI/Basis池），铁匠挖矿合约中的余额只剩下1 wei.。

2020年12月28日11:58:56 AM +UTC

  •	另一个用户从铁匠那里[提取](https://etherscan.io/tx/0xa27fb73caddb1cf24aa7a5afe84eed13db2f0a889a6ee0f3d5e6226a76c0fd9c)他所有余额的大部头（1,007.599009946121991627 BPT）。现在单单是Grap Finance就拥有保险挖矿铁匠合约上DAI/Basis池的所有流动资金，正好是1wei.。

2020年12月28日12:00:21 PM +UTC

  •	Grap Finance:部署者在铁匠挖矿合约上[存回](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd)15 255.552810089260015361 BPT（DAI/Basis pool）。

2020年12月28日12:02:04 PM +UTC

  •	[Grap Finance：部署者领取](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd)了奖励，由于余额只有1 wei，再加上存储/内存问题，这就导致了40,796,131,214,802,500,000.212114436030863813$COVER的铸造。

2020年12月28日12:29:03 PM +UTC

  •	[Grap Finance：部署者](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd)开始通过1inch.exchange在多个交易中尽可能[多](https://etherscan.io/tx/0x01b3517845ed9c6b7b40d57bd71ac1a89fec080c5b8988f764d8226ac5caa959)地[出售](https://etherscan.io/tx/0xaf94d9b537a13819e873b37160594af2b1cc70b420d0b160a02e341566866a6b)代币。

2020年12月28日12:59:27 PM +UTC

  •	[Grap Finance：部署者烧毁](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd)铸造代币

2020年12月28日01:41:01 PM +UTC

  •	[Grap Finance：部署者](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd)将他们通过出售$COVER提取的4351（[1](https://etherscan.io/tx/0x23cb9bdf14eed955a84da3f3cfcf296356c0f897dec0b99e85151a7f084a3051) + [4350](https://etherscan.io/tx/0xc2fd5094c1e108f83222a86bd46b35fc0da35616385d681964b22003643f982e)）ETH发送到部署者账户，占总漏洞损失（940万美元）的34%

________________________________________

**来自Cover的报道**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/12/image-4.png)

**Cover Protocol花了6个小时才公开承认这次攻击。**

_该团队仍在调查当前事件。该漏洞已经不可能被利用。_

_请不要购买[$COVER(]https://twitter.com/search?q=%24COVER&src=cashtag_click)代币，并从sushiswap上的COVER/ETH池中移除您的流动资金。_

_CLAIM/NOCLAIM balancer池不受影响。_

**攻击事件发生8小时后，Cover协议[宣布](https://twitter.com/CoverProtocol/status/1343581331448586245?s=20)他们计划向受影响用户退款。**

_大家好，我们正在探索在铸币漏洞被滥用之前，通过快照提供一个NEW[$COVER](https://twitter.com/search?q=%24COVER&src=cashtag_click)代币。攻击者退回的4350 ETH也将通过快照处理并交LP代币持有者，我们还在调查中。不要购买COVER_

**"逝者不死"在去中心化金融中显得再真实不过了。**将发行第四次迭代的Cover协议代币，向受影响用户退款。

SAFE - SAFE2 - COVER - $RECOVER？

**在一定程度上，坚持不懈是值得钦佩的，但到什么时候才算足够的？**

一些读者应该还记得Cover Protocol的完整历史，在@azeemfi和@chefcoverage都做出了错误的决定后，他们从[SAFE]改名(https://coverprotocol.medium.com/cover-protocol-e202808aa4ef)。随后他们推出了SAFE2，而SAFE2又迁移到了我们今天所熟知的COVER。

社区是否愿意给他们第四次机会？
________________________________________
![](https://lh5.googleusercontent.com/Ogj1lycooZFZrO1GfU4lgsis5tJ2j76L2BHPQ50TC3KuG7mTx_CQ-FcD90AfAQtSQqdc0ERGK95wczwmRdoznGUR9c00f381m3DAhRZp7Ego0j6U4WrxohU-RCMNtE0Sq0c4f55u)

**[Grap Finance](https://medium.com/@grap.finance)是YAM的一个分叉**--他们在去中心化金融夏季没有带来任何值得注意的东西，于是抓住机会摆出一副白帽的样子获得关注，在一天之内就为他们赢得了成千上万的粉丝。

他们将如何处理这个新发现的追随者，还有待观察。

**Grap Finance**的异常活动使他们在过去7天内进入COVER的余额变化前五名之内 。

![](https://lh3.googleusercontent.com/FMvU_UZhki6SB0ery4HcON4MEfMbBSPmrah0QDGPCqgwePElvreCDCKdVct9Mo2-B2sqqgUqx8y4MQOpJIPMtn-VqI4tm3ND37FW_Kyz0sDVWKDvdmyBZpe555KyeVqpQd2hO6by)

他们说没有所谓的负面宣传，接下来的图表似乎证实了这一点--COVER的独特地址在攻击当天增加了1778个，因为机会主义的交易者试图抓住一把下落的刀子。 

![](https://lh5.googleusercontent.com/n3eflB7D7s60xY-dZg_755bKnUbm-8XEpryBbapuAY1UhlCirnheGGcmDL8hX6Bv8im6TzNFOBryHjcrGL9bUPcMShVRB-wepJfTxod4M71KiL-15n9qdBhjJPRPCzuqe62ixMFZ)

在这里，我们看到Binance显示为绿色，COVER的存款大幅增加，因为社区试图在他们最终暂停代币交易之前跳槽。

![](https://lh4.googleusercontent.com/ISdelPif5XcLBEWb4fNDHyOanmb9rPv5Ny47vHbshuH0bevewfDrt6Agt28yYWRiSgxUFSC_NPPX_Vp5oJOWFkCeXByfFP9pO07HniqwKcBtNeBgwCrJNKyepBp22XVFgxQeFyQB)

负责任的行为不见得提供太多奖励，但犯罪的代价总是全额支付。

有人说这是内鬼干的好事。

也许攻击者被人下了毒手，无法保住资金，所以把资金送回去，而从宣传中获利。 

![](https://lh5.googleusercontent.com/8DTMgDPJE8_EL2ldg9LTM8_A4JtUw1oAbAIxFcZj3MOISWVwa5Do7EivF7R5SrcInzstS7lLnHYlA3Sug4uqC95aE_EAZdNOwIeD_QQvB5F9ckPTFrotVFZ2I02JaPT-Gb_J6MwY)

**我们并不声称这些传言是基于事实，**但当当天的事件导致诸如此类(https://support.mxc-exchange.com/hc/en-001/articles/360054776091)公告时，很容易看出这种想法是如何产生的。

![](https://lh3.googleusercontent.com/LJ9XZzZF2hn1qinb-EP8NlGS3vK2QdGWllXXAgmYbHxVCGKF-B07NHSyXREHg7smGNDfyITiFgf7txfb0Eejrn-AVycPUzhnjTFV0dv7hD0Sqmfk_gHEUlonGnnc7J_qGLuzGhce)

**纯粹巧合是不可能的**，这是犯规或绝望。MXC如果根据小道消息上市代币，一定是陷入困境。

Crypto Twitter已经证明了他们的风险偏好依然很强，他们将他们的"救援者"[代币](https://www.coingecko.com/en/coins/grap-finance)的价格暴涨了几千倍，在撰写本文时，其24小时的交易量从236美元增加到5458,084美元。
________________________________________

**埃米利亚诺-博纳西提供了以下引文**：

> 除了技术问题之外，这次活动再次向人们展示了这个生态系统的凝聚力和支持力。
> 
> 我们反脆弱。
> 
> 我非常肯定，在这次事件之后，不仅会出现一个新的Cover，而且更重要的是一个联合体来保证生态系统的安全和及时反应—它也许是白帽小组。
________________________________________

**出血是一笔很大的开支。去中心化金融保险市场一片狼藉。**

先是[NXM](https://www.rekt.news/nxm-hugh-speaks-out/)，现在是Cover。协议不受影响无关紧要，如果我们要写一篇关于你的文章，那么用户对你的项目毫无信心。

[去中心化金融保险必须被全面理解](https://www.rekt.news/nxm-hugh-speaks-out/)。 这里不会出现神迹。

不安全的协议支付高额保费，而其他协议则努力建立他们的无索偿奖金。

[COVER](https://twitter.com/search?q=%24COVER&src=cashtag_click)在4小时内下跌了40倍，而 [$GRAP](https://twitter.com/search?q=%24GRAP&src=cashtag_click)上涨了40倍。

Grap团队在幕后表示["没有收获"](https://twitter.com/GrapFinance/status/1343555258316804101?s=20)，荒诞的故事，半真半假。

**黑客漂白在一连串的指控下撑不了太久。**

调查仍在继续...

![](https://lh6.googleusercontent.com/p6se9Mb3aS2HWRTPsm98ZjKAwuUAel7YOOa02gjrlbP6q_iTmGLiQ21XiTm93L102-HH4pMRqgO5dDMZu5BOJOJYmJxSpg9IPRL9S7pHZTbfTksMZkuKjEZKamLrSyh-oxey40pq)
