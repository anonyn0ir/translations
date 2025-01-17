---
title: Alpha Finance - REKT
date: 13 февраля 2021
rekt: 
  количество: 37500000
  аудит: Quantstamp, Peckshield
  дата: 13 февраля 2021
tags:
  - Alpha Finance
  - Кронье
  - rekt
excerpt: Темные искусства DeFi по-прежнему приносят больше денег. ~$37.5M было украдено с помощью сложной схемы из фальшивой магии, путаницы и обвинений. Жертва узнала нападающего.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/header-alpha-homora.png
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/header-alpha-homora.png)
**Темные искусства DeFi по-прежнему приносят больше денег.**

Далее следует одна из наших самых драматичных историй.

**Повесть о фальшивой магии, путанице и обвинениях, приведших к самому большому взлому в истории DeFi.**

~$37.5 миллионов было украдено с помощью сложной схемы DeFi-обмана. Пока все думали, что под ударом был Iron Bank, на сейфы Alpha Finance была направлена атака из множества транзакций.

Убийство произошло в [зеркальном коридоре](https://youtu.be/F-BqDWG72iM). Из-за растущей взаимосвязанности протоколов DeFi вкупе со сложностью атаки сообщество так и не поняло, кто же стал жертвой, а кто должен был всё исправлять.

Вредоносный контракт атакующих заставил код Homora “поверить”, что он (код) - один из них. Дальше он стал манипулировать данными о долгах внутри системы.

**Это была схватка один на один между протоколом и атакующим.** Эксплуатируемый контракт еще не был обнародован и не был доступен пользователям, поэтому их это напрямую не затронуло. Мы еще не сталкивались с такой наглой работой изнутри. Alpha Finance быстро заявили, что у них был [“главный подозреваемый”](https://twitter.com/AlphaFinanceLab/status/1360623172433760256?s=20).

Почему контракт остался в главной сети, если он еще не был готов? Мы задали вопрос Alpha Finance, и они нам ответили:

>“Мы запустили несколько пулов на уровне контрактов, как например sUSD, а не на уровне пользовательского интерфейса, потому что мы собирались запускать новые пулы и в том числе sUSD на следующей неделе.” 

**Большие игроки тут же засуетились, чтобы спасти свой капитал в неразберихе.** SBF вывел на [$400 миллионов](https://twitter.com/_wilbur4ce_/status/1360636958595305474?s=20)  FTT с Cream Finance, а [Three Arrows Capital](https://etherscan.io/address/0x5cfd0cddf989959a6a6c3ad985ce324460d46dfd) послал  $ALPHA на [$3 с лишним миллиона](https://twitter.com/Raez_x/status/1360542616849375233?s=20) на Binance. А там цель очевидна - продать. 

Все токены, имеющие отношение к атаке, упали в цене. 

Токен управления Alpha Homora - [ALPHA](https://www.coingecko.com/en/coins/alpha-finance) - упал с $2.25 до $1.78.

Токен управления Iron Bank - [CREAM](https://www.coingecko.com/en/coins/cream) - упал с $288.32 до $193.51. 
Токен [AAVE](https://www.coingecko.com/en/coins/aave), управленец от создателей противоречивого флэш-займа, благодаря которому стали возможными многочисленные атаки подобного рода, упал с $518 до $492 в тот же день.

**Ценообразование токенов, однако, не самая интересная часть в этой истории...**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/linebreak-shanghai2.png)

Команда Alpha Finance составила отличный [пост-мортем](https://blog.alphafinance.io/alpha-homora-v2-post-mortem/), и то, что они обнаружили, было потрясающе. Совокупный результат нашего расследования показал, что урон был намного серьезнее, чем предполагалось. 

Время покажет, будет ли Alpha Finance обнародовать обвинения. Но, судя по их первоначальному заявлению о главном подозреваемом, продолжение следует. 

**Из официального пост-мортема следует, что атаковавший должен был знать следующее, чтобы устроить нападение:**

- **У HomoraBankv2 есть пул sUSD на контрактном уровне, так как готовится выпуск. Он не доступен в пользовательском интерфейсе и о нем не объявляли.**
- **В кредитном пуле sUSD не было ликвидности,** значит атакующий может полностью управлять суммой и общей долей долга, раздувая их.
- **При вычислении функции заимствования имеется ошибка округления,** которая имеет значение только тогда, когда злоумышленник является единственным заемщиком.
- **Функция resolveReserve может увеличить totalDebt без увеличения totalDebtShare,** а функция, предназначенная для сбора доходов в резервный пул, действительно может быть вызвана кем угодно.
- HomoraBankv2 принимает любой настраиваемый контракт (spell), при условии, что инвариант удостоверяет, что коллатерал > займ (spell по своему принципу похож на стратегию в Yearn).

При таком количестве свидетелей грабители оставили после себя четкий след из зацепок. В редких случаях контратаки жертвы определили нападавшего.

Чтобы осуществить эту атаку, нужна была информация изнутри, это очевидно благодаря описанию выше. Тем не менее, инсайдер мог попасть туда несколькими путями, из-за количества протоколов и задействованных аудиторских фирм. 

_rekt больше не занимается обвинениями, но нам интересно, как Alpha Finance разберется с этой ситуацией._

**Как это случилось [по версии to Alpha Finance:](https://blog.alphafinance.io/alpha-homora-v2-post-mortem/)**

**1.** Хакер создал вредоносный контракт spell (эквивалент стратегии в Yearn). https://etherscan.io/tx/0x2b419173c1f116e94e43afed15a46e3b3a109e118aba166fcca0ba583f686d23

**2.** Хакер обменивает ETH -> UNI, поставляет ETH + UNI в пул Uniswap (получает ETH/UNI токен LP). В той же транзакции обменивает ETH -> sUSD на Uniswap и кладёт sUSD в Iron Bank протокола Cream (получает cysUSD).
https://etherscan.io/tx/0x4441eefe434fbef9d9b3acb169e35eb7b3958763b74c5617b39034decd4dd3ad

**3.** Дает HomoraBankv2 команду выполнить, используя вредоносный spell (в позицию 883): Взять в долг 1000е18 sUSD. Депозит UNI-WETH LP в WERC20, и использовать как коллатерал (чтобы обойти проверку коллатерал > займ). В этот момент у атакующего 1000е18 sUSD долговых акций (потому что он первый заемщик).
https://etherscan.io/tx/0xcc57ac77dc3953de7832162ea4cd925970e064ead3f6861ee40076aca8e7e571

**4.** Дает HomoraBankv2 команду выполнить, снова используя вредоносный spell (в позицию 883): Выплатить 1000000098548938710983 sUSD (фактическая задолженность с начисленными процентами составляет 1000000098548938710984 sUSD), что приводит к выплате доли на 1 меньше, чем общая доля. В итоге у хакера сейчас долг в 1 minisUSD и 1 долговая доля.
https://etherscan.io/tx/0xf31ee9d9e83db3592601b854fe4f8b872cecd0ea2a3247c475eea8062a20dd41

**5.** Дает команду resolveReserve банку sUSD, начисляя 19709787742196 долга, в то время как totalShare остается равной 1. Текущий статус: totalDebt = 19709787742197, totalShare = 1. 
https://etherscan.io/tx/0x98f623af655f1e27e1c04ffe0bc8c9bbdb35d39999913bedfe712d4058c67c0e

**6.** Дает HomoraBankv2 команду выполнить, снова используя вредоносный spell (повторяет 16 раз, каждый раз удваивая сумму займа): Взять в долг 19709787742196 minisUSD и перевести атакующему (каждый раз удваивая, так как totalDebt удваивается при каждом успешном займе). Каждый займ меньше значения totalDebt на 1, в результате чего соответствующая доля займа = 0, поэтому протокол обрабатывает это как займ без долга. В конце транзакции хакер вносит 19.54 sUSD в Iron Bank протокола Cream.
https://etherscan.io/tx/0x2e387620bb31c067efc878346742637d650843210596e770d4e2d601de5409e3

**7.** Процесс продолжается: даёт HomoraBankv2 команду выполнить, снова используя вредоносный spell (повторяет 10 раз, каждый раз удваивая сумму займа). В конце транзакции хакер вносит 1321 sUSD в Iron Bank протокола  Cream.
https://etherscan.io/tx/0x64de824a7aa339ff41b1487194ca634a9ce35a32c65f4e78eb3893cc183532a4

**8.** Делает флэш-займ в Aave (берет в долг 1,800,000 USDC). Переводит 1,800,000 USDC в 1,770,757.56254472419047906 sUSD и вносит в Cream, чтобы у хакера было достаточно ликвидности для займов с помощью настраиваемого контракта spell. Продолжает удваивать займы в sUSD, с 1,374,960.72 sUSD до 677,223.15 sUSD (всего 10 раз). Переводит 1,353,123.59 sUSD в 1,374,960.72 USDC на Curve. Берет займ 426,659.27 USDC на Cream (хакер уже внёс sUSD на этапе b.)
https://etherscan.io/tx/0x7eb2436eedd39c8865fcc1e51ae4a245e89765f4c64a13200c623f676b3912f9

**9.** Повторяет шаг 8, но уже с ~10M USDC (без займа USDC в конце).
https://etherscan.io/tx/0xd7a91172c3fd09acb75a9447189e1178ae70517698f249b84062681f43f0e26e

**10.** Повторяет с 10М USDC (без займа USCD в конце).
https://etherscan.io/tx/0xacec6ddb7db4baa66c0fb6289c25a833d93d2d9eb4fbe9a8d8495e5bfa24ba57

**11.**Берёт займ 13,244.63 WETH + 3.6M USDC + 5.6M USDC + 4.26M DAI. Поставляет стейблкоины на Aave (чтобы получить aTokens, таким образом  USDC и USDT не могут быть заморожены). Поставляет aDAI, aUSDT, aUSDC в пул Curve a3crv.
https://etherscan.io/tx/0x745ddedf268f60ea4a038991d46b33b7a1d4e5a9ff2767cdba2d3af69f43eb1b

**12.** Добавляет a3crv LP токен в индикатор ликвидности Curve.
https://etherscan.io/tx/0xc60bc6ab561af2a19ebc9e57b44b21774e489bb07f75cb367d69841b372fe896

**13.** Остальные транзакции направлены на поставки в Tornado Cash, GitCoin Grants. По 1 тысяче ETH посылается на адреса разработчиков  Cream и Alpha.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/linebreak-shanghai.png)

**Эта история уникальна своим действующим составом.** 

Когда дело касается работы белых шляп / черных шляп, всегда ожидаешь некоторой двойственности и смены ролей. Но не часто встретишь такие четкие обвинения со стороны жертвы. 

Андре Кронье (Andre Cronje), который всего за несколько недель до этого был [партнером Yearn](https://twitter.com/AndreCronjeTech/status/1347194324237176832?s=20) и Alpha Homora, сегодня [написал об атаке](https://twitter.com/AndreCronjeTech/status/1360674224797483010?s=20):

>Изучите внимательно проделанную работу. 9 транзакций. 4 разные манипуляции. В одной из них точный долговой расчет. На то, чтобы разобраться в этом, у команд исследователей ушли часы. Alpha немедленно приняли меры по смягчению последствий. Это было сделано в течение нескольких минут после обнаружения. 

[И ответ от Banteg:](https://twitter.com/bantg/status/1360678595551707139?s=20)
>Подстава совершенно безумная. Это ни за что бы не обнаружил кто-то, случайно просматривающий контракты, особенно в неопубликованном материале.

**Возможно, это приведет к еще одному приобретению для Yearn; имя Кронье упоминается четырежды в пост-мортеме, и [схема выглядит очень знакомой...](https://rekt.eth.link/decentralised-monopoly/)**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/alpha-finance-conclusion.png)
**Сколько еще может продолжаться эта эра анонимных хакеров?** 

Список возможных подозреваемых настолько маленький, что становится легче вычеркнуть невиновных и выследить потенциальных злоумышленников. В данном случае список даже еще меньше обычного. 

“Не доверяй, проверяй” - замечательная мантра при работе с кодом. Но и она не убережет от растущей социальной паранойи в высших кругах децентрализованных финансов. Мы живем в период беспрецедентного роста криптовалют и DeFi, когда цена бездействия очень высока. Ментальная нагрузка разработчиков DeFi растет изо дня в день. 

Поверх строчек кода возводят империи, а будущее финансов строится на наших глазах.

**Разработчики заняты гонкой к небесам, а в это время инсайдеры помогают хакерам в подполье ковырять дыры в своем фундаменте.** 

Когда одна башня падает, остальные смотрят и учатся на ошибках. Еще до того, как осядет пыль, толпы придут в движение и неустанные команды вернутся в гонку, чтобы стать еще сильнее. 

**Как долго они смогут продолжать в таком же темпе, пока неизбежная ошибка не сорвет с них маску анонимности?**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/02/af-gif.gif)
