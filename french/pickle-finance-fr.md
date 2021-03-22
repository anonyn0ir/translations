---
title: Pickle Finance - REKT
slug: pickle-finance-rekt
date: 22 Nov 2020
rekt: 
  amount: 19700000
  audit: MixBytes, Haechi
  date: 22 Nov 2020
tags:
  - pickle finance
  - Rekt
excerpt: La fermentation de la finance se poursuit. Même les cornichons ont une durée de conservation. Pickle Finance est devenue la dernière victime de l’épidémie de hack en cours. Cependant, cette-fois, quelque chose semble différent…
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/rr.jpeg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/rr.jpeg)

**La fermentation de la finance se poursuit. Même les cornichons ont une durée de conservation.**

Le jar [cDAI](https://github.com/pickle-finance/contracts#pickle-jars-pjars) de Pickle Finance s’est fait [hacker](https://bloxy.info/tx/0xe72d4e7ba9b5af0cf2a8cfb1e30fd9f388df0ab3da79790be842bfbed11087b0) pour 19,7 millions de DAI via une vulnérabilité impliquant de faux «Pickle Jars».

Pickle Finance est devenue la dernière victime de [l’épidémie de hack en cours](/hack-epidemic/).

**Cependant, cette-fois, quelque chose semble différent…**

Alors que Twitter tentait de tabler sur une nouvelle fatalité financière, Rekt a commencé à enquêter.

Nous avons contacté l'équipe de Stake Capital, qui a examiné le code et nous a avertis que d'autres Jars pourraient être à risque.

Nous avons ensuite rapidement contacté l’équipe de Pickle Finance et instauré une cellule de crise entre des membres de Stake Capital ([@bneiluj](https://twitter.com/bneiluj), [@vasa_develop](https://twitter.com/vasa_develop)) de Yearn ([@bantg](https://twitter.com/bantg)), de [Pickle Finance](https://twitter.com/picklefinance) et de développeurs aguerris ([@samczsun](https://twitter.com/samczsun), [@emilianobonassi](https://twitter.com/emilianobonassi)).

Au fur et à mesure que nous étudiions le dossier, il devenait évident que nous faisions face à quelque chose de très différent des récents hacks de style Lego de la DeFi de ces dernières semaines.

**Ceci n’était pas un arbitrage.**

L’attaquant avait une excellente connaissance de Solidity et de EVM, et avait sûrement porté une attention particulière au code de Yearn pendant un bon moment, car la vulnérabilité était similaire à celle qui avait été [découvert](https://github.com/iearn-finance/yearn-security/blob/master/disclosures/2020-10-10.md) dans ce code un mois auparavant.

Les Jars de Pickle sont en grande partie un fork des yVaults de Yearn. Ces Jars sont contrôlés par un contrat appelé le Controller, qui a une fonction permettant aux utilisateurs de swaps leur actifs entre les différents Jars.

Malheureusement, il n’y a pas de whitelist définissant quel Jar est autorisé à utiliser cette fonction de swap.

Le hacker a créé un faux Jar et a swappé des fonds issus du Jar originel. Cela a été possible car le [swapExactJarForJar](https://twitter.com/emilianobonassi/status/1330239233538318339?s=20) n’a pas vérifié quel Jar était whitelisté.

L'équipe de Pickle Finance savait qu'elle avait besoin d'aide et était plus que disposée à travailler avec d’autres personnes pour éviter tout dégât supplémentaire.

Pickle a essayé de call “withdrawALL”, mais la transaction a [échoué](https://etherscan.io/tx/0xb108205dc90466104f10d3e465593825ea88420cd8db6df29afd57e62df5cba6).

La demande de retrait devait passer par la Gouvernance du DAO qui avait un timelock de 12 heures.

Seul un membre du multisig de Pickle avait la possibilité d’outrepasser ce timelock, et il dormait. 

Cela signifiait donc que les admins ne pouvaient pas vider les Pickle Jars, mais cela ne les protégeait pas non plus d’un nouveau hack.

[Pickle Finance](https://twitter.com/picklefinance/status/1330256787002564610?s=20) et [Curve](https://twitter.com/bneiluj/status/1330255575339438088?s=20) ont envoyé des avertissements pour prévenir les utilisateurs de retirer leurs fonds immédiatement, mais 50 millions de dollars restaient potentiellement vulnérables dans les Pickles Jars, tandis que les hackers éthiques enquêtaient sur l’exploit et s'assuraient de la sécurité des fonds restants. 

L’équipe de sauvetage devait soit réveiller l’admin endormi, soit drainer les Jars eux-mêmes.

![](https://lh5.googleusercontent.com/iBloOUNiyzcS6t7vuiT8Ric31fzGktin3XSZ53MAGk0eJiylu53vsQJ_BdPOHba_7yH81037JWZX_H48bzbwH5AoNMn3jFz8Q_YplF9Xk8sm47IHRK07RnTIB8I8Ebeba4vJCCJp)

**L’équipe a dû surmonter cinq épreuves :**

1. Réunir l’équipe de Pickle Finance, répartie à travers différents fuseaux horaires, pour commencer l'opération de sauvetage des fonds en pushant les transactions dans le timelock de 12h (via 3 des 6 multisigs) pour retirer les fonds.

2. Amener des milliers d’investisseurs à retirer leurs fonds (et les décourager de redéposer dans la pool une fois que la TVL, qui chute, entraîne l'APY à connaître une inflation de plus de 1000%)

3. Réaliser des contrôles de sécurité sur les autres jars pour voir s’il y a des possibilités d’attaques

4. Dupliquer l’attaque de manière préventive avant que quelqu’un ne réattaque les Jars

5. Éviter de se faire front-run en essayant de sauver les 50k restants.

**Combien de temps pouvons-nous continuer à nous en remettre à l’aide de hackers pseudo éthiques anonymes ?**

Les attaquants ont bien plus à gagner que les défenseurs ; pourquoi coordonneraient-ils une contre-attaque aussi éprouvante ?

Certes, la gloire revient aux hackers éthiques, mais l’argent va aux hackers malveillants. **Ce n’est pas tenable sur le long-terme**.

Combien de temps avant que même les hackers les plus éthiques ne succombent à la tentation ?

**Analyse**

En publiant ces informations techniques, nous sommes conscients que nous pourrions déclencher de nouveaux hacks. Nous avons discuté des conséquences potentielles avec Pickle Finance et d'autres développeurs, et il a été établi qu’il n’y a à notre connaissance aucun fork opérationnel de Pickle qui pourrait être affecté par des attaques de type copycat.

La communication sélective introduirait un aspect de responsabilité, nous avons donc opté pour une publication libre. Si un protocole exécute actuellement un fork du code de Pickle, l’équipe devrait déjà être au courant du déroulement des évènements, et avoir pris ses précautions contre des actions de type hack par copycat.

Le graphique suivant a été créé par [@vasa_develop](https://twitter.com/vasa_develop).

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/Pickle-Exploit-Overview.png)

Le fichier d’origine peut être trouvé [ici](https://lucid.app/lucidspark/invitations/accept/8f291e25-bf50-4a77-913d-31ddfb62754b).

**Pour plus de détails, consulter le post-mortem complet des équipes [ici](https://github.com/banteg/evil-jar/blob/master/readme.md)**.

Il sera intéressant de voir comment la relativement jeune assurance “[Cover Protocol](https://twitter.com/CoverProtocol/status/1330238732558098437?s=20)” gère cet incident vu que c’est un montant important pour leur premier claim. Le vote via snapshot pour le claim de l’assurance peut être trouvé [ici](https://snapshot.page/#/cover/proposal/QmPSkV68ihhP8EAZbNoQVsTpUh82wiX18ckyEwiUbChRjQ).

![](https://lh5.googleusercontent.com/HcyTLZyj6aAciaM5wFLPJl04zSx8n_iqwYnnetTg_ATBVappkijm1K2TtSjkbAAwsDNFcJCaiz1uibep5WAC4-56uyMRDn8p5jk-iLHk53qklgC1Jc_4JiOZrLkr3jZ-ictipp2N)

**Faire arriver un produit à maturation prend du temps.**

Pendant des décennies, les évangélistes du développement rapide ont pressé les développeurs, poussant à l’échec rapide et à sortir le produit dès qu'il devenait un minimum viable. Ces idées ne fonctionnent pas lorsqu'il s'agit de construire dans un environnement si hostile.

**Échouer rapidement dans la DeFi coûte cher.**

Nous n’avons pas simplement besoin d’une nouvelle méthodologie. Nous avons besoin d’un changement de paradigme permettant de créer rapidement des itérations sans risque de se faire rekt en même temps.

Débarrassons-nous de l'idée selon laquelle l’idée qu’un audit est une garantie de sécurité. Il s’agit plutôt - la plupart du temps - d’un snapshot dans le style d’une checklist de mesures de sécurité appliquée à des cibles mobiles qui évoluent souvent en quelque chose de radicalement différent, et généralement peu de temps après que le projet est arrivé sur le mainnet. 

Les audits de MixBytes (3 octobre) et de Haechi (20 octobre) ont été réalisés avant l'ajout du ControllerV4 (23 octobre), qui était l'un des principaux vecteurs d'attaque.

**Les meilleures équipes dans l'avenir de la finance seront celles capables de gérer le compromis entre la nécessité de sortir rapidement un produit et celle de le sortir en toute sécurité**, faisant constamment auditer et tester rigoureusement leur robots de monnaies composables.

Les audits doivent être un processus régulier et continu, mais pas une simple case à cocher avant le lancement.

**Les cornichons ne restent frais que s'ils restent dans leur bocal...**

![](https://lh6.googleusercontent.com/Bx_HYNlFKOcaH6XtCcUCcE5TlykgAkp3vka10Tq1KkOV_bK4YxOtjJTcUt73XhYoauO3_I9SQeu55sTKkjAj0brsKfis-lPGuRpPth03tGxuxEF46oU5lJm_mgvkIL1ro_AYZh6F)photo @[martinkrung ](https://twitter.com/martinkrung)
