---
title: Akropolis - REKT
date: 12 Nov 2020
rekt: 
  amount: 2000000
  audit: CertiK, SmartDec
  date: 12 Nov 2020
tags:
  - akropolis
  - delphi
  - Rekt
excerpt: L’Acropole ne s’est pas fait rekt de la sorte depuis la bataille de Salamine en 480 avant J-C. Un Roi Xerxès des temps modernes a de nouveau rasé l’Acropole, volant pour plus de 2,000,000 de DAI via une combinaison de flash loans et de réentrance.

banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/84604-1.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/84604-1.jpg)

**Périclès doit se retourner dans sa tombe.**

L’Acropole ne s’est pas fait rekt de la sorte depuis la bataille de Salamine en 480 avant J-C.

Un Roi Xerxès des temps modernes a de nouveau rasé l’Acropole, volant pour plus de 2,000,000 de DAI via une combinaison de flash loans et de réentrance. 

Les admins d’Akropolis ont initialement tenté de faire croire qu'ils étaient simplement en train de s'occuper de quelques “fixes”.

![](https://lh5.googleusercontent.com/MElhS0VhaZ0DA_lMRYeLoRNafz1YWpafkzgdcV_K9F-HNxz1V7H85KDGkQdP3npLM9Nql6LjtEqzKVUnHMdL8OzlWbsZ9JbFl_L7JQJc_MWKJpYwIRr_AVzsBUvrpEtLpc-xpkDi)

Nous savons maintenant qu'il y a eu un burn de 2 millions de dollars.

![](https://lh5.googleusercontent.com/OGE_yvAkXzHlE9USnNhS0g0NpV3bqHKBj8Z7bAcVT3B0ejQs8bBkWfWJrmqo_83zWyVTq7aOG_JaLTItr7uL_k2TiKOHN7JEqmwp1T6IOY9w9ENZr6ZtbWE2B29XNxAl4ex_UO_r)

Mais comment ?

Le protocole d’Akropolis autorise ses utilisateurs à déposer des tokens dans un vault pour recevoir en retour différents tokens. La quantité de nouveaux tokens que vous recevez en retour est liée au montant total déposé.

Le montant déposé est calculé par la différence de solde entre ce qu’il y avait avant et après l’opération de transfert. 

C’est ici que l’assaillant a abusé du système en créant un malicious token contract qui a de nouveau call deposit (réentrance).

[Voici](https://etherscan.io/address/0xe2307837524db8961c4541f943598654240bd62f#tokentxns) l'attack contract.

1. Création faketoken

2. Dépôt faketoken

3a. Obtention d’un callback to faketoken, dépôt de 25k DAI

3b. Obtention d’un crédit de 25k DAI de dépôts

4. Obtention d’un crédit de 25k DAI de dépôts

5. Retrait de 50k DAI

Source : [samczsun](https://twitter.com/samczsun)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/4d509e7155f551c4d98bb1014b320c61-1.jpg)

L’assaillant ayant pu utiliser son contrat comme un token de dépôt, il a été capable d’utiliser la réentrance avec un flash loan de dYdX, comme expliqué ci-dessous :

![](https://lh4.googleusercontent.com/LxCZ2ZHvBLGPgk7BaoplX3rNuNtfN2JoZ9VeMBZe42MaWMw7ShK_mdgg70RhZJ1DJO4lLn1D8IkAnZ91VKeamI49aW0pDY-7trH07qX2A_ifqbg5xE_1QVLoOxt7qcUBfIYUm8i0)![](https://lh5.googleusercontent.com/D2wa_EEUSuXUk7r9cRAhX-fwHRv91pmeFeWd1bVR9KFO_IZLXzlzt8I2eJhNfGFP9pOiVokZa58Qn4aFUWlycIIt2gSNNZA5pDSbsy3vqMqsG8eZS1yU8N1qfgQP4_UFbZS0kMfV)

[Voici](https://etherscan.io/address/0xe2307837524db8961c4541f943598654240bd62f#tokentxns) l’adresse du hacker. Nous pouvons voir qu'il avait commencé à exécuter des séries d'attaques de 50 000 $ environ 8 heures plus tôt.

Puis il a [envoyé 2 millions](https://etherscan.io/tx/0xf15623567231c67df2b8bcc5540236fbda2c3ac11ecbec427048f11b582cb869) de dollars de ces gains sur une autre adresse, adresse où ils se trouvent toujours au moment de la rédaction de cet article.

Source : [@dogetoshi](https://twitter.com/Dogetoshi/status/1326963117356625931?s=20)

![](https://lh3.googleusercontent.com/dSGoJEDMg3SdSHVshM5N8FaLgkai2s1q7gtmCd7-VPKmeNcCew5OXEVAHOQ_Sa9h7iRL021U54658OC8HnVS6MdQSTMxsyjfu6MOKQ-qP5o6Ay0-Jy3NjnVx2dKYEmgAqTrefgjL)

Il est important de noter que les smart contracts avec lesquels le hacker a interagi ont été audités par deux entreprises de sécurité différentes, Smartdec et Certik.

Si Smartdec possède un [bilan](https://blog.smartdec.net/) globalement positif, Certik voit Akropolis s’ajouter à la longue liste des projets qu’ils ont audités qui ont par la suite été victimes d'un exploit. 

bZx, Lien, [Harvest](/harvest-finance-rekt/), et maintenant Akropolis. Si un audit de sécurité terminé ne doit jamais être considéré comme une garantie de sécurité, un audit de chez Certik a certainement encore moins de valeur qu'auparavant ... 

Même un audit complet et réalisé consciencieusement peut tourner à la mascarade entre les mains d’incompétents. Le fait qu'Akropolis ait été si prompt à mentir à ses utilisateurs tend à prouver que l'entière responsabilité ne tient pas à Certik, et ni même au hacker.

Bien que nous soyons souvent en quête de protocole ne nécessitant pas de confiance,  celle-ci reste primordiale dans les relations humaines, et notamment dans la communication entre un fournisseur de service et ses utilisateurs : il est nécessaire de toujours chercher à préserver cette fragile confiance.

Akropolis a perdu cette confiance, et s’est fait rekt.
