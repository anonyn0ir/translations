---
title: Coinbase & l'Oracle
date: 26 Nov 2020
tags:
  - coinbase
  - oracle
  - liquidation
excerpt: Lors de récentes attaques des hackers ont rendu des millions de dollars à leurs victimes, ou ont simplement laissé l’argent sur la table quand ils auraient pu en prendre bien plus. Si différentes méthodes ont été utilisées pour voler des fonds depuis la récente épidémie de hacks, un personnage lui a joué un rôle central tout du long …
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/MV5BMjQ1NDAwMzI4Nl5BMl5BanBnXkFtZTgwMDkwMTEyMjI@._V1_.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/MV5BMjQ1NDAwMzI4Nl5BMl5BanBnXkFtZTgwMDkwMTEyMjI@._V1_.jpg)

**On ne voit pas plus loin que les choix qu’on ne peut pas comprendre.**

Lors de récentes attaques des hackers ont rendu des millions de dollars à leurs victimes, ou ont simplement laissé l’argent sur la table quand ils auraient pu en prendre bien plus.

Si différentes méthodes ont été utilisées pour voler des fonds depuis la récente épidémie de hacks, un personnage lui a joué un rôle central tout du long …

Selon Morpheus, l’Oracle était au service de la résistance “depuis le début”. Elle est un programme doué de conscience et de sensations qui aide la résistance humaine à libérer l'humanité de l'oppression des Machines.

Récemment, l’Oracle a été constamment attaquée par des agents anonymes qui visent à manipuler sa perception de la réalité afin de maximiser leur profit.

![](https://lh4.googleusercontent.com/nhT68w2sqe78xupagMe6jDYDzLskFBs0GOd2etbcsldnFj0LNkNHCvMRApiO8qLy91wYNoO96OsN4oupin4YuJSDs_uaxUdpvp7Ae4CTaro405Kjt8FcLNajbg3am9mC7UoV-Emi)

> [NEO :](https://youtu.be/CsigSyTME9E?t=87) _La question plus évidente serait donc : comment vous faire confiance?_

> ORACLE : _Bingo. Alors là, pas de doute, tu es dans le pétrin._

**Les problèmes de confiance ne sont pas nouveaux avec les oracles, qui peuvent être aussi bien on-chain que off-chain.**

Comme l'a [écrit](https://samczsun.com/so-you-want-to-use-a-price-oracle/) samczsun:

_Vous avez deux approches possibles. Soit vous pouvez simplement prendre la data existante du prix off-chain via un API ou un échange et l’amener sur on-chain. Soit vous pouvez calculer le prix instantané en consultant des échanges décentralisés on-chain._

Les deux options ont leurs avantages et leurs inconvénients.

Les oracles de prix tels que Uniswap, Kyber ou Balancer ne requièrent guère d’accès privilégié et sont toujours mis à jour, mais ils sont cependant facilement manipulables par les assaillants.

Les oracles off-chain **tel que Coinbase** sont généralement plus lents pour réagir à la volatilité, et ils nécessitent également

**_“des utilisateurs privilégiés pour mettre les data on-chain. Vous devez alors leur faire confiance et espérer qu'ils ne sombrent pas vers le côté obscur de la force et ne soient pas contraints de faire des mauvaises mises à jour.”_**

La liquidation massive d’aujourd’hui était due à une erreur, ou à une manipulation, de l’oracle Coinbase.

**Nous avons assisté à une liquidation de plus de 110 millions de dollars sur Compound Finance en raison de leur dépendance à Coinbase, du fait que cela soit leur unique oracle.**

![](https://lh6.googleusercontent.com/sR9XX4BQ3SiHSNM2iZzUh8msdZQ45UDfTkhhChTlKD55pzU3rNQU8hPyHUJndLeW7jXvbW0CWRErqePHbQQNnZ-KlR8HWbGNz2ImvumqAKO2sDaQozoq5pHTVyB7kmOhc6ZWj9P5)

La populaire paire de yield farming DAI/USDC a vu son prix déréglé quand le DAI est monté à 1,3$, provoquant des liquidations multiples au profit d’agents anonymes qui étaient justement positionnés pour les liquider.

> [Sam Priestley](https://twitter.com/arbingsam/status/1331922588193484800?s=20) explique comment la liquidation peut se produire et comment les gens peuvent en profiter.

> "Quelqu'un a été liquidé pour 49 millions de dollars aujourd'hui. Le liquidateur a reçu 3,7 millions de dollars juste pour avoir call une méthode.

> La victime était un farmer de comp utilisant des leviers. Ils prêtaient des DAI et des USDC et empruntaient des DAI et des USDC. Quand le prix du DAI a changé, leurs comptes ont été en liquidation. S’ils avaient gardé leur DAI et leur USDC dans leur wallet ceci ne serait jamais arrivé.

> Lorsque votre compte est en liquidation, le liquidateur peut choisir de saisir le collatéral qu’il souhaite en échange du remboursement de votre dette. Ici le liquidateur a pris du DAI. Emprunt de DAI depuis Uniswap. Remboursement de la dette en DAI. Obtention de plus de DAI par la liquidation. Remboursement d’Uniswap. Profit.

> Une baleine a pu se sentir en sécurité car elle n’a jamais call la fonction enter-markets pour l’USDC. Mais en empruntant de l'USDC, ils ont activé l'USDC comme collatéral pour leur dette en DAI.”

![](https://lh4.googleusercontent.com/4s6zvtJuvM2gvebHTrXn_Nn5yf2wCtpMGMgQYkWmRFNgmyyT4vcfw1BpOKTNaZQkwMJ2dBo9ObVKOapaqOwykDqfT8f_Dx7dTBATRTD7egKq6y0il5mGetT2Jz6etsB97j0Cm4dC)

Merci à [@arbingsam](https://twitter.com/arbingsam/status/1331922588193484800?s=20) pour l'analyse.

Le graphique ci-dessous montre la flambée du prix du DAI - une fluctuation massive pour une coin supposée stable.

![](https://lh4.googleusercontent.com/CWugWH8TcpdzKzgTzseevvzKjHuVzZGZ7XbUD1k6w5JT4v9Sqx2e0u4WsFoND5rFrb7cPehLXQhpNhwKNrtVOnlc7V51HSHaXMm0zvN9rELvuuTDzvFESAxTCo0SJPsQwnlt_K0k)

[Coinbase](https://blog.coinbase.com/introducing-the-coinbase-price-oracle-6d1ee22c7068) était conscient des problèmes liés au recours à des oracles off-chain lorsqu’il a présenté le sien :

> _“Utiliser des data d’un oracle off-chain nécessite d’avoir confiance dans celui qui publie, et notamment sur le fait qu’il poste les bons prix et garde la clé privée en sécurité”_

Mais plutôt que de chercher à réduire cette nécessité de confiance, ils ont plutôt cherché à rassurer le lecteur en lui rappelant à quel point Coinbase était digne de confiance.

> _Coinbase est l'une des entreprises les plus fiables dans le domaine de la cryptographie et une grande partie de notre mission est de développer la cryptoéconomie. Un flux de prix particulièrement fiable ancré dans l'infrastructure Coinbase peut aider à rendre l’écosystème DeFi plus sûr, réduire les risques systémiques et lancer la prochaine vague de croissance et d’adoption._

Il semble que Robert Leshner les ait crus, comme en témoignent ses dires de l'époque :

> _“L’oracle de prix de Coinbase va augmenter la sécurité et la décentralisation du flux des prix de Compound, c’est qui est une mission cruciale pour le protocole et l’écosystème d’applications construit  sur Compound. Nous ne sommes pas seuls - le reste de la DeFi bénéficiera d’un développement plus rapide, de data cohérentes, et de standards communs.”_

> _— Robert Leshner, Compound CEO_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/image.png)

**Qu’est-ce qui a cloché ?**

Si *“les oracles off-chain nécessitent des utilisateurs privilégiés pour mettre les data on-chain”*, comment cela a-t-il bien pu arriver ?

La [page d'état](https://status.coinbase.com/) de Coinbase affiche actuellement les informations suivantes :

![](https://lh6.googleusercontent.com/WQdMK6Voz-KX1DowA36GhZf8G3xrLN91xG6hFjHpevjVeA8VUL-2b3YPb-QYqyUBb9EjOoRG4c_M-gHNuoaMkmlze58fQUvpkim6SA-GtjkDt9KBh8gjFbMHwcjmk5QCZpt-LNVp)

L’oracle de Coinbase a déjà rencontré des “problèmes” dans le passé, des problèmes qui semblent toujours conduire à des situations particulièrement rentables pour certains acteurs.

Si nous ne pouvons savoir à l’heure actuelle si cela a eu lieu à cause d’une manipulation ou d’un problème technique, nous sommes certains qu’aucun flash loan n’a été utilisé. Manipuler le carnet d’ordres de Coinbase d’une telle façon aurait coûté 100 000 DAI, puisque le carnet de commandes avait une profondeur de 300 000 et que le prix estimé atteignait 1.3$.

Cela est-il arrivé à cause d’un acte malveillant, d’une erreur d'inattention ou d’une technologie désuète ? Dans tous les cas, les robots de liquidation ont su profiter de l’incident.

Utiliser une source unique et centralisée de data comme oracle de prix n’est pas une bonne idée, sachant que Coinbase se révèle réellement peu fiable, tout spécialement s‘il est possible de de supprimer d’un claquement de doigt le carnet d'ordres avec 100k. 

> _"Il y a des programmes un peu partout. Ceux qui font leur travail, qui remplissent leur rôle, sont invisibles. Leur présence est insoupçonnable. Mais les autres… Ils font parler d'eux tout le temps"._

![](https://lh6.googleusercontent.com/7H_rZ46PnRaGA2vlOfTOgp5Lz0wtz7M4nNyuqEnLDDEx8fd2U5j5kOsfyw7MOWSo406JcW5btz4BYFBKT6KwZeAZDsMZayIuWC_K_0HB4zfRwkP03AweiMCJkwT6TX7w3krY1Nfs)

Oh, et ne t'inquiète pas pour le vase
