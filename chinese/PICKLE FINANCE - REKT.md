---
title: PICKLE FINANCE - REKT
date: 2020年11月22日
tags:
  - pickle finance
  - Rekt
excerpt: 金融业持续发酵。即使是泡菜也有保质期。Pickle Finance已成为这次黑客流行病的最新受害者。然而，这一次，有些不一样。
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/rr.jpeg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/rr.jpeg)

**金融业持续发酵。即使是泡菜也有保质期。**

Pickle Finance 的[cDAI](https://github.com/pickle-finance/contracts#pickle-jars-pjars) jar因一个涉及假Pickle jar漏洞， 
被黑客攻击并[盗取](https://bloxy.info/tx/0xe72d4e7ba9b5af0cf2a8cfb1e30fd9f388df0ab3da79790be842bfbed11087b0)了1970万DAI。

Pickle Finance已成为这次[黑客流行病](https://www.rekt.news/hack-epidemic/)的最新受害者。

**然而，这一次，有些不一样...*

当推特试图接受又一起金融灾难时，Rekt已着手进行调查。

我们联系了Stake Capital团队，他们查看了代码，并警告我们其他jar可能存在
风险。

随后，我们迅速联系了Pickle Finance团队，并成立了一个作战情报室，由Stake Capital
（[@bneiluj](https://twitter.com/bneiluj)，[@vasa_develop](https://twitter.com/vasa_develop)）Yearn（[@bantg](https://twitter.com/bantg)）[Pickle Finance](https://twitter.com/picklefinance)的成员和经验丰富的开发人员
[@samczsun](https://twitter.com/samczsun)，[@emilianobonassi](https://twitter.com/emilianobonassi)组成。

随着我们展开工作，很明显，我们正在寻找与最近几周的去中心化金融乐高风格
黑客事件非常不同的东西。

**这不是一次套利。**

攻击者很了解Solidity和EVM，很可能已密切关注Yearn代码一段时间了，
因为该漏洞与一个月前在Yearn代码中[发现](https://github.com/iearn-finance/yearn-security/blob/master/disclosures/2020-10-10.md)的
漏洞类似。

Pickle Jars本质上是Yearn yVaults的一个分叉。这些Jar由一个名为the Controller的合约控制， 
它拥有一个功能，允许用户在Jar之间交换资产。

遗憾的是，并没有允许哪些Jar使用这个交换功能的白名单。

黑客创建了一个假的Pickle Jar，并从原来的Jar中换取资金。这是有可能的
因为[swapExactJarForJar](https://twitter.com/emilianobonassi/status/1330239233538318339?s=20)没有检查"白名单"jar。

Pickle Finance团队知道他们需要帮助，并非常愿意与其他团队合作，以
防止任何进一步的损害。

Pickle曾试图调用"withdrawAll"，但这笔交易[失败](https://etherscan.io/tx/0xb108205dc90466104f10d3e465593825ea88420cd8db6df29afd57e62df5cba6)了。

取款请求必须通过治理DAO，该DAO有12小时时间锁。

Pickle多重签名中只有一个成员有能力绕过时间锁，而他们却睡着了。

这意味着管理员无法清空Pickle Jars，但这并不能保护他们免受另一次黑客攻击。

[Pickle Finance](https://twitter.com/picklefinance/status/1330256787002564610?s=20)和[Curve](https://twitter.com/bneiluj/status/1330255575339438088?s=20)发出警告，告诉用户立即从Pickle中提取资金，然而， 
5000万美元仍留在潜在的脆弱Pickle Jars中，同时白帽团队对该漏洞进行调查， 
并检查剩余资金的安全性。

救援小组要么唤醒沉睡的管理员，要么自己把jar子里的资金抽干。

![](https://lh5.googleusercontent.com/iBloOUNiyzcS6t7vuiT8Ric31fzGktin3XSZ53MAGk0eJiylu53vsQJ_BdPOHba_7yH81037JWZX_H48bzbwH5AoNMn3jFz8Q_YplF9Xk8sm47IHRK07RnTIB8I8Ebeba4vJCCJp)

**团队必须克服五大挑战。**

1. 要让Pickle Finance团队跨越几个时区，开始抢救资金，将交易推送到
12小时时间锁（通过6个多重签名中的3个）来提取资金。

2. 为了让成千上万的投资者撤回资金（还要阻止他们重新投入资金，因为一旦池总锁仓量下降，收益率将膨胀到1000+%。 ）

3. 对其他jar进行安全检查，查看是否有可能发生更多的攻击事件。

4. 复制攻击并在任何人再次入侵jar之前进行白帽攻击。

5. 在试图营救剩下的5万美元时，避免被人抢先一步。

**我们还能继续依靠伪匿名白帽黑客的帮助多长时间？**

攻击者的激励机制显然比保护者更一致；他们为什么要协调
如此惨烈的反击？

荣耀归于白帽黑客，钱却归于黑帽黑客。**这是不可持续的。**

诱惑要多久才能把这些白帽变成黑帽？

**分析**

通过发布这些技术信息，我们意识到我们可能会引发新的黑客。我们
与Pickle Finance和其他开发人员讨论了潜在后果，并确认我们
不清楚Pickle的任何操作分叉可能受到模仿攻击的影响。

选择性披露会带来责任方面的问题，所以我们决定免费
发布这一信息。如果有任何协议正在运行Pickle代码的分叉，他们应该已经意识到正在
展开的事件，并对模仿黑客采取预防措施。

以下图表由[@vasa_develop](https://twitter.com/vasa_develop) 制作。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/Pickle-Exploit-Overview.png)

原始文件可在[此处](https://lucid.app/lucidspark/invitations/accept/8f291e25-bf50-4a77-913d-31ddfb62754b)找到。

**更多详情，请点击[这里](https://github.com/banteg/evil-jar/blob/master/readme.md)查看团队完整事后报告。**

看看相对较新的保险方"[Cover Protocol](https://twitter.com/CoverProtocol/status/1330238732558098437?s=20)"如何处理这一事件是有趣的事； 
对于第一笔索赔来说，这是一笔巨大的金额。保险索赔的快照投票可在[此处](https://snapshot.page/#/cover/proposal/QmPSkV68ihhP8EAZbNoQVsTpUh82wiX18ckyEwiUbChRjQ)
找到。

![](https://lh5.googleusercontent.com/HcyTLZyj6aAciaM5wFLPJl04zSx8n_iqwYnnetTg_ATBVappkijm1K2TtSjkbAAwsDNFcJCaiz1uibep5WAC4-56uyMRDn8p5jk-iLHk53qklgC1Jc_4JiOZrLkr3jZ-ictipp2N)

**腌制是一个缓慢的过程。**

几十年来，敏捷开发的布道者一直告诉开发人员要快速移动，快速失败，并推出
最小可行产品。这些想法并不适合在恶劣的环境中构建。

**在去中心化金融中快迅速失败要付出巨大代价。**

我们不只是需要另一种方法论。我们需要的是一种范式转换，允许快速迭代，同时又能
同时减少被重击的可能性。

让我们放弃审计是安全保障这样的想法。大多数时候它是
适用于移动目标的核对表式安全措施的快照，而这些措施往往在项目进入主网后不久
就会演变成其他东西。

MixBytes（10月3日）和Haechi（10月20日）的审计早在添加ControllerV4（10月23日）之前完成， 
而ControllerV4是关键的攻击因子之一。

**未来金融领域最伟大的团队将表现出以下特点--
有能力处理好快速上线和安全上线之间的平衡点**，不断审核并定期严格测试他们的可组合货币机器人。
定期对机器人进行审计。

审计应该是一个定期和持续的过程，而不是在启动逐项勾选而已。新的去中心化金融
协议会不断变化和调整，安全审计应反映这一点。

腌菜只有在罐子里才能保持新鲜......

![](https://lh6.googleusercontent.com/Bx_HYNlFKOcaH6XtCcUCcE5TlykgAkp3vka10Tq1KkOV_bK4YxOtjJTcUt73XhYoauO3_I9SQeu55sTKkjAj0brsKfis-lPGuRpPth03tGxuxEF46oU5lJm_mgvkIL1ro_AYZh6F)

照片 [@martinkrung](https://twitter.com/martinkrung)
