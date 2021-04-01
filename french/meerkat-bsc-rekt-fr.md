---
title: Meerkat Finance - BSC - REKT
date: 04 Mar 2021
rekt: 
  amount: 32000000
  audit: Unaudited
  date: 04 Mar 2021
tags:
  - BSC
  - Meerkat
  - REKT
excerpt: Un début impressionnant pour le premier grand exploit de la BSC, alors que Meerkat Finance s’installe directement à la troisième place de notre classement.CZ et son équipe vont-ils roll back leur blockchain d’entreprise, ou bien vont-ils laisser leurs utilisateurs subir des pertes ? Cette arnaque de suricates ne laisse aux voleurs aucun endroit où se cacher. 
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-header.png)

**Rétrospectivement, c’était inévitable.** 

Un début impressionnant pour le premier grand exploit de la BSC, alors que Meerkat Finance s’installe directement à la troisième place de notre [classement](https://rekt.eth.link/leaderboard/).

Après une seule journée de fonctionnement, Meerkat Finance s’est fait rug pull pour 13 millions de BUSD et environ 73.000 BNB, soit un montant à l’heure actuelle d’environ 31 millions de dollars.

Nous avons observé la Binance Smart Chain durant leur speed run similaire à celui de l’été de la DeFi sur Ethereum. Maintenant que leur codes copiés d’Ethereum ont accumulé suffisamment de capital, ils semblent entrer dans la phase des _rug pull_.

**La suite des évènements sera intéressante à observer.**

CZ et son équipe vont-ils [roll back](https://twitter.com/cz_binance/status/1125996194734399488?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1125996194734399488%7Ctwgr%5E%7Ctwcon%5Es1_c10&ref_url=https%3A%2F%2Fwww.coindesk.com%2Fbinance-may-consider-bitcoin-rollback-following-40-million-hack) leur blockchain d’entreprise, ou bien vont-ils laisser leurs utilisateurs subir des pertes ?

**Cette arnaque de suricates ne laisse aux voleurs [aucun endroit où se cacher](https://www.youtube.com/watch?v=58UD3jU86pY).**

Où donc pourraient-ils fuir sur une si petite blockchain ? Binance a [fermé ses bridges](https://twitter.com/madcapslaugh/status/1367448466453106693?s=20), fut inaccessible pendant un court instant. Était-ce car le trafic était trop dense, ou bien était-ce une sorte d’écran de fumée ?

Meerkat Finance a d'abord prétendu qu'il s'agissait d'un hack, mais a ensuite supprimé ses comptes,ne laissant d’autre choix aux utilisateurs que de s'en prendre à eux-mêmes, ou _peut-être à Binance_.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-investigate.png)

_Nous remercions chaleureusement [0xdeadf4ce](https://twitter.com/0xdeadf4ce)._

- **Meerkat Finance Deployer upgrade 2 vaults du projet.**
- L’adresse de l’assaillant a call permissionless initialization function à travers les proxies du Vault, permettant à quiconque de devenir le propriétaire du Vault [[2]](https://bscscan.com/tx/0xfcf48681e382e9f9cc1d6a64ff30487306f6b869924c6594075fcc86b3b21f5d)
- L’assaillant draine par la suite les Vaults, il call pour cela une fonction avec la signature 0x70fcb0a7 qui accepte l’adresse du token comme input. La décompilation de l’upgraded-to Smart Contract montre que la seule utilisation de la fonction invoquée a suffit pour supprimer les fonds avec le propriétaire comme bénéficiaire.

Normalement, si le contrat a une fonction qui permet au propriétaire de récupérer les actifs utilisés dans la stratégie/le vault, c’est que vous faites confiance à l'équipe de projet.

Ils peuvent débrancher la machine quand ils le souhaitent.

C'est pourquoi des projets comme Yearn ajoutent des checks comme indiqué dans l'image ci-dessous, afin que l'équipe ne puisse sauver que les fonds qui ne sont pas activement utilisés par la stratégie/le vault.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-code.png)

Les deux vaults affectés utilisaient le pattern du Transparent Proxy Upgrade d’OpenZeppelin, permettant d’upgrade la logique du Vault vers une nouvelle logique d’implémentation par le call de la fonction upgradeTo(address newImplementation) sur le level du proxy du Vault.

L’implémentation précédente du Vault de BUSD est localisée à [0x49509a31898452529a69a64156ab66167e755dfb](https://bscscan.com/address/0x49509a31898452529a69a64156ab66167e755dfb), l’implémentation précédente du Vault de WBNB est localisée lui à [0x3586a7d9904e9f350bb7828dff05bf46a18bb271](https://bscscan.com/address/0x3586a7d9904e9f350bb7828dff05bf46a18bb271), les deux étant des contrats vérifiés et peu visibles.

**Meerkat Finance Deployer call upgradeTo() deux fois :**

- au block 5381239, réglant l’implémentation du Vault sur [0x9d3a4c3acee56dce2392fb75dd274a249aee7d57](https://bscscan.com/tx/0x063970f8625f250101a7da8abf914748cf8eaaaa9458041f1928501accfe5d6c)
- au block 5381246, reglant l’implementation du Vault BUSD sur [0xb2603fc47331e3500eaf053bd7a971b57e613d36](https://bscscan.com/tx/0xf19fa4bcff4adaebeddd28c851458ba0f01ffedd52b62df56ace94e7c8842553)

Ceci a changé la logique du Vault pour introduire deux fonctions notables qui n'ont pas fait partie des implémentations initiales.

- init(address owner)
- Selon le bytecode décompilé, cette fonction établit l’adresse sur le slot 0 du stockage à l’adresse fournie à la fonction.

**Il n’y a pas de check de permission, faisant de cette fonction nouvellement ajoutée l’ultime porte dérobée des Vaults.**

L’utilisation d’un pattern Initializer spécifique dans les  proxies transparents est une bonne pratique et a été aussi mise en oeuvre dans les premières implémentations de Vault, et il est donc très compliqué de ne pas voir derrière l’ajout de init() method autre chose qu’un vol planifié des fonds.

- 0x70fcb0a7(address _param1)

Le code source n’est pas disponible, le source décompilé est limité à pouvoir checker que le caller est égal au slot de stockage 0 définit par init() method et à transférer le balanceOf() du token contract fourni avec param1, en utilisant l’adresse du Vault comme cible de la requête. Les deux fonctions ne font pas partie des implémentations du Vault précédent.   

En comparant la taille du bytecode des anciennes et des nouvelles implémentations, on peut affirmer que la nouvelle implémentation fait seulement 1/4 de la taille de la logique précédente. 

Puisque les upgrades ont été faites par Meerkat Finance Deployer, il apparait que le scénario le plus probable, si l’on prend en compte toutes les données on-chain, soit celui d’un rug pull intentionnel, même si la piste d’une compromission de clés privées n’est pas totalement à écarter.

A l’heure où nous écrivons ces lignes les fonds ont été partiellement divisés entre plusieurs adresses, et envoyés à ce qui appartient apparemment au Binance Bridge hébergé par Binance Exchange.

Le Bridge de [Binance.org](http://binance.org/) est actuellement suspendu, probablement pour éviter que les fonds ne soient facilement déplacés vers d'autres blockchains.

**Chronologie (04.03.2021)**

**Mar-04-2021 08:53:10 AM +UTC**

Meerkat Finance Deployer upgrade le Vault WBNB sur le contrat 0x9d3a4c3acee56dce2392fb75dd274a249aee7d57

**Mar-04-2021 08:53:31 AM +UTC**

Meerkat Finance Deployer upgrade le Vault BUSD sur le contrat 0xb2603fc47331e3500eaf053bd7a971b57e613d36

**Mar-04-2021 08:54:31 AM +UTC**

L’assaillant call method 0x70fcb0a7 sur le Vault BUSD pour transférer 13,968,039 BUSD

**Mar-04-2021 08:54:55 AM +UTC**

L’assaillant call method 0x70fcb0a7 sur le Vault WBNB pour transférer 73,635 WBNB

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-linebreak.png)

**Les mêmes jeux sont joués sur des blockchains différentes, mais les rapports de force ne sont pas les mêmes. Cz veille au grain, et les bridges prennent feu : les voleurs n’ont nul part où se cacher.**

Même au sein du groupe Telegram [Meerkat_Rugpull](https://t.me/Meerkat_Rugpull) les membres du chat n'étaient pas totalement d'accord sur la façon dont ils voulaient que Binance gère la situation.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-poll.png)

**Binance _peut-il_ roll back la blockchain et rembourser ses utilisateurs ?**

La réponse n’est pas si évidente : si les 21 mystérieux [validateurs](https://docs.binance.org/smart-chain/validator/guideline.html) pourraient en théorie organiser un remboursement, c’est en réalité peu probable. Cela ne ferait qu'alimenter les problèmes de la CeDeFi et qaugmenter la charge de travail des (probablement déjà stressés) avocats de la BSC.

Binance aura sûrement déjà planifié à l'avance la manière dont ils géreraient un tel scénario. La manière dont ils gèrent cette affaire créera un précédent.

Bien que que cela ne soit pas le [premier rug pull à hauteur de plusieurs millions](https://twitter.com/news_of_bsc/status/1354880400984739842?s=20), c’est le premier depuis la montée en puissance de PancakeSwap et l'augmentation du nombre d'utilisateurs qui l'a accompagnée.

Ignorez le cas improbable où quelqu'un de Binance interviendrait pour trouver un distributeur de merkle et retourner les fonds : l'argent a disparu.

**Force est donc de constater que les protocoles sur la BSC ne sont pas plus sécurisés que ceux sur Ethereum.**

CZ ne vous sauvera pas. Leur transactions sont moins chères, mais il n’y a pas là-bas de contenu original.

_Que deviendra cette blockchain d’entreprise quand la L2 d’Eth sera là ?_ 

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/mf-rektkat.png)
