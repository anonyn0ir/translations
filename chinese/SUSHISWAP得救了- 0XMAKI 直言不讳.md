---
title: SUSHISWAP得救了- 0XMAKI 直言不讳
date: 2020年11月29日
tags:
  - sushiswap
  - 0xmaki
excerpt: 刚出了油锅，又进了火炕。匿名开发人员0xMaki在创始人Nomi大厨放任贪婪后，承担了SushiSwap的主要开发工作。
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/header-6.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/header-6.jpg)

**刚出了油锅，又进了火炕。**

匿名开发人员[0xMaki](https://twitter.com/0xMaki)在创始人Nomi大厨放任[贪婪](https://twitter.com/NomiChef/status/1304442495342796800)后，承担了
SushiSwap的主要开发工作。

在去中心化金融夏季结束并且菜场倒闭后，很多人以为SushiSwap已经
死去。然而，他们的开发人员从未[停止](https://twitter.com/zhusu/status/1329932138171404290?s=20)过建设，最近，SushiSwap带着新菜谱
卷土重来。

**いらっしゃいませ（欢迎）!!!**

然而，在Omakase bar的日子并不轻松。

**昨天深夜，一名匿名的行动者在他们的智能合约上戳了个洞，
偷走了约1.5万美元。**

Rekt联系了0xMaki，想听听他的说法。

![](https://lh5.googleusercontent.com/bLAbz--dDRJoIQjlauDxi08j9x-pObms6J3_LmI2hhMGNs5kCYYxs-Dz13TsdF6IRgQ36NlQ-CiJpWUCZ9IVZaYGMju15bhw3vwVmG6WzAigF_sPkGojiOPjj6Ve3vdCiUJEOBZN)

**0xMaki**：自从[南森](https://research.nansen.ai/sushiswap-farming/)报告出炉后，我就一直在为Sushibar提供服务，以便
减轻套利者的机会。我曾见过一些规模较小的异常交易，但
认为这并没有什么不妥，因为Sushibar还在正常运营。

第一个micro-tx大概是2-3天前送来的，但昨天变成了自动化，比如说
"工业级"。

这里第一次[提到](https://discord.com/channels/748031363935895552/753626532500734014/782428289868365884)了一个关于Sushibar的问题。（[Discord](https://discord.com/channels/748031363935895552/753626532500734014/782428289868365884)）

**Monstar**

@0xMaki源 義経sushibar到底是怎么回事？里面有各种异常交易， 
而且看起来那些在sushibar里盯着的人并没有从他们那里得到任何寿司

[TX 1](https://etherscan.io/tx/0x3534241a7354a8f9c8a9d0209730167a888d923b08c19c20623cd78637faadd0)

[TX 2](https://etherscan.io/tx/0x3ffcfc9985622ad7cf0fdc2eb582ad7ce8bf9e9295fd7a4de44354fdd71a688a)

[TX 3](https://etherscan.io/tx/0xc75a8ca881d4da75774f51006651c9946311d40145ce69d07aee3a85627153d6)

**0xMaki 源義経** 回复了Monstar

它按预期工作，据我了解，只是非常非常非常非常小的数量，

看起来像一个失败的TX，看着它

**Monstar**

我认为那是不对的

因为sushibar里可供索赔的金额与这些交易相比
明显下降

他们好像是在宣称自己是LP代币（不知道怎么会这样）
而不是以寿司为名

所以，它不是转换为寿司并奖励质押者

**0xMaki 源義経**

目前在找对象

也许它只是表现得很怪异的无聊应用程序。

**Monstar**

我想人们想出了一个方法来绕过无聊的应用程序（已编辑）

而不与Sushibar里的所有人分享寿司。

但我不知道如何复制他们正在做的事情，所以我不能测试它。

是的，他们绝对是

[https://etherscan.io/tx/0x7c6af5ca27ceb04aad514ddcaee8afc6dd4eb79d0816e24b007e7db205e93ce3](https://etherscan.io/tx/0x7c6af5ca27ceb04aad514ddcaee8afc6dd4eb79d0816e24b007e7db205e93ce3)

[https://etherscan.io/address/0x1925e832c22522e0d9947ee4677120b2f28e4cd4#internaltx]
(https://etherscan.io/address/0x1925e832c22522e0d9947ee4677120b2f28e4cd4#internalt)你可以
查看该钱包的所有索赔（已编辑）

**0xMaki 源義経**

@Monstar 我们目前已制定一些步骤进行修复，资金没有问题，只有一个利用
Sushibar索取费用的问题，虽然令人厌倦，但这是一个很好的bug赏金。

今天，我们将放弃约10000美元，因为有人在Sushibar里

**Rekt**：谢谢你的链接。你的第一想法是什么？

**0xMaki**：我的第一印象是，Sushibar不可能出现问题吧，
对吗？一定是在前端...Tx是没有任何意义的。但后来Sushibar没有捞到钱的时候， 
里面应该有更多的钱。

大约15分钟后，我意识到情况不妙，于是我马上联系了[Banteg](https://twitter.com/bantg)。

![](https://lh5.googleusercontent.com/2nOrhx84dL0WXXOLQy-RuEuZQo05qVC2rS7DtAYxQ207NRzWglhhEUhIO6dsES1F9ls81HYZINxkn5f2idaSXxlcgKuDDUVTe160boHCzME0RqL8Ci6R-gdZlcXTYl2Aj4jJStv5)
![](https://lh5.googleusercontent.com/e9ULQE7bDt7_iZJyvYGz3oph9OzHxyilopiD0JmhhOv09ZfsJxtFS9ubho8a4eof3YflICXhptgZsU4ZhApjNGyYtpkEscsW7s8SOoG1pn120KB57RyRvZLu5yumbm9jz0hVPcPg)

Banteg也没办法，他的时间是早上6点，他当时忙着处理pickle。所有的寿司开发人员都在睡觉--欧洲/东京时区，只有我在北美。

**Rekt**：你找了谁来帮忙？

**0xMaki**：我找来了[Andy](https://twitter.com/andy8052)，他目前在yEarn担任策略师；他是前makerdao智能合约工程师
和前Coinbase员工[Daniel Que](https://twitter.com/danielque)

**Rekt**：花了多长时间才修好？

**0xMaki**：花了3 -4个小时进行复制并找到问题。

**Rekt**：损失了多少钱？

**0xMaki**：只损失了1.5万，因为Sushibar每天只累计2-3万。0.05%用于
奖金池，而且这一切都需要手动完成，有tx失败的风险。

**Rekt：黑客攻击还是漏洞利用？**

**0xMaki**：完全是漏洞利用，聪明的家伙，他应该得到资金。我想我已经找到了
他...

**Rekt**：你是羡慕不已还是觉得尴尬？

**0xMaki**：羡慕不已！我不可能感到尴尬!能目睹这些黑客攻击/漏洞利用确实令人深刻印象，
即使有强大的审计，也总会出现一些
我们未必会计划或想到的新情况。

这使得生态系统更加强大，更有弹性。

我们只从这个攻击者那里损失了1.5万，也许还有其他个人也在做同样的事情，
我需要仔细观察一下--我们发现这个人，因为他开始影响到了
整个Sushibar。

总之，在我所在地的时间23:28左右，我们（0xMaki和Andy）开始修复这个问题。

![](https://lh6.googleusercontent.com/AfYQkR2nEmDTLYAIcqA0n-6GtaGpsDSSDB6Y-NykyBE2znVpyhpTcqNTSt_Wx-8B2V1OSScQyW8Ekxvgr8NiK-pABsM26u4aGxzIckiwstGUMhB_0MqLAOxGJjxSfQRm0MMXUR1v)

然后我们检查了规模较小的交易，只是想确认一下它们是否是良性的，然后--
该死--原来他们不是。

安迪刚坐飞机回来，他受到时差之苦，熬不住了，只好去
睡觉，所以只有我一个人，直到...

![](https://lh5.googleusercontent.com/AoC4V0gDiIzCSg0MedJONypm9V7KpfN4kQZc3qmeRvGN2CyaHsOGQv_0fEosKO6766h3M_VynadJdaKHAnj7aUg7_Po7BCzDCLOjzKfCXlC_1AbQKjuG-57IN4TvEhqyDppvaIDj)

（[Samczsun](https://twitter.com/samczsun)）

**Rekt**：他是怎么发现的？

**0xMaki**：因为我已在没有任何.sol jedi的情况下被抛弃了，我就联系了他

**Rekt**：.sol-diers

![](https://lh6.googleusercontent.com/XmqXGATsYH7SArH7jLF82J1KLSczUODpWDI6AfY4yXUSJYrPQNoAt-TE8sueyr97jK83hDBrAK4lYtm0XfZvxGRhbPM3jNbpLuCHd4eHO4e1lSuTkrYE0KpiA384Y4et4IYy8Kw4)

![](https://lh4.googleusercontent.com/AVz2977b1kJ93j9w8YlTFnQ728CBJhIKkie-4Gn-MDdqIErJbSXCYr-qLbTpxiCT70IPzzmQy6aBZ7jtrO0V4ZQsXY1FSoCawBsVPv3uwkAxYzoA3Lrsd7qRFd5-ikwliik1l0rQ)

![](https://lh4.googleusercontent.com/CzyFAdpwpd5iAHD-S5EHgPAnlPl_B_IhbS8rNOsE5T5g-X_HLimDvQi6hIm8sQu_GCBTog_KKRxDwj1gXafHuywBpCdHFmthdL-GylfH0h6gkX-Ep91ucovdYvan78k_cdzHzPJg)

![](https://lh4.googleusercontent.com/Cv4Ty0uF7kAY9EMIETzT26Eabe2jnfyQtFGsoA6qRJSrG1Lk7GIQlIKlLtngeneyL-kz5Q7m1S5dft6pooiYQ7r9jQMzHQsnTSjXgpjx1kVT4VOy6cHJ650KAwL_ErFcKCJbJltE)

**0xMaki**：但很遗憾...当时已经很晚了，他像任何一个正常人一样在周六晚上有计划， 
是吗？

回到原点，没人能帮上忙...

试过Nomi大厨，所有核心开发，在主团队频道留下分步流程， 
希望有人醒悟

然后我想起了[丹尼尔](https://twitter.com/danielque)，他从一开始就一直在跟进我们，所以我
联系了他，接通了电话，向他做了简要描述。

![](https://lh5.googleusercontent.com/j49oC75qzLg9IBSO0zD5190VA4aZK2jETW8GG4S1XHZPEAKRKuu1Ney6hjysi_J3rn2DLUZ9WJDUFGgaR8ug8bIFNgdIGWqJ7tzgFHKkAURTBsmFKnHHp9Aj62Uh5Cy_UHpvl0dm)

Rekt：你还在和Nomi说话吗？

**0xMaki**：没有了。

![](https://lh5.googleusercontent.com/KxNo_yX9tboZIjfc6xvqsUs_Z13C9OSb28xmCCuF_1UFKbhDNs_el1Nd7nFflSzBGefGiA5r3w7deozbKxFk-SfGPTxDg-DzXWVFyUP3EzkHdRLjFFvtcu7hqMSq8KEgMsYh-zgo)

**0xMaki**：02:35，我们已进行复制！！！。我们已经弄清楚这个漏洞是如何运作的，并且
能够进行复制，所以我们可以做修复工作。

03:19我们已修复。

![](https://lh6.googleusercontent.com/KmbawxTOw3xF7yC0w63X6K_XzBY85q5G4c4LAuWLqWEnq64DZcNbbUxnAHVY6iKnNUZdle8IgJrm1yf2E5VqA9skhtkLDFWwkex7tVZxfDb2TYI3sE_ML3AAoF4PJV0NTHNcNmhW)

**0xMaki**： 事情看起来好了很多，团队正在觉醒，并且正进行修复工作。同时
--我转向我们的剥削者，看到他主要是SNX和ETH的持有者。

我浏览了他的tx--这不是一个为了黑客而做的账户，这是一个人在瞎折腾
并寻找漏洞。

**Rekt**：你凭什么这么说？

**0xMaki**：小费。他在SNX和ESD中收到了很多小费，所以他是一个在两个社区里
经常出入的人，极有可能是Discord。

我对照了谁收到和谁在多个日期发送了某些小费，果然...

![](https://lh4.googleusercontent.com/v8i6j6fMZvLnlXWy2qTbgcKVCTOoVmuNzCrBFKGpa3UJ_VGt_wW59AO2pIepBC7DObq-eKnV_aX7xX2P5iOL-z6-U4ArJd_hWbCL0N6IeQDrY4qlzRyNdEA0nX5f4MOD0jJ91k7x)

一个来自SNX社区的内部人士帮我确定了小费的接收者。

![](https://lh5.googleusercontent.com/HEooziQ-CV7OH0y1_D-Fo9uhj8kEYEE2kqmQkge3MDEB-avcdoOOQFvaPnxhkLeG3Ld41GDuZ4t5yS8EiuaieOuIBn2m0mDfFEIzjB1XLGqrzrBRorAosQo_xDC63AXm3p_K2tWI)

就这样，整个团队都醒了，我们制定了一个[初步的](https://etherscan.io/address/0x280ac711bb99de7c73fb70fb6de29846d5e4207f)修复方案，而攻击也已经
停止了。这时，这个消息传到了[推特](https://twitter.com/Juan_Snow1/status/1332992258115657730?s=20)上。

**编者注**此后我们从嫌疑人获得了以下无可争议的证据--。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/image-1.png)

"不可能是我"

**0xMaki**：由于这笔钱属于纯利润，没有人损失任何资金，因为这笔钱
注定要给xSushi的持有人。我们将从库房中送出价值1.5万的寿司--
按比例分配的。

**Rekt**：那就不严重了，吃点小菜吧!对嫌疑人有什么最后要说的吗？

**0xMaki**：联系我吧！我们还有更多的智能合约让你去探索，而且我们支付bug赏金!

我还要[感谢](https://twitter.com/0xMaki/status/1332993111950319618?s=20)所有参与报道的人，包括攻击者。
