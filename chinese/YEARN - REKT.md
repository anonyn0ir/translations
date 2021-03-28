---
title: YEARN - REKT
date: 2021年2月5日
tags:
  - yearn
  - Rekt
excerpt: 没有大而不倒的协议。闪电贷的强大功能使蓝筹股褪变为黑筹。即使强大如Yearn也沦为套利者的受害方。Yearn会被CeFi保释吗？
banner: https://lh6.googleusercontent.com/2htMKXFnd_RYudETxssIO-ztLBIhBXwlq4jADQmX80p682WvwhLmjSjoYhE5spF_f_Yfan8DLIe4B2NwLLIec9tH5wt9H_RyRertgtKzELIVQrq3XTwFhwULAoP9BHzzmCeyqsWg
---

![](https://lh6.googleusercontent.com/2htMKXFnd_RYudETxssIO-ztLBIhBXwlq4jADQmX80p682WvwhLmjSjoYhE5spF_f_Yfan8DLIe4B2NwLLIec9tH5wt9H_RyRertgtKzELIVQrq3XTwFhwULAoP9BHzzmCeyqsWg)


**没有大而不倒的协议。**

> _闪电贷的强大功能使蓝筹股褪变为黑筹。对Yearn DAI v1金库的套利攻击表明，即使我们最有经验的开发人员仍然会犯错误。_

黑客使用9笔闪电贷攻击该金库。金库共损失1100万美元，其中攻击者获利270万美元，Curve流动性提供者得到350万美元，Curve质押者得到350万美元，支付Aave v2闪电贷手续费花去140万美元。

**DeFi系统处于恒定变化之中，日益增加的相互交织的协议创建了一部拥有无数运动零件的永动机。**

我们行业的发展步伐迅猛，每天都有新想法和潜在的攻击行为出现。

不断变化的环境意味着即使经过时间考验的产品也不能保证绝对的安全性。

**对于曾经被视为不可战胜的团队来说，沦为套利者的受害者必定是一种耻辱，但是我们也并不乐意指出那些在我们领域创造如此巨大价值的开发人员工作中存在的缺陷。**

尽管未提及闪电贷，但Yearn团队已发布了他们的被黑后的分析版本。

Igor Igamberdiev在Twitter上对此次攻击进行了更详细的分析。

攻击者获利：

-51.3万DAI

-170万USDT

-剩余50.6万3CRV（每个价值约1美元）

攻击者执行了11笔交易。

1 /从dYdX闪电贷11.6万ETH

2 /从Aave v2闪电贷9.9万ETH

3 /以ETH作为抵押物在Compound上借入1.34亿USDC和1.29亿DAI

4 /向3crv Curve池中添加1.34亿USDC和3600万DAI

5 /从3crv Curve池取出1.65亿USDT

6 /重复五次

-存款9300万DAI到yDAI金库（每次少一些）

-添加1.65亿USDT到3crv池

-从yDAI金库取出9200万DAI（每次少一些）

-从3crv池取出1.65亿USDT

7 /最后一次不是取出USDT，而是提取3900万DAI和1.34亿USDC

8 /偿还Compound借款

9 /偿还闪电贷借款

每次操作攻击者拥有更多3crv代币，这样以后他可以将其兑换成稳定币。

攻击者合约： https://etherscan.io/address/0x62494b3ed9663334e57f23532155ea0575c487c5Attac(https://etherscan.io/address/0x62494b3ed9663334e57f23532155ea0575c487c5Attac)

Tornado交易＃1

https://etherscan.io/tx/0x7ee28e342573ff7b8fb4bd2e4373e742cf80d8f8c7f8764cc6b70439dc33f037(https://etherscan.io/tx/0x7ee28e342573ff7b8fb4bd2e4373e742cf80d8f8c7f8764cc6b70439dc33f037)

Tornado交易＃2

https://etherscan.io/tx/0x13c12895d44f8b890af2187b93b97bec01dd34eeb026ac9669d8412e57d64446(https://etherscan.io/tx/0x13c12895d44f8b890af2187b93b97bec01dd34eeb026ac9669d8412e57d64446)

Tornado交易＃3

https://etherscan.io/tx/0x6b07e3faaa419ea5a3d58929e07b872f8529441064eb576d61ef5edd697f7256(https://etherscan.io/tx/0x6b07e3faaa419ea5a3d58929e07b872f8529441064eb576d61ef5edd697f7256)

Tornado交易＃4

https://etherscan.io/tx/0xcacdc95bd65556426bae39025ddb1deafb65acb908be49fb7186bb750fault(https://etherscan.io/tx/0xcacdc95bd65556426bae39025ddb1deafb65acb908be49fb7186bb750fault)

出现套利机会是因为金库迁移时取消了赎回费。

**读者也知道闪电贷之下并没有什么新意**，因此，能够阻止这种情况发生的Yearn开发人员也如此。表明这只是一个利用金库迁移过程中所犯错误的机会主义者。

流言和看戏在DeFi社区仍然有较高关注度。许多人认为这次攻击是对Cronje较早前批评Julien Bouteloup,Stake DAO的一位贡献者，虚伪的报复。

![](https://lh6.googleusercontent.com/JTjkSs0iTtatTK92Vs53mx1qb5FlCSkjxf9-BTxvo2BgB69Ftki6dPveLUvORlGpo4eH906UxH8ckMkkxwacqYO7e-itzE4eWMCZbbuQ4twuwni6lWYZAAwPaPJVInaOdAhqqxAH)

尽管我们的许多读者（和您的匿名作者）会暗中乐于观看两个开发人员之间的争斗，但事实证明，这些怀疑是错误的，因为在提出批评之前的几个小时攻击者的帐户已获得资金，并且合约已写好。

![](https://lh6.googleusercontent.com/qK0b6N34P6dMIF4bt_pK08fPtPbcmI1dOmmXx3lThk76IKdsmEEyVpbl_5Yz9CqEFJoH4jQE0thf2uL30EnUd_h2Zq0ayyHk6PF14iiP7ZYSAzAktdMZzXTxA23UDgRt5IgUdcOE)

作为我们行业中两个最杰出的开发者，势必会有一些竞争。对他们工作的热情以及把名誉与编写涉及上亿美元的代码联系在一起的责任使工作关系承受了巨大的压力。

**还值得注意的是，并非所有最好的开发人员都在Twitter上。**

**如果DeFi协议从中心化公司收到退款，那么在什么时候它不再是DeFi？**

Tether冻结了在黑客攻击中被盗的170万美元。过去，Tether也曾补偿过误将代币发到合约地址而受损失的用户。

**如果Tether销毁这些被盗的代币并铸造相同数量的代币以将资金返还Yearn，那么它们与任何中央银行都没有什么不同。**

Yearn开发人员@fubuloubu过去曾反对使用Tether，但在这次他们介入之后似乎改变了主意。

![](https://lh4.googleusercontent.com/EQrZYxGPLP25hIXWLkUI5DUQbVBX8tDe6x_yOJf-P-ebQ9LvaRc0EXcN2N188mDCp1rXFMG92dq7l08jkrygHMXahVYECcHtNQbAcCwjVsWHeZPmhuC_gyRWfDXK2fSXWpVwGbay)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/image.png)

当去中心化让我们获利的时候我们都喜欢它，不过退款的时候最好能中心化。

**这次攻击直接进入了最大的DeFi集团之一的心脏地带，动摇了曾经被视为坚不可摧的堡垒的基础。**

即使是业内最优秀的公司也会犯错，但这不应阻止我们鼓励他们开发。

当紧张局势加剧并且DeFi团队开始站队反对另一方时，我们所有人最好开阔视野并着眼更大的布局。

我们制造抗衡[传统金融](https://www.rekt.news/cefi-rekt/)的武器。我们不应该通过内斗来遏制创新的潮流，真正的战斗是[我们对他们](https://www.rekt.news/stable-coins-the-empire-strikes-back/)。

最终，当我们回首这一时期，只剩下对所有在如此早期阶段抱有上述愿景的人们的尊敬。

昨晚Yearn的盔甲出现首次裂痕。他们的过错会使社区失去信心，还是我们都可以团结起来支持这家DeFi巨头，并帮助他们变得更强大？

![](https://lh5.googleusercontent.com/gwQf4mTtg264KPREnhva2DtM_OLqf7XuW2GCxxaHxhldpl46z-mwe5Mva9_Y61jzO5oIqO5GONSjtrQk-eTKtk1nQyaFnzcCaZm9oG-0dBxTOcCW_6hTAz2VkaI1_Oe6va25J5LD)

