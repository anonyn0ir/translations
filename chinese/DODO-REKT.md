---
title: DODO-REKT
date: 2021年3月9日
tags:
  - DODO
  - REKT
excerpt: 它死了还是刚上床睡觉？DODO被人用假币攻击黑走200万美元，但动机尚不清楚。可以肯定的是，无论是黑客还是白帽，只黑200万美元？必须加倍努力呀。
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-header.png
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-header.png)

**它死了还是刚上床睡觉？**

DODO被人用假币攻击黑走200万美元，但动机尚不清楚。

可以肯定的是，无论是黑客还是白帽，只黑200万美元？必须加倍努力呀。

Twitter仍然是DeFi最快的新闻来源-甚至DODO团队也依靠[Luciano](https://twitter.com/Luciano_vPEPO/status/1369055985684381696?s=20)告诉他们，他们自己的$WCRES/$USDT池被人用假币榨干了。

以下分析摘自DODO的官方发布，感谢[@samczsun](https://twitter.com/samczsun)，[@tzhen](https://twitter.com/tzhen)，[派盾](https://twitter.com/peckshield)和[慢雾](https://twitter.com/SlowMist_Team)。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-linebreak.png)

**该漏洞针对多个DODO V2众筹池，即WSZO，WCRES，ETHA和FUSI池。**

由于这些漏洞，总共黑走约380万美元，其中188万美元有望被退回（有关更多信息，请参见下文）。

DODO V2众筹池智能合约有一个错误，该错误允许多次调用init（）函数。这意味着开发人员可以通过以下步骤执行攻击：

1. 攻击者创建假币，并通过调用init（）函数来初始化智能合约

2. 攻击者调用sync（）函数并设置“reserve”变量为0，它表示代币余额

3. 攻击者再次调用init（）进行重新初始化-这次使用“真实”代币（即DODO池中的代币）

4. 攻击者使用闪电贷从池中转移所有真实代币并绕过检查

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-suspects.png)

**总而言之，此漏洞利用涉及两个人。我们将它们称为“个人A”和“个人B”。**

个人B具有抢跑机器人的所有特征，这是因为：

· 他们使用以开头0s的前缀构造了他们的合约地址

· 他们使用CHI gastoken

· 他们设置了超高的gas价格；在一种情况下，他们提高交易配置到93,148 gwei。

此外，个人B的攻击要比个人A的成功攻击提前大约十分钟。

**个人A**

[个人A](https://etherscan.io/address/0x368a6558255bccac517da5106647d8182c571b23)已经通过samczsun与DODO团队取得联系，并提出退还从DODO池中取出的资金。以下是有关个人A的操作的详细说明：

个人A与中心化交易所进行交互。

个人A从币安[提取](https://etherscan.io/tx/0x970b32a8c81dd3fc47fa118621726fc418ec3526c4379470a4000ed7b448360f)0.46597 ETH：

个人A快速[执行](https://etherscan.io/tx/0x300de107cbca466abe121112848daaf7f5f0d15625d54773dd0bbbff4e276e93)连续7次BUSD提款交易（请参阅示例链接），可能涉及币安桥：

个人A将其资金转移到另一个钱包地址。

个人A两次转移67416 BUSD到0xa305fab8bda7e1638235b054889b3217441dd645- [第一次](https://etherscan.io/tx/0xbee2f507b2f4b4321927a9762dac757df12fe1ba2d6f85314273b9ea542a5c13) - [第二次](https://etherscan.io/tx/0x56dbf6421c6e6bd779ab0c12fd49e1f7714dd85023aa74abae1940f8d88669cf)

个人A两次转移59,245.324743 USDT到0xa305fab8bda7e1638235b054889b3217441dd645 ：[第一次](https://etherscan.io/tx/0x306d08f3d8af85dfdea7a6edb336d7504e8ecc7c609e4b940d188ba68e11cab5) - [第二次](https://etherscan.com/tx/0xaf80cf58c88f0e0f2f44e3902e4c7cd2c17122511fbc6c2d9b2cd43fbc4199b9)

个人A针对DODO智能合约执行了两笔漏洞利用。

第一笔针对DODO-USDT测试合约，并且资金已[转移]到(https://etherscan.io/address/0x328410f276d4fe83fc78fa56ad32d9821a5e5c1c#tokentxns)到0xa305fab8bda7e1638235b054889b3217441dd645。

第二笔针对WCRES-USDT合约，资金已[转移](https://etherscan.com/address/0x910fd17b9bfc42a6eea822912f036ef5a080be8a#tokentxns)到0x56178a0d5f301baf6cf3e1cd53d9863437345bf9。

资金现在位于以下两个地址中：

[0xa305fab8bda7e1638235b054889b3217441dd645](https://etherscan.io/address/0xa305fab8bda7e1638235b054889b3217441dd645)

[0x56178a0d5f301baf6cf3e1cd53d9863437345bf9](https://etherscan.io/address/0x56178a0d5f301baf6cf3e1cd53d9863437345bf9)

**个人B**

个人B最有可能是机器人。 （一个robododo）

**疑似机器人智能合约：** 0x00000000e84f2bbdfb129ed6e495c7f879f3e634

**触发帐户地址：** 0x3554187576ec863af63eea81d25fbf6d3f3f13fc

**个人B针对DODO合约执行了3笔漏洞利用：**

**ETHA-USDT： **

[0x0b062361e16a2ea0942cc1b4462b6584208c8c864609ff73aaa640aaa2d92428](https://etherscan.io/tx/0x0b062361e16a2ea0942cc1b4462b6584208c8c864609ff73aaa640aaa2d92428)

**WSZO-USDT： **

[0xff9b3b2cb09d149762fcffc56ef71362bec1ef6a7d68727155c2d68f395ac1e8](https://etherscan.io/tx/0xff9b3b2cb09d149762fcffc56ef71362bec1ef6a7d68727155c2d68f395ac1e8)

**vETH-WETH，设置93,148 gwei： **

[0x561f7ccb27b9928df33fa97c2fb99ea3750593e908f9f0f8baf22ec7ca0c5c4a](https://etherscan.io/tx/0x561f7ccb27b9928df33fa97c2fb99ea3750593e908f9f0f8baf22ec7ca0c5c4a)

**资金目前在以下两个地址：**

0x00000000e84f2bbdfb129ed6e495c7f879f3e634(https://etherscan.io/address/0x00000000e84f2bbdfb129ed6e495c7f879f3e634)

0x3554187576ec863af63eea81d25fbf6d3f3f13fc(https://etherscan.io/address/0x3554187576ec863af63eea81d25fbf6d3f3f13fc)

目前DODO团队正在试图联系上述地址的拥有者。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-linebreak2.png)

一位匿名用户拿走了相对较少的200万美元。

帽子的颜色可能会根据可用的金额而变化。

小数目=追求影响力的白帽-大数目=拿走再加上数百万。

**我们只能想象这些人正在积累的个人宝库。** 那里有很多机会，而不仅仅是针对那些选择学习编程的人。

值得注意的是，甚至团队本身也依靠Twitter更新了解自己的协议。这提醒我们确实还处于该行业的早期阶段。

扬名立业的机会很明显-您如何使用权力仍由您自己决定。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-conc.png)

图片致谢-[harrikallio.com](https://harrikallio.com/portfolio/dodo-mauritius-island/)和[@BxST23](https://twitter.com/BxST23)
