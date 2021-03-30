---
title: EMINENCE退款--干还是DAI
date: 2020年9月29日
tags:
  - Eminence 
  - Cronje 
  - defi
excerpt: 在社区成员的威胁逼迫下，安德烈·克罗涅和团队已迅速采取行动，在9月29日EMN合同被掠走1500万美元后，退还了神秘退回的800万美元。
---

在社区成员的威胁逼迫下，安德烈·克罗涅和团队已迅速采取行动，在9月29日[EMN合同被掠走](https://rekt.news/eminence-rekt-in-prod/)1500万美元后，退还了神秘退回的800万美元。

为什么会有人退回800万美元？

这是一次复杂的黑客攻击事件，可能要花好几天的时间去策划，为什么他们会选择几分钟后才归还一半的钱呢？

难道Yearn知道攻击者的身份？

如果你是黑客，你是愿意拿着1500万美元，被人公布资料，还是拿着800万美元，安享晚年？

这些只是9月29日戏剧性的漏洞和退款事件发生后，社区提出的一些问题。

以下网站提供了该漏洞涉及的三笔交易完整分析。

[交易1 2020年9月29日，上午01:20:41 +UTC](https://ethtx.info/0x3503253131644dd9f52802d071de74e456570374d586ddd640159cf6fb9b8ad8)

[交易2 2020年9月29日，上午01:22:28 +UTC](https://ethtx.info/0x045b60411af18114f1986957a41296ba2a97ccff75a9b38af818800ea9da0b2a)

[交易3 2020年9月29日，上午01:23:28 +UTC](https://ethtx.info/0x4f0f495dbcb58b452f268b9149a418524e43b13b55e780673c10b3b755340317)

8分钟后，进行了回款交易。

[回款交易2020年9月29日，上午01:31:04 +UTC](https://ethtx.info/0x7bc97357364222207f1f011b22ad98ba78fcd3c25d3398346caa3928cdf4a4dd)

关于谁是这起劫案的责任人，有好几种理论，有人在争论这是否真的是一起黑客攻击事件，还是只是利用了未完成的代码。

[@mierzwik](https://twitter.com/mierzwik)写了这篇关于（[0x762bfbd](https://etherscan.io/address/0x762bfbd8dc93fac514fd89c027e81621e8597441)）机器人响应的[文章](https://medium.com/@mierzwik/hey-bot-give-me-all-your-money-e1f692594f2e)，其中显示了该机器人如何在EMN攻击前一周盗取400 个UNI。

[@frankresearcher](https://twitter.com/FrankResearcher)此后下了不少功夫，即对黑客/漏洞中使用的同一个钱包进行调查。 

![](https://lh6.googleusercontent.com/qov3BuEa6rc6VT97cxBh7jgvRYxeOMDi8PbS3qgjTyIKLVIZwE5d8yA1TtDPCuXM-7WmFhMAma9hdVdskBbEEZWG3XMl3ntRdiGVKhbnk2aDnlzTBOSpf1Iz0R_hTbj4yFdLxKVz)

[此处](https://twitter.com/FrankResearcher/status/1310885102407254021?s=20)阅读弗兰克的其余推文。他继续假设了各种地址在黑客/漏洞中的作用。

弗兰克基于链上数据的假设。

0x223034e = [$ENM](https://twitter.com/search?q=%24ENM&src=cashtag_click)黑客

0x762bfbd = 黑客退出的合同 $UNI

0x2d033fe = 0x762bfbd的创建者地址

0x2f14f72 = 资助创建者的地址（很可能是一个所有者）

这是一项正在进行的调查，立即订阅，我们会及时为您更新。

![](https://lh5.googleusercontent.com/bElo-Tzz3WEbKufKV60H8JybrfXU_jwZ4m5XmRARI3FsQCE9v57iOqnrOb89woPqABSKOBpGd6oMpwr4okPa42bKsiXrzNYkuoUNwXTN7sM6P9pxmXKpxBma5XIxHC5AzE5wMTnq)
 
在他所说的"优雅的解决方案" Yearn开发人员@bantg使用Uniswap LP分发代码和哈希树（merkle tree）实现退款。   

![](https://lh4.googleusercontent.com/N6RtgR2lbxx_noX8jN7NPq5o3kmScgGaOhpQnBgS6-QPU3l7GnWvEvbGBGybHNOKsMmpgR_gOCAxA4BALyDaHXkub1i89MDIyVjRDN-spFd7TgejtVFygH88VbZnjSPgsOytYUYu)
![](https://lh6.googleusercontent.com/KBuK7SdgDK_F5xS3SDpMwR3mawVkKuG4YhPOS90HjyjY1JewDai5IXxp7dsA3ROWvabWdhr2AI7YX2GeJhlT92bbIFctdRKwk-SjE_O0IXogKOYFLDALNu5DAZQEzww3gNFGzbmX)

Milkyklim为那些从10923319-10954777区块之间的yyFI合约中索赔并遭受5%费用问题的人创建了类似的yyFI退款[解决方案](https://gist.github.com/banteg/b2a3b78cdd59ea346afc56181e7a07cd)。 

![](https://lh4.googleusercontent.com/FiHtOA8Xk-LxkXVD4Cm-eq0ftH7tPFPxNoCmbzX1EXzppq4Hz_Ge9RIgHdD8gzV02dexKQGrljMg46xXl0mJTrocaHofDR2fdgpOYcA2bDxGAxH8fM0NE9rWTajN5duN4i4NG3ro)

youreminence.financial上提供退款服务后，退款按每分钟25万美元的速度进行发放。 

![](https://lh4.googleusercontent.com/Cj0OwsQJkhLnq8Lheqzy6Qa_rLUbG0x4h_xkBLpeLSZPETYI5Tt4TaGlA9_4HACZw-0mSCnW0kYejV0F88Hb6nWlvTTEUTlhx3pMeGczF2nJ9QzwR3pdO5ydhQk_pfT3OG6FheMR)

这导致800万美元的退款在短短20分钟内就被领走了一半。 

![](https://lh3.googleusercontent.com/jSpxxX0Z1wyYeVZlXFy6ToRnqV0kpyzqiaVS-t_UB8GSuYgPCfLkzfAnIwZJWweng1Ymx2l3lVTa3TGKOjGMbPCamGtfvLtSn_hT8fsE1yjeeAHD5tYfvvAnC5kSUSR3IxsFnM9l)

与创作这次快照退款所投入的专注度和工作量形成鲜明对比的是，似乎很多用户在提出退款申索时并没有给予足够的重视，只是简单地复制了banteg的截图，结果将自己的全部索赔直接捐赠给banteg和团队。

[340 DAI的100%小费](https://etherscan.io/tx/0x6a17f1b30b8c5479e6542fb3d6189cf67f34bbc85cba7d669cbf72367bfb724f)

[66.9DAI的100%小费](https://etherscan.io/tx/0xa7ad9985bc7ba00070f5ef18b766e10ca4c0d155cf4ca6ae2e11df9af41b6fc1)

[993.3 DAI的100%小费](https://etherscan.io/tx/0x835b998d086ea0aee96d1e0a3e5b558c62da8d621959f213c10bed6250c9f9c0)

[995.1 DAI的100%小费](https://etherscan.io/tx/0x7c759f66b058eb2dceb8a67a648dd4d0a0857bbfd38f51e8b058d18673f1c616)

小费交易的完整清单可在[以下网站](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f?a=0x7a1057e6e9093da9c1d4c1d049609b6889fc4c67)找到

有人质疑，为什么会有这种将索赔作为100%小费返还的选项，而本来上限可以定在10%或20%。

令人意外的是，那些从退款中受益最大的人留下的小费相对于他们的索赔比例最小。 

![](https://lh5.googleusercontent.com/w3CD80RlDF-F-FnDBUlO5UdU0pEm4X5tgy87FpLXyBGXXQInQ4_9A9op0xp8bTaPrNjtLaAkGDe8G1AhR61qyW-YuGJUXCW_JDyCXM6xsNKh47TGPCimBoez_F1dqVcwc7rr-0Xs)

贪婪的鲸鱼...以下是通过youreminence.finance获得的关于DAI索赔和捐赠的更多数据，这些数据由Alphaleakers提供。 

![](https://lh6.googleusercontent.com/goJyvxqXCAg8kCYnCZj5di0wvRE5I4BtroyTdY3GK88wyX67fJ4rAoWSPkTtXVa_CQ5Lo7Oba2kS0K_t8AHtvgoAkLBzKv8wHk_OIk3T4UOr1ux3SSsYBpjcAOzmoE-0ZRYq6kG4)

rektHQ由社区发起，服务对象为社区人群。我们非常感激最近几天向我们提供知识和支持的社区成员。我们在此介绍你的故事和意见，我们会保护你的身份并推广你的故事，将诚实和准确放在首位。

以下评论文章摘自匿名社区成员，rektHQ非常尊重那些为今日文章贡献思想和信息的人。我们的收件箱对于任何希望与我们联系的人开放，并且我们会匿名处理您发给我们的邮件。

_一如既往，rektHQ对这篇通讯中的内容或观点不承担任何责任。_
________________________________________
**匿名用户1**

从两个方面来看，我对800万美元的退款金额不感兴趣。

首先是因为这对安德烈构成威胁，导致他要求yearn金库协助退还800万美元。我尚未看到威胁的性质，但如果提出退款申索，则会开创一个非常危险的先例，它加强了威胁项目成员是一个可行的行动路线，以获得你所期望的结果这样一种观念。

第二种观点显然是道德风险方面，这在CT上已进行过详细讨论。奥地利经济学家在描述干预主义时喜欢使用"道德风险"一词，用去中心化金融通俗的话来说，就是指degens在越来越多的高风险和未经审计的项目上退化，因为他们"期望"在这种情况下能得到部分救助。这种风险转移在现实世界中肯定存在，各大银行都期望联邦政府能在他们陷入困境时伸出援手。但我们真的想在去中心化金融领域复制这种情况吗？

利用EMN的人都表现出极大的主动性和独创性，但更重要的是，他/她基本上分享了一个蓝图，即如何进行简单但获利丰厚的攻击，并将注意力转移到他们攻击的项目上，任由他们承担所有的愤怒和威胁。我们甚至可能开始看到利用者会给他们刚刚戏耍过的系统打小费这种新常态，类似于盗贼之间不言而喻的行为准则。

无论这起最新的事件在未来几周内把我们带向哪里，都值得考虑它向这个领域的所有危险分子发出的信息，甚至是那些中立的道德流氓，看着这些犯罪者一次又一次地逍遥法外。

**匿名用户2**

从技术角度来说，我觉得由于是先在测试网上部署，所以实现起来不够全面。

不可否认，要想在分叉主网并在本地进行uniswap、balancer或bonding curve测试，还是比较困难的，所以我可以理解"尽可能多的测试"，但真正的测试则发生在prod...

然而，这种说法让低劣的开发人员和欺诈者得以消失，鉴于最近"Uniswap" rug pull的数量太可怕了。

我的意思是事后看来，这是，也不是安德烈的错，考虑到他被炒得沸沸扬扬，对于它可能已经发生了，貌似很有道理。

我的意思是，开发时你能在认知上考虑的事情只有这么多，你更专注于项目路线图，而不是这些额外的degen defi风险，诚然这些风险还在出现。

团队是否在这背后工作，还是会有同样的问题。

我想是时间上有点乱了，大家都不喜欢保持这么多的沟通渠道，尤其是有很多新的开发人员加入了 $YFI社区...

安德烈转发了这张照片，然后人们开始制造一个阴谋，说要给大家一个惊喜。

我个人也是这么认为的，只是加密文化太扭曲了，人们喜欢谜题和匿名，对自己很不利，但这是我的偏见。

退款方面，说明这个项目还是本着诚意继续下去。

也说明这些高TVL degen的行为都是平易近人的。

一般来说，人们冒着巨大风险，不管什么空间，什么资产类别。

你不能责怪人家把掠走的资金返还给那些[#半rekt](https://twitter.com/hashtag/halfrekt?src=hashtag_click)，就像你不能责怪掠夺者一开始就返还一半资金一样。

严格来说，我还没有达到安德烈的水平，睡前就有预感这可能是扯后腿，但实际上，这只是整个偶然性的叙述。

大家真的需要多睡一会了。
