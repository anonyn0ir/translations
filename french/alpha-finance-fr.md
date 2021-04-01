---
title: Alpha Finance - REKT
date: 13 Feb 2021
rekt: 
  amount: 37500000
  audit: Quantstamp, Peckshield
  date: 13 Feb 2021
tags:
  - Alpha Finance
  - Cronje
  - rekt
excerpt: Les arts sombres de la DeFi restent les plus rentables. 37,5 millions de dollars disparus dans un conte de fausse magie, de confusion et d'accusation. La victime a désigné son agresseur.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/header-alpha-homora.png
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/header-alpha-homora.png)

**Les arts sombres de la DeFi restent les plus rentables.**

Ce qui suit est l’une de nos histoires les plus spectaculaires jusqu’à présent.

**Un conte rempli de fausse magie, de confusion et d’accusation donnant lieu à l’heure actuelle au plus gros hack de la DeFi.**

~37,5 millions de dollars ont été volés dans une complexe magouille de DeFi, une attaque multi-transactions ayant été utilisée pour piller les coffres d'Alpha Finance, laissant croire à beaucoup de gens qu’Iron Bank était la véritable victime.

Ce meurtre a eu lieu dans un [palais des glaces](https://youtu.be/F-BqDWG72iM). La nature de plus en plus imbriquée des protocoles DeFi, combinée à la complexité de l'attaque, a laissé la communauté confuse aussi bien quant à l'identité de la véritable victime qu’à l’identité du responsable devant s'acquitter des réparations.

Le contrat des attaquants a fait “croire” au code Homora que leur contrat malveillant était l'un des leurs afin de manipuler le nombre de dettes interne de leur système.

**Ce fut un duel privé entre le protocole et l'assaillant**. Le contrat exploité n'avait pas été encore annoncé et n’était pas disponible pour les utilisateurs, ce qui signifie qu’ils n’étaient pas directement concernés. Jamais pour l’instant n’avons-nous vu un complot interne aussi flagrant, et Alpha Finance n'a pas tardé à indiquer qu'ils avaient un [“suspect n°1”](https://twitter.com/AlphaFinanceLab/status/1360623172433760256?s=20).

Pourquoi le contrat a-t-il été laissé sur le mainnet s'il n'était pas encore prêt ? Nous avons demandé à Alpha, qui nous a répondu ce qui suit :

> Nous avons lancé plusieurs pools, par exemple sUSD, à l’étape contrat et non à celle de l'interface utilisateur, car nous nous préparions à lancer de nouveaux pools, dont sUSD la semaine prochaine.

**Les gros parieurs sont vite sortis afin de protéger leurs fonds durant l’embrouillamini.** SBF a retiré [400 millions de dollars](https://twitter.com/_wilbur4ce_/status/1360636958595305474?s=20) de FTT depuis Cream Finance et [Three Arrows Capital](https://etherscan.io/address/0x5cfd0cddf989959a6a6c3ad985ce324460d46dfd) a envoyé [3 millions de dollars](https://twitter.com/Raez_x/status/1360542616849375233?s=20) d'ALPHA vers Binance, où le seul but pouvait être de les vendre.

Tous les tokens liés à l'attaque ont vu leur valeur diminuer. 

Le token de gouvernance d’Alpha Homora, le [ALPHA](https://www.coingecko.com/en/coins/alpha-finance) est passé de 2,25 $ à 1,78 $.

Le token de gouvernance d'Iron Bank, [CREAM](https://www.coingecko.com/en/coins/cream), a chuté de 288.82 $ à 193.51 $.

[AAVE](https://www.coingecko.com/en/coins/aave), le token de gouvernance du service hébergeant le controversé flash loan qui a rendu possible tant d’attaques de cette nature, a pour sa part vu sa valeur chuter de 518 $ à à 492 $ au cours de la journée.

**Mais la variation du cours des prix des tokens n’est pas ce qu’il y a de plus captivant dans cette histoire…**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/linebreak-shanghai2.png)

L'équipe Alpha Finance a rédigé un excellent [post-mortem](https://blog.alphafinance.io/alpha-homora-v2-post-mortem/), et ce qu'ils ont trouvé était surprenant. Les éléments apportés par notre enquête conjointe laissent croire à un niveau de corruption bien plus profond que prévu. 

Reste à savoir si Alpha Finance rendra publiques ses accusations, mais leur déclaration initiale, où ils affirment avoir un suspect n°1, laisse à penser que des représailles sont à venir.

**D'après le post-mortem officiel, nous pouvons en déduire que l'attaquant devait connaître les éléments suivants pour mener à bien son attaque :**

- **HomoraBankv2 dispose d'une pool sUSD à l’étape de contrat en vue de la préparation de sa prochaine version. Elle ne dispose pas d’interface utilisateur et n’a pas été annoncée publiquement.**
- **Il n'y avait pas de liquidité dans le pool de prêts sUSD**, ainsi l'attaquant peut entièrement manipuler et gonfler le montant total de la dette et la part totale de la dette.
- **Il y a une erreur d'arrondi dans le calcul de la fonction d'emprunt**, qui n’est effective que lorsque l'attaquant est le seul emprunteur.
- **La fonction resolverReserve peut augmenter totalDebt sans augmenter totalDebtShare** et la fonction, destinée à collecter des revenus à la pool de réserve, peut en effet être call par n'importe qui.
- HomoraBankv2 accepte n'importe quel spell personnalisé, tant que l'invariant valide que le collatéral > emprunt (un spell est similaire à une stratégie sur Yearn).

Sous le regard de tant d’utilisateurs, les voleurs ont laissé une piste jonchée d’indices et, par un mouvement assez singulier de contre-attaque, les victimes ont identifié leur agresseur.

Des informations internes, mentionnées ci-dessus, étaient des conditions nécessaires afin de mener à bien cette attaque. Cependant, en raison du large éventail de protocoles et de cabinets d'audit impliqués, ces informations peuvent avoir fuitées de plusieurs sources. 

_Si rekt ne cherche plus à porter d’accusations, nous sommes impatients de voir comment Alpha Finance va gérer la situation._

**Voici le déroulement des faits selon [Alpha Finance](https://blog.alphafinance.io/alpha-homora-v2-post-mortem/)** :

**1.** L’attaquant a créé un evil spell (l'équivalent d’une stratégie sur Yearn). https://etherscan.io/tx/0x2b419173c1f116e94e43afed15a46e3b3a109e118aba166fcca0ba583f686d23

**2.** L’attaquant a swap ETH -> UNI, et a fourni ETH + UNI à la pool UNISWAP (obtenant des tokens LP ETH/UNI). Dans la même transaction, il swap ETh -> sUSD sur Uniswap et dépose les sUSD à l’Iron Bank de Cream (obtenant des cysUSD).
https://etherscan.io/tx/0x4441eefe434fbef9d9b3acb169e35eb7b3958763b74c5617b39034decd4dd3ad

**3.** Call execute vers HomoraBankv2 en utilisant l’evil spell (créant la position 883), accomplissant : 
Emprunt de 1000e18 sUS. 
Dépôt UNI-WETH LP vers ERC-20, et utilisation comme collatéral (pour contourner le collatéral -> emprunt check). 
Pendant le processus, l'attaquant a des parts de dette de 1000e18 sUSD (car l'assaillant est le premier emprunteur).
https://etherscan.io/tx/0xcc57ac77dc3953de7832162ea4cd925970e064ead3f6861ee40076aca8e7e571

**4.** Call execute sur HomoraBankv2 en utilisant encore l’evil spell (vers la position 883), accomplissant :
Repay 1000000098548938710983 sUSD (la dette réelle avec intérêt s'accumule à 1000000098548938710984 sUSD), résultant en une part de remboursement de 1 de moins que la part totale. 
Dès lors, l’attaquant a maintenant 1 minisUSD de dette et 1 en part de dette.
https://etherscan.io/tx/0xf31ee9d9e83db3592601b854fe4f8b872cecd0ea2a3247c475eea8062a20dd41

**5.** Call resolveReserve sur la bank sUSD, la dette s’accumulant à 19709787742196, alors que totalShare reste 1. 
Etat actuel : 19709787742197, tandis que totalShare = 1.
https://etherscan.io/tx/0x98f623af655f1e27e1c04ffe0bc8c9bbdb35d39999913bedfe712d4058c67c0e

**6.** Call execute sur HomoraBankv2 en utilisant encore l’evil spell, accomplissant (16 fois répétés, doublant à chaque fois le montant emprunté) : 
Emprunt de 19709787742196 minisUSD et transfert à l’assaillant (le montant doublant à chaque fois, puisque totalDebt double à chaque fois que l'emprunt est réussi). Chaque emprunt est 1 de moins que la valeur de totalDebt, rendant la part d’emprunt correspondante = 0, ainsi le protocole traite cela comme une absence de dette d’emprunt. 
A la fin de la transaction, l’assaillant dépose 19.54 sUSD sur l’Iron Bank de Cream.
https://etherscan.io/tx/0x2e387620bb31c067efc878346742637d650843210596e770d4e2d601de5409e3

**7.** On continue le processus : call execute sur HomoraBankv2 en utilisant encore l’evil spell, accomplissant (répété 10 fois, doublant à chaque fois le montant emprunté). 
À la fin de la transaction, l’attaquant dépose 1321 sUSD à l’Iron Bank de Cream).
https://etherscan.io/tx/0x64de824a7aa339ff41b1487194ca634a9ce35a32c65f4e78eb3893cc183532a4

**8.** Flash loan depuis Aave (emprunt de 1,800,000 USDC). 
Swap de 1,800,000 USDC en 1,770,757.56254472419047906 sUSD, et dépôt dans Cream pour avoir assez de liquidité pour que l’attaquant emprunte en utilisant le custom spell. 
Poursuite du doublement de l'emprunt de sUSD, on passe de 1322,70 sUSD à 677223,15 sUSD (total de 10 fois). 
Swap de 1,353,123.59 sUSD en 1,374,960.72 USDC sur Curve. 
Emprunt de 426,659.27 USDC depuis Cream (puisque l’assaillant a déjà déposé les sUSD à l’étape b).
https://etherscan.io/tx/0x7eb2436eedd39c8865fcc1e51ae4a245e89765f4c64a13200c623f676b3912f9

**9.** Répétition de l’étape 8 mais avec ~10M USDC (pas d'emprunt USDC à la fin).
https://etherscan.io/tx/0xd7a91172c3fd09acb75a9447189e1178ae70517698f249b84062681f43f0e26e

**10.** Répétition avec ~10M USDC (pas d'emprunt USDC à la fin).
https://etherscan.io/tx/0xacec6ddb7db4baa66c0fb6289c25a833d93d2d9eb4fbe9a8d8495e5bfa24ba57

**11.** Emprunt de 3,244.63 WETH + 3.6M USDC + 5.6M USDT + 4.26M DAI. 
L’assaillant fournit les Stablecoins sur Aave (pour obtenir des aTokens, afin que les USDC & USDT ne soient pas gelés). 
Il fournit des aDAI, aUSDT et aUSDC sur la pool a3Crv de Curve.
https://etherscan.io/tx/0x745ddedf268f60ea4a038991d46b33b7a1d4e5a9ff2767cdba2d3af69f43eb1b

**12.** Il ajoute les tokens LP a3Crv à la jauge de liquidité de Curve.
https://etherscan.io/tx/0xc60bc6ab561af2a19ebc9e57b44b21774e489bb07f75cb367d69841b372fe896

**13.** Lors des autres transactions il effectue des dépôts sur Tornado Cash, GitCoin Grants. 1,000 ETH sont envoyés sur les adresses CREAM et Alpha de l’utilisateur.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/linebreak-shanghai.png)

**Le casting de cette histoire est unique.**

Nous avons toujours considéré qu’il y avait une frontière floue et mouvante entre les hackers éthiques et les malicieux, mais il est rare de voir des accusations aussi limpides de la part de la victime.

Andre Cronje, qui a [associé Yearn](https://twitter.com/AndreCronjeTech/status/1347194324237176832?s=20) à Alpha Homora quelques semaines avant ces évènements, a commenté aujourd'hui [l'attaque](https://twitter.com/AndreCronjeTech/status/1360674224797483010?s=20) :

> Prenez le temps d'étudier l'exploit. 9 transactions. 4 manipulations différentes. Une comprenant le calcul exact de la dette. Il a fallu des heures de recherche aux équipes pour comprendre ce qui s’est passé. Alpha a pris des mesures immédiates pour atténuer l'exploit. Cela a été fait dans les minutes après la découverte initiale.

[Banteg a répondu](https://twitter.com/bantg/status/1360678595551707139?s=20) :

> Le setup est absolument incroyable. Il est absolument impossible que ce soit fait par quelqu’un qui aurait regardé les contrats à la va-vite, et surtout en ce qui concerne les trucs pas encore annoncés.

**Cela mènera peut-être à une autre acquisition de Yearn ; le nom de Cronje est mentionné 4 fois dans le post-mortem, et la manière de procéder semble familière...**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/alpha-finance-conclusion.png)

**Combien de temps cette ère propice aux hackers anonymes peut-elle durer ?** 

Comme la liste des suspects possibles est très restreinte il devient relativement aisé d'écarter et de traquer les attaquants potentiels, et alors celle-ci se réduit comme peau de chagrin. 

“La confiance n’exclut pas le contrôle” est un excellent mantra lorsque l’on travaille dans le codage, pourtant elle n'empêche pas la paranoïa sociale croissante qui doit se développer dans les cercles supérieurs de la finance décentralisée. Nous vivons une période de croissance sans précédent pour la cryptomonnaie et la DeFi, où le coût de l’absence de travail n’a jamais été aussi élevé. La pression sur les développeurs DeFi augmente de jour en jour.

Les empires sont construits sur des lignes de code et l'avenir de la finance se construit juste sous nos yeux. 

**Les développeurs sont engagés dans une course vers le ciel, tandis que des personnes corrompues intégrées dans le système travaillent main dans la main avec des hackers, sabotant les fondations de leurs œuvres.** 

Quand un bastion s’effondre, les autres l’observent et en tirent des conséquences. Avant même que la poussière ne retombe, les foules déjà s’en vont et les équipes, implacables, poursuivent inexorablement leur rêve de construction de forteresse imprenable.

**Combien de temps les hackers pourront maintenir cette intensité avant que l'inéluctable erreur ne fasse tomber leur cape d’invisibilité ?**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/af-gif.gif)
