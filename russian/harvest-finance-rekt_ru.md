---
title: Harvest Finance - REKT
date: 26 октября 2020
rekt: 
  количество: 25000000
  аудит: Haechi, Peckshield
  дата: 26 октября 2020
tags:
  - harvest finance
  - флэш-кредит
  - взлом
excerpt: Урожаем косилку не остановить. Талантливый фермер воспользовался флэш-кредитами, чтобы накосить 33.8 миллиона долларов в пулах FARM_USDT и FARM_USDC.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/10/reaper-3.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/10/reaper-3.jpg)

**Урожаем косилку не остановить.**

Талантливый фермер воспользовался [флэш-кредитами](https://etherscan.io/tx/0x9d093325272701d63fdafb0af2d89c7e23eaf18be1a51c580d9bce89987a2dc1/advanced#internal), чтобы накосить 33.8 миллиона долларов в пулах FARM_USDT и FARM_USDC.

В смутные времена некоторые обращаются к священным писаниям за наставлениями на путь истинный.

Из десяти казней, которые уничтожили урожай в древнем Египте, первым было наказание кровью, а второе - жабами.

Барон Ротшильд советовал покупать тогда, когда на улицах льется кровь.

Теперь, когда пьянящие дни лета DeFi прошли и объем ликвидности у DFI-PERP оптимистично растет, поведение более Просвещенных Фермеров стало совсем не христианским.   

Исход 8:2-4:

> _«Я поражаю всю область твою жабами; И на тебя, и на народ твой, и на всех рабов твоих взойдут жабы.»_

В нашей криптографической мета вселенной разработчик - это раб. Как и было предсказано в древних писаниях, разработчики Harvest Finance с ног до головы все покрыты лягушками. 

![](https://lh4.googleusercontent.com/EEKvX8W_B4lZHA9MSaEJA9qThrhZa6rh-AoQOczdOT6lSxVwJ4F9O1tY4uUSdJ0-xuv7VGP9Mo89i63_LF-W-Rqgq28qoytLxTBpggpZeA4pz9ndUb1_jiN7itRThjNxu3MV33PU)

**Анализ арбитражной атаки**

fUSDT [упал на 13.7%](https://twitter.com/jiecut42/status/1320574109005348864?s=20), а $FARM [упал на 67%](https://www.coingecko.com/en/coins/harvest-finance) всего за два часа после того, как хакер взял флэш-кредит размером в $50 миллионов USDT. Затем он воспользовался Y-пулом Curve Finance, чтобы обменять фонды и непропорционально вытянуть цены стейблкоинов.

Подробный анализ транзакций [здесь](https://ethtx.info/mainnet/0x9d093325272701d63fdafb0af2d89c7e23eaf18be1a51c580d9bce89987a2dc1).

Выполнение следующих действий заняло 7 минут. Источник: [@valentinmihov](https://twitter.com/valentinmihov/status/1320667338321154048?s=20)

1. Обменять 11.4 миллиона USDC на USDT -> цена USDT повышается

2. Вложить 60.6 миллиона USDT в Vault

3. Обмен 11.4 миллиона USDT на USDС -> цена USDT падает

4. Вывести 61.1 миллиона USDT из Vault -> прибыль составила 0.5 миллиона

5. [Взять те же исходные и повторить 32 раза.](https://etherscan.io/address/0xf224ab004461540778a914ea397c589b677e27bb) (без какого-либо предварительного тестирования)

6. [Перевести в renBTC ](https://app.zerion.io/0x3811765a53c3188c24d412daec3f60faad5f119b/history)и выйти на BTC / [ETH ](https://etherscan.io/tx/0x5abe6f9b498471042f6c9f68c63fc3d84398b95a3a9e58c621cee09b3c972879)через Tornado Cash

Атакующий смог вывести больше USDT на четвертом этапе из-за того, что цена USDT изменилась. Так как цена USDT была ниже во время вывода, его доля в пуле Vault стоила больше USDT.

На лимит в 10 миллионов газа приходится примерно 4 цикла, и хотя прибыль с каждого цикла составляет меньше 1%, ~$500 за каждый повтор прибавляются быстро.  

Механизм расчета цены для депозитов и выводов LP стал причиной эксплоита. Это значит, что атака могла быть перенесена на пул renBTC, на пул FARM_TUSD и на пул FARM_DAI. Однако, хакер предпочел остановиться после слива $25 миллионов, то есть 17% от доступного содержимого в пулах FARM_USDT и FARM_USDC, но он легко мог бы продолжить сливать все содержимое пула, которое составляло $400 миллионов, если бы ему того захотелось.

Код стратегии FARM_USDT выглядит вот так

![](https://lh3.googleusercontent.com/3WZVjYk0XPg_KMkyG8owAtDZUdOPU_PlUaMwHSkl4IYQjAJTeS_yj96Gu0sHTlfukzmqtxdcMUfpVhfmZrAaw05ImW5ceVByqOuEyad2GevtkP0wb_lj_EuqRrI5PB6Su1nCh_vT)

Это значит, что был рассчитан определенный индекс цены.

Так как они уточняют в конце «tokenIndex», можем предположить, что они не просто используют get_virtual_price(), а вместо этого делают некоторые базовые вычисления. Источник: [Andre Cronje](https://twitter.com/AndreCronjeTech)

![](https://lh4.googleusercontent.com/RI7-hbXD-8H7Oi3O_mnwPND-Ik4LyPffaqYUX4C9AoT182ohHliSF-9YrArkfQem8CZhY95vlmkTQtIe9ttvxuwBPDSkdI55zYstQzIRThZEXpyFJiScbmtP4pwcHkF2qNvSrph6)

Значение толерантности функции проверки арбитража было недостаточно высоким, но трехпроцентное значение толерантности проскальзывания по умолчанию было слишком высоким. 

[Источник: PancakeBunnyFin](https://twitter.com/PancakeBunnyFin/status/1320615021588537347)

Не только сам хакер нажился на своих действиях.  Провайдеры ликвидности и разработчики Harvest тоже получили внушительную сумму денег, потому что хакер решил выбросить крошки ($2,478,549.94) в Harvest Deployer в виде USDT и USDC.

Harvest заявил, что эти деньги будут возвращены пострадавшим пользователям пропорционально их потерям с помощью снэпшота.

> Это не хакер. Просто обычный* сочный арбитраж на  $24M (0x53f) на [@harvest_finance](https://twitter.com/harvest_finance?ref_src=twsrc%5Etfw)
>
> Флэш-кредит стоимостью $50M USDC на [@UniswapProtocol](https://twitter.com/UniswapProtocol?ref_src=twsrc%5Etfw)
> 
> Обмен $11M (USDC/USDT) на [@CurveFinance](https://twitter.com/CurveFinance?ref_src=twsrc%5Etfw)
> 
> ~61M в Хранилище fUSDT
> 
> Обмен $11M USDT/USDC yUSDT
> 
> Вывод $61M с прибылью $0.5M
> 
> Повтор и отмывка на [@TornadoCash](https://twitter.com/TornadoCash?ref_src=twsrc%5Etfw) [t.co/nFTuyU3s6w](https://t.co/nFTuyU3s6w) [pic.twitter.com/2oXQ2PsY32](https://t.co/2oXQ2PsY32) &mdash;
>  
> Julien Bouteloup (@bneiluj) [26 октября 2020](https://twitter.com/bneiluj/status/1320686478486347778?ref_src=twsrc%5Etfw)

**Прибыль счастливчиков - провайдеров ликвидности**

Ниже приводятся примерные цифры. [Источник: Jiecut42](https://twitter.com/jiecut42)

Хакер - $24,000,000

Провайдеры ликвидности на Uniswap - $6,000,000

Разработчики Harvest - $2,500,000

Провайдеры ликвидности Curve - $1,000,000

Газ Ethereum - $100,000

Комиссия RenVM $20,000

![](https://lh6.googleusercontent.com/O91Z60MeY81zTI2Lu6g3OAAxdJec9tJjcWcY6rbgRPZYW-i8tShq44_XVuhbx2oUao-CsKSqzhPYyHHZRSbvuMrIUwGeOd2npe4Z7KXOox7S_NKK95IEx6ooqh_5MlN8qgtizZu0)

Источник этого сладкого пирога: [BitcoinWhiskers](https://twitter.com/BitcoinWhiskers)

Имея доступ ко всем пулам [Curve](https://www.curve.fi/), держатели veCRV получили прибыль от прохождения дополнительного объема средств через Curve, так как хакер сгенерировал ~500 тысяч долларов комиссии с трейдинга, которая будет поделена между  всеми, кто делает стакинг CRV. Прирост сборов по трейдинговой комиссии Curve составил больше 8,000% по сравнению с днем накануне того, как хакер [обменял](https://etherscan.io/tx/0xb460b70f11a93364fecf1f3c3ec49f053aecd2d6d9912c012170aa7a0de2d526)свыше $100M на USDT и USDC.

![](https://lh4.googleusercontent.com/P9kpiXDdXJYtJTO1byo7ylD8Ht4_vJNDbSZZtUcG2MzXflb5VxaW634Su-jKF3W9yNKAeJ49BKnQjiaPBYy3w018NmCpTXJ2bcK9kjniEy6E2hENqHwYk2yJebULie9UzMaFm55m)![](https://lh4.googleusercontent.com/Az3qJ6dKLbNiXRkUOshi9tgw5Qg0WcRbxF2KhGoxT4GJQ4dOdLT_CpGK6fFkwHHsrnfN0mhcTIZaBdRq-QYWqH7_bCWft16ow-zNO7R0i6YGTBdQGjysjheUKSbZjCJ8V0cyOSws)

У провайдеров ликвидности Uniswap тоже был урожайный день благодаря работе этого анонимного супер фермера.  

Общий объем торговли Uniswap подскочил с $148 миллионов до $1 миллиарда за 24 часа.

92% этого объема поступило от пары USDT/ETH и USDC/ETH, создав  $5.76 миллионов гонораров для провайдеров ликвидности.

![](https://lh3.googleusercontent.com/fZW3t_eeYeEjsBaluQwSbmHCc2ZP7H5PNBeFUvw0uSxxJqwNs4mL6UvIKWTWGHZ_7rLGpMuveEAzJ_GVLNJbEZOfRi9S8zYV7BWyknpQCgctrsomzLm4Dzbi6qNwuzbzG8gOFGeI)![](https://lh3.googleusercontent.com/T9IWn6M9JIV_82qkS-t6SC9iSOK6r1TNWO6aBCRerRNaxKXZso62bpGa5vypvVvQaUEfgIcLRkZ5QLoBU3ibErYg4cUDmb7p6CpGjR1NFVQHdtEzXy483uACgcJ-_RQMFfelFO-s)

Источник: [Larry Cermak](https://twitter.com/lawmaster/status/1320614508772163584?s=20)

**Конфиденциальный источник**

Разоблачение и защита наших источников составляют огромную часть нашей работы в Rekt. Пока наш автор писал эту статью, с нами связался один человек по поводу информации о том, что делал Harvest Finance за несколько дней до событий прошлой ночи. 

Следующая ниже информация дана без комментариев.

> _Со мной связалась команда Harvest Finance, им нужно было сотрудничество по продвижению пулов ликвидности для двух классов активов._

> _Первый класс был BTC, не требующий доверия, второй класс  был FARM/ETH._

![](https://lh5.googleusercontent.com/BI91M7nD8yCLZuJtX0Tpas4RCBD8xnGWl2LrRu4PTbO_CrQUDP2GDuhR45vrUpnOSc-hxuvuKTZ76DT8U58QVgvFxa7CNkQL2KXINn1Hsxw7csVd2b3VYOp8Mhw9_tM-fD58ZFOp)

> _Я решил не продолжать работать с ними, потому что что-то меня отталкивало._

> _Я не говорю, что дело в команде Harvest, но когда я увидел, что проскальзывание в смарт-контракте составляло 3%, и что эксплоит был направлен на бездоверительные биткоины, что само по себе «новинка»..._

> _Я думаю, что если это не Julien, тогда это сами Harvest Finance, или хакер EMN, или кто-то, хорошо разбирающийся во флэш-кредитах._

**Запрос на возмещение ущерба**

Как обычно, возник спор о способности протоколов блокировать или исправлять подобные действия в будущем. В группе Telegram  протокола Curve некоторые высказывали мнение, что Curve должен иметь возможность блокировать подобные действия, однако действующие смарт-контракты [нельзя остановить](https://twitter.com/CurveFinance/status/1320694100090376193?s=20) или модифицировать.

Также прозвучали призывы в сторну renBTC, чтобы они возместили гонорары, которые заработали благодаря действиям хакеров. Это спорная тема, которая заставляет пользователей взвешивать «за» и «против» использования децентрализованных протоколов.   

**Пренебрежение безопасностью**

Всего три недели назад, 6 октября, Harvest Finance опубликовали [обновление безопасности](https://medium.com/harvest-finance/week-6-update-security-rules-everything-around-me-62a681a3692a) в котором говорилось, что они обеспечивали безопасность своей территории посредством «тщательных аудитов безопасности», проводимых компаниями [Peckshield](https://twitter.com/peckshield), [Haechi Labs](https://haechi.io/) и [CertiK](https://twitter.com/certik_io).

Следует отметить, что Peck Shield и CertiK проводили аудит Bzx перед тем, как те подверглись трем взломам ранее в этом году.

Мы ждем их комментариев об этой ситуации.

Разработчики и кажется даже специализированные охранные организации не привыкли брать в расчет влияние флэш-кредитов на свой код.

Мастерски управляться с флэш-кредитами это как участвовать в рыцарском турнире XII века на Харли-Дэвидсоне с АК-47 наперевес; никто этого не ожидает, плебеи получают rekt и проходят годы, прежде чем  необразованные массы могут защитить себя от таких экспертов дикой торговли.

Harvest Finance ответили на случившееся в славном пассивно-агрессивном тоне.

![](https://lh6.googleusercontent.com/R_kCRELgxVg20qoViEkHb43yiEoWnuslyOQJaPlG0djFHM8FAJEumBYLQP-URiPun5EdcOpKhBOLGHmsi0h36Z6-LdRxFKwD9ABzrFezDcLcNLXtEPBc896I1HcwxfLHCuz5R9IF)

[twitter.com/harvest_finance/status/1320624369543057409](https://twitter.com/harvest_finance/status/1320624369543057409)

![](https://lh4.googleusercontent.com/kgpAOlAQRPTcNrx-HJzhDhO04Y9CttjxSfNJ3udyDNvVG5D75NbarZjK3aQ_76axChzA05kmDzDOlSyC9mFX98Odw1U5fSucvIw6zo7JOdjBjANdqm7WN-pac8GzxozyBjZQ6qWK)

**Правдивая терминология**

Арбитраж / эксплоит / взлом.

Разница между терминами становится все более размытой, в то время как тот факт, что «код это закон» становится четко ясным. 

Harvest Finance использовали термин «экономическая атака». Некоторые видят в этом преступление, а другие просто действия более способного пользователя, фарминг доходности с использованием современной техники.

Это меритократия или анархо-капитализм?

В любом случае это точно очень развлекает.

_caveat emptor._

> Только тот фермер, который старательно сажает семена весной, осенью собирает урожай.  [Б. Ч.  Форбс
](https://en.wikipedia.org/wiki/B._C._Forbes)
