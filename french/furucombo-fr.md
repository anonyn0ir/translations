---
title: Furucombo - REKT
date: 01 Mar 2021
rekt: 
  amount: 14000000
  audit: Haechi
  date: 27 Feb 2021
tags:
  - Furucombo
  - rekt
excerpt: Il vaut mieux prendre son temps plutôt que de rater son coup. rekt monte sur le ring avec Limzero et Kurt Barry pour enquêter sur le knock-out à 14 millions de dollars de Furucombo. "L'approbation infinie" n'est jamais sûre.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-header.png)

**Il vaut mieux prendre son temps plutôt que de rater son coup.** 

Nous avons entendu parler de [Furucombo](https://twitter.com/furucombo/status/1365743632460910593?s=20) mais nous étions déjà pris ailleurs - les petites équipes ne peuvent pas toujours tout expédier à temps, surtout si les hackers travaillent le week-end. Si vous êtes un détective spécialisé en DeFi avec des compétences à partager, contactez-nous et racontez-nous votre parcours : nous pourrions avoir une place ici pour vous à rekt.news.

Un hacker a riposté lors d’une contre-attaque, a brisé Furocombo et l’a assommé, lui dérobant pour 14 millions de dollars dans plusieurs portefeuilles qui avaient donné à l’application une "approbation infinie”.

Une approbation infinie signifie une confiance illimitée - ce que nous ne pouvons pas nous permettre en DeFi.

**“Ne crois pas, vérifie”, mais qui a le temps ou l'argent de disponible pour le gas pour approuver des montants fixes chaque fois qu'ils effectuent des transactions ?**

Les personnes qui ont utilisé FuruCombo ont dû fournir une certaine approbation, mais il semble que certains en aient trop donné, recevant une dure leçon de vie en retour. 

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-linebreak.png)

De ce que nous connaissons d’un exploit “d’evil contract”, [l'assaillant](https://etherscan.io/address/0xb624E2b10b84a41687caeC94BDd484E48d76B212) a fait croire au [proxy contract](https://etherscan.io/address/0x17e8Ca1b4798B97602895f63206afCd1Fc90Ca5f) de Furucombo que Aave V2 avait une nouvelle [implémentation](https://etherscan.io/address/0x86765dde9304bea32f65330d266155c4fa0c4f04).

La nouvelle implémentation était, bien entendu, malveillante, et avait la capacité de transférer tous les tokens approuvés aux adresses contrôlées par l’attaquant, et ce car les utilisateurs avaient autorisé les contrats de Furucombo à utiliser leurs tokens en leur nom.

**[Kurt Barry](https://twitter.com/Kurt_M_Barry/status/1365876788757471234?s=20) a fourni l’analyse suivante :**

Une des [transactions de vol de fonds](https://etherscan.io/tx/0x5af11a27e98a167b61b01fea093cf612d5ec76c20fd2032f2d1aa49c8b1ee529) a été envoyée au _proxy_ de Furucombo, en spécifiant le proxy AAVE v2 Lending Pool comme “gestionnaire” pour la première et seule action.

Vous pouvez voir les traces d'exécution ci-dessous, disponibles sur [ethtx.info](https://ethtx.info/). Notez les nested delegatecalls.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx1.png)

Les gestionnaires doivent être approuvés dans un registre ; au moment de la transaction (mais plus maintenant), ce proxy était un gestionnaire valide.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx2.png)

Le proxy de FC delegatecalls le proxy Aave v2, qui ainsi expulse l’adresse de l'implémentation d’un slot de stockage spécifique, mais comme c’est un delegatecall, il le lit depuis le stockage du proxy de FC, et l’adresse extraite est l’exploit contract du hacker.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx3.png)

Si nous regardons la [transaction précédente](https://etherscan.io/tx/0x6a14869266a1dcf3f51b102f44b7af7d0a56f1766e5b1908ac80a6a23dbaf449#statechange…) du hacker:

Nous voyons que le hacker a utilisé son malicious contract pour faire en sorte que les proxy de FC delegatecall le proxy de AAVE v2, en invoquant la initialize function, définissant le slot de l'implémentation.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx4.png)
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-tx5.png)

Une fois que le delegatecall a exécuté le code du hacker dans le contexte du proxy de FC, il n’y avait plus rien à faire. La victime avait autorisé le proxy de FC à déplacer ses stETH, et le code exploité a tout envoyé au hacker.

On prend les mêmes et on recommence.

**Résumé :**

- Le proxy de FC a fait caller-specified delegatecalls pour les gestionnaires approuvés, laissant son stockage se faire modifier.
- Un gestionnaire a fait caller-specified delegatecalls à une adresse lue depuis l’emplacement
- Le gestionnaire a exposé une fonction pour définir cette adresse.


**Ce que nous avons appris :**

- une “trust list” est utile mais n’est pas une garantie.
- Les développeurs devrait auditer comment une fonction delegatecallee’s peut affecter le stockage du caller
- il faut envisager de restreindre les fonctions ou les paramètres des callees
- il faut se méfier des inputs fournis par l’utilisateur


**Il n’y a pas que des particuliers qui ont perdu gros dans cette histoire : Cream Finance également, puisque l’attaquant a directement ‘emprunté’ dans leur trésorerie.**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-cream.png)

[Igor Igamberdiev](https://twitter.com/FrankResearcher/status/1365744024611655690?s=20) a donné une liste des biens qui ont été volés :

- 3,9k stETH
- 2.4M USDC
- 649k USDT
- 257k DAI
- 26 aWBTC
- 270 aWETH
- 296 aETH
- 2.3k aAAVE
- 4 WBTC
- 90k CRV
- 43k LINK
- 7.3k cETH
- 17.2M cUSDC
- 69 cWBTC
- 142.2M BAO
- 38.6k PERP
- 30.4k COMBO
- 75k PAID
- 225k UNIDX
- 342 GRO
- 19k NDX

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-ropebreak.png)

**Nous avons parlé au passionné de DeFi Limzero [(@pleyuh)](https://twitter.com/pleyuh/status/1365998455638876161?s=20) après avoir découvert qu'il était l'un des plus touchés.**

**rekt :**

_Comment ça s’est passé pour toi ?_

_Comment as-tu compris que Furucombo était attaqué et comment as-tu réagi ?_

**Limzero :**

J’étais tranquille à la maison avec des amis. J’ai ouvert TG sur mon portable pour voir ce qui se passait et j’ai vu sur le groupe ["The daily ape"](https://t.me/thedailyape) de [Darren](https://twitter.com/Darrenlautf) qu’il y avait un exploit lié à Furucombo.

J’ai vérifié une de mes adresses que j’avais utilisé sur furucombo et j’ai remarqué le transfert de mes aAAve et de certains de mes aETH.

J’ai pris peur parce que j’avais des prêts actifs et je ne voulais pas que mes dépôts se fassent liquider. J’ai vu que mon health factor était descendu à 1.15, et j’ai donc vite remboursé les prêts.

J’ai remarqué que l’attaquant avait drainé tous mes aAAVE mais seulement 1/3 de mes aETH, et je suppose que mon bas niveau de HF a dû l'empêcher de continuer à transférer mes fonds. Je pense qu’on peut dire que j’ai eu de la chance d' avoir des prêts actifs.

Après avoir remboursé les prêts pour protéger les dépôts, j'ai révoqué toutes les autorisations liées aux tokens que j'avais données à cette adresse.

Je n’arrêtais pas de reporter depuis des semaines le moment où j’allais le faire (pour des histoire de prix de gas). Il semble que ce retard me coûte cher.

J'ai remarqué le transfert de mes fonds par le hacker 90m après le hack.

**rekt :**

_Ce fut une grosse perte pour toi ?_

_Comment te sens-tu psychologiquement, te sens-tu plus sur tes gardes ou moins confiant quant à l'utilisation de la DeFi après l'attaque ?_

**Limzero :**

C'était en soi une grosse perte, mais pas au point de mettre en jeu la survie de mon portefeuille.

J'ai eu très peur pendant quelques minutes car j'avais peur que tous mes aTokens aient pu être liquidés, mais quand j'ai vu que mon health factor était supérieur à 1,1, j’ai été soulagé.

Je prends l’expérience toute entière comme une coûteuse leçon de sécurité. Avoir des autorisations infinies à partir d'une adresse avec de gros montants était une très bête erreur  de ma part. A bien y regarder, c’était une ape tax que je devais finalement payer. C’est le premier hack / exploit de smart contract qui me touche après plusieurs années dans cet univers. J'ai de la chance que des situations plus graves ne m'aient pas encore atteint.

En fait c’est le premier exploit depuis l’exploit de COVER, mais j’ai tourné la page :P

Je ne me sens pas moins confiant dans l'utilisation de la DeFi. Ces types de risques étaient connus.

J'ai cependant pris des mesures pour augmenter ma cybersécurité.

**rekt :**

_Peux-tu nous parler de ces mesures ?_

**Limzero :**

Je ne préfère pas, désolé.

Ca en fait partie justement 😋

**rekt :**

_Quelles mesures recommanderais-tu à nos lecteurs de prendre pour qu’ils améliorent leur sécurité ?_

**Limzero:**

1) Utilisez un portefeuille physique
2) Evitez windows
3) Utiliser une machine spécialement dédiée au Web 3 pour interagir avec les contrats
4) Des mot de passe uniques ou des gestionnaires de mot de passe + VPN
5) Soyez discret sur les réseaux sociaux
6) Utilisez plusieurs adresses pour ne pas mettre tous vos oeufs dans le même panier
7) Utiliser des nouvelles adresses pour des nouveaux farms
8)Révoquez les autorisations des adresses que vous utilisez souvent

Je suis loin d’être un expert en sécurité. Ce sont des conseils basiques suggérés par des gens plus pointus dans la crypto.

9) lisez REKT xD

**rekt :**

_Un dernier mot pour nos lecteurs ?_

**Limzero:**

“S’il vous plaît, ne me hackez plus”

Aussi, si vous avez des doutes pour votre sécurité, songez à laisser une petite partie de vos holds sur des échangeurs centralisés de premier rang comme Kraken, Coinbase, Gemini, Binance au cas où vos portefeuilles se feraient hacker.

C’est tout pour moi.

**rekt:**

_Merci pour l’échange._

**Limzero:**

Merci ! J’espère ne plus avoir à vous parler lol.

---

**Une attaque basique avec un fix basique** - n’utilisez pas “approbation infinie” à moins que vous ayez une confiance infinie. Les approbations individuelles ne sont pas une petite dépense, mais ne cherchez pas à économiser en matière de  sécurité.

Des sites tels que [Debank](https://debank.com/) ou [Etherscan](https://etherscan.io/tokenapprovalchecker) vous permettent de surveiller et de révoquer les approbations de votre portefeuille, et comme Limzero l’a déclaré, ce n’est pas une tâche qu’il faut remettre à plus tard.

Ne baissez jamais votre garde, les hackers sont toujours à l'affût de la moindre ouverture, et ces attaques ont lieu bien plus souvent que vous ne pourriez le croire.

**Il n’y a pas d’arbitre sur le ring, vous seul êtes responsable de votre propre sécurité, mais une fois que vous avez appris les ficelles du métier, le jeu en vaut la chandelle.**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/furu-conc.png)
