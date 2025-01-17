---
title: Барсуки в берлоге sushi
date: 26 января 2021
tags:
  - sushi
excerpt: Басруки всегда ходят по одним и тем же тропинкам во время своих ночных вылазок за едой. Поэтому в лесу появляются хорошо проторенные тропы. Если на привычном пути возникает какая-то помеха или препятствие, это сбивает животное с толку. В итоге им приходится спариваться не с тем партнером.

banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/header-3.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/header-3.jpg)

**Басруки всегда ходят по одним и тем же тропинкам во время своих ночных вылазок за едой. Поэтому в лесу появляются хорошо проторенные тропы.**

**Если на привычном пути возникает какая-то помеха или препятствие, это сбивает животное с толку. В итоге им приходится спариваться не с тем партнером.**

Мы получили тревожный сигнал о сделке, в которой [опытный пользователь DeFi](https://etherscan.io/address/0x51841d9afe10fe55571bdb8f4af1060415003528) трансформировал 0.001 в 81.68 ETH с помощью токена [DIGG](https://www.coingecko.com/en/coins/digg) проекта  [Badger DAO](https://app.badger.finance/).

Изучив поподробнее, мы выяснили, что хотя атака и имела место быть, но утечка уже устранена. То, что воспринималось как угроза всему протоколу SushiSwap, оказалось лишь смышленым падальщиком, который подобрал объедки.

**Уже ранее замеченный кошелек воспользовался брешью, которая вновь зазияла из-за забывчивости команды SushiSwap.**

**Эта транзакция показалась нам подозрительной на первый взгляд. Но, поговорив с командой Sushi, мы поняли, что особого повода для беспокойства не было.**

Вот что представляла собой эта [транзакция](https://etherscan.io/tx/0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b). SushiMaker попытался перевести 0.05% комиссии с обмена DIGG/WBTC (за ~24 часа) через пул DIGG/ETH, в котором было мало ликвидности и высокое проскальзывание. В результате провайдерам ликвидности пары DIGG/ETH пришлось заплатить несоразмерную комиссию.

Эту комиссию предполагалось выплатить холдерам XSUSHI, но вместо них ее получил хакер.

**Как ему удалось?**

Решение проблемы было найдено несколькими неделями ранее, но его нужно было встроить вручную в каждый пул. Во время работ падальщик и пробрался внутрь и забрал комиссию, предназначавшуюся холдерам xSushi.

**Когда новые пары добавлялись в программу [Onsen](https://sushiswap.fi/onsen) протокола Sushiswap, были добавлены и несколько пар без Эфириума. Но конкретно в случае  пары DIGG/WBTC для нее не был создан “мост” в SushiMaker.**

SushiMaker это смарт-контракт, который собирает 0.05% комиссию с трейдинга и позволяет перераспределять её между пользователями, которые отдали в стакинг SUSHI в обмен на xSUSHI, чтобы получать дополнительное вознаграждение в SUSHI не теряя времени. 

По умолчанию SushiMaker продает накопленные сборы (и их пары) в ETH, а затем в SUSHI.

Мост означает, что, когда SushiMaker продает сборы какого-либо актива, не используя ETH-пару, то он может продать их любому активу вне Эфириума, который может присвоить себе ликвидность.

Если моста нет, то может быть добавлена ликвидность с целью создания ETH-пары, с помощью которой SushiMaker будет пытаться конвертировать сборы с этого актива и как следствие пострадает из-за высокой цены из-за маленького объема ликвидности. 

**Как следствие, сборы, накопленные в контракте SushiMaker, пойдут на вознаграждение провайдеров ликвидности этой ETH-пары, но не владельцев xSUSHI, как изначально предполагалось.**

**К счастью, никакие соответствующие позиции провайдеров ликвидности или xSUSHI не пострадали. Потеряна только прибыль с актива за предыдущий день (0.05% сборов со свопов DIGG/WBTC - 81 ETH).**

Для решения этой проблемы держателей xSUSHI в контракте мейкера был установлен мост для DIGG-пар. Этот мост также интегрирован в SushiMaker.

**Дискуссия в дискорде SushiSwap дала нам более четкое понятие о механизме атаки:**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/1.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/2.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/01/3.png)

**Мы проанализировали адрес падальщика и выяснили, что он - известный пользователь ботов и флэш-кредитов.**

![](https://lh4.googleusercontent.com/mbHCt8MYOKLIbVMR8ZEUaz0LHxerb8pKXbTDahY_U_KS_IocDL9ymBER2j0VVVHSIAQQLKb7mc3XorPJV382OJK0KUFe1rvEQcr4-3zJqOg_t435UtQzUtwjB_UGGgODeEsgWbCg)
![](https://lh4.googleusercontent.com/KLD2d5wTEfMmuh5P7IBIy4k17OMfA4UGgnNSZQ38roXBLH4-8DDMlLEc_9KNs4YIHTSkzh3sVdHsSHR_c-RZYTwBfqbwzKUF6yUJ-UjP5y1c0mQpmgyRTl_0McCU1lrNgKrJH-zC)

Данные с [Nansen](https://nansen.ai/)

Мы нашли несколько транзакций, которые говорят о том, что вот [этот пользователь](https://etherscan.io/address/0x51841d9afe10fe55571bdb8f4af1060415003528) пытался воспользоваться брешью и украсть комиссию, причитающуюся провайдерам ликвидности.

[0x90fb0c9976361f537330a5617a404045ffb3fef5972cf67b531386014eeae7a9](https://etherscan.io/tx/0x90fb0c9976361f537330a5617a404045ffb3fef5972cf67b531386014eeae7a9)

[0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b](https://etherscan.io/tx/0x0af5a6d2d8b49f68dcfd4599a0e767450e76e08a5aeba9b3d534a604d308e60b)

[0xcec93808a657d00cbb0245711e9419d0ea278b3a60a9a6d0a8c3353523c0e982](https://etherscan.io/tx/0xcec93808a657d00cbb0245711e9419d0ea278b3a60a9a6d0a8c3353523c0e982)

[0xe0527f7befaea54257113a09c8b3f4cd416e11a0e196cd2ba2e5e07c47767ddf](https://etherscan.io/tx/0xe0527f7befaea54257113a09c8b3f4cd416e11a0e196cd2ba2e5e07c47767ddf)

---

**Могла произойти катастрофа, но обошлось лишь небольшим позором для команды SushiSwap.**

Несмотря на то, что хакеру удалось провести свою махинацию, мы можем считать, что для SushiSwap это был предупредительный выстрел. А им на данный момент доверено защищать [$1.9 миллиарда TLV](https://defillama.com/protocol/sushiswap).

В обсуждении в Discord говорится, что они не будут автоматизировать это исправление. Вместо этого они будут как и раньше стараться не забыть применять его каждый раз. Это настораживает.

**Зачет допускать возможность человеческой ошибки, если в этом нет необходимости?**

Даже если код децентрализован, разработчики берут на себя огромную ответственность, работая с протоколами с таким огромным объемом активов. Последствия стресса часто недооценивают, и мы знаем, как много разработчиков становятся жертвами эмоционального выгорания. Во время написания кода много чего может пойти не так. Поэтому, может быть команде SushiSwap стоило бы немного больше полагаться на автоматизированность в данной ситуации.

**Эта история служит напоминанием о том, что протоколы находятся под постоянным наблюдением хакеров и арбитражеров. Те следят за каждым их движением и пытаются залезть в карман или полностью вырубить.**

Тем не менее, эта проверка работает в обе стороны: даже такие любители из Твиттера как “simp2win” могут распознать хакера издалека. Это очень похвально, но лучше бы 791им предоставить анализ экспертам.

Мы любим хакеров, которым есть что сказать. Поэтому нам было приятно получить следующее сообщение через [Ethereum call data](https://twitter.com/EtherText/status/1354078163022868481?s=20).

[**_Почему этот чувак simp2win написал в твиттере, что я заработал 10 миллионов? лол, хотелось бы._**](https://etherscan.io/tx/0x48963b96df0949a893401635b0900064aecae780ec0950cbbd4122005eb4e14a)
