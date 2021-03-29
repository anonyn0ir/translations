---
title: 狐獴金融 - BSC - REKT
date: 2021年3月4日
tags:
  - BSC
  - Meerkat
  - REKT
excerpt: 由于Meerkat Finance直冲我们排行榜第三名，这是BSC上首个令人印象深刻的重大漏洞。CZ和他的团队会回滚他们的区块链，抑或用户承担损失？这场狐獴骗局让窃贼无处可藏。
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-header.png
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-header.png)

**回想起来，这是不可避免的。**

这是BSC上首个令人印象深刻的重大漏洞，因为狐獴金融直冲我们[排行榜](https://rekt.eth.link/leaderboard/)第三名。

运营仅一天后，狐獴金融就携带1300万BUSD和约73000个BNB跑路，目前总额约为3100万美元。

我们一直在关注币安智能链，因为他们在以太坊的DeFi之夏速度跟上。现在，他们复制的代码已经积累了足够的资金，进入*跑路*阶段。

**结局很有趣。**

CZ和他的团队会[回滚](https://twitter.com/cz_binance/status/1125996194734399488?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1125996194734399488%7Ctwgr%5E%7Ctwcon%5Es1_c10&ref_url=https%3A%2F%2Fwww.coindesk.com%2Fbinance-may-consider-bitcoin-rollback-following-40-million-hack)他们的区块链，抑或用户承担损失？

**这场狐獴骗局让窃贼[无处可藏](https://www.youtube.com/watch?v=58UD3jU86pY)。**

在这么小的链上他们能跑去哪呢？币安已经关闭了[桥](https://twitter.com/madcapslaugh/status/1367448466453106693?s=20)，甚至[bscscan.com](https://bscscan.com/)都宕机了一小会儿。这是太拥堵了，还是某种类型的烟雾弹？

狐獴金融首先声称这是一种黑客行为，但随后删除了他们的帐户，只剩下BSC用户自己，也许该谴责的是币安。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-investigate.png)

感谢[0xdeadf4ce](https://twitter.com/0xdeadf4ce)。

· **狐獴金融Deployer升级了该项目的2个金库。**

· 攻击者地址通过金库代理调用无需许可的初始化函数，该代理允许任何人成为金库所有者 [2](https://bscscan.com/tx/0xfcf48681e382e9f9cc1d6a64ff30487306f6b869924c6594075fcc86b3b21f5d)。

· 随后，攻击者通过调用签名为0x70fcb0a7的函数来抽干金库，该函数接受代币地址作为入参。升级后的智能合约的反编译显示了该金库调用函数的唯一用途是挪走资金，金库所有者为受益人。

通常，如果合约具有允许所有者取出用于策略/金库主动管理的资产，那么您就是在信任项目团队。

他们可以随时拔插头。

这就是为什么Yearn之类的项目会添加如下图所示的校验的原因，以便团队只能挽救那些未被策略/金库主动使用的资金。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-code.png)

两个受影响的金库都使用OpenZeppelin的透明代理升级模式，通过在金库代理级别调用upgradeTo（address newImplementation）函数，可以将金库逻辑升级到新的逻辑实现。

BUSD金库的先前实现位于[0x49509a31898452529a69a64156ab66167e755dfb](https://bscscan.com/address/0x49509a31898452529a69a64156ab66167e755dfb)，WBNB金库的先前实现位于 [0x3586a7d9904e9f350bb7828dff05bf46a18bb271](https://bscscan.com/address/0x3586a7d9904e9f350bb7828dff05bf46a18bb271)，两者都是不起眼且经过验证的合约。

猫鼬金融Deployer两次调用upgradeTo（）：

· 在区块高度5381239，设置WBNB金库实施版到0x9d3a4c3acee56dce2392fb75dd274a249aee7d57(https://bscscan.com/address/0x9d3a4c3acee56dce2392fb75dd274a249aee7d57)

· 在区块高度5381246，设置BUSD金库实施版到0xb2603fc47331e3500eaf053bd7a971b57e613d36(https://bscscan.com/address/0xb2603fc47331e3500eaf053bd7a971b57e613d36)

它改变金库逻辑，引入两个值得注意的函数，他们并不是初始实现的一部分。

· init（address owner）

· 根据反编译的字节码，此函数将存储插槽0上的地址设置为提供给该函数的地址。

**并没有权限检查，使得新添加的函数成为金库的最终后门。**

在透明代理中使用特定的Initializer模式是最佳实践，并且已在第一个金库实现中应用，因此很令人怀疑的是，除了谋划窃取金库资金外，打算添加init（）方法的意图是啥。

· 0x70fcb0a7（address _param1）

获取不到源代码，反编译源代码仅限于检查调用者是否等于init（）方法中设置的存储插槽0，以及转出的使用param1作为代币合约的balanceOf()函数入参，并使用Vault作为查询目标。这两个函数都不是以前的金库实现的一部分。

比较旧的和新的实现的字节码大小，可以说新的实现仅是先前逻辑大小的1/4。

由于升级是由狐獴金融Deployer完成的，因此鉴于链上数据的各个方面，最有可能发生的情况是蓄意“跑路”，而私钥泄露的可能性很小。

截至撰写本文时，资金已部分地分配到各个地址中，并发送到了由币安交易所托管的看似属于币安桥的地方。

[Binance.org](http://binance.org/)桥目前已被暂停，可能是阻止资金轻易转移到其他链。

**时间轴（2021年4月3日）**

**2021年4月3日上午08时53分10秒（UTC时间）** 狐獴金融Deployer升级WBNB金库合约至0x9d3a4c3acee56dce2392fb75dd274a249aee7d57

**2021年4月3日上午08时53分31秒（UTC时间）** 狐獴金融Deployer升级BUSD金库合约至0xb2603fc47331e3500eaf053bd7a971b57e613d36

**2021年4月3日上午08时54分31秒（UTC时间）** 攻击者调用BUSD金库上的方法0x70fcb0a7转移出13,968,039 BUSD

**2021年4月3日上午08时54分55秒（UTC时间）** 攻击者调用WBNB金库上的方法0x70fcb0a7转移出73,635WBNB

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-linebreak.png)

**相同的游戏在不同的链上进行，但是力量平衡是不同的。随着CZ的关注和烧掉桥，强盗无处躲藏。**

即使在[狐獴跑路](https://t.me/Meerkat_Rugpull)电报群中，聊天成员也没就希望Binance如何处理这种情况达成一致意见。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-poll.png)

**币安能回滚链并退还他们的用户资金吗？**

答案尚不清楚-理论上讲21名[神秘验证者](https://docs.binance.org/smart-chain/validator/guideline.html)可以安排退款，但这不太可能。这只会助长CeDeFi问题，并为（可能已经感到压力很大的）BSC律师制造更多工作。

Binance将预先计划如何应对这种情况。他们如何处理这种情况将开创先例。

尽管这不是BSC上第一个[数百万跑路](https://twitter.com/news_of_bsc/status/1354880400984739842?s=20)事件 ，但它是PancakeSwap兴起以及随之而来的用户数量增加以来的第一个。

忽略币安有人加紧安排Merkle分发并归还资金这一不太可能发生的事件，这笔钱找不回来了。

**因此，我们发现BSC上的协议并不比以太坊安全。**

CZ不会救您。他们的交易价格便宜，但是没有原生开发。

一旦Eth L2到来，这个企业链将会变成什么样？

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-rektkat.png)
