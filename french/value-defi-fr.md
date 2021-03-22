---
title: Value DeFi - REKT
date: 14 Nov 2020
rekt: 
  amount: 7000000
  audit: Peckshield
  date: 14 Nov 2020
tags:
  - value defi
  - rekt
  - flash loan
excerpt: S’y connaissaient-ils réellement en flash loans ? La valeur d'une réputation est volatile. L'humilité confère de la stabilité : si vous vous mettez trop en avant, vous êtes sur de vous faire rekt à un moment ou à un autre. Value DeFi a été exploité hier pour un montant avoisinant les 7,000,000 de dollars. Une nouvelle rude leçon de la famille des flash loans.

banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/jumpoutwindow-7.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/jumpoutwindow-7.jpg)

**S’y connaissaient-ils réellement en flash loans ?**

La valeur d'une réputation est volatile. L'humilité confère de la stabilité : si vous vous mettez trop en avant, vous êtes sur de vous faire rekt à un moment ou à un autre.

Value DeFi a été exploité hier pour un montant avoisinant les 7,000,000 de dollars. Une nouvelle rude leçon de la famille des flash loans.

**Prix avant le hack - 2.73 $**

**Prix après le hack - 1.87 $**

**Publier ce tweet un jour avant le hack ?**

![](https://lh4.googleusercontent.com/odnNjSzV6LwKmdxXPY63HQ4SPBnxjtGstMRf3v4URKQwAqb1y_16m7O4_QRYXQq3dH5wlZiubb2ZzXrmWr0irFKbud0DFgKWAxP0OIKSHPImB_XrOFsE2n3Kwnc-xjcH08CajSd7)

**_Ça n'a pas de prix._**

_(Ce tweet a été depuis supprimé, mais notre screenshot est toujours là.)_

Malgré leurs affirmations audacieuses en matière de sécurité, il semble que l'équipe de Value DeFi ne savait pas que les retraits pouvaient être effectués non seulement via le bank contract, mais également à partir du Vault contract via Proxy.

Value DeFi a utilisé le prix spot de Curve comme oracle.

![](https://lh5.googleusercontent.com/8LivNANeDVuLd7utYUylaCzk-gG0oe_bUBZh3_XIOeilHQ-xPIpSjQ3yjQwOwhDEQUDgHT7H4C_2-0W6fT6H39XJTw2rrCv1jMqp_aj6QhTZC4DrrIGQPKeIfEH4SvPgoBLdODU1)

La manipulation a eu lieu aux étapes 5 et 6.

Le retrait à l'étape 7 utilise la mauvaise fonction de Curve pour faire le calcul.

Source : [@emilianobonassi](https://twitter.com/emilianobonassi)

![](https://lh6.googleusercontent.com/sCMxoK0s_EMlbZfZUYx-BVe9Wuq5iXDAXptoHOAsp2SXYhOgA1ZFJ7VXf83WXrRhyY38Xlf1-qXTUqMU5RMQy0u1Lw0TBNs9zV7IfwT6LJCnRrwJ4EqNvnKv3s7TcUIkWhKGQLrH)

Source : [@FrankResearcher](https://twitter.com/FrankResearcher/status/1327649421492957184?s=20)

15h24 : L'exploit est arrivé à un moment particulièrement peu propice pour Value DeFi, à peine 20 minutes avant le lancement d'une AMA.

![](https://lh6.googleusercontent.com/AOmdisLDuND1OnUWiBCw9dNc_SsCuSRGqZcbhapOyv05JX8Nk3zwMaVB9mIQROSOvXywGoc18QOGkie-y8Sq8WMeNzt0DRDJ3N3iWK0I8U8b4yV8VShPpSe-P63Xi4PdeqL4tVCH)

A 15h41, un utilisateur a posé une question sur la chute de la TVL, qui avait dépassé les [11 millions de dollars](https://discordapp.com/channels/738345978750435408/745301208532516875/777212546746286120) plus tôt dans la journée.

![](https://lh6.googleusercontent.com/CHKktTxXvzd1xPwEX3K1twFBsL1v6KSNjCncFX6wpdunbOAPU2mi4votbubCgKmvrCguM-PLWW7PBHe1Ms_Cf7bEjHMIq-V84zGFUqGnp-h3LwZs4lIwQ-AXH-_l6-36ocfAtIPG)

À 15h42, l'inquiétude grandissait et les membres du groupe espéraient un bug de l’UI.

![](https://lh4.googleusercontent.com/piTSCrkU79lUUJidljebpv2PdMwmVC7JFeBN87kakfy-6gY_QFvDsoF_ZJq3EJRSTl4Ah_NuDZXOlsRrrxDeKV4_tKQ2diz6d94wCFzrpGI08h4Uxk7TjopdPK4j-9RgwoPSeTKY)

Puis, à 15h49, le [etherscan link](https://etherscan.io/tx/0x46a03488247425f845e444b9c10b52ba3c14927c687d38287c0faddc7471150a) fut lâché comme une bombe dans le chat.

![](https://lh5.googleusercontent.com/UkZdx33K3bt2fyUrVmBO1IT4YM0d8xbrHCK0YYavvlmcwXf9oxFmBg0-aWyorFb3e1q0nsrGaYVIPGc_0rtyY0cAsbxczJ96iUGQaKYxgTRPDqI5KcOoqt3Tj-gV70cqHQ5ziARN)

7,000,000,000 de dollars avaient été retirés du vault de Value DeFi, puis 2,000,000 de dollars, accompagnés de la note suivante, furent retournés :

![](https://lh5.googleusercontent.com/_b3-umHgK4n0lvMJcrgMjVZkHTIpbdzd_OHLV73C0C4A4PBIqr_lfvDrahBPwdgmJOfDDmgBEiQ6R7-f8-H1ZBh9E3Y-5WgGbGwwk28XSfD4JcURbK9NcP3RAqWVaD7wYEzjtalp)

À 16h00, juste au moment où l'AMA devait commencer, Stani Kulechov publia le tweet suivant :

![](https://lh6.googleusercontent.com/dBkWmYCfLAx2j6xhO4SeB9FEuMNPOgrFQRzSoYUvwv5rbydivcMqj70HauqhJM0mTx8VIp_nK1jJ4ubvNgZ4H8d4EpoUBAXFwdVrbvsWKvaMKP27fgnPMmS7SEfFyaCAVnS-lFiz)

Pendant ce temps, dans l'AMA :

![](https://lh6.googleusercontent.com/e3_MrE8GywtpCPum9fpVI4dItHOA3J4Jcqqv04eGDuI4crIPMv0YfZyLCpVpVMdOsOrvv_0CWIvb38LNMxDd21RRgmvtgyc7HW5PMuw5_HrhorudSvWRBYAwoRsCk9fl1nqJpqVY)

L'équipe Value a reconnu le hack sur leur [Discord](https://discordapp.com/channels/738345978750435408/744758563376857210/777202671068381195) à 16h05, mais les questions de l’AMA se sont poursuivies pendant 40 minutes sur des sujets sans rapport, jusqu'à ce que…

![](https://lh6.googleusercontent.com/vrOHsSMhnYTH7ezrLuhy1twz47KQEtpq4rxcNs4OOChEARyJBaIVVYVvmojSyuoVHpazliLTy0sBCvXDgnyz-9pywr6HNYHlItnFKgz-tbng1Ygu6mGm0IHWdsN-ymAHX2_dJ0wh)

[$FARM](/harvest-finance-rekt/), [$AKRO](/akropolis-rekt/) et maintenant [$VALUE](https://bloxy.info/tx/0x46a03488247425f845e444b9c10b52ba3c14927c687d38287c0faddc7471150a) ont été victimes de flash loans. De bien rudes leçons pour des protocoles fragiles, des leçons qui exposent la faiblesse de leur plateforme avant qu’une partie de la somme ne leur soit restituée en signe de “bonne foi”.

Il n’y a que des projets à moitié sérieux qui ont été ciblés, ceux qui possèdent une activité soutenue et une TVL honorable.

**Tente-t-on de nous apprendre quelque chose avec ces attaques ?**

Les flash loans sont un sujet controversé dans l’univers de la DeFi, et s'ils ont été la cause de bien des attaques et des exploits ces derniers mois, on pourrait affirmer que cela accélère simplement notre processus d'apprentissage et nous aide à éliminer les protocoles les plus faibles.

**Sans les flash loan, nous attendrions que ça soit une baleine qui le fasse.** Il est préférable que nous traversions cette épreuve maintenant, durant la genèse de la finance décentralisée, alors que les personnes qui sont prêtes à prendre des risques expérimentent, tentent des choses et lancent quotidiennement de nouveaux produits. 

Les flash loan sont là pour enseigner et donner une leçon d'humilité à ceux qui brûlent les étapes. Ils sont le summum de la DeFi - irréalisables ailleurs, les flash loans sont le parfait exemple des nouvelles possibilités offertes par la technologie.

**Une fonctionnalité de la DeFi, pas un exploit de code.**

Les protocoles les plus solides ne sont pas affectés par ces attaques. Certains en bénéficient même.

**Les flash loans relèvent la barre bien plus haut pour les développeurs de la DeFi.**

Tant que les nouvelles normes ne seront pas respectées, les individus comme les protocoles continueront de se faire rekt. Ce sera douloureux, et ce sera fait en public, mais grâce à cela nous serons en mesure d’en tirer des leçons. La DeFi en sortira plus forte, et nous développerons alors de meilleures habitudes, des codes plus solides, et un environnement plus sûr pour les futurs utilisateurs.
