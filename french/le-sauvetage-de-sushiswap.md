---
title: Le sauvetage de SushiSwap - 0XMAKI se livre
date: 29 Nov 2020
tags:
  - sushiswap
  - 0xmaki
excerpt: Directement dans le feu sans passer par le wok - Le développeur anonyme 0xMaki a pris le rôle de développeur principal de SushiSwap après que son fondateur, Chef Nomi, ait sombré dans la cupidité.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/header-6.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/header-6.jpg)

**Directement dans le feu sans passer par le wok.**

Le développeur anonyme [0xMaki](https://twitter.com/0xMaki) a pris le rôle de développeur principal de SushiSwap après que son fondateur, Chef Nomi, ait sombré dans [la cupidité](https://twitter.com/NomiChef/status/1304442495342796800).

Après la fin de l’été de la DeFi et la chute du farming de tokenfood, beaucoup ont cru que SushiSwap était mort et enterré. Mais les développeurs n’ont [jamais](https://twitter.com/zhusu/status/1329932138171404290?s=20) cessé de construire et SushiSwap est revenu avec un nouveau menu. 

**いらっしゃいませ!!!**

Mais tout n’a pas été facile dans le bar Omakase.

**Tard au cours de la nuit dernière, un acteur anonyme a fait une brèche dans le smart contract et volé pour ~15,000 $ avant que l’équipe des chefs Sushi ne le chasse de la cuisine.**

Rekt a contacté 0xMaki pour entendre sa version de l'histoire.

![](https://lh5.googleusercontent.com/bLAbz--dDRJoIQjlauDxi08j9x-pObms6J3_LmI2hhMGNs5kCYYxs-Dz13TsdF6IRgQ36NlQ-CiJpWUCZ9IVZaYGMju15bhw3vwVmG6WzAigF_sPkGojiOPjj6Ve3vdCiUJEOBZN)

**0xMaki:**

Depuis le rapport de [Nansen](https://research.nansen.ai/sushiswap-farming/), je sers moi-même au Sushibar afin d’atténuer les risques d’arbitrage. J’ai vu quelques transactions bizarres, mais je trouvais que cela restait correct dans l’ensemble puisque le bar fonctionnait toujours correctement. 

La première micro transaction a eu lieu il y a peut-être 2-3 jours mais ce n’est devenu automatique qu’hier, à un “niveau industriel” pour ainsi dire.

Voici la première [remontée](https://discord.com/channels/748031363935895552/753626532500734014/782428289868365884) d’un problème avec le Sushibar ([Discord](https://discord.com/channels/748031363935895552/753626532500734014/782428289868365884)).

**Monstar**

@0xMaki 源 義経 qu’est ce qu’il se passe avec le sushibar ? Il y a plein de transactions bizarres et il semble que les gens qui stackent au bar n’en tirent aucun sushi ?

[TX 1 ](https://etherscan.io/tx/0x3534241a7354a8f9c8a9d0209730167a888d923b08c19c20623cd78637faadd0)

[TX 2](https://etherscan.io/tx/0x3ffcfc9985622ad7cf0fdc2eb582ad7ce8bf9e9295fd7a4de44354fdd71a688a)

[TX 3](https://etherscan.io/tx/0xc75a8ca881d4da75774f51006651c9946311d40145ce69d07aee3a85627153d6)

**0xMaki 源 義経** répond à Monstar

Cela fonctionne comme ça devrait, ça concerne vraiment une très très très très petite somme de ce que je comprends.

Ça ressemble à une transaction perdue, je vais regarder ça

**Monstar**

Je pense qu’il y a un problème

Parce que le montant dans le bar disponible à claim a drastiquement chuté depuis ces transactions. 

Ils semblent qu’ils sont en train de claim les LP tokens pour eux-mêmes (je sais pas comment c’est possible) au lieu de claim de la bonne façon.

Donc ça ne se convertit pas en sushi et ça ne récompense pas les stakers.

**0xMaki 源 義経 :**

Je suis en train de regarder ça avec quelqu’un en ce moment

C’est peut-être juste la boring app qui agit bizarrement

**Monstar :**

Je pense que les gens ont trouvé un moyen de contourner la boring app (modifié)

et de ne pas partager les sushi avec tout le monde dans le bar

mais je ne sais pas comment reproduire ce qu'ils font donc je ne peux pas le tester

ouais, c’est sûr que c’est ce qu’ils font

[https://etherscan.io/tx/0x7c6af5ca27ceb04aad514ddcaee8afc6dd4eb79d0816e24b007e7db205e93ce3](https://etherscan.io/tx/0x7c6af5ca27ceb04aad514ddcaee8afc6dd4eb79d0816e24b007e7db205e93ce3)

[https://etherscan.io/address/0x1925e832c22522e0d9947ee4677120b2f28e4cd4#internaltx](https://etherscan.io/address/0x1925e832c22522e0d9947ee4677120b2f28e4cd4#internaltx) 

tu peux voir tous les claims depuis ce portefeuille ici (modifié)

**0xMaki 源 義経**

@Monstar nous sommes en train de travailler à la résolution du problème actuellement et aucun fonds n’est en danger, c’est juste un exploit du sushibar pour les frais, c’est chiant mais c’est une prime aux bugs.

Nous allons renoncer à environ 10k pour les gens du Sushibar

---

**rekt** : 

*Merci pour le lien. Quelles ont été tes premières réactions ?*

**0xMaki** : 

Je me suis d’abord dit : c’est impossible que le bar rencontre un problème non ? Ça doit venir de l’interface utilisateur… La transaction n’avait aucun sens. Mais il se trouve que le bar ne rapportait plus d’argent et qu’il aurait dû en contenir beaucoup plus.

Environ 15 minutes plus tard, je me rends compte que ça ne va pas, et je contacte donc immédiatement [Banteg](https://twitter.com/bantg)

![](https://lh5.googleusercontent.com/2nOrhx84dL0WXXOLQy-RuEuZQo05qVC2rS7DtAYxQ207NRzWglhhEUhIO6dsES1F9ls81HYZINxkn5f2idaSXxlcgKuDDUVTe160boHCzME0RqL8Ci6R-gdZlcXTYl2Aj4jJStv5)

![](https://lh5.googleusercontent.com/e9ULQE7bDt7_iZJyvYGz3oph9OzHxyilopiD0JmhhOv09ZfsJxtFS9ubho8a4eof3YflICXhptgZsU4ZhApjNGyYtpkEscsW7s8SOoG1pn120KB57RyRvZLu5yumbm9jz0hVPcPg)

Banteg ne pouvait pas donner de coup de main, il était 6 heures du matin pour lui et il avait travaillé toute la journée sur le truc de Pickle. Tous les devs de Sushi étaient en train de dormir - Fuseaux horaires Europe / Tokyo, je suis le seul basé en Amérique du Nord.

**rekt** : 

*Qui t’a aidé ?*

**0xMaki :** 

J'ai reçu de l'aide d'[Andy ](https://twitter.com/andy8052) stratège chez yEarn / ex-makerdao smart contract engineer et de [Daniel Que](https://twitter.com/danielque), un ancien de chez Coinbase

**rekt :**

*Combien de temps cela a-t-il pris pour résoudre le problème ?*

**0xmaki :**

Je dirais 3 à 4 heures pour reproduire et trouver le problème.

**rekt :**

*A combien s'élèvent les pertes ?*

**0xmaki :**

Il n’y a eu que 15k de perdus car le sushibar n’augmente que de 20-30k par jour. 0.05% vont dans les pools, et tout doit être fait manuellement, avec le risque que la transaction échoue.

**rekt :**

*Hack ou exploit ?*

**0xMaki :**

C’est clairement un exploit, et un intelligent - il mérite de toucher les fonds. Je pense d'ailleurs que  j’ai fini par le retrouver…

**rekt :**

*Es-tu plutôt impressionné ou gêné ?*

**0xMaki :**

Je suis réellement impressionné ! Il n’y a pas de raison d’être gêné. C’est fascinant de voir tous ces hacks / exploits arriver, même avec les audits les plus solides il y a toujours une sorte de nouveau scénario que nous n'avions prévu ou auquel on aurait même pas pensé qui émerge. 

Cela rend l’écosystème plus solide et plus résilient.

Nous n’avons perdu que 15k à cause de cet assaillant, peut-être y a-t-il eu d’autres personnes à faire ça, il faudra que je m’y penche - nous avons débusqué celui-là car il a commencé à affecter tout le bar.

Bref, il était environ 23h28 chez moi quand nous (0xMaki et Andy) avons commencé à résoudre le problème. 

![](https://lh6.googleusercontent.com/AfYQkR2nEmDTLYAIcqA0n-6GtaGpsDSSDB6Y-NykyBE2znVpyhpTcqNTSt_Wx-8B2V1OSScQyW8Ekxvgr8NiK-pABsM26u4aGxzIckiwstGUMhB_0MqLAOxGJjxSfQRm0MMXUR1v)

Ensuite, nous avons inspecté les petites transactions, juste pour vérifier qu'elles étaient anodines, et là - merde - il s'avère qu'elles ne l’étaient pas.

Andy venait de rentrer d'un vol, il subissait le décalage horaire et ne pouvait pas rester debout, il a dû aller dormir, je me suis retrouvé seul, jusqu’à ce que…

![](https://lh5.googleusercontent.com/AoC4V0gDiIzCSg0MedJONypm9V7KpfN4kQZc3qmeRvGN2CyaHsOGQv_0fEosKO6766h3M_VynadJdaKHAnj7aUg7_Po7BCzDCLOjzKfCXlC_1AbQKjuG-57IN4TvEhqyDppvaIDj)

[(samczsun)](https://twitter.com/samczsun)

**rekt :**

*Comment a-t-il été mis au courant ?*

**0xMaki:**

Je l’ai contacté puisque je me suis retrouvé tout seul sans aucun .sol jedi.

**rekt :**

*.sol-diers*

![](https://lh6.googleusercontent.com/XmqXGATsYH7SArH7jLF82J1KLSczUODpWDI6AfY4yXUSJYrPQNoAt-TE8sueyr97jK83hDBrAK4lYtm0XfZvxGRhbPM3jNbpLuCHd4eHO4e1lSuTkrYE0KpiA384Y4et4IYy8Kw4)
![](https://lh4.googleusercontent.com/AVz2977b1kJ93j9w8YlTFnQ728CBJhIKkie-4Gn-MDdqIErJbSXCYr-qLbTpxiCT70IPzzmQy6aBZ7jtrO0V4ZQsXY1FSoCawBsVPv3uwkAxYzoA3Lrsd7qRFd5-ikwliik1l0rQ)
![](https://lh4.googleusercontent.com/CzyFAdpwpd5iAHD-S5EHgPAnlPl_B_IhbS8rNOsE5T5g-X_HLimDvQi6hIm8sQu_GCBTog_KKRxDwj1gXafHuywBpCdHFmthdL-GylfH0h6gkX-Ep91ucovdYvan78k_cdzHzPJg)
![](https://lh4.googleusercontent.com/Cv4Ty0uF7kAY9EMIETzT26Eabe2jnfyQtFGsoA6qRJSrG1Lk7GIQlIKlLtngeneyL-kz5Q7m1S5dft6pooiYQ7r9jQMzHQsnTSjXgpjx1kVT4VOy6cHJ650KAwL_ErFcKCJbJltE)

**0xMaki:** 

Mais malheureusement... il était tard et il avait des trucs de prévu comme toute personne normale un samedi soir j’imagine ?!

Retour à la case départ, et personne pour m’aider…

J’ai essayé de contacter Chef Nomi et tous les core devs, en laissant un guide étape par étape dans le groupe de l’équipe principale dans l’espoir que quelqu’un se réveille

Puis je me suis souvenu de [Daniel](https://twitter.com/danielque), quelqu’un avait qui on était en contact depuis le début, je l’ai contacté, appelé et briefé

![](https://lh5.googleusercontent.com/j49oC75qzLg9IBSO0zD5190VA4aZK2jETW8GG4S1XHZPEAKRKuu1Ney6hjysi_J3rn2DLUZ9WJDUFGgaR8ug8bIFNgdIGWqJ7tzgFHKkAURTBsmFKnHHp9Aj62Uh5Cy_UHpvl0dm)

**rekt:** 

_Tu parles toujours à Nomi ?_

**0xMaki:** 

Non.

![](https://lh5.googleusercontent.com/KxNo_yX9tboZIjfc6xvqsUs_Z13C9OSb28xmCCuF_1UFKbhDNs_el1Nd7nFflSzBGefGiA5r3w7deozbKxFk-SfGPTxDg-DzXWVFyUP3EzkHdRLjFFvtcu7hqMSq8KEgMsYh-zgo)

**0xMaki :**

02h35 et nous avions enfin une reproduction ! Nous avions compris comment l'exploit fonctionnait et avons pu le reproduire, afin de travailler sur un correctif.

À 03h19 nous avions la correction

![](https://lh6.googleusercontent.com/KmbawxTOw3xF7yC0w63X6K_XzBY85q5G4c4LAuWLqWEnq64DZcNbbUxnAHVY6iKnNUZdle8IgJrm1yf2E5VqA9skhtkLDFWwkex7tVZxfDb2TYI3sE_ML3AAoF4PJV0NTHNcNmhW)

**0xMaki:**

Les choses allaient mieux, l’équipe était en train de se réveiller et on travaillait sur un correctif. Pendant ce temps-là je suis allé voir celui qui avait fait l’exploit, et j’ai vu que c’était principalement un détenteur de SNX et de ETH.

J’ai regardé un peu ses transactions - ça n’était pas à un compte créé pour le hack, on avait affaire à quelqu’un qui fouinait à droite à gauche et a trouvé un exploit.

**rekt :**

_Qu’est-ce qui te fait dire ça ?_

**0xMaki:** 

Les pourboires. Il a reçu des pourboires en SNX et ESD, c'est donc quelqu'un qui traîne dans les deux communautés, probablement via Discord.

J’ai croisé des sources et listé qui envoyait et qui recevait des pourboires sur plusieurs dates, et bingo…

![](https://lh4.googleusercontent.com/v8i6j6fMZvLnlXWy2qTbgcKVCTOoVmuNzCrBFKGpa3UJ_VGt_wW59AO2pIepBC7DObq-eKnV_aX7xX2P5iOL-z6-U4ArJd_hWbCL0N6IeQDrY4qlzRyNdEA0nX5f4MOD0jJ91k7x)

Un initié de la communauté SNX m'a aidé à identifier les destinataires des pourboires.

![](https://lh5.googleusercontent.com/HEooziQ-CV7OH0y1_D-Fo9uhj8kEYEE2kqmQkge3MDEB-avcdoOOQFvaPnxhkLeG3Ld41GDuZ4t5yS8EiuaieOuIBn2m0mDfFEIzjB1XLGqrzrBRorAosQo_xDC63AXm3p_K2tWI)

On en était donc là, toute l'équipe était réveillée, nous avions une [correction préliminaire](https://etherscan.io/address/0x280ac711bb99de7c73fb70fb6de29846d5e4207f) et l'attaque avait été arrêtée. C’est à ce moment que la nouvelle est arrivée sur [Twitter](https://twitter.com/Juan_Snow1/status/1332992258115657730?s=20).

**Note de l’éditeur** Nous avons depuis reçu cette irréfutable preuve d'innocence de la part du suspect :

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/image-1.png)

"c’est impossible que ça soit moi"

**0xMaki:**

Personne n'a perdu de fonds puisque l'argent était des purs profits destinés aux détenteurs de xSushi. Nous enverrons de notre trésorerie une valeur de 15k en Sushi divisé au prorata.

**Rekt :**

_Rien de grave donc, un repas léger ! Un message de fin pour le suspect ?_

**0xMaki:** 

Contacte moi ! Nous avons d'autres smart contracts dont il faut que tu trouves des brèches : nous offrons des récompenses ! 
Je voudrais également [remercier](https://twitter.com/0xMaki/status/1332993111950319618?s=20) toutes les personnes impliquées dans l’histoire, _y compris_ l’assaillant.
