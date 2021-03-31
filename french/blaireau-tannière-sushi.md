---
title: Un blaireau dans la tannière de Sushi
date: 26 Jan 2021
tags:
  - sushi
excerpt: Le blaireau est connu pour suivre un itinéraire toujours identique lorsqu’il sort en dehors de sa tanière pour fourrager sa nourriture chaque nuit. Cette habitude crée des chemins battus à travers les champs et les bois. Quand l’itinéraire d’un blaireau est modifié ou obstrué d’une quelconque manière, l’animal devient confus et finit par s'établir avec le mauvais partenaire.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/header-3.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/header-3.jpg)

**Le blaireau est connu pour suivre un itinéraire toujours identique lorsqu’il sort en dehors de sa tanière pour fourrager sa nourriture chaque nuit. Cette habitude crée des chemins battus à travers les champs et les bois.** 

**Quand l’itinéraire d’un blaireau est modifié ou obstrué d’une quelconque manière, l’animal devient confus et finit par s'établir avec le mauvais partenaire.** 

Nous avons été informé d’une transaction qui a permis à un [utilisateur expérimenté](https://etherscan.io/address/0x51841d9afe10fe55571bdb8f4af1060415003528) de la DeFi de transformer ses 0.001 ethers en 81.68 ETH à travers le token [DIGG](https://www.coingecko.com/en/coins/digg) de [Badger DAO](https://app.badger.finance/).

Après des recherches plus approfondies, nous avons trouvé que bien qu’il y ait eu un exploit, les dégâts avaient déjà été cloisonnés et ce qui pouvait s’apparenter à une menace contre l'entièreté du protocole Sushiswap n’était simplement qu’un charognard plutôt malin qui profitait des restes laissés sur place. 

**Un portefeuille déjà identifié utilisait un ancien point faible qui avait été rouvert, en conséquence d’un oubli malheureux de la part de l’équipe de Sushi.** 

**Si l’opération en question nous semblait alarmante, après une discussion avec l’équipe de Sushi, il était clair que la situation n’était en fait pas si préoccupante.**

La [transaction](https://etherscan.io/tx/0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b) en question montre la tentative de ShushiMaker de convertir 0.05% des frais d’échanges journaliers de la paire DIGG/WBTC à travers une réserve de liquidité DIGG/ETH faiblement garnie, ce qui causa un important slippage lors de l’échange et un braquage des frais des fournisseurs de liquidité de la paire DIGG/ETH. 

Ces frais qui auraient dû être distribués aux possesseurs d’XSUSHI sont partis dans les poches de l’assaillant. 

**Comment a-t-il fait ?** 

Bien qu'une solution ait été créée quelques semaines auparavant, elle devait être appliquée manuellement pour chaque nouvelle réserve de liquidité. Cette manœuvre manuelle n'avait pas été effectuée sur la paire sur la paire et le charognard a été capable de s'immiscer et de prendre possession de ces frais, destinés aux possesseurs de xSushi. 

**Quand une vague de nouvelles paires a été ajoutée au programme [Onsen](https://sushiswap.fi/onsen) de Sushiswap, certaines n’étaient pas composées d'éthers, mais pour le cas précis de la paire DIGG/WBTC, aucun bridge n’avait été mis en place au sein du SushiMaker.** 

SushiMaker est le smart contract qui permet de récupérer 0.05% des frais d’échange pour les distribuer aux utilisateurs ayant bloqué leurs SUSHI en tant que xSUSHI afin d’obtenir des récompenses supplémentaires sans subir de pertes impermanentes. 

Par défaut, SushiMaker vend les frais accumulés (et leurs paires) en ETH puis en SUSHI.

Ce bridge fait donc en sorte que lorsque SushiMaker vend les frais d'un actif sans passer par une paire avec de l’ETH, il peut le faire avec un un actif autre que l'ETH qui dispose d'une liquidité appropriée.

Sans ce bridge, de la liquidité peut être apportée pour créer une paire ETH sur laquelle le contrat SushiMaker tentera d’échanger les frais pour cet actif, subissant un impact sur le prix important à cause du manque de liquidité sur la paire.  

**Les frais accumulés au sein du contrat SushiMaker ont donc récompensé les fournisseurs de liquidité sur la paire ETH et non les possesseurs de xSUSHI comme cela devait être le cas initialement.** 

**Heureusement, aucune perte à déclarer pour les fournisseurs de liquidités ou d’xSUSHI puisque seuls les frais de la paire DIGG/ETH (0.05% de frais sur les swaps sur la paire - 81 ETH) ont été perdus.** 

Un bridge a été mis en place pour les paires DIGG pour résoudre ce problème pour les participants à xSUSHI. Il a également été ajouté au contrat SushiMaker. 

**Une conversation  sur le discord de Sushiswap nous permet d’en savoir plus sur les mécanismes derrière cette attaque :**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/1.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/2.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/3.png)

**Nous avons analysé plus en détail l’adresse du charognard et il s’est avéré être un fin connaisseurs des bots DeFi et de l’utilisation de flash loans.**

![](https://lh4.googleusercontent.com/mbHCt8MYOKLIbVMR8ZEUaz0LHxerb8pKXbTDahY_U_KS_IocDL9ymBER2j0VVVHSIAQQLKb7mc3XorPJV382OJK0KUFe1rvEQcr4-3zJqOg_t435UtQzUtwjB_UGGgODeEsgWbCg)

![](https://lh4.googleusercontent.com/KLD2d5wTEfMmuh5P7IBIy4k17OMfA4UGgnNSZQ38roXBLH4-8DDMlLEc_9KNs4YIHTSkzh3sVdHsSHR_c-RZYTwBfqbwzKUF6yUJ-UjP5y1c0mQpmgyRTl_0McCU1lrNgKrJH-zC)

_Data de [Nansen](https://nansen.ai/)_

Nous avons retrouvé différentes transactions qui montrent que cet [utilisateur](https://etherscan.io/address/0x51841d9afe10fe55571bdb8f4af1060415003528) a tenté d’utiliser à son avantage cette vulnérabilité et de voler les frais des fournisseurs de liquidités.

[0x90fb0c9976361f537330a5617a404045ffb3fef5972cf67b531386014eeae7a9](https://etherscan.io/tx/0x90fb0c9976361f537330a5617a404045ffb3fef5972cf67b531386014eeae7a9)

[0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b](https://etherscan.io/tx/0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b)

[0xcec93808a657d00cbb0245711e9419d0ea278b3a60a9a6d0a8c3353523c0e982](https://etherscan.io/tx/0xcec93808a657d00cbb0245711e9419d0ea278b3a60a9a6d0a8c3353523c0e982)

[0xe0527f7befaea54257113a09c8b3f4cd416e11a0e196cd2ba2e5e07c47767ddf](https://etherscan.io/tx/0xe0527f7befaea54257113a09c8b3f4cd416e11a0e196cd2ba2e5e07c47767ddf)

---

**Ce qui aurait pu être un désastre n’a finalement été qu’une légère humiliation pour l’équipe de Sushiswap.** 

Bien que l'assaillant ait réussi son exploit, nous pouvons considérer cela comme un avertissement sans frais pour SushiSwap, qui a actuellement [1,9 milliard de dollars TVL](https://defillama.com/protocol/sushiswap) à protéger.

Cette conversation sur Discord indiquant qu’ils ne vont pas automatiser cette réparation mais continuer à se contenter d’appliquer cette correction dès que nécessaire est assez préoccupante.

**Pourquoi autoriser une marge d'erreur humaine si ce n'est pas nécessaire ?**

Bien que le code puisse être décentralisé, les développeurs assument une énorme responsabilité lorsqu'ils travaillent sur des protocoles avec une TVL aussi énorme. Les effets du stress sont souvent sous-estimés et nous voyons de nombreux développeurs être victimes de «burn out». De nombreuses choses peuvent mal se passer quand on code, alors peut-être que Sushiswap tirerait des bénéfices d'une automatisation de temps en temps.

**Cette histoire nous rappelle que les protocoles sont constamment surveillés par des hackers et des arbitragistes qui traquent chacun de leurs mouvements et tentent de leur faire les poches voire même de les mettre au tapis.**

Cependant, cet examen va dans les deux sens - même des amateurs tels que le Twittos “simp2win” peuvent observer les pirates de loin. Leur effort est louable, mais peut-être devraient-ils laisser les analyses aux experts.

Nous adorons les hackers qui ont quelque chose à dire, nous étions donc très heureux de les voir envoyer un message via [Ethereum call data](https://twitter.com/EtherText/status/1354078163022868481?s=20).

[*Qui est ce type sur Twitter, simp2win, qui dit que je me suis fait 10 millions ? lol si seulement*](https://etherscan.io/tx/0x48963b96df0949a893401635b0900064aecae780ec0950cbbd4122005eb4e14a)
