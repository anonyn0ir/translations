---
title: Eminence - Rekt in prod
date: 29 Sep 2020
tags:
  - yfi
  - defi
  - hack
  - Eminence
  - Cronje
excerpt: La communauté crypto a connu une nouvelle crise d'hystérie la nuit dernière, alors que les yeux de centaines d'utilisateurs se sont rivés sur le projet non publié d'Andre Cronje, et ont rapidement acheté pour 15 millions de dollars du mystérieux token $EMN.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/12/tease.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/12/tease.jpg)
**Le projet non publié d'Andre Cronje, Eminence, a été piraté pour 15 millions de dollars.**

La communauté crypto a connu une nouvelle crise d'hystérie la nuit dernière, alors que les yeux de centaines d'utilisateurs se sont rivés sur le projet non publié d'Andre Cronje, et ont rapidement acheté pour 15 millions de dollars du mystérieux token $EMN.

Après quelques tweets promotionnels inexpliqués, les utilisateurs ont surveillé avec ardeur le compte de Cronje à la recherche du moindre indice sur ce qui se tramait. Dès que les nouveaux contrats ont été [deployés](https://etherscan.io/address/0x2d407ddb06311396fe14d4b49da5f0471447d45c#tokentxns.) à partir de l'adresse financière de yEarn, la partie était lancée.

Des centaines d'utilisateurs ont participé à ce projet d'enquête participatif pour essayer de comprendre ce qui se passait, et de voir comment en tirer profit.

Les utilisateurs ont établi un lien entre les graphiques du compte Twitter eminence.finance et un MMORG inachevé appelé Eminence, Xander's Tales.

> [pic.twitter.com/tV9LSzPXlV](https://t.co/tV9LSzPXlV) > &mdash; eminence.finance (@eminencefi) [28 Septembre 2020](https://twitter.com/eminencefi/status/1310628912339316736?ref_src=twsrc%5Etfw)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/09/xanders.png)

> Vous l’entendez ici en premier, alpha leak garanti, je sens le grand retour d’un vieux jeu de carte avec un twist à la sauce NFT/DEFI… [$ENM](https://twitter.com/search?q=%24ENM&src=ctag&ref_src=twsrc%5Etfw)
>
> Faites quelques recherches sur "Eminence : Xander's Tales" et vous verrez que [@AndreCronjeTech](https://twitter.com/AndreCronjeTech?ref_src=twsrc%5Etfw) suit même l'artiste qui dirige le projet... 👀
>
> Plus d’infos très vite, suivez-moi 
> &mdash; Kiyo (@IslandKiyo) [28 Septembre 2020](https://twitter.com/IslandKiyo/status/1310709943062888455?ref_src=twsrc%5Etfw)

Les contrats qui avaient été déployés comprenaient le token EMN, qui pouvait être échangé contre d'autres tokens tels que eYFI, eAAVE ou eSNX. Ces tokens, ainsi que le lancement surprise, correspondaient parfaitement à ce qu’on lisait l'un des précédents tweets d'André concernant le projet financier yEarn à venir.

> Le nouveau système de yearn est probablement le plus complexe à ce jour. Il intègre [@synthetix_io](https://twitter.com/synthetix_io?ref_src=twsrc%5Etfw)[@AaveAave](https://twitter.com/AaveAave?ref_src=twsrc%5Etfw)[@chainlink](https://twitter.com/chainlink?ref_src=twsrc%5Etfw)[@iearnfinance](https://twitter.com/iearnfinance?ref_src=twsrc%5Etfw) et fonctionnera sur L1/L2.
>
> Nous nous demandons si nous devons rédiger des documents de type whitepaper pour fournir des explications avant le lancement, ou simplement lancer le produit et surprendre tout le monde ?
> &mdash; Andre Cronje (@AndreCronjeTech) [23 Septembre 2020](https://twitter.com/AndreCronjeTech/status/1308812154527780865?ref_src=twsrc%5Etfw)

La réputation de Cronje en tant que constructeur de la DeFi de premier plan, combinée à sa promotion du compte Twitter d'Eminence, a provoqué une véritable hystérie, et 15 millions de dollars ont été injectés dans le mystérieux contrat afin d'être échangés contre des CEM ou un des eTokens.

> 🚨 le système Yearn a été confirmé.
>
> LANCÉ À LA SURPRISE TOUT LE MONDE.
>
> JFC le cinglé est en train de le refaire.
>
> LONG [$YFI](https://twitter.com/search?q=%24YFI&src=ctag&ref_src=twsrc%5Etfw)[pic.twitter.com/XO5ZkJxDCq](https://t.co/XO5ZkJxDCq) > &mdash; BlueKirby.eth // YFI 🔥 (@bluekirbyfi) [28 Septembre 2020](https://twitter.com/bluekirbyfi/status/1310708762643181575?ref_src=twsrc%5Etfw)

Bien que le token EMN soit issu d'une bonding curve relativement plate, de nombreux utilisateurs ont acheté les tokens "en seconde main" sur Uniswap, ce qui a conduit à quelques heures d'arbitrage très rentable pour ceux qui se sentaient à l'aise pour interagir directement avec le contrat.
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/09/image.png)

Vers 04h00 UTC, les 15 millions de dollars contenus dans le contrat ont été soudainement drainés.

[@fifikobayashi](https://twitter.com/fifikobayashi/status/1310929902946852864?s=20) a écrit un court résumé sur la façon dont l'attaque a été menée.

- Utilisation d’un flash loan pour minter du EMN
- Manipulation du prix du EMN à la baisse en burnant des EMN pour des eTokens
- EMN est basé sur une bonding curve, donc quand la supply baisse, le prix aussi.
- Short d’EMN en brûlant l’autre moitié des EMN flashés de retour en DAI, qui a alors connu une inflation en raison de la chute de la valeur curve-induced de EMN.


Bien que les [hacks](/epic-hack-homie/) ne soient pas un phénomène inhabituel dans le domaine de la crypto, ce qui s'est passé ensuite l'est certainement.

11 minutes après avoir [retiré](https://etherscan.io/address/0x223034edbe95823c1160c16f26e3000315171ca9#tokentxns) 15 millions de dollars en DAI, l'assaillant a renvoyé 8 millions de dollars dans le Yearn: Deployer contract 01:31:04 AM +UTC [renvoyé](https://etherscan.io/tx/0x7bc97357364222207f1f011b22ad98ba78fcd3c25d3398346caa3928cdf4a4dd) 8 millions de dollars dans le Yearn: Deployer contract 01:31:04 AM +UTC

Ethereum Transaction Hash (Txhash) Details | Etherscan

Informations détaillées sur la transaction Ethereum (ETH) pour le [txhash 0x7bc97357364222207f1f011b22ad98ba78fcd3c25d3398346caa3928cdf4a4dd.](https://etherscan.io/tx/0x7bc97357364222207f1f011b22ad98ba78fcd3c25d3398346caa3928cdf4a4dd)

L'état de la transaction, la confirmation du bloc, les frais de gas, les Ether (ETH) et le transfert de token sont indiqués

![](https://etherscan.io/tx/0x7bc97357364222207f1f011b22ad98ba78fcd3c25d3398346caa3928cdf4a4dd)

![](https://etherscan.io/images/favicon3.ico)

![](https://etherscan.io/images/brandassets/etherscan-logo-circle.png)

![](https://etherscan.io/tx/0x7bc97357364222207f1f011b22ad98ba78fcd3c25d3398346caa3928cdf4a4dd)

Les théories vont bon train quant à l'identité de ceux qui sont à l'origine du hack et à la raison pour laquelle ceux-là rendraient l'argent. Certains n'hésitent pas à pointer du doigt les créateurs de Yearn Finance, affirmant qu'il s'agit d'un complot interne.

> Alors... est-ce [@bantg](https://twitter.com/bantg?ref_src=twsrc%5Etfw) qui a utilisé plusieurs bots et crée une inflation de TARÉ sur [#EMN](https://twitter.com/hashtag/EMN?src=hash&ref_src=twsrc%5Etfw) (et d’autres) pour arb DAI pour finalement tout dumper pour de la liquidité croissante ? [https://t.co/vKOKs7IlxF](https://t.co/vKOKs7IlxF)[https://t.co/rbb8H6c78H](https://t.co/rbb8H6c78H)[https://t.co/V7ocyAQg0J](https://t.co/V7ocyAQg0J)[@ChainLinkGod](https://twitter.com/ChainLinkGod?ref_src=twsrc%5Etfw)[@AndreCronjeTech](https://twitter.com/AndreCronjeTech?ref_src=twsrc%5Etfw)[pic.twitter.com/9Dle86Yffy](https://t.co/9Dle86Yffy) > &mdash; Spicetoshi (@Spicetoshi) [29 Septembre 2020](https://twitter.com/Spicetoshi/status/1310884921783787522?ref_src=twsrc%5Etfw)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/09/andrechan.jpg)

En fin de compte, ce sont ceux qui ont déposé des fonds dans les contrats non audités qui sont responsables de la perte de leur argent. Cependant, beaucoup ont qualifié d'irresponsable la promotion par Cronje du contrat inachevé, le FOMO général qui en a résulté étant facilement prévisible.

Une chose est sûre : beaucoup de gens ont perdu de l'argent hier soir.

> Peut-on trinquer pour notre frère 🐋 baleine ici présent, qui a dépensé 130 548 $ en [$EMN](https://twitter.com/search?q=%24EMN&amp;src=ctag&amp;ref_src=twsrc%5Etfw) il y a 1 heure et demie et qui vient de vendre le tout pour 368$.[https://t.co/5iVIHS93Pv](https://t.co/5iVIHS93Pv)[https://t.co/GBUMc62Eqs](https://t.co/GBUMc62Eqs)[pic.twitter.com/jIa7WVwP6s](https://t.co/jIa7WVwP6s) > &mdash; fomosaurus 🦖 (@fomosaurus) [29 Septembre 2020](https://twitter.com/fomosaurus/status/1310761830353186816?ref_src=twsrc%5Etfw)

> SUIVI DU POST : Un homme dépense 100k pour gagner 348$ - Gros respect pour pour ce génie absolu de roi des dégénérés qui a tout risqué pour un ETH. [$EMN](https://twitter.com/search?q=%24EMN&amp;src=ctag&amp;ref_src=twsrc%5Etfw)[pic.twitter.com/IZnBSTMfqs](https://t.co/IZnBSTMfqs)
> &mdash; end i i i (@end0xiii) [29 Septembre 2020](https://twitter.com/end0xiii/status/1310777947545051136?ref_src=twsrc%5Etfw)

#rekt

> Je venais juste d’acheter pour plus de 100,000 de dollars de[$EMN](https://twitter.com/search?q=%24EMN&amp;src=ctag&amp;ref_src=twsrc%5Etfw) avant le hack/exploit. je crois que ma vie est finie
> &mdash; zerosum (@zerosum666) [29 Septembre 2020](https://twitter.com/zerosum666/status/1310757909756891136?ref_src=twsrc%5Etfw)

Cronje affirme avoir reçu de multiples menaces concernant les fonds perdus, et a demandé à Yearn Treasury de l'aider à redistribuer les 8 millions de dollars restitués.

Malgré ce revers majeur, Andre continue de construire, et a publié ce tweet plus tôt dans la journée.

> je continue de travailler sur [@eminencefi](https://twitter.com/eminencefi?ref_src=twsrc%5Etfw). J’adore le metaverse et la metaconomy.
>
> Je vais également continuer à déployer des contrats de test. J'ai plus de ~100 contrats déployés, dont probablement plus de la moitié présentent des vulnérabilités.
>
> S'il vous plaît, attendez les annonces officielles.
> &mdash; Andre Cronje (@AndreCronjeTech) [29 Septembre 2020](https://twitter.com/AndreCronjeTech/status/1310802116391428097?ref_src=twsrc%5Etfw)

Les développeurs de Yearn, [Banteg](https://twitter.com/bantg) et [Klim K](https://twitter.com/milkyklim) ont également travaillé dur pour aider les personnes touchées, et ont créé un snapshot de EMN et des eTokens afin d'essayer de dédommager ceux qui ont perdu de l'argent.

Les utilisateurs peuvent vérifier leur éligibilité [ici](https://gist.github.com/banteg/2ec7b0aec54267adf7d98136eee07cd9) (diviser par 1e18)

[rektHQ](https://twitter.com/RektHQ) n'a pas été impliqué dans la création de cette liste, et aucun détail n'est définitif.

> Puisque nous avons reçu 8M de DAI, nous travaillons à les distribuer aux personnes qui se sont fait rekt. J'ai terminé la première version du snapshot qui utilise les taux de la bonding curve de EMN, eCRV, eLINK, eAAVE, eYFI, eSNX au bloc 10954410. Cela comprend 3656 adresses. [pic.twitter.com/dT3WryyGrD](https://t.co/dT3WryyGrD) > &mdash; banteg (@bantg) [29 Septembre 2020](https://twitter.com/bantg/status/1310823410289836032?ref_src=twsrc%5Etfw)

Les faits d'hier soir ont été le couronnement de plusieurs évènements, attitudes et concepts différents qui ont surgi au cours des derniers mois.

Ceux qui ont FOMO sur des contrats non audités ont été bien récompensés dans le passé. Or, bien que beaucoup sur Twitter soient désireux de promouvoir ce style de comportement digne d’un “Chad", il est peut-être temps de reconsidérer ce style de lancement surprise.

La réputation jusqu'alors irréprochable du développeur d’YFI vient d'en prendre un sacré coup. Nous sommes maintenant à ce qui semble être un tournant dans la DeFi, où, espérons-le, les développeurs et les utilisateurs sauront tirer les leçons de cet événement.

D'ici là, nous attendons avec impatience la véritable sortie d'Eminence : Xander's Tales.
