---
title: AKROPOLIS - REKT
date: 2020年11月12日
tags:
  - akropolis
  - delphi
  - Rekt
excerpt: 自公元前480年萨拉米纳战役以来，阿克罗波利斯从未被如此毁坏过。现代国王泽克西斯又Akropolis彻底摧毁，通过结合使用闪电贷和重入攻击盗取200万DAI。
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/84604-1.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/84604-1.jpg)

佩里克勒斯会死不瞑目。

自公元前480年萨拉米纳战役以来，Akropolis从未被如此毁坏过。

现代国王泽克西斯又把Akropolis彻底摧毁， 通过结合使用闪电贷
和重入攻击盗取200万DAI。

起初，Akropolis的管理人员试图声称他们只是在进行一些"修复"工作。

![](https://lh5.googleusercontent.com/MElhS0VhaZ0DA_lMRYeLoRNafz1YWpafkzgdcV_K9F-HNxz1V7H85KDGkQdP3npLM9Nql6LjtEqzKVUnHMdL8OzlWbsZ9JbFl_L7JQJc_MWKJpYwIRr_AVzsBUvrpEtLpc-xpkDi)

现在我们知道他们被盗取了200万。

![](https://lh5.googleusercontent.com/OGE_yvAkXzHlE9USnNhS0g0NpV3bqHKBj8Z7bAcVT3B0ejQs8bBkWfWJrmqo_83zWyVTq7aOG_JaLTItr7uL_k2TiKOHN7JEqmwp1T6IOY9w9ENZr6ZtbWE2B29XNxAl4ex_UO_r)

但是怎么盗取的呢？

Akropolis协议允许用户将代币存入金库，并获得不同的代币作为回报。你能拿回多少新的代币，
取决于你存入的存款金额。

存款金额是由转账操作前和转账后的余额差额计算的。

下面是攻击者如何利用这个系统，他创建了一份恶意的代币合约，这份合约
再次调用存款函数（重入）。[这](https://etherscan.io/address/0xe2307837524db8961c4541f943598654240bd62f#tokentxns)就是攻击合约。

1. 创建假币

2. 存入假币

3a.获得回调假币，存入2.5万DAI。

3b.因存入2.5万DAI而获得授信。

4. 因存入2.5万DAI而获得授信。

5. 提取5万DAI

向[samczsun](https://twitter.com/samczsun)致谢

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/4d509e7155f551c4d98bb1014b320c61-1.jpg)

因为攻击者能够使用他们的合约作为押金代币，他们能够通过dYdx闪电贷来使用
重入，如下图所示。

![](https://lh4.googleusercontent.com/LxCZ2ZHvBLGPgk7BaoplX3rNuNtfN2JoZ9VeMBZe42MaWMw7ShK_mdgg70RhZJ1DJO4lLn1D8IkAnZ91VKeamI49aW0pDY-7trH07qX2A_ifqbg5xE_1QVLoOxt7qcUBfIYUm8i0)

![](https://lh5.googleusercontent.com/D2wa_EEUSuXUk7r9cRAhX-fwHRv91pmeFeWd1bVR9KFO_IZLXzlzt8I2eJhNfGFP9pOiVokZa58Qn4aFUWlycIIt2gSNNZA5pDSbsy3vqMqsG8eZS1yU8N1qfgQP4_UFbZS0kMfV)

[这](https://etherscan.io/address/0xe2307837524db8961c4541f943598654240bd62f#tokentxns)是黑客的地址。我们可以看到，他们在8小时前就已经开始
对5万元分批执行攻击。

随后，他们将所得中的[200万美元](https://etherscan.io/tx/0xf15623567231c67df2b8bcc5540236fbda2c3ac11ecbec427048f11b582cb869)发送到另一个地址，在撰写本文时，这笔钱仍在那里。

向[@dogetoshi](https://twitter.com/Dogetoshi/status/1326963117356625931?s=20)致谢

![](https://lh3.googleusercontent.com/dSGoJEDMg3SdSHVshM5N8FaLgkai2s1q7gtmCd7-VPKmeNcCew5OXEVAHOQ_Sa9h7iRL021U54658OC8HnVS6MdQSTMxsyjfu6MOKQ-qP5o6Ay0-Jy3NjnVx2dKYEmgAqTrefgjL)

我们应该注意到，黑客所交互的智能合约已由
两家独立的安全公司Smartdec和Certik进行了审核。

Smartdec有着相当不错的[记录](https://blog.smartdec.net/)，但是，对于Certik来说，Akropolis是一个不受欢迎的新代币，
他们在漏洞曝出之前审核的项目名单越来越多。

bZx、Lien、[Harvest](https://www.rekt.news/harvest-finance-rekt/)以及现在的Akropolis。完善的安全审计永远不应该被视为安全保证，但
Certik的审计肯定不如以前那么重要了...

即使是一份制作精良、审核彻底的合约，如果落在奸商中，也会变成一场
烂摊子。Akropolis这么快就对用户撒谎，说明责任并不全在Certik或黑客身上。

虽然我们经常追求无信任的协议，但当涉及到用户和服务提供者之间的人际沟通时，
信任的脆弱性应始终受到保护。

Akropolis已经失去了这种信任，被彻底打倒了。
