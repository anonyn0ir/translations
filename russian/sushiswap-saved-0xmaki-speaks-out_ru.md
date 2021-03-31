---
title: Спасение SushiSwap - 0xMaki даёт показания
date: 29 ноября 2020
tags:
  - sushiswap
  - 0xmaki
excerpt: Из вока да в полымя: анонимный разработчик 0xMaki возглавил разработку SushiSwap после того, как основатель Chef Nomi позволил своей жадности жадности взять верх.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/header-6.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/header-6.jpg)
**Из вока да в полымя.**

Анонимный разработчик [0xMaki](https://twitter.com/0xMaki) возглавил разработку SushiSwap после того, как основатель Chef Nomi позволил своей [жадности](https://twitter.com/NomiChef/status/1304442495342796800) жадности взять верх.

После того, как лето DeFi прошло и фарминг фуд-токенов сошел на нет, многие смирились с мыслью, что SushiSwap мертв и похоронен. Однако, разработчики проекта не прекращали работу [ни на минуту](https://twitter.com/zhusu/status/1329932138171404290?s=20), и вот недавно SushiSwap вернулся с новым меню.

**いらっしゃいませ!!!**

Но все было не так просто в баре Omakase.

**Вчера поздно ночью неизвестный проковырял дыру в их смарт-контракте и стащил $15 тысяч, пока команда суши-поваров не выгнала его из кухни.**

Rekt обратился к 0xMaki за его версией событий. 

![](https://lh5.googleusercontent.com/bLAbz--dDRJoIQjlauDxi08j9x-pObms6J3_LmI2hhMGNs5kCYYxs-Dz13TsdF6IRgQ36NlQ-CiJpWUCZ9IVZaYGMju15bhw3vwVmG6WzAigF_sPkGojiOPjj6Ve3vdCiUJEOBZN)

**0xMaki:** После публикации отчета [Nansen ](https://research.nansen.ai/sushiswap-farming/) я сам управлялся в Sushibar, чтобы снизить возможности арбитража. Я видел парочку странных небольших транзакций. Но я решил, что ничего страшного в этом не было, потому что бар работал прекрасно.

Первая микро-транзакция произошла дня 2-3 назад, но вчера она стала автоматической, я бы даже сказал «промышленного уровня».

Вот первое [упоминание](https://discord.com/channels/748031363935895552/753626532500734014/782428289868365884) неполадок в Sushibar. ([Discord](https://discord.com/channels/748031363935895552/753626532500734014/782428289868365884))

**Monstar**

@0xMaki 源 義経 что происходит с суши-баром? Там полно всяких разных странных транзакций и похоже, что люди, делающие стакинг в баре не получают с него никаких суши.

[Транзакция 1 ](https://etherscan.io/tx/0x3534241a7354a8f9c8a9d0209730167a888d923b08c19c20623cd78637faadd0)

[Транзакция 2](https://etherscan.io/tx/0x3ffcfc9985622ad7cf0fdc2eb582ad7ce8bf9e9295fd7a4de44354fdd71a688a)

[Транзакция 3](https://etherscan.io/tx/0xc75a8ca881d4da75774f51006651c9946311d40145ce69d07aee3a85627153d6)

**0xMaki 源 義経** ответил Monstar

все работает как надо, просто сумма очень очень очень очень маленькая, насколько я понимаю

похоже, что кто-то потерял транзакцию, сейчас проверю 

**Monstar**

Я так не думаю

потому что доступный к выводу остаток в баре очень сильно упал из-за этих транзакций

такое впечатление, что они выводят сами токены провайдеров ликвидности (не знаю, как такое может быть возможно), вместо того, чтобы выводить sushi, как положено

поэтому нет конвертации в sushi и стейкеры не получают вознаграждение

**0xMaki 源 義経**

проверяем сейчас вместе с одним человеком

может просто приложение boring странно себя ведет

**Monstar**

я думаю, кто-то сообразил, как обойти приложение boring (изменено)

и не делиться суши ни с кем в баре

но я не знаю, как воспроизвести то, что они делают, поэтому не могу протестировать

да, точно

[https://etherscan.io/tx/0x7c6af5ca27ceb04aad514ddcaee8afc6dd4eb79d0816e24b007e7db205e93ce3](https://etherscan.io/tx/0x7c6af5ca27ceb04aad514ddcaee8afc6dd4eb79d0816e24b007e7db205e93ce3)

[https://etherscan.io/address/0x1925e832c22522e0d9947ee4677120b2f28e4cd4#internaltx](https://etherscan.io/address/0x1925e832c22522e0d9947ee4677120b2f28e4cd4#internaltx) здесь видно все выводы с этого кошелька (изменено)

**0xMaki 源 義経**

@Monstar мы работаем над решением проблемы на данный момент, все фонды в безопасности, просто обычный эксплоит суши-бара, забрали комиссию, отстой, но хороший баг-баунти

мы отдадим сегодня 10k в пользу клиентов Sushibar

---

**Rekt:** Спасибо за ссылку. Что первым пришло тебе на ум?

**0xMaki:** Сперва я подумал: ну невозможно же, чтобы с баром что-то случилось, правильно?! Должно быть, дело во фронтенде. Транзакция была бессмысленной. Но когда в бар перестали поступать деньги, я подумал, что, что проблема намного глубже.

Примерно через 15 минут я понял, что дело плохо и сразу же связался с [Banteg](https://twitter.com/bantg)

![](https://lh5.googleusercontent.com/2nOrhx84dL0WXXOLQy-RuEuZQo05qVC2rS7DtAYxQ207NRzWglhhEUhIO6dsES1F9ls81HYZINxkn5f2idaSXxlcgKuDDUVTe160boHCzME0RqL8Ci6R-gdZlcXTYl2Aj4jJStv5)![](https://lh5.googleusercontent.com/e9ULQE7bDt7_iZJyvYGz3oph9OzHxyilopiD0JmhhOv09ZfsJxtFS9ubho8a4eof3YflICXhptgZsU4ZhApjNGyYtpkEscsW7s8SOoG1pn120KB57RyRvZLu5yumbm9jz0hVPcPg)

Banteg не смог мне помочь, у него было 6 утра и он был занят работой над той штукой picke / cornichon. Все разработчики Sushi спали - они все в Европейском / Токийском часовом поясе, я один в северной Америке. 

**Rekt:** К кому ты обратился за помощью?

**0xMaki:** Мне смогли помочь [Andy ](https://twitter.com/andy8052)a специалист по стратегиям из yEarn / бывший makerdao smart contract engineer и [Daniel Que](https://twitter.com/danielque) - экс-Coinbase

**Rekt:** Сколько времени ушло на починку?

**0xMaki:** 3-4 часа, чтобы воспроизвести и найти проблему.

**Rekt:** сколько было потеряно?

**0xMaki:** Потеряно всего 15 тысяч, потому что суши-бар может накапливать только 20-30 тысяч в день. 0.05% идет в пулы, и все надо делать вручную, и есть риск, что транзакция не пройдет.

**Rekt: Хакерская атака или эксплоит?**

**0xMaki:** Однозначно эксплоит, и очень умный - он заслужил эти деньги. Кстати, мне кажется, я его нашел...

**Rekt:** Ты больше впечатлен или обескуражен?

**0xMaki:** Однозначно впечатлен! Уж точно не обескуражен! Очень увлекательно наблюдать за всеми этими атаками / эксплойтами. Даже при серьезных аудитах всегда появляются какие-то новые сценарии, которые мы не планировали и о которых не подумали.

Это делает экосистему сильнее и устойчивее.

С этим атакующим мы потеряли всего 15 тысяч, может быть был кто-то еще, кто делал то же самое, надо будет изучить получше. Мы заметили этого, потому что из-за него начал страдать весь бар.

В любом случае, в 23:28 по моему времени мы (0xMaki и Andy) начали устранять проблему.

![](https://lh6.googleusercontent.com/AfYQkR2nEmDTLYAIcqA0n-6GtaGpsDSSDB6Y-NykyBE2znVpyhpTcqNTSt_Wx-8B2V1OSScQyW8Ekxvgr8NiK-pABsM26u4aGxzIckiwstGUMhB_0MqLAOxGJjxSfQRm0MMXUR1v)

Потом мы проверяли небольшие транзакции, просто чтобы удостовериться, что они неопасные, и тут - черт - они оказались опасными.

Andy только что вернулся из перелета, он валился с ног от смены часовых поясов, ему пришлось пойти спать, поэтому я остался один, пока... 

![](https://lh5.googleusercontent.com/AoC4V0gDiIzCSg0MedJONypm9V7KpfN4kQZc3qmeRvGN2CyaHsOGQv_0fEosKO6766h3M_VynadJdaKHAnj7aUg7_Po7BCzDCLOjzKfCXlC_1AbQKjuG-57IN4TvEhqyDppvaIDj)

[(samczsun)](https://twitter.com/samczsun)

**Rekt:** Как он узнал?

**0xMaki:** Я ему написал, потому что остался один, без единого .sol джедая.

**Rekt:** .sol-даты

![](https://lh6.googleusercontent.com/XmqXGATsYH7SArH7jLF82J1KLSczUODpWDI6AfY4yXUSJYrPQNoAt-TE8sueyr97jK83hDBrAK4lYtm0XfZvxGRhbPM3jNbpLuCHd4eHO4e1lSuTkrYE0KpiA384Y4et4IYy8Kw4)![](https://lh4.googleusercontent.com/AVz2977b1kJ93j9w8YlTFnQ728CBJhIKkie-4Gn-MDdqIErJbSXCYr-qLbTpxiCT70IPzzmQy6aBZ7jtrO0V4ZQsXY1FSoCawBsVPv3uwkAxYzoA3Lrsd7qRFd5-ikwliik1l0rQ)![](https://lh4.googleusercontent.com/CzyFAdpwpd5iAHD-S5EHgPAnlPl_B_IhbS8rNOsE5T5g-X_HLimDvQi6hIm8sQu_GCBTog_KKRxDwj1gXafHuywBpCdHFmthdL-GylfH0h6gkX-Ep91ucovdYvan78k_cdzHzPJg)![](https://lh4.googleusercontent.com/Cv4Ty0uF7kAY9EMIETzT26Eabe2jnfyQtFGsoA6qRJSrG1Lk7GIQlIKlLtngeneyL-kz5Q7m1S5dft6pooiYQ7r9jQMzHQsnTSjXgpjx1kVT4VOy6cHJ650KAwL_ErFcKCJbJltE)

**0xMaki:** но жаль... было поздно, и у него были планы, как у любого нормального человека в субботу вечером, я думаю?!

И все сначала, никто не может помочь...

Попытался связаться с Chef Nomi, со всеми главными разработчиками, оставил пошаговое описание атаки в основном чате команды в надежде, что кто-то проснется

Потом я вспомнил про [Daniel](https://twitter.com/danielque), мы были с ним в контакте с самого начала, я связался с ним, позвонил и ввел в курс дела.

![](https://lh5.googleusercontent.com/j49oC75qzLg9IBSO0zD5190VA4aZK2jETW8GG4S1XHZPEAKRKuu1Ney6hjysi_J3rn2DLUZ9WJDUFGgaR8ug8bIFNgdIGWqJ7tzgFHKkAURTBsmFKnHHp9Aj62Uh5Cy_UHpvl0dm)

**Rekt:** Ты еще разговариваешь с Nomi?

**0xMaki:**  Нет.

![](https://lh5.googleusercontent.com/KxNo_yX9tboZIjfc6xvqsUs_Z13C9OSb28xmCCuF_1UFKbhDNs_el1Nd7nFflSzBGefGiA5r3w7deozbKxFk-SfGPTxDg-DzXWVFyUP3EzkHdRLjFFvtcu7hqMSq8KEgMsYh-zgo)

**0xMaki:** Было 02:35 и у нас получилось воспроизвести!!! Мы поняли принцип эксплоита и могли его воспроизвести, а значит могли разработать решение.

В 03:19 у нас было решение.

![](https://lh6.googleusercontent.com/KmbawxTOw3xF7yC0w63X6K_XzBY85q5G4c4LAuWLqWEnq64DZcNbbUxnAHVY6iKnNUZdle8IgJrm1yf2E5VqA9skhtkLDFWwkex7tVZxfDb2TYI3sE_ML3AAoF4PJV0NTHNcNmhW)

**0xMaki:** Ситуация наладилась, команда просыпалась и работала над решением. Я тем временем занялся эксплоитером и увидел, что у него были в основном SNX и EHT.

Я просмотрел его транзакции, этот аккаунт не создавался для хакерской атаки, он ошивался по окрестностям и искал возможность для эксплоита.

**Rekt:** Почему ты так думаешь?

**0xMaki:** Чаевые. Он много раз получал чаевые в SNX и ESD. Значит, это кто-то, кто проводит много времени в обоих сообществах, скорее всего в Discord.

Я проверил по датам, кто получал и кто отправлял чаевые много раз подряд, и - бинго...

![](https://lh4.googleusercontent.com/v8i6j6fMZvLnlXWy2qTbgcKVCTOoVmuNzCrBFKGpa3UJ_VGt_wW59AO2pIepBC7DObq-eKnV_aX7xX2P5iOL-z6-U4ArJd_hWbCL0N6IeQDrY4qlzRyNdEA0nX5f4MOD0jJ91k7x)

Инсайдер из сообщества SNX помог мне идентифицировать получателя чаевых.

![](https://lh5.googleusercontent.com/HEooziQ-CV7OH0y1_D-Fo9uhj8kEYEE2kqmQkge3MDEB-avcdoOOQFvaPnxhkLeG3Ld41GDuZ4t5yS8EiuaieOuIBn2m0mDfFEIzjB1XLGqrzrBRorAosQo_xDC63AXm3p_K2tWI)

Так что вот так, вся команда проснулась, у нас было [предварительное](https://etherscan.io/address/0x280ac711bb99de7c73fb70fb6de29846d5e4207f) решение и атаку удалось прекратить. И вот тогда новости попали в [Twitter](https://twitter.com/Juan_Snow1/status/1332992258115657730?s=20).

**Замечание редактора** После этого мы получили неоспоримое доказательство от подозреваемого - 

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/image-1.png)

«это не мог быть я»

**0xMaki:** Ничьи фонды не были потеряны, потому что украденные деньги предназначались на выплату чистой прибыли держателям xSushi. Мы выделим из нашей казны на 15 тысяч монет и разошлем их пропорционально всем пострадавшим.

**Rekt:** Тогда ничего серьезного, кто-то устроил себе легкий перекус! Хочешь что-нибудь передать подозреваемому напоследок?

**0xMaki:** Свяжись со мной! У нас для тебя есть много смарт-контрактов, которые ты можешь поковырять,  и мы платим баг-баунти!

Я еще хочу [поблагодарить](https://twitter.com/0xMaki/status/1332993111950319618?s=20) всех, кто принимал участие в этом спасении, _включая атакующего._
