---
title: Cover - REKT
date: 29 Dec 2020
rekt: 
  amount: 9400000
  audit: Arcadia Group
  date: 29 Dec 2020
tags:
  - cover
  - Rekt
excerpt: La prochaine fois, prenez-soin de vos services bordel. Les pièces s'accumulent, mais celles-ci ne sont pas en chocolat : nous sommes en plein classique Hollywoodien, un film noir d’assurance. Les revenus en noir et blanc des polices d'assurance se prêtent bien aux histoires Hollywoodiennes. 
banner: https://lh4.googleusercontent.com/IgAdM7JctrErxRd1kLmyJz4CEUbBDH1xZdsE4h7YZ_6NTRmWbF3p7rNREX-4BcKiTRH9FygNeZXSOzLCe2PqmVZ2NrWz5fb6ZKpPREHc4x3zsCoF8RcQvhj9Sx5XlBDiM04p1Xnh
---

![](https://lh4.googleusercontent.com/IgAdM7JctrErxRd1kLmyJz4CEUbBDH1xZdsE4h7YZ_6NTRmWbF3p7rNREX-4BcKiTRH9FygNeZXSOzLCe2PqmVZ2NrWz5fb6ZKpPREHc4x3zsCoF8RcQvhj9Sx5XlBDiM04p1Xnh)

**La prochaine fois, prenez-soin de vos services bordel.**

Les pièces s'accumulent, mais celles-ci ne sont pas en chocolat : nous sommes en plein classique Hollywoodien, un film noir d’assurance.

Les revenus en noir et blanc des polices d'assurance se prêtent bien aux histoires Hollywoodiennes.

**Dans [Assurance sur la mort](https://www.youtube.com/watch?v=yKrrAa2o9Eg) (1944), l'assurance est la force motrice du bien et du mal.**

Le film tire son nom d'une clause d’une assurance-vie qui est doublée si le décès de l’assuré est accidentel. 

Cela donne un scénario à rebondissements où un vendeur d’assurance échafaude tout un plan pour maquiller le meurtre du mari de sa maîtresse en accident afin de recevoir un double paiement.

**Ne prenez jamais rien pour argent comptant**. Les péripéties et les scripts de la DeFi ne sont jamais simples et linéaires  L’anonymat et la composabilité sont un terreau fertile pour les complots, et il y a plusieurs façons de profiter d’un seul accident, si bien que les joueurs les plus malins n'héritent pas toujours de la récompense la plus ostensible. 

**9,4 millions de dollars ont été volés, 3,2 millions de dollars récupérés et 6,2 millions de dollars perdus.**

**COVER (anciennement appelé SAFE) a chuté de [~90%](https://www.coingecko.com/en/coins/cover-protocol) lorsqu’une faille permettant de mint à l’infini a été découverte et exploitée**, faisant augmenter l'offre totale de tokens de 48 billiards pour cent, soit de 84 477 tokens totaux à 40 796 131 214 802 600 000.

Six adresses différentes ont mint du COVER via cette faille avant qu’elle ne soit refermée. Certains ont gardé l’argent, d’autres non.

Parmi ces six adresses ayant exploité la faille, [Grap Finance](https://medium.com/@grap.finance), jusqu'alors [inconnue](https://etherscan.io/token/0xC8D2AB2a6FdEbC25432E54941cb85b55b9f152dB), est celle qui a fait le plus parler d’elle, ayant profité de l'occasion pour se présenter comme un groupe de hackers éthiques en revendant ses COVER mintés pour des ETH afin dans les rendre avec un message cinglant.

**Le code fait loi, mais les failles demeurent** - nous pouvons compter sur les attaquants pour en profiter, mais nous savons que les choses sont rarement aussi simples qu'elles ne le paraissent.

Qui avait une couverture sur $COVER ? Nous sommes allés le découvrir.

![](https://lh3.googleusercontent.com/StXzSYZ9O3fWgBSfhG1AUgJwfNlHvh20UIr03MSxmDW94rKhJfr9VJnyjxUyRAhgxAmGY7yeVnqokpMW3rk6ZzpZOB0bQuDCTxMzRAlParXEr6lNlN_WkI_xHSo6hxk5ul1n9D5y)

**Rekt OPSEC**

La première attaque s’est faite en [quatre étapes](https://twitter.com/vasa_develop/status/1343571127331737600?s=20) par un seul attaquant, mais l’histoire est devenue plus compliquée lorsque la faille fut rendue [publique](https://twitter.com/Luciano_vPEPO/status/1343509612583145472?s=20), et que d’autres wallets ont reproduit le processus.

Les chronologies suivantes sont extraites du [post-mortem officiel de Cover](https://coverprotocol.medium.com/12-28-post-mortem-34c5f9f718d4). Pour une analyse plus poussée, veuillez vous référer à l’analyse [étape par étape](https://www.notion.so/Cover-Infinite-Mint-Exploit-0a234cc279484982ae559bb5ab54532a#6359c6970a1b414499b76241a7e7b967) faite par [@vasa_dev](https://twitter.com/vasa_develop).

**Chronologie de l’Exploitant 1**

Dec-28–2020 04:09:27 AM +UTC

- **Une nouvelle [pool Balancer](https://etherscan.io/address/0x59686e01aa841f622a43688153062c2f24f8fded) a été ajoutée au Blacksmith contract** depuis le multisig de l’équipe grâce à [une transaction](https://etherscan.io/tx/0xe5173fffaed3342b53d41319dc538e7923e287e962df2d27f5e425c633db45d4) liée à l'expiration de couvertures.

Dec-28–2020 08:08:12 AM +UTC

- **Un assaillant [exécute](https://etherscan.io/tx/0xd721b0ef2886f14b75548b70d2d1fd82bea085ca24f5de29b833a64cfd8f7a50) le premier dépôt sur le contrat**, déposant 1,326,880 tokens BPT.

Dec-28–2020 at 08:11:16 AM +UTC

- **Le même assaillant a ensuite [call](https://etherscan.io/tx/0xadf27f5dd052482d46fdf69a5208a27cc7352522c7c19bbde5aee18f6ea4373b) withdraw(),** exploitant le contrat  pour ~703.64 $COVER et retirant 1,326,878.99 BPT.

Dec-28–2020 08:47:15 AM +UTC

- **La première vente de tokens $COVER liés à l’exploit peut être trouvée [ici](https://etherscan.io/tx/0x66128a1685605b1798c852e14db0b0232a56e3bebf7f3f35b168642801754beb).** Pendant ce temps, plusieurs comptes ont abusé de l'exploit et vendu leurs $COVER sur le marché.

Dec-28–2020 09:18:28 AM +UTC

- **L'assaillant [continue de mint](https://etherscan.io/tx/0xf81fb72ee096e0d7afe4b99a55b723110604fb26ec82846043cfc396e1fa79da)** alors que le vecteur d’attaque est toujours là.

**Au total, l’Exploitant 1 a volé pour environ 4.4 millions de dollars de fonds avant de les transférer sur cette [adresse](https://etherscan.io/address/0x85abf036ca922e56fed670f4d3ce53fc4ea52b95#tokentxns).**

Il semble que cette faille ait initialement été découverte par pur hasard, l'Exploitant 1 ayant à l’origine une mauvaise OPSEC, un wallet classique alimenté par un échangeur nécessitant un KYC, et une activité régulière depuis trois ans. Certains prétendent connaître l'identité de cet exploiteur et lui [suggèrent](https://twitter.com/0xRevert/status/1343743516544028672?s=20) de restituer les fonds.

---

**Selon un scénario digne de la DeFi, l’assaillant originel a attiré peu d'attention par rapport à Grap Finance, qui ont pour leur part saisi l'opportunité de jouer le rôle du hacker éthique.**

**Chronologie de Grap Finance**

Dec-28–2020 11:54:47 AM +UTC

- **[Grap Finance: Deployer](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd) (EOA) [dépose](https://etherscan.io/tx/0x77490baee41a9b35a6e87d49453c7329c7517c10ce6ce26b4c142692a2877e65) 15,255.552810089260015362 BPT (DAI/Basis pool)** au sein du Blacksmith farming contract.

Dec-28–2020 11:58:04 AM +UTC

- **[Grap Finance: Deployer](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd) [retire](https://etherscan.io/tx/0x88ce99fc1cb695db82d83ce5fe587396744841d3a123687f95b18df6a3106818) ses 15,255.552810089260015361 BPT**(DAI/Basis pool), ne laissant que 1 wei dans son solde dans le Blacksmith farming contract.

Dec-28–2020 11:58:56 AM +UTC

- **[Un autre utilisateur](https://etherscan.io/address/0xdf1aefb979d180b4d67cca9abb4c5108c89dc8a4) [retire](https://etherscan.io/tx/0xa27fb73caddb1cf24aa7a5afe84eed13db2f0a889a6ee0f3d5e6226a76c0fd9c) la plupart de son solde** (1,007.599009946121991627 BPT) de Blacksmith. Désormais, Grap Finance dispose à lui seul de toutes les liquidités dans la pool DAI/Basis sur le contrat Shield Mining Blacksmith, soit exactement 1 wei.

Dec-28–2020 12:00:21 PM +UTC

- **[Grap Finance: Deployer](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd) [redépose](https://etherscan.io/tx/0xbd1fcda7006ddd58b18cb3bfbd01ef2d1a979be596e1c73be1d7d65fd7eb8215) 15,255.552810089260015361 BPT** (DAI/Basis pool) sur le Blacksmith farming contract.

Dec-28–2020 12:02:04 PM +UTC

- **[Grap Finance: Deployer](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd) [claim](https://etherscan.io/tx/0xca135d1c4268d6354a019b66946d4fbe4de6f7ddf0ff56389a5cc2ba695b035f) les récompenses**, et en raison du solde de seulement 1 wei combiné au problème de stockage/mémoire, cela amène un mint de 40 796 131 214 802 500 000.212114436030863813 $COVER.

Dec-28–2020 12:29:03 PM +UTC

- **[Grap Finance: Deployer](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd) commence à [vendre](https://etherscan.io/tx/0xaf94d9b537a13819e873b37160594af2b1cc70b420d0b160a02e341566866a6b) [autant](https://etherscan.io/tx/0x01b3517845ed9c6b7b40d57bd71ac1a89fec080c5b8988f764d8226ac5caa959) de tokens que possible** sur 1inch.exchange via de multiples transactions.

Dec-28–2020 12:59:27 PM +UTC

- **[Grap Finance: Deployer](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd) [burn](https://etherscan.io/tx/0xe6c068ca3605228b2435a414f2b372057340f77d3fe9f1d3967eb1ad128cb5d2) les tokens mintés**

Dec-28–2020 at 01:41:01 PM +UTC

- **[Grap Finance: Deployer](https://etherscan.io/address/0x00007569643bc1709561ec2e86f385df3759e5dd) envoie les 4351 ([1](https://etherscan.io/tx/0x23cb9bdf14eed955a84da3f3cfcf296356c0f897dec0b99e85151a7f084a3051) + [4350](https://etherscan.io/tx/0xc2fd5094c1e108f83222a86bd46b35fc0da35616385d681964b22003643f982e)) qu’ils ont extrait en vendant les $COVER au compte deployer**, ce qui représente 34% du total des pertes liées à l’exploit (9,4 millions de dollars).

---

**Couvert pas Cover**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/12/image-4.png)

**Il a fallu six heures au protocole Cover pour admettre publiquement l'attaque.**

> _L'équipe enquête toujours sur l'incident actuel. L'exploit n'est plus possible._
>
> _S’il vous plaît, n'achetez PAS de tokens _[$COVER](https://twitter.com/search?q=%24COVER&src=cashtag_click)_, et retirez vos liquidités de la pool COVER/ETH sur sushiswap._
>
> _Les pools d'équilibrage CLAIM/NOCLAIM ne sont pas affectées._

**Huit heures après l'attaque, le protocole Cover [a annoncé](https://twitter.com/CoverProtocol/status/1343581331448586245?s=20)** son plan en vue du remboursement des utilisateurs concernés.

> _Bonjour tout le monde, nous envisageons de fournir un token [NEW_$_COVER](https://twitter.com/search?q=%24COVER&src=cashtag_click) via snapshot d’avant que l’exploit de minting n’ait été réalisé. Les 4350 ETH qui ont été retournés par l'attaquant seront également traités via snapshot aux détenteurs de tokens LP. L’enquête suit son cours. N'ACHETEZ PAS DE COVER._

**L’expression "Ce qui est mort ne peut plus mourir” apparaît être plus vraie que jamais dans la DeFi**. Une quatrième itération du token du protocole COVER sera émise pour rembourser les utilisateurs concernés.

_SAFE - SAFE2 - COVER - $RECOVER?_

**La persévérance est admirable jusqu'à un certain point, mais trop n’est il parfois pas trop ?**

Certains lecteurs se souviendront de l'histoire complète de Cover Protocol, qui, anciennement SAFE, [changea de nom](https://coverprotocol.medium.com/cover-protocol-e202808aa4ef) après que @azeemfi et @chefcoverage eurent pris de mauvaises décisions. Ils avaient ensuite lancé SAFE2, qui migra pour devenir le COVER que nous connaissons aujourd'hui.

La communauté est-elle prête à leur offrir une QUATRIÈME chance?

---

![](https://lh5.googleusercontent.com/Ogj1lycooZFZrO1GfU4lgsis5tJ2j76L2BHPQ50TC3KuG7mTx_CQ-FcD90AfAQtSQqdc0ERGK95wczwmRdoznGUR9c00f381m3DAhRZp7Ego0j6U4WrxohU-RCMNtE0Sq0c4f55u)

**[Grap Finance](https://medium.com/@grap.finance) est un fork de Yam** qui n’a pas réussi à briller durant l’été 2020 de la DeFi. Ils ont sauté sur l'occasion afin d'attirer l'attention en se présentant comme des hackers éthiques, ce qui leur a valu de gagner des milliers de followers en une seule journée.

Reste à voir ce qu'ils feront de ce nouveau départ.

Cette activité soudaine a placé **Grap Finance** dans les cinq principales Dapps pour les changements de solde de COVER au cours des 7 derniers jours.

![](https://lh3.googleusercontent.com/FMvU_UZhki6SB0ery4HcON4MEfMbBSPmrah0QDGPCqgwePElvreCDCKdVct9Mo2-B2sqqgUqx8y4MQOpJIPMtn-VqI4tm3ND37FW_Kyz0sDVWKDvdmyBZpe555KyeVqpQd2hO6by)

Un succès de scandale reste une exposition publicitaire comme une autre, et cela semble être confirmé par le graphique suivant. 1,778 nouvelles adresses uniques ont utilisé COVER, et notamment des traders opportunistes cherchant à dépouiller la victime encore fraîche.

![](https://lh5.googleusercontent.com/n3eflB7D7s60xY-dZg_755bKnUbm-8XEpryBbapuAY1UhlCirnheGGcmDL8hX6Bv8im6TzNFOBryHjcrGL9bUPcMShVRB-wepJfTxod4M71KiL-15n9qdBhjJPRPCzuqe62ixMFZ)

Ci-dessous, Binance est en vert. On constate une énorme augmentation des dépôts COVER, la communauté essayant de quitter le navire avant de finalement voir le trading du token s'arrêter.

![](https://lh4.googleusercontent.com/ISdelPif5XcLBEWb4fNDHyOanmb9rPv5Ny47vHbshuH0bevewfDrt6Agt28yYWRiSgxUFSC_NPPX_Vp5oJOWFkCeXByfFP9pO07HniqwKcBtNeBgwCrJNKyepBp22XVFgxQeFyQB)

Un comportement responsable peut ne pas rapporter énormément, mais le salaire du péché est toujours payé en totalité.

Certains disent que c'était un complot interne qui a mal tourné.

Peut-être que les assaillants ont été doxxés, qu’ils n'ont pas pu garder les fonds, qu’ils les ont renvoyés et ont alors profité d'un petit coup de publicité à la place.

![](https://lh5.googleusercontent.com/8DTMgDPJE8_EL2ldg9LTM8_A4JtUw1oAbAIxFcZj3MOISWVwa5Do7EivF7R5SrcInzstS7lLnHYlA3Sug4uqC95aE_EAZdNOwIeD_QQvB5F9ckPTFrotVFZ2I02JaPT-Gb_J6MwY)

**Nous ne prétendons pas que ces rumeurs soient fondées sur des faits, mais il est facile de voir comment de telles idées surgissent lorsque les événements de la journée mènent à des annonces comme [celles-ci](https://support.mxc-exchange.com/hc/en-001/articles/360054776091).**

![](https://lh3.googleusercontent.com/LJ9XZzZF2hn1qinb-EP8NlGS3vK2QdGWllXXAgmYbHxVCGKF-B07NHSyXREHg7smGNDfyITiFgf7txfb0Eejrn-AVycPUzhnjTFV0dv7hD0Sqmfk_gHEUlonGnnc7J_qGLuzGhce)

**Une pure coïncidence étant inconcevable**, il s’agit là soit d’un acte criminel soit d’un cri de désespoir. MXC doit être tombé bien bas s'il répertorie les tokens en fonction des potins.

La sphère crypto de Twitter a prouvé que son appétit pour le risque restait important en pumpant le prix du [token](https://www.coingecko.com/en/coins/grap-finance) de leurs sauveurs de milliers de points, faisant passer son volume de négociation en 24 heures de 236 $ à 5,458,084 $ au moment de la rédaction de ces lignes.

---

**Emiliano Bonassi nous a livré la citation suivante :**

> _Si l’on met de côté le problème technique, cet événement a de nouveau montré à quel point cet écosystème est cohérent et solidaire._
>
> _Nous sommes antifragiles._
>
> _Je suis presque sûr qu'après cet événement émergera non seulement un nouveau protocole d’assurance, mais aussi et surtout un collectif hyper réactif pour garantir la sécurité de l’écosystème - peut-être L’Équipe des Hackers Éthiques._

---

**Le sang coûte cher. Le marché DeFi de l'assurance est dans un sale état.**

D'abord [NXM](/nxm-hugh-speaks-out/) et maintenant Cover. Qu’importe si le protocole n'est pas affecté. Si nous devons écrire un article sur vous, c’est que la confiance de l'utilisateur dans votre projet s’est déjà envolée.

**L'assurance DeFi doit être exhaustive**. Point de Divine Providence dans notre monde.

Les protocoles non sécurisés paient des bonus élevées, tandis que d'autres travaillent dur dans l’ombre sans rien réclamer.

En 4 heures, [COVER](https://twitter.com/search?q=%24COVER&src=cashtag_click) a baissé de x40 tandis que [$GRAP](https://twitter.com/search?q=%24GRAP&src=cashtag_click) a augmenté de 40x.

**[“Pas de gains”](https://twitter.com/GrapFinance/status/1343555258316804101?s=20) assure l'équipe Grap de derrière leur écran**, un beau conte qui ne raconte pas toute la vérité.

**Les hackers malveillants ne sauraient garder leur masque de super-héros bien longtemps dans la tempête d'accusations.**

L’enquête continue...

---

![](https://lh6.googleusercontent.com/p6se9Mb3aS2HWRTPsm98ZjKAwuUAel7YOOa02gjrlbP6q_iTmGLiQ21XiTm93L102-HH4pMRqgO5dDMZu5BOJOJYmJxSpg9IPRL9S7pHZTbfTksMZkuKjEZKamLrSyh-oxey40pq)
