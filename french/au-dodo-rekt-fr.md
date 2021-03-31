---
title: AU DODO - REKT
date: 09 Mar 2021
rekt: 
  amount: 2000000
  audit: Unaudited
  date: 09 Mar 2021
tags:
   - DODO
   - REKT
excerpt: Est-il mort ou est-il simplement allé se coucher ? DODO a été hacké pour 2 millions de dollars via une attaque au faux token, sans que le mobile ne soit réellement connu. Mais que cela ait été fait par un hacker éthique ou par un hacker malveillant, seulement 2 millions de dollars ? Il faudra plus s’appliquer la prochaine fois.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-header-twt.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-header.png)

**Est-il mort ou est-il simplement allé se coucher ?**

DODO a été hacké pour 2 millions de dollars via une attaque au faux token, sans que le mobile ne soit réellement connu.

Une chose demeure certaine : que cela ait été fait par un hacker éthique ou par un hacker malveillant, seulement 2 millions de dollars ? Il faudra plus s’appliquer la prochaine fois. 

Twitter demeure la source d’informations la plus rapide pour la DeFi - même l'équipe de DODO s'est appuyée sur [Luciano](https://twitter.com/Luciano_vPEPO/status/1369055985684381696?s=20) pour annoncer que leur propre pool de $WCRES / $USDT avait été drainée en utilisant des faux tokens.

L'analyse suivante est tirée du communiqué officiel de DODO, avec l’aimable participation de [@samczsun](https://twitter.com/samczsun), [@tzhen](https://twitter.com/tzhen), [PeckShield](https://twitter.com/peckshield), et [SlowMist](https://twitter.com/SlowMist_Team).

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-linebreak.png)

**L’exploit a ciblé plusieurs Crowpools de DODO V2, en l'occurrence les pools WSZO, WCRES, ETHA et FUSI.**

Au total, environ 3,8 millions de dollars, dont 1,88 million qui devraient être restitués (voir ci-dessous pour plus d'informations), ont été drainés à la suite de ces exploits.

Le smart contract Crowdpooling DODO V2 a un bug qui fait que la fonction init() peut être call plusieurs fois. Cela signifie qu’un exploiter peut mener une attaque en effectuant les étapes suivantes :

**1.** L’exploiter crée une contrefaçon de token et initialise le smart contract en callant la fonction ()init

**2.** L’exploiter call la fonction sync() et règle la variable “reserve”, qui représente le solde de token, à 0

**3.** L’exploiter call une nouvelle fois init() pour réinitialiser - cette fois-ci avec un “vrai” token (i.e les tokens des pools DODO)

**4.** L’exploiter utilise un flash loan pour transférer tous ses vrais tokens des pools et contourner la vérification du flash loan

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-suspects.png)

**Pour résumer, deux individus sont impliqués dans cet exploit. Nous les appellerons l'individu A et l'individu B.**

L'individu B a toutes les caractéristiques d’un bot de frontrunning car :

- Il a construit son adresse de contrat avec un préfixe constitué de plusieurs 0
- Il utilise le gastoken CHI
- Il fixe des prix de gas extrêmement élevés ; à un moment, il a augmenté la configuration de la transaction jusqu’à 93,148 gwei.

De plus, les exploits de l'individu B ont précédé d'environ dix minutes les exploits réussis de l'individu A.

**Individual A**

[L'individu A](https://etherscan.io/address/0x368a6558255bccac517da5106647d8182c571b23) a déjà contacté l'équipe de DODO par le biais de samczsun et a proposé de renvoyer les fonds retirés des pools de DODO. Voici un compte-rendu détaillé des actions de l'individu A :

_L’individu A a interagi avec une plateforme d’échange centralisée._

L'individu A [a retiré](https://etherscan.io/tx/0x970b32a8c81dd3fc47fa118621726fc418ec3526c4379470a4000ed7b448360f) 0.46597 ETH de Binance:  

L'individu A [a effectué](https://etherscan.io/tx/0x300de107cbca466abe121112848daaf7f5f0d15625d54773dd0bbbff4e276e93), en les enchaînant rapidement, 7 transactions de retrait de BUSD (voir le lien pour un exemple), en utilisant éventuellement le Binance Bridge.

_L'individu A transfère ses fonds vers une autre adresse de portefeuille._

L'individu A a transféré 67416 BUSD à 0xa305fab8bda7e1638235b054889b3217441dd645 deux fois - [UN](https://etherscan.io/tx/0x306d08f3d8af85dfdea7a6edb336d7504e8ecc7c609e4b940d188ba68e11cab5) - [DEUX](https://etherscan.io/tx/0x56dbf6421c6e6bd779ab0c12fd49e1f7714dd85023aa74abae1940f8d88669cf)

Individual A a transféré 59,245.324743 USDT à 0xa305fab8bda7e1638235b054889b3217441dd645 deux fois - [UN](https://etherscan.io/tx/0xbee2f507b2f4b4321927a9762dac757df12fe1ba2d6f85314273b9ea542a5c13) - [DEUX](https://etherscan.com/tx/0xaf80cf58c88f0e0f2f44e3902e4c7cd2c17122511fbc6c2d9b2cd43fbc4199b9)

L’individu A a réalisé deux exploits contre les smart contracts de DODO.

La première concernait le test contract DODO-USDT, et les fonds ont été [transférés](https://etherscan.io/address/0x328410f276d4fe83fc78fa56ad32d9821a5e5c1c#tokentxns) à 0xa305fab8bda7e1638235b054889b3217441dd645. 

Le second était contre le contrat WCRES-USDT, et les fonds ont été [transférés](https://etherscan.com/address/0x910fd17b9bfc42a6eea822912f036ef5a080be8a#tokentxns) à 0x56178a0d5f301baf6cf3e1cd53d9863437345bf9.

**Les fonds se trouvent actuellement sur les deux adresses suivantes :**

[0xa305fab8bda7e1638235b054889b3217441dd645](https://etherscan.io/address/0xa305fab8bda7e1638235b054889b3217441dd645)

[0x56178a0d5f301baf6cf3e1cd53d9863437345bf9](https://etherscan.io/address/0x56178a0d5f301baf6cf3e1cd53d9863437345bf9) 

**L’individu B**

L’individu B est très probablement un bot (un _robododo_).

**Le smart contract du bot suspecté :** 0x00000000e84f2bbdfb129ed6e495c7f879f3e634 

**L'adresse du compte déclencheur :** 0x3554187576ec863af63eea81d25fbf6d3f3f13fc

**L’individu B a exécuté 3 exploits contre les contrats de DODO :**

**ETHA-USDT:** [0x0b062361e16a2ea0942cc1b4462b6584208c8c864609ff73aaa640aaa2d92428](https://etherscan.io/tx/0x0b062361e16a2ea0942cc1b4462b6584208c8c864609ff73aaa640aaa2d92428)

**WSZO-USDT:** [0xff9b3b2cb09d149762fcffc56ef71362bec1ef6a7d68727155c2d68f395ac1e8](https://etherscan.io/tx/0xff9b3b2cb09d149762fcffc56ef71362bec1ef6a7d68727155c2d68f395ac1e8)

**vETH-WETH, avec 93,148 gwei:** [0x561f7ccb27b9928df33fa97c2fb99ea3750593e908f9f0f8baf22ec7ca0c5c4a](https://etherscan.io/tx/0x561f7ccb27b9928df33fa97c2fb99ea3750593e908f9f0f8baf22ec7ca0c5c4a)

**Les fonds se trouvent actuellement sur les deux adresses suivantes :**

[0x00000000e84f2bbdfb129ed6e495c7f879f3e634](https://etherscan.io/address/0x00000000e84f2bbdfb129ed6e495c7f879f3e634)

[0x3554187576ec863af63eea81d25fbf6d3f3f13fc](https://etherscan.io/address/0x3554187576ec863af63eea81d25fbf6d3f3f13fc) 

L'équipe de DODO essaie actuellement de contacter les propriétaires des adresses ci-dessus.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-linebreak2.png)

**Une somme relativement modique de 2 millions de dollars a été subtilisée par un agent anonyme.** 

Il est probable que la moralité du hacker évolue selon la somme potentielle du butin. 

> Petite somme = hacker éthique pour se faire mousser - Somme importante = tu la prends et tu l’ajoutes aux autres millions.

**Nous ne pouvons qu'imaginer les trésors personnels que ces personnes accumulent**. Les opportunités affluent de toutes parts dans cet eldorado, et pas seulement pour ceux qui choisissent d'apprendre à coder.

Il est intéressant de noter que les équipes elles-mêmes s'appuient sur Twitter pour se tenir à jour sur leurs propres protocoles. Cela nous rappelle que nous n'en sommes vraiment qu'aux premiers stades de cette industrie.

_L’occasion de vous faire un nom se présente devant vous : ce que vous ferez avec le pouvoir entre les mains ne dépend que de vous._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/dodo-conc.png)

Source des images : [harrikallio.com](https://harrikallio.com/portfolio/dodo-mauritius-island/) & [@BxST23](https://twitter.com/BxST23) 
