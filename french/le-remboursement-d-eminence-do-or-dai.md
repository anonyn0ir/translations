---
title: LE REMBOURSEMENT D'ÉMINENCE - DO OR DAI
date: 02 Oct 2020
tags:
  - Eminence
  - Cronje
  - defi
excerpt: Se voyant forcer la main par les menaces des membres de la communauté, Andre Cronje et son équipe ont rapidement pris des mesures pour rembourser les 8 millions de dollars qui ont été mystérieusement rendus après que le contrat EMN a été exploité pour 15 millions de dollars le 29 septembre.
---

Se voyant forcer la main par les menaces des membres de la communauté, Andre Cronje et son équipe ont rapidement pris des mesures pour rembourser les 8 millions de dollars qui ont été mystérieusement rendus après que [contrat EMN a été exploité](/eminence-rekt-in-prod/) pour 15 millions de dollars le 29 septembre.

Mais pourquoi quelqu'un voudrait-il rendre 8 millions de dollars ?

Il s'agissait d'un hack sophistiqué qui a probablement nécessité des jours de travail. Pourquoi le hacker a-t-il décidé de rendre la moitié de l'argent seulement quelques minutes après l’avoir effectué ?

Est-il possible que Yearn connaisse l'identité de son assaillant ?

Si vous étiez le hacker, préféreriez-vous avoir 15 millions de dollars et être doxxé, ou bien 8 millions de dollars et profiter de votre vie en paix ?

Ce ne sont là que quelques-unes des questions que la communauté se pose après le spectaculaire exploit puis le remboursement survenus le 29 septembre.

Une analyse complète des trois transactions impliquées dans l'exploit est disponible ci-dessous.

[Transaction 1 Sep-29-2020 01:20:41 AM +UTC](https://ethtx.info/0x3503253131644dd9f52802d071de74e456570374d586ddd640159cf6fb9b8ad8)

[Transaction 2 Sep-29-2020 01:22:28 AM +UTC](https://ethtx.info/0x045b60411af18114f1986957a41296ba2a97ccff75a9b38af818800ea9da0b2a)

[Transaction 3 Sep-29-2020 01:23:28 AM +UTC](https://ethtx.info/0x4f0f495dbcb58b452f268b9149a418524e43b13b55e780673c10b3b755340317)

La transaction du renvoi est intervenue 8 minutes plus tard.

[Return Transaction Sep-29-2020 01:31:04 AM +UTC](https://ethtx.info/0x7bc97357364222207f1f011b22ad98ba78fcd3c25d3398346caa3928cdf4a4dd)

Plusieurs théories circulent sur l'identité du responsable de ce braquage, et certains se demandent s'il s'agit vraiment d'un hack ou si cela n’est pas plutôt qu’simple exploit de code inachevé.

[@mierzwik](https://twitter.com/mierzwik) a écrit cet [article](https://medium.com/@mierzwik/hey-bot-give-me-all-your-money-e1f692594f2e) sur le bot responsable de cette attaque ([0x762bfbd](https://etherscan.io/address/0x762bfbd8dc93fac514fd89c027e81621e8597441), dans lequel il montre comment le bot a volé 400 UNI une semaine avant l'attaque du REM.

[@frankresearcher](https://twitter.com/FrankResearcher) a depuis fait un excellent travail en enquêtant sur le même portefeuille utilisé dans ce hack / cet exploit.

![](https://lh6.googleusercontent.com/qov3BuEa6rc6VT97cxBh7jgvRYxeOMDi8PbS3qgjTyIKLVIZwE5d8yA1TtDPCuXM-7WmFhMAma9hdVdskBbEEZWG3XMl3ntRdiGVKhbnk2aDnlzTBOSpf1Iz0R_hTbj4yFdLxKVz)

Vous pouvez lire le reste des tweets de Frank [ici](https://twitter.com/FrankResearcher/status/1310885102407254021?s=20). Il poursuit son analyse en émettant des hypothèses sur le rôle des différentes adresses impliquées dans le hack / l’exploit.

Les hypothèses de Frank se basent sur des data on-chain :

0x223034e = le hacker de [$ENM](https://twitter.com/search?q=%24ENM&src=cashtag_click)

0x762bfbd = le contrat à partir duquel le hacker a retiré les [$UNI](https://twitter.com/search?q=%24UNI&src=cashtag_click)

0x2d033fe = l’adresse du créateur de 0x762bfbd

0x2f14f72 = l’adresse qui a financé le créateur (très probablement un seul propriétaire)

Cette enquête est toujours en cours, inscrivez-vous dès maintenant et vous serez tenu au courant de la suite des événements.

![](https://lh5.googleusercontent.com/bElo-Tzz3WEbKufKV60H8JybrfXU_jwZ4m5XmRARI3FsQCE9v57iOqnrOb89woPqABSKOBpGd6oMpwr4okPa42bKsiXrzNYkuoUNwXTN7sM6P9pxmXKpxBma5XIxHC5AzE5wMTnq)

Dans ce qu'il a décrit comme une “[solution élégante](https://github.com/banteg/your-eminence)” le développeur de Yearn, @bantg, a utilisé le code de distribution de LP Uniswap et une implémentation d'arbre merkle pour procéder au remboursement.

![](https://lh4.googleusercontent.com/N6RtgR2lbxx_noX8jN7NPq5o3kmScgGaOhpQnBgS6-QPU3l7GnWvEvbGBGybHNOKsMmpgR_gOCAxA4BALyDaHXkub1i89MDIyVjRDN-spFd7TgejtVFygH88VbZnjSPgsOytYUYu)
![](https://lh6.googleusercontent.com/KBuK7SdgDK_F5xS3SDpMwR3mawVkKuG4YhPOS90HjyjY1JewDai5IXxp7dsA3ROWvabWdhr2AI7YX2GeJhlT92bbIFctdRKwk-SjE_O0IXogKOYFLDALNu5DAZQEzww3gNFGzbmX)

Milkyklim a créé une [solution](https://gist.github.com/banteg/b2a3b78cdd59ea346afc56181e7a07cd) de remboursement yYFI similaire pour ceux qui ont claim le contrat yYFI entre les blocs 10923319-10954777 et ont été pénalisés par un problème de frais de l'ordre de 5 %.

![](https://lh4.googleusercontent.com/FiHtOA8Xk-LxkXVD4Cm-eq0ftH7tPFPxNoCmbzX1EXzppq4Hz_Ge9RIgHdD8gzV02dexKQGrljMg46xXl0mJTrocaHofDR2fdgpOYcA2bDxGAxH8fM0NE9rWTajN5duN4i4NG3ro)

Une fois que les remboursements ont été mis à disposition sur youreminence.finance, les remboursements ont été distribués à un rythme de 250,000 $ par minute.

![](https://lh4.googleusercontent.com/Cj0OwsQJkhLnq8Lheqzy6Qa_rLUbG0x4h_xkBLpeLSZPETYI5Tt4TaGlA9_4HACZw-0mSCnW0kYejV0F88Hb6nWlvTTEUTlhx3pMeGczF2nJ9QzwR3pdO5ydhQk_pfT3OG6FheMR)

Ainsi, la moitié du remboursement de 8 millions de dollars a été réclamée en seulement 20 minutes.

![](https://lh3.googleusercontent.com/jSpxxX0Z1wyYeVZlXFy6ToRnqV0kpyzqiaVS-t_UB8GSuYgPCfLkzfAnIwZJWweng1Ymx2l3lVTa3TGKOjGMbPCamGtfvLtSn_hT8fsE1yjeeAHD5tYfvvAnC5kSUSR3IxsFnM9l)

Si l’équipe s’est pliée en quatre pour créer ce snapshot, il semble que de nombreux utilisateurs n'aient pas été suffisamment attentifs au moment de demander leur remboursement et aient simplement copié la capture d'écran de banteg, ce qui a eu pour effet de renvoyer la totalité de leur claim à banteg et son équipe.

[100% tip for 340 DAI](https://etherscan.io/tx/0x6a17f1b30b8c5479e6542fb3d6189cf67f34bbc85cba7d669cbf72367bfb724f)

[100% tip for 66.9 DAI ](https://etherscan.io/tx/0xa7ad9985bc7ba00070f5ef18b766e10ca4c0d155cf4ca6ae2e11df9af41b6fc1)

[100% tip for 993.3 DAI](https://etherscan.io/tx/0x835b998d086ea0aee96d1e0a3e5b558c62da8d621959f213c10bed6250c9f9c0)

[100% tip for 263.1 DAI](https://etherscan.io/tx/0x7c759f66b058eb2dceb8a67a648dd4d0a0857bbfd38f51e8b058d18673f1c616)

La liste complète des transactions de pourboires peut être consultée [ici](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f?a=0x7a1057e6e9093da9c1d4c1d049609b6889fc4c67).

Certains se sont demandé pourquoi cette option de remboursement de claim sous la forme d'un pourboire à 100 % avait été rendue possible, alors qu'elle aurait pu être plafonnée à 10 ou 20 %.

Il est aussi intéressant de noter que ceux qui ont le plus profité de ce remboursement sont ceux qui ont laissé le plus petit pourcentage de pourboires par rapport à leur claim.

![](https://lh5.googleusercontent.com/w3CD80RlDF-F-FnDBUlO5UdU0pEm4X5tgy87FpLXyBGXXQInQ4_9A9op0xp8bTaPrNjtLaAkGDe8G1AhR61qyW-YuGJUXCW_JDyCXM6xsNKh47TGPCimBoez_F1dqVcwc7rr-0Xs)

Baleines cupides... 

Voici quelques chiffres supplémentaires sur les claims et les dons de DAI via youreminence.finance, grâce à l'aimable coopération d'Alphaleakers.

![](https://lh6.googleusercontent.com/goJyvxqXCAg8kCYnCZj5di0wvRE5I4BtroyTdY3GK88wyX67fJ4rAoWSPkTtXVa_CQ5Lo7Oba2kS0K_t8AHtvgoAkLBzKv8wHk_OIk3T4UOr1ux3SSsYBpjcAOzmoE-0ZRYq6kG4)

rektHQ est fait par et pour la communauté. Nous sommes très reconnaissants envers les membres de la communauté qui nous ont contactés ces derniers jours pour nous offrir leurs connaissances et leur soutien. Notre objectif est de relayer vos histoires et vos opinions, de protéger votre identité et de promouvoir votre récit, tout en plaçant l'honnêteté et l'exactitude au-dessus de tout.

Les articles d'opinion suivants proviennent de membres anonymes de la communauté. rektHQ a beaucoup de respect pour ceux qui ont contribué à l'article d'aujourd'hui par le biais de leurs réflexions et de leurs informations. Notre boîte de réception reste ouverte pour toute personne qui souhaiterait nous contacter, toujours en tout anonymat.

_Comme toujours, rektHQ décline toute responsabilité quant au contenu ou aux opinions présentées dans cette newsletter._

---

**ANON 1**

Je ne suis pas partisan du remboursement des 8 millions de dollars pour deux raisons.

Tout d'abord en raison des menaces proférées à l'encontre d'Andre pour que celui-ci demande à la trésorerie de Yearn de l'aider à rembourser les 8 millions de dollars. Je n'ai pas connaissance de la nature exacte de ces menaces, mais le fait d'être allé jusqu'au bout du remboursement crée un précédent très dangereux qui tend à renforcer l'idée que menacer les membres d’un projet est un comportement viable pour obtenir le résultat que vous souhaitez. 

La seconde raison est évidemment celle liée à l'aléa moral, point qui a déjà été longuement discuté sur CT. Les économistes autrichiens adorent utiliser le terme "aléa moral" pour décrire l'interventionnisme, ce qui, en termes simples de DeFi, fait référence au fait que les degen s'engagent comme des dégénérés qu’ils sont dans des projets de plus en plus risqués et non contrôlés parce qu'ils "s'attendent" à être partiellement renfloués dans des situations comme celles-ci. Ce type de transfert de risque existe bel et bien dans le monde réel où les grandes banques s'attendent à ce que le gouvernement fédéral les renfloue si elles connaissent des moments difficiles. Mais voulons-nous vraiment reproduire cela dans l’univers de la DeFi ? 

Quelle que soit la personne qui a exploité EMN, elle a fait preuve d'une grande capacité d’initiative et d'une grande ingéniosité. Mais, plus important encore, elle a en substance partagé un plan détaillé sur la manière de mener une attaque simple mais lucrative et de détourner l'attention vers le projet même qu'elle a attaqué, lui faisant ainsi endosser toute la colère et les menaces injustifiées. Il se pourrait même que cela devienne la nouvelle norme pour les exploiteurs que de donner un pourboire aux systèmes qu'ils viennent de manipuler, devenant en quelque sorte un code de conduite tacite entre voleurs.

Quelle que soit l'issue de ce dernier incident dans les semaines à venir, il convient de s'interroger sur le message que celui-ci envoie à tous les agents malveillants de cet environnement, ou même aux personnes neutres et soucieuses éthiquement qui regardent ces malfaiteurs s'en tirer, encore et toujours, en toute impunité.


**ANON 2**

Sur le plan technique, je pense que l'implémentation était un peu maladroite car elle a d'abord été déployée sur le testnet.

Il est admis qu'il est encore relativement difficile de forker le mainnet et de l'exécuter localement pour tester uniswap, balancer ou bonding curve, donc même si je peux comprendre le "tester autant que possible", nous savons que les vrais tests se font en prod…

Cependant, ce genre de discours ouvre la voie aux développeurs minables et aux arnaqueurs, ce qui, étant donné le nombre récent de cas de rug pull "d’Uniswap" recensés récemment, est effroyable.

Je veux dire qu'avec le recul, c'était *et* ce n'était pas la faute d'Andre. Il y a eu tellement de battage médiatique autour de lui que l'idée que cela puisse arriver était tout à fait plausible.

Je veux dire qu'il y a tellement de choses auxquelles vous pouvez penser cognitivement lorsque vous développez, que vous êtes plus concentré sur la roadmap du projet que sur ces risques de degen supplémentaires liés à la DeFi qui, de l’aveu général, sont toujours en train d'émerger.

Que l'équipe travaille derrière cela ou non, ce serait toujours le même problème.

Je suppose que le timing a été un peu foiré en ce qui concerne le volet communication. Les gens préfèrent ne pas maintenir autant la communication, surtout vu le nombre de nouveaux développeurs qui ont rejoint la communauté 
[$YFI](https://twitter.com/search?q=%24yFi&src=cashtag_click)...

Andre a retweeté la photo, puis les gens ont commencé à imaginer un complot pour prendre tout le monde par surprise.

Personnellement, j'avais aussi cette impression. La culture crypto est tellement tordue que les gens aiment les énigmes et l'anonymat, à son propre détriment, mais c'est simplement mon point de vue.

Sur la question du remboursement, cela permet de montrer que le projet sera toujours poursuivi en toute bonne foi.

Cela montre également qu'il y a une touche humaine dans toutes ces actions de degen de haute TVL.

Les gens prennent beaucoup de risques en général, quel que soit le domaine ou la classe d'actifs.

On ne peut pas reprocher aux gens de rendre les fonds d'un exploiteur à ceux qui sont [#halfrekt](https://twitter.com/hashtag/halfrekt?src=hashtag_click), tout comme on ne peut pas reprocher à l'exploiteur de rendre la moitié des fonds en premier lieu.

Je ne suis techniquement pas au niveau d'Andre, et j'avais l'intuition que cela aurait pu être tiré au clair avant d'aller dormir, mais, en fait, c'était juste une histoire de pur hasard.

Tout le monde a juste besoin de davantage de sommeil.
