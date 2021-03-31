---
title: Harvest Finance - REKT
date: 26 Oct 2020
rekt: 
  amount: 25000000
  audit: Haechi, Peckshield
  date: 26 Oct 2020
tags:
  - harvest finance
  - flash loan
  - hack
excerpt: La faucheuse ne se plie pas à la récolte. Un talentueux farmer a utilisé des flash loans afin de récolter 33,8 millions de dollars dans les pools FARM_USDT et FARM_USDC.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/10/reaper-3.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/10/reaper-3.jpg)

**La faucheuse ne se plie pas à la récolte.**

Un talentueux farmer a utilisé des [flash loans](https://etherscan.io/tx/0x9d093325272701d63fdafb0af2d89c7e23eaf18be1a51c580d9bce89987a2dc1/advanced#internal) afin de récolter 33,8 millions de dollars dans les pools FARM_USDT et FARM_USDC.

En ces périodes troublées, certains se tournent vers les textes sacrés pour être guidés.

Dix plaies ont ruiné les récoltes de l'Égypte ancienne : la première a apporté du sang, la seconde, des grenouilles.

Le baron de Rothschild avait conseillé d’acheter quand le sang coule dans les rues. 

Maintenant que les enivrants jours de l’été de la DeFi sont terminés, le DFI-PERP a une liquidité en gueule de bois, et même les farmers les plus illuminés par la Grâce adoptent des comportements peu chrétiens.

Nous pouvons lire dans dans l’Exode les versets suivants :

> _“Je vais frapper par des grenouilles toute l'étendue de ton pays.(...)Les grenouilles monteront sur toi, sur ton peuple, et sur tous tes serviteurs.”_

Dans notre métaverse cryptographique, le développeur est le serviteur, et comme cela a été prophétisé dans les anciens rouleaux, les développeurs de Harvest Finance ont certainement des grenouilles sur eux.

![](https://lh4.googleusercontent.com/EEKvX8W_B4lZHA9MSaEJA9qThrhZa6rh-AoQOczdOT6lSxVwJ4F9O1tY4uUSdJ0-xuv7VGP9Mo89i63_LF-W-Rqgq28qoytLxTBpggpZeA4pz9ndUb1_jiN7itRThjNxu3MV33PU)

**Analyse de l'arbitrage**

Le fUSDT a chuté de [13.7%](https://twitter.com/jiecut42/status/1320574109005348864?s=20) et le $FARM de [67%](https://www.coingecko.com/en/coins/harvest-finance) en à peine deux heures alors que le hacker a contracté un flash loan de 50 millions d’USDT, avant d’utiliser la pool Y de Curve Finance pour swap les fonds et étirer les prix du stablecoin dans des mesures disproportionnées.  

Analyse détaillée des transactions [ici.](https://ethtx.info/mainnet/0x9d093325272701d63fdafb0af2d89c7e23eaf18be1a51c580d9bce89987a2dc1)

Les actions suivantes se sont déroulées en 7 minutes. Source : [@valentinmihov](https://twitter.com/valentinmihov/status/1320667338321154048?s=20)

1. Swap de 11.4 millions d’USDC en USDT -> Le prix de l’USDT monte

2. Dépôt de 60.6 millions d’USDT dans le Vault

3. Échange de 11.4 millions d’USDT en USDC -> Le prix de l’USDT descend

4. Retrait de 61.1 millions d’USDT du Vault -> profit de 0.5 million

5. [On prend les mêmes et on recommence, et ce 32 fois](https://etherscan.io/address/0xf224ab004461540778a914ea397c589b677e27bb) (sans aucun test préalable)

6. [Conversion en renBTC](https://app.zerion.io/0x3811765a53c3188c24d412daec3f60faad5f119b/history) et sortie en BTC / [ETH](https://etherscan.io/tx/0x5abe6f9b498471042f6c9f68c63fc3d84398b95a3a9e58c621cee09b3c972879) via Tornado Cash

L’assaillant a pu retirer plus d'USDT à l'étape 4 en raison de son changement de prix. Comme le prix de l'USDT était plus bas au moment du retrait, ses parts avaient plus d’USDT dans la pool du Vault.

Environ 4 cycles peuvent entrer dans une limite de 10m de gas, et bien que le bénéfice sur chaque cycle soit inférieur à 1%, ~500k$ par répétition s'additionnent rapidement.

Le mécanisme de calcul du prix pour les dépôts et les retraits de LP a été l’origine de l’exploit, ce qui signifie que cette attaque aurait pu être reportée sur la pool renBTC, la pool FARM_TUSD et la pool FARM_DAI. Mais l’assaillant à décidé de s'arrêter après avoir drainé 25 millions de dollars, soit 17% de ce qui était disponible dans les pools FARM_USDT et FARM_USDC, même s’il aurait pu facilement continuer à drainer la pool tout entière pour un montant total de 400 millions de dollars si telle avait été sa volonté. 

La stratégie FARM_USDT a le code suivant

![](https://lh3.googleusercontent.com/3WZVjYk0XPg_KMkyG8owAtDZUdOPU_PlUaMwHSkl4IYQjAJTeS_yj96Gu0sHTlfukzmqtxdcMUfpVhfmZrAaw05ImW5ceVByqOuEyad2GevtkP0wb_lj_EuqRrI5PB6Su1nCh_vT)

Ce qui indique qu'un certain indice de prix a été calculé.

Cependant, comme ils spécifient "tokenIndex", nous pouvons supposer qu'ils n'utilisent pas seulement get_virtual_price() mais qu’à la place ils font un calcul sous-jacent. 

Source : [Andre Cronje](https://twitter.com/AndreCronjeTech)

![](https://lh4.googleusercontent.com/RI7-hbXD-8H7Oi3O_mnwPND-Ik4LyPffaqYUX4C9AoT182ohHliSF-9YrArkfQem8CZhY95vlmkTQtIe9ttvxuwBPDSkdI55zYstQzIRThZEXpyFJiScbmtP4pwcHkF2qNvSrph6)

La valeur de tolérance de la fonction de vérification de l’arbitrage n’était pas assez élevée, tandis que la valeur de tolérance de slippage par défaut était trop élevée de 3%. 

Source : [PancakeBunnyFin](https://twitter.com/PancakeBunnyFin/status/1320615021588537347)

Le hacker n’a pas été le seul à profiter de ses actions. Les Lps et les développeurs de chez Harvest ont aussi reçu une importante somme d’argent, puisque le hacker a décidé de renvoyer des miettes ($2,478,549.94) de son festin au déployeur Harvest sous la forme d’USDT et d’USDC.

Harvest a depuis déclaré que cela serait retourné à ceux affectés par le hack grâce à un snapshot.

> Pas de hacker. Simplement un juteux arbitrage de 24 millions de dollars (0x53f) sur [@harvest_finance](https://twitter.com/harvest_finance?ref_src=twsrc%5Etfw)
>
> 50 millions d’USDC en flash loan sur [@UniswapProtocol](https://twitter.com/UniswapProtocol?ref_src=twsrc%5Etfw)
> Swap de 11 millions de $ (USDT/USDT) [@CurveFinance](https://twitter.com/CurveFinance?ref_src=twsrc%5Etfw)
> ~61M on fUSDT Vault
> Swap de 11 millions de $ USDT/USDC yUSDT
> Retrait de 61 millions de $ avec un profit de 0.5 millions de $
> Répétition & blanchiment sur [@TornadoCash](https://twitter.com/TornadoCash?ref_src=twsrc%5Etfw) [t.co/nFTuyU3s6w](https://t.co/nFTuyU3s6w) [pic.twitter.com/2oXQ2PsY32](https://t.co/2oXQ2PsY32) > &mdash; Julien Bouteloup (@bneiluj) [26 octobre 2020](https://twitter.com/bneiluj/status/1320686478486347778?ref_src=twsrc%5Etfw)

**Un bénéfice chanceux pour les fournisseurs de liquidité.**

Les chiffres approximatifs sont les suivants. Source : [Jiecut42](https://twitter.com/jiecut42)

Hacker - 24,000,000 $

LPs de chez Uniswap  - 6,000,000 $

Développeur de chez Harvest  - 2,500,000 $

LPs de chez Curve  - 1,000,000 $

Gas d’Ethereum - 100,000 $

Frais RenVM - 20,000 $

![](https://lh6.googleusercontent.com/O91Z60MeY81zTI2Lu6g3OAAxdJec9tJjcWcY6rbgRPZYW-i8tShq44_XVuhbx2oUao-CsKSqzhPYyHHZRSbvuMrIUwGeOd2npe4Z7KXOox7S_NKK95IEx6ooqh_5MlN8qgtizZu0)

Source : [BitcoinWhiskers](https://twitter.com/BitcoinWhiskers) pour ce délicieux camembert.

Avec l’exposition à toutes les pools de [Curve](https://www.curve.fi/) les détenteurs de CRV ont profité du volume supplémentaire passant par Curve, le hacker générant ~500k $ de frais de trading qui seront redistribués à tous ceux qui stackent leur CRV. Les frais de trading de Curve ont augmenté de 8,000% par rapport à la veille du jour où le hacker a [swappé](https://etherscan.io/tx/0xb460b70f11a93364fecf1f3c3ec49f053aecd2d6d9912c012170aa7a0de2d526) pour plus de 100 millions de $ en USDT et USDC.

![](https://lh4.googleusercontent.com/P9kpiXDdXJYtJTO1byo7ylD8Ht4_vJNDbSZZtUcG2MzXflb5VxaW634Su-jKF3W9yNKAeJ49BKnQjiaPBYy3w018NmCpTXJ2bcK9kjniEy6E2hENqHwYk2yJebULie9UzMaFm55m)

![](https://lh4.googleusercontent.com/Az3qJ6dKLbNiXRkUOshi9tgw5Qg0WcRbxF2KhGoxT4GJQ4dOdLT_CpGK6fFkwHHsrnfN0mhcTIZaBdRq-QYWqH7_bCWft16ow-zNO7R0i6YGTBdQGjysjheUKSbZjCJ8V0cyOSws)

Les LPs d’Uniswap ont également connu une bonne journée à la ferme grâce aux actions de ce superfarmer.

Le volume total des échanges avec Uniswap est passé de 148 millions de dollars à 1 milliard de dollars en 24 heures.

92% de ce volume provenait des paires USDT/ETH et USDC/ETH, générant 5,76 millions de dollars de frais pour les fournisseurs de liquidité.

![](https://lh3.googleusercontent.com/fZW3t_eeYeEjsBaluQwSbmHCc2ZP7H5PNBeFUvw0uSxxJqwNs4mL6UvIKWTWGHZ_7rLGpMuveEAzJ_GVLNJbEZOfRi9S8zYV7BWyknpQCgctrsomzLm4Dzbi6qNwuzbzG8gOFGeI)![](https://lh3.googleusercontent.com/T9IWn6M9JIV_82qkS-t6SC9iSOK6r1TNWO6aBCRerRNaxKXZso62bpGa5vypvVvQaUEfgIcLRkZ5QLoBU3ibErYg4cUDmb7p6CpGjR1NFVQHdtEzXy483uACgcJ-_RQMFfelFO-s)

Source : [Larry Cermak](https://twitter.com/lawmaster/status/1320614508772163584?s=20)

**Contributeur confidentiel**

Deux de nos missions principales, ici à Rekt, sont de lancer des alertes et de protéger nos contributeurs. 

Pendant que votre auteur rédigeait ce compte-rendu, quelqu'un nous a contacté avec des informations concernant les actions de Harvest Finance quelques jours avant les événements de la nuit dernière.

Les informations suivantes sont présentées sans commentaire.

> _J'ai été contacté par l'équipe de Harvest Finance qui cherchait une collaboration pour la promotion des pools de liquidité pour deux classes d'actifs._

> _La première était trustless BTC, la seconde était FARM/ETH._

![](https://lh5.googleusercontent.com/BI91M7nD8yCLZuJtX0Tpas4RCBD8xnGWl2LrRu4PTbO_CrQUDP2GDuhR45vrUpnOSc-hxuvuKTZ76DT8U58QVgvFxa7CNkQL2KXINn1Hsxw7csVd2b3VYOp8Mhw9_tM-fD58ZFOp)

> _J’ai décidé de ne pas donner suite car quelque chose clochait._

> _Je ne dis pas que c’est l’équipe d’Harvest, mais voir les 3% de slippage dans le smart contract, et le fait que l’exploit soit sur le trustless BTC, qui est une “nouveauté”..._

> _Je pense que si ce n’est pas Julien, alors ce doit être Harvest Finance eux-mêmes, ou le hacker EMN, ou quelqu'un avec une connaissance approfondie des flash loans._ 

**Demandes de remboursement**

Comme d'habitude, un débat s'est ouvert sur la possibilité pour les protocoles de bloquer ou de modifier ce type d'activité à l'avenir. Dans le groupe Telegram de Curve, certains étaient d'avis que Curve devrait pouvoir bloquer ce type d'activité, même si les smart contracts existant [ne peuvent eux être stoppés](https://twitter.com/CurveFinance/status/1320694100090376193?s=20) ou modifié.

Des appels ont également été lancés pour que RenBTC rembourse les frais gagnés grâce à l'activité des hackers. C'est un sujet controversé qui oblige les utilisateurs à peser le pour et le contre de l'utilisation de protocoles décentralisés.

**Des négligences en matière de sécurité**

Il y a seulement 3 semaines de cela, le 6 octobre, Harvest Finance a publié une [mise à jour de sécurité](https://medium.com/harvest-finance/week-6-update-security-rules-everything-around-me-62a681a3692a) statuant qu’ils assuraient la sécurité de leur territoire via “de rigoureux audits de sécurité” de [Peckshield](https://twitter.com/peckshield), [Haechi Labs](https://haechi.io/), et [CertiK](https://twitter.com/certik_io).

Il convient de noter que Peck Shield et CertiK ont également audité Bzx plus tôt cette année, juste avant leurs trois hacks.

Nous attendons leurs commentaires concernant cette affaire.

Les développeurs et apparemment même les sociétés de sécurité spécialisées ne sont pas habitués à devoir prendre en compte l'impact des flash loans sur leur code.

Maîtriser les flash loans revient à participer à un tournoi de joute du XIIe siècle sur une Harley Davidson avec deux AK47. Personne ne s'y attend, la plèbe se fait rekt, et il faudra des années avant que les masses non éduquées puissent se protéger contre ces ces experts du trading sauvage.

Harvest Finance a réagi à ces événements avec un ton agréablement passif-agressif.

![](https://lh6.googleusercontent.com/R_kCRELgxVg20qoViEkHb43yiEoWnuslyOQJaPlG0djFHM8FAJEumBYLQP-URiPun5EdcOpKhBOLGHmsi0h36Z6-LdRxFKwD9ABzrFezDcLcNLXtEPBc896I1HcwxfLHCuz5R9IF)

[twitter.com/harvest_finance/status/1320624369543057409](https://twitter.com/harvest_finance/status/1320624369543057409)

![](https://lh4.googleusercontent.com/kgpAOlAQRPTcNrx-HJzhDhO04Y9CttjxSfNJ3udyDNvVG5D75NbarZjK3aQ_76axChzA05kmDzDOlSyC9mFX98Odw1U5fSucvIw6zo7JOdjBjANdqm7WN-pac8GzxozyBjZQ6qWK)

**Une technologie sincère**

Arbitrage / Exploit / Hack.

Les différences de terminologie deviennent de plus en plus floues, tandis que l’adage “le code fait loi” devient lui parfaitement limpide.

Le terme choisi par Harvest Finance a été “attaque économique d'arbitrage”. Certains considèrent cette activité comme un crime, tandis que d'autres y voient simplement les actions d'un utilisateur plus compétent, du yield farming avec des machines modernes.

Cela relève-t-il de la méritocratie ou de l’anarcho-capitalisme ?

Cela demeure passionnant dans tous les cas.

_Caveat emptor._

Il n’y a que le fermier qui plante minutieusement ses graines au printemps qui peut avoir une récolte en automne. _[B.C. Forbes](https://fr.wikipedia.org/wiki/Bertie_Charles_Forbes)_
