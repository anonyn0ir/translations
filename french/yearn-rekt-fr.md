---
title: Yearn - REKT
date: 05 Feb 2021
rekt: 
  amount: 11000000
  audit: Unaudited
  date: 05 Feb 2021
tags:
  - Yearn
  - REKT
excerpt: L'adage “trop gros pour faire faillite” ne peut s’appliquer à aucun protocole. Même les géants de la DeFi ne sont pas de taille face aux flashloans.
banner: https://lh6.googleusercontent.com/2htMKXFnd_RYudETxssIO-ztLBIhBXwlq4jADQmX80p682WvwhLmjSjoYhE5spF_f_Yfan8DLIe4B2NwLLIec9tH5wt9H_RyRertgtKzELIVQrq3XTwFhwULAoP9BHzzmCeyqsWg
---

![](https://lh6.googleusercontent.com/2htMKXFnd_RYudETxssIO-ztLBIhBXwlq4jADQmX80p682WvwhLmjSjoYhE5spF_f_Yfan8DLIe4B2NwLLIec9tH5wt9H_RyRertgtKzELIVQrq3XTwFhwULAoP9BHzzmCeyqsWg)

**L'adage “trop gros pour faire faillite” ne peut s’appliquer à aucun protocole.**

_Même les géants de la DeFi ne sont pas de taille face aux flashloans._

Une attaque par arbitrage sur le DAI v1 vault de Yearn prouve que même les plus expérimentés de nos développeurs peuvent encore faire des erreurs.

Le vault a été attaqué par 9 flashloans. 11 millions de dollars ont été extraits du vault, dont 2,7 millions ont fini dans la poche de l’assaillant. 3,5 millions de dollars sont partis chez les fournisseurs de liquidité de chez Curve, 3,5 millions également sont partis chez leurs stackeurs, et 1,4 millions ont été payés en frais Aave 2.

**Les écosystèmes DeFi sont en constante évolution. Les protocoles de plus en plus entrelacés forment une machine infinie constituée d'innombrables Lego.**

Le développement de notre industrie se poursuit à une vitesse folle, et chaque jour de nouvelles idées et de nouveaux vecteurs d’attaques sont révélés au grand jour.

Un environnement en constante évolution signifie que même des produits testés en permanence ne sont pas capables de garantir une entière sécurité.

**Si être la victime d’un arbitragiste doit être humiliant pour l’équipe qui paraissait auparavant invincible, on ne tire pas non plus de plaisir à faire remarquer des failles dans le travail des développeurs qui créent tant de valeur pour notre écosystème.**

L’équipe de Yearn a donné sa version des faits après-coup, mais sans que les flashloans ne soient mentionnés.

Igor Igamberdiev a livré une analyse plus détaillée de l'attaque sur Twitter.

Profits de l’assaillant : 

- 513 000 DAI

- 1,7 millions USDT

- 506 000 3CRV (~1 $) restant

L’assaillant a effectué 11 transactions

1. Un flashloan de 116 000 ETH depuis dYdX 

2. Un flashloan de 99 000 ETH depuis Aave v2

3. Un emprunt de 134 millions d’USDC  et de 129 millions de DAI en utilisant ETH comme collatéral chez Compound

4. Un ajout de 134 millions de d’USDC et 36 millions de DAI à la pool 3crv de Curve


5. Un retrait de de 165 millions de d’USDT de la pool 3crv de Curve 


6. 5 répétitions


  \- Un dépôt de 93 millions de DAI dans le vault yDAI (décroissant à chaque itération) 

  \- Un ajout de 165 millions d’USDT à la pool 3crv

  \- Un retrait de 92 millions de DAI depuis le vault yDAI (décroissant à chaque itération)

  \- Un retrait de 165 millions depuis la pool 3crv

7. La dernière fois, un retrait de 39 millions de DAI et 134 millions d’USDC au lieu d’USDT

8. Remboursement des frais Coumpond

9. Remboursement des flash loans

A chaque fois l’assaillant accumulait les tokens 3crv, qu’il a ensuite pu échanger contre des stablecoins.

Contrat de l’assaillant :

https://etherscan.io/address/0x62494b3ed9663334e57f23532155ea0575c487c5Attac

Tornado TX #1

https://etherscan.io/tx/0x7ee28e342573ff7b8fb4bd2e4373e742cf80d8f8c7f8764cc6b70439dc33f037

Tornado TX #2

https://etherscan.io/tx/0x13c12895d44f8b890af2187b93b97bec01dd34eeb026ac9669d8412e57d64446

Tornado TX #3

https://etherscan.io/tx/0x6b07e3faaa419ea5a3d58929e07b872f8529441064eb576d61ef5edd697f7256

Tornado TX #4

https://etherscan.io/tx/0xcacdc95bd65556426bae39025ddb1deafb65acb908be49fb7186bb750f7a369f

L’occasion de faire du profit était possible car les frais de retrait avaient été désactivés pour une migration de vault.

---

**Nos lecteurs savent bien qu’il n’y a rien de nouveau avec les attaques via flash loans**, et _a fortiori_ aussi les développeurs de Yearn le savent aussi. Ils sont assez compétents pour empêcher ce genre de choses d’arriver, ce qui laisse à penser que ceci a été une rare opportunité saisie, liée à une erreur effectuée durant la migration du vault.

Les ragots et les drama vont bon train dans le monde de la DeFi, et beaucoup se sont mis à imaginer cette attaque comme une représaille aux précédentes accusations d’hypocrisie de Cronje contre Julien Bouteloup, l'un des contributeurs de Stake DAO.

![](https://lh6.googleusercontent.com/JTjkSs0iTtatTK92Vs53mx1qb5FlCSkjxf9-BTxvo2BgB69Ftki6dPveLUvORlGpo4eH906UxH8ckMkkxwacqYO7e-itzE4eWMCZbbuQ4twuwni6lWYZAAwPaPJVInaOdAhqqxAH)

Bien que beaucoup de nos lecteurs (et votre auteur anonyme) aimeraient secrètement assister à un tel duel entre les deux développeurs, ces accusations ne sont pas fondées, le compte de l’assaillant et la rédaction du contrat ayant été réalisés des heures avant que cette critique ne soit émise.

![](https://lh6.googleusercontent.com/qK0b6N34P6dMIF4bt_pK08fPtPbcmI1dOmmXx3lThk76IKdsmEEyVpbl_5Yz9CqEFJoH4jQE0thf2uL30EnUd_h2Zq0ayyHk6PF14iiP7ZYSAzAktdMZzXTxA23UDgRt5IgUdcOE)

La concurrence entre eux est évidente, étant deux des développeurs les plus en vue de notre écosystème. La passion pour leur travail et le fait que leur réputation soit liée à l'immense responsabilité de voir des millions de dollars confiés à leur code fait que leurs relations professionnelles sont soumises à un immense stress.

**Il est aussi bon de se rappeler que tous nos meilleurs développeurs ne sont pas sur Twitter.**

---

**Si un protocole DeFi reçoit des remboursements d'une entreprise centralisée, à quel moment cesse-t-il d'être réellement un protocole DeFi ?**

Tether a gelé les 1,7 millions d’USDT volés pendant le hack. Dans le passé, Tether a également remboursé des utilisateurs qui avaient malencontreusement perdu de l’argent en envoyant des tokens à une mauvaise adresse. 

**Si Tether détruit ces tokens volés et en mine ensuite un montant équivalent afin de rembourser Yearn, ils ne sont alors en rien différents d’une banque centrale.**

Le développeur de Yearn @fubuloubu s'était prononcé contre l'utilisation de Tether dans le passé, mais semble avoir subitement changé d'avis après leur intervention.

![](https://lh4.googleusercontent.com/EQrZYxGPLP25hIXWLkUI5DUQbVBX8tDe6x_yOJf-P-ebQ9LvaRc0EXcN2N188mDCp1rXFMG92dq7l08jkrygHMXahVYECcHtNQbAcCwjVsWHeZPmhuC_gyRWfDXK2fSXWpVwGbay)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/image.png)

Nous aimons tous la décentralisation lorsqu'elle nous rapporte des bénéfices, mais les remboursements marchent quand même bien mieux quand c’est centralisé.

---

**Cette attaque a directement frappé au cœur l'un des plus grands conglomérats DeFi, ébranlant les fondations de ce qui était autrefois considéré comme une forteresse impénétrable.**

Même les meilleurs du secteur font des erreurs, mais cela ne doit pas nous empêcher de les encourager à continuer de construire.

Lorsque la tension monte et que les équipes DeFi commencent à prendre parti les unes contre les autres, nous ferions tous bien plutôt de prendre du recul et de regarder la situation avec de la hauteur.

**Nous fabriquons des armes contre la finance traditionnelle. Il ne faut pas restreindre le flux de l’innovation par des querelles intestines, mais se rappeler qui est notre véritable ennemi et lui faire front tous ensemble.**

Avec le temps, nous n’aurons que du respect pour tous les acteurs qui ont cru dans la vision que nous avons eu dès cette période si précoce. 

Hier soir, la première fissure est apparue dans l'armure de Yearn. Leur erreur fera-t-elle perdre la foi à la communauté, ou au contraire sera-t-elle l’occasion pour nous tous de nous rallier derrière ce géant de DeFi et les aider à devenir encore plus forts ?

![](https://lh5.googleusercontent.com/gwQf4mTtg264KPREnhva2DtM_OLqf7XuW2GCxxaHxhldpl46z-mwe5Mva9_Y61jzO5oIqO5GONSjtrQk-eTKtk1nQyaFnzcCaZm9oG-0dBxTOcCW_6hTAz2VkaI1_Oe6va25J5LD)
