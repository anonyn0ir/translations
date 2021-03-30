---
title: HARVEST FINANCE - REKT
date: 2020年10月26日
tags:
  - harvest finance
  - 闪电贷
  - 黑客
excerpt: 收割机对收获不闻不问。一位技术娴熟的耕作者利用闪电贷，从FARM_USDT和FARM_USDC池中收获了3380万美元。
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/10/reaper-3.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/10/reaper-3.jpg)

**收割机对收获不闻不问。**

一位技术娴熟的耕作者利用[闪电贷](https://etherscan.io/tx/0x9d093325272701d63fdafb0af2d89c7e23eaf18be1a51c580d9bce89987a2dc1/advanced#internal)，从FARM_USDT和FARM_USDC池中收获了3380万美元。

在动荡不安的时代，一些人转向神圣之文以寻求指导。

在破坏古埃及收成的十场瘟疫中，第一场带来了鲜血，第二场；
青蛙

罗斯柴尔德男爵建议人们在街上血流满地的时候买入。

如今，去中心化金融夏季盛世已圆满落幕，DFI-PERP的流动性已趋于平稳，而
觉悟的耕作者已明显地变得非常残暴。

在《出埃及记》7:25 8-15中，我们读道

> _"我将用青蛙给你们整个国家带来一场瘟疫。青蛙会爬到你和你的人民还有你所有的_
> _官员身上。"_

在我们的密码学元年，开发人员就是官员，正如古卷中所预言的那样，Harvest Finance
的开发者们肯定已经把青蛙都抓起来了。

![](https://lh4.googleusercontent.com/EEKvX8W_B4lZHA9MSaEJA9qThrhZa6rh-AoQOczdOT6lSxVwJ4F9O1tY4uUSdJ0-xuv7VGP9Mo89i63_LF-W-Rqgq28qoytLxTBpggpZeA4pz9ndUb1_jiN7itRThjNxu3MV33PU)

**套利分析**

fUSDT[下跌13.7%]((https://twitter.com/jiecut42/status/1320574109005348864?s=20))，$FARM[下跌67%](https://www.coingecko.com/en/coins/harvest-finance)，两小时内黑客拿出5000万美元USDT闪贷，
然后利用Curve Finance Y池换取资金，将稳定币价值拉大。

[这里](https://ethtx.info/mainnet/0x9d093325272701d63fdafb0af2d89c7e23eaf18be1a51c580d9bce89987a2dc1)提供了详细的交易分析。

以下行动持续了7分钟。功劳归于[@valentinmihov](https://twitter.com/valentinmihov/status/1320667338321154048?s=20)

1. 将1140万USDC兑换成USDT ->USDT价格上涨。

2. 将6,060万USDT存入金库。

3. 将1140万USDT兑换成USDC ->USDT价格下跌

4. 从金库中提取6110万USDT -> 50万美元利润

5. [冲洗并重复32次](https://etherscan.io/address/0xf224ab004461540778a914ea397c589b677e27bb)。（无需事先测试）

6. 通过Tornado Cash[转换为renBTC](https://app.zerion.io/0x3811765a53c3188c24d412daec3f60faad5f119b/history)并退出到BTC / [ETH](https://etherscan.io/tx/0x5abe6f9b498471042f6c9f68c63fc3d84398b95a3a9e58c621cee09b3c972879)

由于USDT的兑换价格，攻击者能够在第四步提取更多的USDT。由于撤资时USDT的价格较低，他们的股份
代表了金库池中更多的USDT。

大约4个循环可以容纳1千万的GAS限制，虽然每个循环的利润不到1%。
每次重复~50万美元，增加得很快。

LP存款和取款的价格计算机制是利用的源头，也就是说这种攻击可能会延续到renBTC池、FARM_TUSD池和FARM_DAI池。
然而，黑客在耗尽FARM_USDT中和FARM_USDC池的2500万美元或17%的可用资金后选择了停止
，尽管如果他们愿意的话，可以很容易地继续将整个池子的资金抽干， 总金额为4亿美元。

FARM_USDT策略的代码如下

![](https://lh3.googleusercontent.com/3WZVjYk0XPg_KMkyG8owAtDZUdOPU_PlUaMwHSkl4IYQjAJTeS_yj96Gu0sHTlfukzmqtxdcMUfpVhfmZrAaw05ImW5ceVByqOuEyad2GevtkP0wb_lj_EuqRrI5PB6Su1nCh_vT)

这表明计算了一些价格指数。

然而，由于他们指定了"tokenIndex"，我们可以假设他们不只是使用get_virtual_price()，而是
做了一些基础计算。功劳归于[Andre Cronje](https://twitter.com/AndreCronjeTech)

![](https://lh4.googleusercontent.com/RI7-hbXD-8H7Oi3O_mnwPND-Ik4LyPffaqYUX4C9AoT182ohHliSF-9YrArkfQem8CZhY95vlmkTQtIe9ttvxuwBPDSkdI55zYstQzIRThZEXpyFJiScbmtP4pwcHkF2qNvSrph6)

套利检查功能容许范围不够高， 
但默认滑点容许范围3%则太高。

功劳归于[PancakeBunnyFin](https://twitter.com/PancakeBunnyFin/status/1320615021588537347)

从他们的行为中获利的不仅仅是黑客。LP和Harvest开发人员也得到了一笔合理数额的资金，因为黑客
选择以USDT和USDC向Harvest部署者
抛回一些残羹剩饭（2,478,549.94美元）。

Harvest此后表示，将使用快照按比例返还给受影响的用户。

> 没有黑客。只有在[@harvest_finance](https://twitter.com/harvest_finance?ref_src=twsrc%5Etfw)上简单的* 2400万美元（0x53f）诱人套利。

> 5000万美元的USDC闪电贷 [@UniswapProtocol](https://twitter.com/UniswapProtocol?ref_src=twsrc%5Etfw) 
> 兑换1100万美元（USDC/USDT） [@CurveFinance](https://twitter.com/CurveFinance?ref_src=twsrc%5Etfw) 
> ~6100万美元的fUSDT Vault 
> 兑换1100万美元USDT/USDC 
> yUSDT 提取$6100万，获利$50万
> 重复并洗干净[@TornadoCash](https://twitter.com/TornadoCash?ref_src=twsrc%5Etfw) 
> - Julien Bouteloup (@bneiluj) [2020年10月26日](https://twitter.com/bneiluj/status/1320686478486347778?ref_src=twsrc%5Etfw)

**幸运的流动性提供者收益**

大致数字如下。功劳归于[Jiecut42](https://twitter.com/jiecut42)

黑客--24 000 000美元

Uniswap LP--6,000,000美元

Harvest开发人员--2,500,000美元

Curve LP--1 000 000美元

Ethereum Gas--100,000美元

RenVM费用 20,000美元

![](https://lh6.googleusercontent.com/O91Z60MeY81zTI2Lu6g3OAAxdJec9tJjcWcY6rbgRPZYW-i8tShq44_XVuhbx2oUao-CsKSqzhPYyHHZRSbvuMrIUwGeOd2npe4Z7KXOox7S_NKK95IEx6ooqh_5MlN8qgtizZu0)

功劳归于[BitcoinWhiskers](https://twitter.com/BitcoinWhiskers)提供这张美丽的饼状图。

由于接触到所有的[Curve](https://www.curve.fi/)池，veCRV持有者已经从通过Curve的额外交易量中获利， 
因为黑客产生了约50万美元的交易费，这些费用将由所有
质押CRV的人分享。Curve交易费比前一天增加了8000%以上，因为黑客
[兑换](https://etherscan.io/tx/0xb460b70f11a93364fecf1f3c3ec49f053aecd2d6d9912c012170aa7a0de2d526)1亿多美元的USDT和USDC。

![](https://lh4.googleusercontent.com/P9kpiXDdXJYtJTO1byo7ylD8Ht4_vJNDbSZZtUcG2MzXflb5VxaW634Su-jKF3W9yNKAeJ49BKnQjiaPBYy3w018NmCpTXJ2bcK9kjniEy6E2hENqHwYk2yJebULie9UzMaFm55m)
![](https://lh4.googleusercontent.com/Az3qJ6dKLbNiXRkUOshi9tgw5Qg0WcRbxF2KhGoxT4GJQ4dOdLT_CpGK6fFkwHHsrnfN0mhcTIZaBdRq-QYWqH7_bCWft16ow-zNO7R0i6YGTBdQGjysjheUKSbZjCJ8V0cyOSws)

Uniswap LP也因为这位匿名超级耕作者的行为而大发神威。

Uniswap的总交易量在24小时内从1.48亿美元飙升至10亿美元。

其中92%的交易量来自USDT/ETH和USDC/ETH交易对， 
产生了576万美元的手续费。

![](https://lh3.googleusercontent.com/fZW3t_eeYeEjsBaluQwSbmHCc2ZP7H5PNBeFUvw0uSxxJqwNs4mL6UvIKWTWGHZ_7rLGpMuveEAzJ_GVLNJbEZOfRi9S8zYV7BWyknpQCgctrsomzLm4Dzbi6qNwuzbzG8gOFGeI)
![](https://lh3.googleusercontent.com/T9IWn6M9JIV_82qkS-t6SC9iSOK6r1TNWO6aBCRerRNaxKXZso62bpGa5vypvVvQaUEfgIcLRkZ5QLoBU3ibErYg4cUDmb7p6CpGjR1NFVQHdtEzXy483uACgcJ-_RQMFfelFO-s)

功劳归于[Larry Cermak](https://twitter.com/lawmaster/status/1320614508772163584?s=20)

**机密资料提供者**

举报和保护我们的撰稿人是我们在Rekt工作的重要组成部分。当您的作者
在写这篇报道时，有人联系我们，提供了关于Harvest Finance 在昨晚事件前几天行动的信息。

以下信息不作评论。

> Harvest Finance团队与我联系，就两类资产的流动性池
> 提供激励寻求合作。

> 第一个是去信任的BTC，第二个是FARM/ETH。

![](https://lh5.googleusercontent.com/BI91M7nD8yCLZuJtX0Tpas4RCBD8xnGWl2LrRu4PTbO_CrQUDP2GDuhR45vrUpnOSc-hxuvuKTZ76DT8U58QVgvFxa7CNkQL2KXINn1Hsxw7csVd2b3VYOp8Mhw9_tM-fD58ZFOp)

> 我没有跟进他们，因为有些事情让人不快。

> 我并不是说是Harvest team，但看到智能合约3%的滑点，以及事实上
> 漏洞是在去信任的BTC上，这真"新奇"...

> 我认为，如果这不是Julien，那么一定是Harvest Finance，或者EMN黑客，或者是
> 有深厚闪电贷知识的人。

**退款申请**

一如既往，关于协议今后能否屏蔽或修改这类活动的问题， 
已引起了一场辩论。在Curve电报群里，有人认为，Curve应该可以屏蔽
这种类型的活动，然而现有的智能合约无法[被阻止](https://twitter.com/CurveFinance/status/1320694100090376193?s=20)或修改。

还有人呼吁renBTC退还他们从黑客活动中赚取的费用。这是一个
颇具争议的话题，迫使用户考虑使用去中心化协议的利弊。

**马虎的安全**

就在三周前的10月6日，Harvest Finance发布了一个[安全更新公告](https://medium.com/harvest-finance/week-6-update-security-rules-everything-around-me-62a681a3692a)，称他们
正在通过[Peckshield](https://twitter.com/peckshield)、[Haechi Labs](https://haechi.io/)和[CertiK](https://twitter.com/certik_io)的"严格安全审计"
来确保其土地安全。

需要指出的是，Peck Shield和CertiK在今年年初的三次黑客攻击之前，也对Bzx进行了审计。

我们等待他们对这一情况的评论。

开发人员甚至似乎连专门的安全公司都不习惯于
必须考虑闪电贷对其代码的影响。

掌握闪电贷，就像在哈雷戴维森双雄上转战12世纪的马术比赛--
挥舞着AK47；谁也没想到，平民百姓被打倒了，而且要等几年， 
直到没有受过教育的群众能够保护自己不受这种野蛮商人的伤害。

Harvest Finance以一种愉快的被动攻击语气回应了这一事件。

![](https://lh6.googleusercontent.com/R_kCRELgxVg20qoViEkHb43yiEoWnuslyOQJaPlG0djFHM8FAJEumBYLQP-URiPun5EdcOpKhBOLGHmsi0h36Z6-LdRxFKwD9ABzrFezDcLcNLXtEPBc896I1HcwxfLHCuz5R9IF)

twitter.com/harvest_finance/status/1320624369543057409

![](https://lh4.googleusercontent.com/kgpAOlAQRPTcNrx-HJzhDhO04Y9CttjxSfNJ3udyDNvVG5D75NbarZjK3aQ_76axChzA05kmDzDOlSyC9mFX98Odw1U5fSucvIw6zo7JOdjBjANdqm7WN-pac8GzxozyBjZQ6qWK)

**真实术语**

套利/掠夺/黑客

术语差异变得越来越模糊，而"代码即法律"的
事实却变得清楚明了。

Harvest Finance使用的术语是套利经济攻击。有人认为这种活动构成犯罪，
而另一些人只是看到了一个更有能力的使用者行为，用现代机械进行产量耕作。

这是一种功利主义，还是无政府资本主义？

不管是哪种方式，肯定具有娱乐效果。

购者留心。

> 只有在春天忠实地播种的耕作者，才会在秋天收获丰收。
> [伯蒂·查尔斯·福布斯](https://en.wikipedia.org/wiki/B._C._Forbes)
