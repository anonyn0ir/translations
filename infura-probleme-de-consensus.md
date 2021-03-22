---
title: Infura - Problème de consensus
date: 11 Nov 2020
tags:
  - geth
  - infura
  - ethereum
  - Fork
excerpt: Le consensus n’est pas qu’une question d’accord, il tend avant tout à changer les choses. Nous avons assisté à une série de problèmes sur le réseau Ethereum, des failles de consensus ayant affecté le mainnet.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/12-angry-men-1.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/12-angry-men-1.jpg)

**Le consensus n’est pas qu’une question d’accord, il tend avant tout à changer les choses.**

Nous avons assisté à une série de problèmes sur le réseau Ethereum, des failles de consensus ayant affecté le mainnet.

Les services utilisant les anciennes versions des nœuds se sont retrouvés bloqués sur une chain minoritaire, affectant par effet domino toutes les applications qui en dépendaient.

La plupart des utilisateurs ont appris le problème quand l’API de Infura est tombée en panne. Infura est le plus grand fournisseur de nœuds sur le réseau Ethereum, fournissant des outils et une infrastructure à la plupart des applications et plateformes d’échanges centralisées utilisées sur le Web 3.0, parmi lesquelles Metamask, Uniswap ou encore Binance.

La dégradation du service d’Infura a révélé que Binance soit dépend d’Infura, soit utilise des nœuds obsolètes, ce qui dans tous les cas n’est pas digne d’une plateforme d’échange aussi importante.

Bien qu’il puisse paraître étrange qu’Infura n’utilise pas les dernières versions de [geth](https://geth.ethereum.org/downloads/) il apparaît logique qu’un opérateur de telle envergure ne passe pas directement sur la dernière version : sauf en cas de hardfork, il n’y a pas de raison urgente d'abandonner un code de travail fiable pour passer à un inconnu.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/add3dbfcb32773693acdf1699dc73e8f.png)

Le moteur de recherche et d'analyse Blockchair a également rencontré des problèmes, et a publié le tweet suivant :

> _Nous rencontrons actuellement des problèmes avec notre explorateur_ [#Ethereum](https://twitter.com/hashtag/Ethereum?src=hashtag_click) _et travaillons sur une correction. Il semble qu’il y ait un split de chain, et certains nœuds (dont les nôtres et ceux de certains miners) sont bloqués sur une chain minoritaire._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/Emh9J7sW8AEB_FT.jpg)

Le développeur principal de Blockchair, [Nikita Zhavonronkov](https://twitter.com/nikzh/status/1326455533927329792?s=20), a signalé avoir reçu l'erreur suivante :

> _########## BAD BLOCK #########_

> _<…>_

> _Error: invalid merkle root (remote: 57cc91ee8b91b956592a27b14386abc2aba723b5f4f9e5d3181ace6b5d3cd433 local: 1f9ee59bfa683a25c7a15b626995a3ad7c58c571b40df96eea31e5c5eed9732d)_

**Deux importantes vulnérabilités ont été détectées sur le réseau geth**, toutes deux par [John Youngseok Yang](https://github.com/johnyangk) (Software Platform Lab), ce qui lui a rapporté 20 000 points dans le [classement](https://bounty.ethereum.org/).

Pour éviter la multiplication d’exploits, les failles de consensus ne font pas l’objet de discussions sur GitHub Issues, de sorte que les détails spécifiques des vulnérabilités ne sont pas encore connus. Pour ceux qui souhaitent en savoir plus sur les détails techniques, [Mhswende](https://twitter.com/mhswende/status/1326489526450221056?s=20) déclare que

> _“Il pourrait bien y avoir un article ou une présentation devcon à ce sujet à l'avenir”_

Afin de minimiser les perturbations, les développeurs d'Ethereum ont décidé de hard fork.

Comme l’a écrit [Péter Szilágyi](https://twitter.com/peter_szilagyi/status/1326476649278414850?s=20) sur Twitter :

> _Ça a été un hard fork inopiné (d’une mauvaise chain à une bonne). Cela dit,réparer discrètement un bug dormant depuis plus de deux ans avait moins de chance de provoquer une perturbation que de sensibiliser les gens à ce problème. Nous nous efforçons de minimiser les dégâts potentiels_

Ceux qui se plaignent de la panne d’Infura feraient bien d‘en tirer des leçons. Gardez vos nœuds à jour, car une fois que vous déléguez votre nœud à une autre partie, celle-ci a la mainmise sur la direction des événements. 

Infura a fait preuve de transparence durant toute l'affaire, et il est incontestable que l’équipe travaille dur pour résoudre le problème.

Infura est de nouveau [en ligne](https://forkmon.ethdevops.io/), et les mises à jour des statuts peuvent être consultées [ici](https://status.infura.io/).

**La panne d'Infura a fait réaliser à beaucoup d'entre nous à quel point nous étions dépendants de cette seule entité.**

**Il s’agit d’un service centralisé agissant comme un gardien de notre système décentralisé.**

**Les individus comme les institutions doivent réfléchir à leur stratégie pour l'avenir.**

L’apparente compétence des grandes plateformes d’échanges centralisées telles que Binance ou Bithumb semble s’être évaporée,ceux-là ayant été contraints de désactiver les retraits d’ETH et d’ERC-20 durant la panne, en dépit de leur devoir de protéger les utilisateurs de tels incidents.

**Nous ne pouvons pas à ce point-là compter sur Infura.** En raison de la dépendance par défaut de MetaMask vis-à-vis du fournisseur de nœuds centralisés, l'ensemble du réseau Ethereum a été temporairement déserté, et le gaz s'est réduit à seulement 12 gwei.

Ceci est la preuve d'une dépendance malsaine, et un indicateur clair du préjudice potentiel qui pourrait découler d'une telle dépendance.

Voulons-nous que notre société numérique reproduise les mêmes erreurs qu'ailleurs, en étant dépendante de points de défaillance uniques et centralisés ?

**Nous avions créé un Internet gratuit, mais l'avons offert à un petit groupe d'autorités centralisées** - Chrome, Safari, Brave… Nous avons construit un internet alternatif où les valeurs originelles d'anonymat et de décentralisation sont toujours présentes, mais nous l'appelons le "Dark Net" et son accès est limité à des logiciels alternatifs souvent bloqués.

Nous ne pouvons pas réserver le même avenir à la cryptomonnaie.

[David Mihal](https://twitter.com/dmihal/status/1326520031379853313?s=20) écrit:

> _La panne d'Infura d'aujourd'hui a poussé les utilisateurs à se démener pour trouver un autre fournisseur RPC._

> _J’ai vite fait rassembler_ [**http://ethereumnodes.com**](https://ethereumnodes.com/) pour créer une liste centrale de points de terminaison RPC publics et gratuits & leur statut actuels._

[Michael O’Rourke](https://twitter.com/o_rourke/status/1326509249825038336?s=20) a souligné que :

> _Si votre Metamask est en panne, vous pouvez changer le fournisseur RPC en Pocket avec l'URL suivante_

> [https://eth-mainnet.gateway.pokt.network/v1/5f3453978e354ab992c4da79](https://t.co/7a76Xoo8Qu?amp=1)

**Tout échec de consensus est un problème grave.** Un hard fork surprise indique que ces vulnérabilités, si elles n'avaient pas été contrôlées, auraient pu être très dommageables pour Ethereum.

Heureusement, grâce au regard aiguisé des chasseurs de primes aux bugs et au travail assidu des développeurs d'Ethereum, aucune perte n’est à déplorer, et, comme l'a écrit Nikita Zhavonronkohov sur Twitter, la correction semble être assez aisée...

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/end2.jpg)

Images tirées du film [12 hommes en colère](https://www.imdb.com/title/tt0050083/)
