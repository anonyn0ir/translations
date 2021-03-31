---
title: Compounder Finance - REKT
date: 02 декабря 2020
rekt: 
  количество: 12000000
  аудит: Solidity Finance
  дата: 02 декабря 2020
tags:
  - c3pr
  - аудит
  - rugpull
excerpt: Rekt-косилка знает, как заставить людей говорить. В самом конце, когда общая заблокированная стоимость приближается к нулю, а просадка становится невыносимой, в чат заходит безликая фигура... Наш анонимный автор выследил и допросил злоумышленника, устроившего рагпул протокола Compounder Finance стоимостью $12M.
banner: https://lh6.googleusercontent.com/TLkLMvzALcncoyVu5MGEumqmlOqk7KWADtRJ8Uj62TXUWi_SZg_gw9iiF9hVi_vgMp55Jvpy5Bl0d_ZxOcmJfZnEALbmRDkcrfbNPaO3F4b-qsIEjOfU3Tp4bKk54JN2wzTCVDhE
---

![](https://lh6.googleusercontent.com/TLkLMvzALcncoyVu5MGEumqmlOqk7KWADtRJ8Uj62TXUWi_SZg_gw9iiF9hVi_vgMp55Jvpy5Bl0d_ZxOcmJfZnEALbmRDkcrfbNPaO3F4b-qsIEjOfU3Tp4bKk54JN2wzTCVDhE)
**Rekt-косилка знает, как заставить людей говорить.**

В самом конце, когда TLV приближается к нулю, а просадка становится невыносимой, в чат заходит безликая фигура.

Когда протокол смертельно ранен, и пришло время сваливать из этого бренного мира, появляется четвертый всадник Апокалипсиса в формате .gif, чтобы провести его в загробную жизнь. 

**[Compounder.finance](http://compounder.finance/) подвергся рагпулу, который стоил ему $12,000,000.**

В нашем непостоянном сообществе жадность и отчаяние наказываются и награждаются в равной, но непредсказуемой степени.

Здесь у грешника есть надежда, что его проступки забудутся, когда он под покровом анонимности сбежит из чейна.

Тут на сцену выходит Rekt, чтобы дать грешникам возможность исповедаться - рассказать о своих методах, чтобы мы все могли поучиться. 

**Compounder.finance мгновенно удалил свой сайт и Твиттер.**

**Нашим детективам больше ничего не оставалось, как проанализировать полный аудит безопасности.**

В штаб-квартире [RektHQ](https://twitter.com/RektHQ), сейчас много работы, и прежде чем мы начали расследование, прошло несколько часов... Когда мы связались с аудиторами и попросили их прокомментировать это дело, они были нам совсем не рады.

![](https://lh4.googleusercontent.com/j_yn7CTMvy6RhjtNHFw7jRwsT0Eossl9zY3lzlm5Uq-hxz2AE-V1Zf97vT11BfwAU-HH1YVRhIEfA6YqwHpDAaSA_dVNpY_VoSvGcUgGXyRdHVVqVOX03YWiJ1AWkK48OKTX6Nsf)

> **_Пожалуйста, не посылайте мне такую фигню про смерть, на минуту я действительно испугался за свою безопасность. У кого нервы послабее может и пожаловаться на такое или еще что в этом роде._**

После того, как наш детектив немного успокоил их, Solidify.finance предоставили нам полный [лог чата](https://solidity.finance/audits/CP3R/ChatLogs.pdf) их переписки с compounder.finance.

![](https://lh6.googleusercontent.com/jmSOsLERtND5cPjpj5zRKXEsyPg-vqXNGixs02ru1ZYLSMTjxSN4S8ZtDflMFHiI4ImG7ou-B6XA6P201hR94CjS09-Pk7rVkQ2WR4mu0u8SIpjnXx2FPXr99UBJMc8phplKmMlk)

К нам обратились и другие пострадавшие, и показали ранние переписки с админами compounder, в которых высказывали свои опасения.

![](https://lh5.googleusercontent.com/-wS-a_Bpwg90_-BScXqJTSVhYm1nsNF2WyFBwrTUUslw-wy4eYm_t2cb0LUCwny5jLWGmfJZNN6uDQxSkcbJVOakKBpJJMjXaWr9mLxrhxxFkm_SY_gWUfFq15bg3TUft-UlUBsl)

Solidify.finance нам сказали, что они уже кратко переговорили с админами. Они действительно проводили аудит контракта. Но они написали в отчете, что несмотря на контроль пулов таймером, но тот не обеспечивал никакой защиты. 

Следующее сообщение взято из логов их чата. 

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/12/image.png)

На этом этапе нашего расследования solidify.finance все еще были подозреваемыми.  Мы хотели узнать, почему они посчитали, что  команде compounder.finance «можно доверять».

![](https://lh3.googleusercontent.com/zAnDE5lhy4th23b04O90LfyMOzuZNKVQpGJSbvm1l9nyik3ALWHNN9w2ESpA9vVgbhUr4mG8RKoWHJs9vA-xxlg5tSHWy0cdYedy26u46htRO2F6DM6ueioCBHkqYyA336fkbeNY)![](https://lh4.googleusercontent.com/3cTLMXUqzGK79tC0tquzA-fJHOgDMyfrNrJywsKGRyCvSNUPI6C097QgqvUeOBASoWAnvVnx4GGcYpkJgD2rHxcrc9uBkkoToqtqzn1DNBOlmBmk6gP-ueO1kwfyQtYjfYerCmsK)

Просматривая логи чата, мы заметили, что там осталось одно имя пользователя - «keccak». Все остальные учетные записи были удалены. 

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/12/image-1.png)
![](https://lh6.googleusercontent.com/2Rer5ONASpGduNUGsKPIG7WjVnvSk0qldLQC3qKVl1GaC8H9eTkAEuwRxApHZV1-eRNs4z18n2lRWjM9_aKDwDjunZPqkUIn2cUh1APe3MTSUnpjhd1YkInL0NMzc9L391CWpNtN)

Solidify.finance сказали нам, что keccak удалил свой аккаунт. Но мы уже нашли его и пытались войти с ним в контакт.

![](https://lh4.googleusercontent.com/n843mEGRcOHYLt5WsOuC5CpMrwAyICOJ9Mj92qHGWjSUko2CSgUhwsRMQhTKUNj0mQnFebVnlX3GXJ9J6aEErSbqYIf0nAAjR7SargO3_dm1xuUIRiLP3mHlF23pxpMjVqZ-Bk6B)

К сожалению, Vlad не захотел говорить по телефону, поэтому мы послали ему сообщение, не надеясь на ответ.

До тех пор, пока...

![](https://lh6.googleusercontent.com/iCjWb4HeUCo8uB3eZLfksQFxFJdMEruvDsRzzFmwqYZcDzlXOePo-OmTAsbF1HMT89YxccN-Xs1pGl39sI8B4V4HkKx5EDMqSMxLLqiahIAcE9urNAvJUfcMbqAYSGuzEEOpnt2U)

Vlad был готов к разговору. К сожалению, он не очень нам помог.

![](https://lh6.googleusercontent.com/HE93DRIaDmYVHG4436QTGIPxZKsXJ0Ly4UXIojAKIPrpapwfQUyEJofxc4X2hZqyTwRkVnRALWfghAwR_BzCD6r0rPK1JQ-nQ5N2zpKhaLJuKVe8WYRj81PdojtL9oV9X9g4a75t)![](https://lh5.googleusercontent.com/KnQgeeZ8ui5i0loOefPMXBmxwqOOWX0cJB9TZCWAmE9Mt1COguIZB9C8v6D3niEhzCNJuCbj68G0L5eslhSSa83M3XKpLAxSRJ-PUftnrtbN1sLy3fUCmM6JfCUYiySLc9d5wejK)

С Vlad / keccak все еще можно связаться в Telegram, по имени пользователя @keccak, но он больше не отвечает и уже удалил изображения из аккаунта.
Мы прилагаем его старые аватары, чтобы у вас была полная информация и для вашего собственного расследования.

Нам сообщили, что - _Это волк из знаменитого украинского мультика на русском языке, который говорит: «ты заходи, если что»_

_Слева плакат с анти-пропагандой ядерного оружия._

К сожалению, пострадавшим пользователям это мало чем поможет.

![](https://lh6.googleusercontent.com/-C_fEe5K7VtTZBgWbN1x0T08gdPgA644Vf_UlKT7ZpIwM8Yvg0-VF_NbIlm3B6aPfgFVcicuLn60v12XKHvN0IMPukME0JQS1wO15OBo0mG00qKujj9N8rM3dFCpkOZ5HTZVvR2q)

**Как только стало ясно, что Vlad не будет с нами говорить, мы наведались в официальную группу Compounder в Телеграм. Там нам стало понятно, что наша репутация бежит впереди нас.**

![](https://lh6.googleusercontent.com/Bgibey9mMbZwxbZvLI3RpEsUKgqENRRGjySROwVuypAQaVeNqCnW4ZjPLOyXkLuzFDdAFs0UOXCVjeRdgZhrC3Fwaemg-0Jjfb0QSDBzvcDI_xggCXfFiRg52tqg3GwHIRQ9Qz6d)

Промотав чат, мы увидели все типичные признаки поведения людей после только что выдернутого из-под ног ковра.

![](https://lh6.googleusercontent.com/3NDRvDXQyKMx7QH_4iiJs6BwoganIn8R0YE0fqk1z0MH8cRljLJwu8hUBaj_HYldnAuLBU1cP9yw6mEOuWfesjjBnhzs4UVDbZ3QjI9EWV7RdifLXikt3fy5jsB2IOoNy2dZNd9D)

**Даже крупные игроки робеют перед мощью рагпулов. Вот этот [лидер группы](https://twitter.com/defiyield_info) потерял $1,000,000 и создал свою собственную [группу](https://t.me/compounderopsec) для расследования (686 участников) в попытке возмездия.**

![](https://lh4.googleusercontent.com/NymcDlq36Hf0ZJWBbN4BDjIlBI4rHhOTYmDMYGgvSNYjFLYG_Y6VWgubCqj9FTl7_AjBfx3uji0gstUdJkec4jTgzNPZT6lqT88cEj11ZchK9X8yPaNP7YTNmmif0D2ps8pkyR8T)

Ветка обсуждения находится [здесь](https://twitter.com/defiyield_info/status/1333731633393004545?s=20).

**Статистика**

В ходе нашего расследования **мы представили Solidify.finance нашему сотруднику [@vasa_develop](https://twitter.com/vasa_develop) из Stake Capital** и попросили их вместе поработать над созданием полного постмортема этого инцидента.

Следующие данные взяты из их [отчета](http://simpleaswater.com/cp3r).

**Украденные активы (8):**

- 8,077.540667 завернутых Ether ($4,820,030.07)
- 1,300,610.936154161964594323 монет yearn из yCRV Vault ($1,521,714.80)
- 0.016390153857154838 монет Compound (COMP) ($1.79)
- 105,102,172.66293264 монет Compound USDT ($2,169,782.85)
- 97,944,481.39815207 Compound USD Coin ($2,096,403.68)
- 1,934.23347357 Compound Wrapped BTC ($744,396.89)
- 23.368131489683158482 проценты Aave от YFI ($628,650.174379401)
- 6,230,432.06773805 Compound Uniswap ($466,378.99)

**Кошельки с фондами после рагпула**

- [https://etherscan.io/address/0x944f214a343025593d8d9fd2b2a6d43886fb2474](https://etherscan.io/address/0x944f214a343025593d8d9fd2b2a6d43886fb2474)
- 1,800,000 DAI
- [https://etherscan.io/address/0x079667f4f7a0b440ad35ebd780efd216751f0758](https://etherscan.io/address/0x079667f4f7a0b440ad35ebd780efd216751f0758)
- 5,066,124.665456504419940414 DAI
- 39.05381415 WBTC
- 4.38347845834390477 CP3R
- 0.004842656997849285 COMP
- 0.000007146621650034 UNI-V2
- Начиная с того момента, как в Deployer были впервые [переведены средства через Tornado.cash](https://etherscan.io/tx/0x2fc406e07328e04022b555b5cab69bc932d29d1115eca3d121cbd49da90fb817) и до рагпула Deployer послал ETH на 7 разных адресов. Большинство из этих платежей были одноразовыми. [На один из этих адресов](https://etherscan.io/address/0x8f332c9ffb2be270d5c1c0de3fdac3d993517593) пришло 4 разных платежа в ноябре: 19-го, 20-го, 22-го и 23-го. Большая часть средств с этого кошелька в итоге оказалась на  [другом адресе,](https://etherscan.io/address/0xd6c35c1828a7062e21468768c546a64dd1be1602) содержащем больше 1 миллиона KORE (до того, как он совершил рагпул, существовало всего 10k KORE).

Главным(и) виновникам(и) этой атаки были 7 вредоносных контрактов Strategy, которые были добавлены в кодовую базу после аудита. 

Не-вредоносная функция withdraw(), получаемая от контракта Strategy выглядит примерно так.

![](https://lh5.googleusercontent.com/t_BQNl6cnQmq98OvUsKf63yo8N93mJWbEOimWOmpkk8RyQHiOCXnBd7Q5iNRRzXZuemKX9vQ66bysjBdZFxaSClpp_jPERv2b6rH7XDgewnUUI6GWJrMEORb7S1339TOjV7nc8uL)

Обратите внимание, что там есть несколько проверок: 

![](https://lh5.googleusercontent.com/ZKGym0FbW_OC44MliLLqmvMJjbr2RanORW_G8pcdXTnWby52DXxayqpkIXFeJOEtpxbRZdncWo7yzSXyyAIsRmtF1kDXh1MAPS6-LmHqyOgt3Cuh_3s0dA1nJAbzEzmmQpYip2LV)

В 7 вредоносных контрактах Strategy эти проверки отсутствовали. Это дало контракту Controller (который был под контролем [«strategist» рагпулера](https://etherscan.io/address/0x079667f4f7a0b440ad35ebd780efd216751f0758)) возможность вывести активы из стратегии.

(Обратите внимание на отсутствующие проверки во вредоносной функции вывода на изображении ниже) 

![](https://lh4.googleusercontent.com/LX2pt7hp6dieDg5bU-6hMQkIFeAh9ZCABSIADVQZ62Y6OXcF6lRk6eAWuYog5Hlz2GP2_o5tNmDhbKHF0bEYr1vjHRoOPCXn03Gdq-uyiSgushapH-slIkt87Dl7BSQC5QRHw0ou)

Всю операцию рагпуллинга можно разделить на 4 шага.

**Шаг 1**

[Compounder.Finance: Deployer](https://etherscan.io/address/0x079667f4f7a0b440ad35ebd780efd216751f0758) развернул 7 вредоносных стратегий с управляемыми функциями withdraw().

**Шаг 2**

[Compounder.Finance: Deployer](https://etherscan.io/address/0x079667f4f7a0b440ad35ebd780efd216751f0758) Установил и Подтвердил 7 вредоносных стратегий в StrategyController с помощью транзакций Timelock (24 ч.). 

**Шаг 3**

[Compounder.Finance: Deployer](https://etherscan.io/address/0x079667f4f7a0b440ad35ebd780efd216751f0758) (strategist) задал параметр inCaseStrategyTokenGetStuck() для StrategyController, что вынудило управляемую им функцию withdraw() во вредоносных стратегиях перевести токены из стратегий в StrategyController. Сделал то же самое во всех 7 вредоносных стратегиях.

**Шаг 4**

[Compounder.Finance: Deployer](https://etherscan.io/address/0x079667f4f7a0b440ad35ebd780efd216751f0758) (strategist)  задал параметр inCaseTokensGetStuck() для StrategyController, что перевело токены из StrategyController на адрес [Compounder.Finance: Deployer](https://etherscan.io/address/0x079667f4f7a0b440ad35ebd780efd216751f0758) (strategist). Теперь [Compounder.Finance: Deployer](https://etherscan.io/address/0x079667f4f7a0b440ad35ebd780efd216751f0758) (strategist) полностью контролирует 8 активов стоимостью $12,464,316.329.

После этого активы были переведены на разные адреса, перечисленные [здесь](https://www.notion.so/Compounder-Finance-Post-Mortem-Report-9bf6b17dc1304606bb975968039a6dc8).

**Отличная работа от** [**@vasa_develop](https://twitter.com/vasa_develop)**.

**Если вы разоблачитель, кибер-сыщик или детектив, специализирующийся в Etherscan и вам есть, чем поделиться, свяжитесь с нами.**

---

![](https://lh3.googleusercontent.com/4Ov6KyZOXXKLhn3ia1GsHXTlqJrJufMyscsMjjs8Ndd7OF6aVv6ULbfwodnZRZN_00m-iF4Bd3IZgCy4_z29XT8544n1sPjSd3COIRottpQgTgZ-1eF9jcJ75U6bBoveI6cSlg5g)

**Судный день:**

Кто виноват?

После проведенного анализа **мы знаем, что это не аудиторы.** Они добросовестно выполнили [свою](https://solidity.finance/audits/CP3R/) работу, убедившись, что Compounder.finance защищен от внешних атак, и к тому же озвучив свои опасения в  аудиторском [отчете](https://solidity.finance/audits/CP3R/) и в [чате TG](https://solidity.finance/audits/CP3R/ChatLogs.pdf).

Может быть, им стоило бы озвучить эти опасения чуть погромче, но в итоге вся ответственность всегда лежит на вкладчике.

Compounder.finance использовал timelock как индикатор того, что они не станут делать рагпул. Теперь мы знаем, что этому методу нельзя доверять. Если он используется, то нужно установить автоматическую систему предупреждения или панель управления, чтобы следить за транзакциями на этом адресе.

24-х часов, по-видимому, недостаточно, чтобы предупредить пользователей о необходимости вывести средства.

**Не все проекты, где основатели анонимны, являются аферами. Вся эта индустрия была основана анонимом.**

Однако, почти все мошеннические проекты были основаны анонимами. Нам как сообществу нужно опасаться таких проектов; особенно тех, которые используют источники фондов, которые нельзя отследить. Как например Tornado.cash.

**Само по себе наличие аудиторского отчета недостаточно, чтобы обеспечить безопасность проекта и законность.** Аудиты часто фокусируются больше на рисках от внешних атак, чем от внутренних. Возможно, в этой области аудиторам стоит усовершенствоваться. 

Даже при наличии аудитов, таймеров и сжигания ключей вкладчики всегда находятся во власти других пользователей, которые могут в любой момент слить огромное количество монет на рынок. 

![](https://lh5.googleusercontent.com/m44dt8mlCqX_pt-Pm7xDUEJJFvZ78tpUndfyCPqpOfsz40B0i8siXxY_TnFHZIati3P8IPlKtrsn4urG_lCY66X5hRagresLo5uRqwIbuDpkHW4-2C0ar1TOG7lqrpLvBCFK6MlF)

**Solidify.Finance: Официальное заявление**

_Команда протокола The Compounder заменила безопасные/прошедшие аудит контракты Strategy на вредоносные контракты «Evil Strategy», что позволило им украсть пользовательские фонды. Они сделали это с помощью публичного, но полностью не управляемого 24-х часового таймера._

_В нашем аудиторском отчете и в переписке с командой C3PR мы затронули проблему централизованного контроля в их руках.  Во власти команды было обновить стратегию пулов, и в данном случае они провели его с намерением украсть фонды пользователей. В целях прозрачности мы открываем доступ ко всем логам наших переписок с командой C3PR [здесь:](https://solidity.finance/audits/CP3R/ChatLogs.pdf)_

_Исторически так сложилось, что наши аудиты всегда фокусировались на рисках для проектов от внешних атак, включая дискуссии о рисках с командами проектов, как в этом случае. Мы воспользуемся этим печальным событием как возможностью научиться на наших ошибках. В дальнейшем мы будем предоставлять больше солидных деталей на легкодоступном языке касательно рисков, вытекающих из контроля разработчиков._

![](https://lh4.googleusercontent.com/9YXkVrtF4HWEpH_Wyf9N7T6ttzQGR7m-Dfg5At40sFJV4Rz0FbF_7FLEn_E5SM2D6HSeG7iymcg7T9DSLJkBP8SSCL0EuTWdiia6nnGhXD1vy-4ChPhbQh_seYfFHXRb94Wh1ILc)

Мы все знаем, что нужно читать смарт-контракты, прежде чем инвестировать, но языковой барьер очень высок. Не все знают, на что нужно обратить внимание, а те, кто знают, не заинтересованы делиться своими находками.

В случае с C3PR те пользователи, что прислушивались, с самого начала знали об опасности.  И код, сделавший рагпул возможным, всегда там был. 

Несмотря на это, в контракте накопилось больше $12,000,000, и теперь это один из самых больших рагпулов в истории.

![](https://lh5.googleusercontent.com/5GlWMNDDXxJnsVsr0MxTgGKLmHwwlEjF7ufbN7LefUMdNaGsPDSCExLRHjavO4Vg4lQkR_wzRNF4jFxOqH6v4BsMmFUS7UXF_wMyR8S1xdjGVloDBVwR-bS6EZ1bBnPDFtXDvdMt)
