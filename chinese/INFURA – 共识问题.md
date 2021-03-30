---
title: INFURA – 共识问题
date: 2020年11月11日
tags:
  - geth
  - infura
  - 以太坊
  - 分叉
excerpt: 共识不仅仅是达成一致，而是要一起改变。现今整个以太坊网络都出现了问题，因为主网遭受共识缺陷。
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/12-angry-men-1.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/12-angry-men-1.jpg)

**共识不仅仅是达成一致，而是要一起改变。**

现今整个以太坊网络都出现了问题，因为主网遭受共识缺陷。

运行旧版本的geth节点的服务发现自己卡在了少数链上，
对所有依赖它们的应用程序产生了连锁反应。

大多数用户是在Infura API发生故障时才得知这一问题的。Infura是以太坊网络上最大的节点提供商， 
他们为一些最常用的Web 3.0应用和CEX提供工具和基础设施， 
如Metamask、Uniswap和Binance。

Infura服务降级显示，Binance要么依赖Infura，要么运行过时的
节点，两者都不适合如此大规模的交易所。

Infura没有运行最新的geth版本，虽然这看起来很奇怪，但这样的做法是有道理的，
因为大规模的运营商不会直接使用最新的geth版本，因为在没有硬分叉的情况下，
没有迫切的理由从一个稳定的工作代码切换到一个未知的代码。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/add3dbfcb32773693acdf1699dc73e8f.png)

搜索和分析引擎Blockchair也出现了问题，发布了以下推文；

> 我们的[以太坊](https://twitter.com/hashtag/Ethereum?src=hashtag_click)资源管理器出现了问题，正在进行修复工作。似乎
> 出现了链分叉，一些节点（包括我们和一些矿工的）被卡在少数链上。

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/Emh9J7sW8AEB_FT.jpg)

Blockchair的首席开发人员[妮基塔·扎沃龙科夫](https://twitter.com/nikzh/status/1326455533927329792?s=20)（Nikita Zhavoronkov）报告称收到了以下错误。

> ########## BAD BLOCK #########

> <...>

> 错误：无效的Merkle root（远程：
> 57cc91ee8b91b956592a27b14386abc2aba723b5f4f9e5d3181ace6b5d3cd433 local:
> 1f9ee59bfa683a25c7a15b626995a3ad7c58c571b40df96eea31e5c5eed9732d)

**在geth网络中发现了两个严重的漏洞**，这两个漏洞都是由[JohnYoungseok Yang](https://github.com/johnyangk)（软件平台实验室）发现，
使他在以太坊赏金计划[排行榜](https://bounty.ethereum.org/)上获得2万分。

为避免漏洞，Github Issues上不讨论共识缺陷，所以目前尚不清楚
漏洞的具体细节。对于那些渴望了解更多技术细节的人来说，
[Mhswende](https://twitter.com/mhswende/status/1326489526450221056?s=20)指出，

> "将来很可能会有一篇关于这个问题的专文或devcon演示"

为了最大限度地减少干扰，以太坊开发人员决定要硬分叉。

正如[佩特·西拉吉](https://twitter.com/peter_szilagyi/status/1326476649278414850?s=20)（Péter Szilágyi）在推特上写道；

> _这是一个"未宣布的硬分叉"（从坏链到好链）。也就是说，默默地修复了一个蛰伏2年以上的bug，_
> _与提高对它的认识相比，造成混乱的几率要小得多。我们_
> _力求将潜在损失降到最低。_

对于抱怨Infura发生故障的人来说，这个事件应能及时提醒人们， 
让你的节点保持更新，因为一旦你把你的节点委托给另一方， 
他们如何开展业务由他们决定。

Infura已对整个事件进行了透明化处理，并且显然正在努力解决这个问题。

Infura已重新[上线](https://forkmon.ethdevops.io/)，状态更新可在[此处](https://status.infura.io/)找到。

**Infura发生故障使我们许多人意识到我们是多么的依赖这个单一实体。**

**这是一个中心化的服务，作为我们的去中心化系统的守门人。**

**个人和机构都需要考虑他们的前进方式。**

Binance和Bithumb等大型可信交易所的认知能力已经下降，
因为他们被迫在故障期间禁用ETH和ERC-20提现功能，尽管他们有责任让用户
不受此类事件的影响。

**我们不能在这个程度上依赖Infura。**由于MetaMask对中心化节点提供商的默认依赖，
整个以太坊网络暂时变得荒凉，gas费也减少到只有12gwei。

这证明了一种不健康的依赖性，也清楚地表明了这种依赖性可能带来的
潜在危害。

我们是否希望我们的数字社会重蹈覆辙，
依赖中心化的单点故障？

**我们建立了一个免费的互联网，但却把它交给了统一管理机构**--Chrome浏览器、Safari浏览器、Brave...。
我们建立了一个另类的互联网，在这里，匿名和去中心化原始价值得以延续，但
但我们却把它贴上了暗网的标签，访问仅限于替代性的、常被封锁的软件。

我们不能让同样的事情发生在加密货币上。

[大卫·米哈尔](https://twitter.com/dmihal/status/1326520031379853313?s=20)（David Mihal）写道：

> _今天发生Infura故障事件，使得用户争相寻找替代的RPC供应商。_

> _我刚刚把[**http://ethereumnodes.com**](https://ethereumnodes.com/)放在一起，作为一个_
> _公共的、免费的RPC端点及其当前状态的中心列表。_

[迈克尔·奥罗克](https://twitter.com/o_rourke/status/1326509249825038336?s=20)（Michael O’Rourke）指出

> 如果您的Metamask发生故障了，您可以使用以下网址将RPC提供者改为Pocket。

> [_https://eth-mainnet.gateway.pokt.network/v1/5f3453978e354ab992c4da79..._](https://t.co/7a76Xoo8Qu?amp=1)

**任何未能达成共识的问题都是一个严重的问题。**一个未公布的硬分叉表明，这些漏洞如果
不加以控制，可能会对以太坊造成很大危害。

幸运的是，由于bug赏金猎人的锐利目光和以太坊开发人员的勤奋工作，没有造成任何损失，
正如尼基塔·扎冯龙科霍夫（Nikita Zhavonronkohov）在推特上所写的那样，修复方式似乎
挺简单...

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/end2.jpg)

图片来自12怒汉
