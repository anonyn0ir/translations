---
title: Akropolis - REKT
date: 12 ноября 2020
rekt: 
  количество: 2000000
  аудит: CertiK, SmartDec
  дата: 12 ноября 2020
tags:
  - akropolis
  - delphi
  - Rekt
excerpt: Акрополь не подвергался такому rekt со времен Саламинского сражения в 480 году до н.э. Царь Ксеркс наших дней снова стер Акрополь с лица земли, украв $2,000,000 DAI с помощью комбинации флэш-кредитов и повторного входа. 
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/84604-1.jpg
---

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/84604-1.jpg)
Перикл, наверное, в гробу переворачивается.

Акрополь не подвергался такому rekt со времен Саламинского сражения в 480 году до н.э.

Царь Ксеркс наших дней снова стер Акрополь с лица земли, украв $2,000,000 DAI с помощью комбинации флэш-кредитов и повторного входа. 

Поначалу админы Akropolis попытались создать видимость, что они просто выполняли «ремонтные работы». 

![](https://lh5.googleusercontent.com/MElhS0VhaZ0DA_lMRYeLoRNafz1YWpafkzgdcV_K9F-HNxz1V7H85KDGkQdP3npLM9Nql6LjtEqzKVUnHMdL8OzlWbsZ9JbFl_L7JQJc_MWKJpYwIRr_AVzsBUvrpEtLpc-xpkDi)

Теперь мы знаем, что их поимели на 2 миллиона долларов. 

![](https://lh5.googleusercontent.com/OGE_yvAkXzHlE9USnNhS0g0NpV3bqHKBj8Z7bAcVT3B0ejQs8bBkWfWJrmqo_83zWyVTq7aOG_JaLTItr7uL_k2TiKOHN7JEqmwp1T6IOY9w9ENZr6ZtbWE2B29XNxAl4ex_UO_r)

Но как?

Протокол Akropolis позволяет пользователям вкладывать токены в хранилище и получать взамен другие токены. Количество токенов, которые вы получаете назад, зависит от того, сколько вы вложили.

Количество вложенных токенов вычисляется по разнице между балансом до и после выполнения трансфера.

Вот как атакующий использовал систему в своих интересах, создав вредоносный контракт на создание токенов, который вызвал функцию повторного вклада (повторный вход). [Это](https://etherscan.io/address/0xe2307837524db8961c4541f943598654240bd62f#tokentxns) контракт атаки.

1. Создать фальшивый токен

2. Вложить фальшивый токен

3a. Получить callback фальшивого токена, вложить 25к DAI

3б. Получить на свой счет 25к DAI депозитов

4. Получить на свой счет 25к DAI депозитов

5. Вывести 50к DAI

Источник [samczsun](https://twitter.com/samczsun)
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2020/11/4d509e7155f551c4d98bb1014b320c61-1.jpg)

Потому как атакующий мог использовать свой контракт как вкладываемый токен, он смог использовать повторный вход с помощью флэш-кредита dYdx, как объясняется внизу. 

![](https://lh4.googleusercontent.com/LxCZ2ZHvBLGPgk7BaoplX3rNuNtfN2JoZ9VeMBZe42MaWMw7ShK_mdgg70RhZJ1DJO4lLn1D8IkAnZ91VKeamI49aW0pDY-7trH07qX2A_ifqbg5xE_1QVLoOxt7qcUBfIYUm8i0)![](https://lh5.googleusercontent.com/D2wa_EEUSuXUk7r9cRAhX-fwHRv91pmeFeWd1bVR9KFO_IZLXzlzt8I2eJhNfGFP9pOiVokZa58Qn4aFUWlycIIt2gSNNZA5pDSbsy3vqMqsG8eZS1yU8N1qfgQP4_UFbZS0kMfV)

[Это](https://etherscan.io/address/0xe2307837524db8961c4541f943598654240bd62f#tokentxns)iадрес хакера. Видно, что он начал выполнять серии атак по $50k примерно на 8 часов раньше.

Затем он [ послал $2 миллиона](https://etherscan.io/tx/0xf15623567231c67df2b8bcc5540236fbda2c3ac11ecbec427048f11b582cb869) из полученных денег на другой адрес, где они находятся в момент написания статьи.

Источник: [@dogetoshi](https://twitter.com/Dogetoshi/status/1326963117356625931?s=20)

![](https://lh3.googleusercontent.com/dSGoJEDMg3SdSHVshM5N8FaLgkai2s1q7gtmCd7-VPKmeNcCew5OXEVAHOQ_Sa9h7iRL021U54658OC8HnVS6MdQSTMxsyjfu6MOKQ-qP5o6Ay0-Jy3NjnVx2dKYEmgAqTrefgjL)

Стоит отметить, что смарт-контракт, с которым взаимодействовал хакер, прошел аудит в двух разных охранных компаниях, Smartdec и Certik.

У Smartdec довольно таки приличный послужной [список](https://blog.smartdec.net/). А для Certik, к сожалению, Akropolis стал нежеланным новым проектом в списке тех, кого они аудировали, и кто потом подвергся эксплоиту.

bZx, Lien, [Harvest](/harvest-finance-rekt/), и теперь Akropolis. Даже если выполненный аудит безопасности никогда не должен считаться гарантией безопасности, но аудит Certik точно принес меньше пользы, чем должен был...

Даже качественно сделанный и тщательно проаудированный контракт может превратиться в говношоу, если попадет в плохие руки.  Тот факт, что Akropolis так легко соврали своим пользователям говорит о том, что не вся вина лежит на Certik и хакере.

Даже если мы всегда стремимся выбирать протоколы, не требующие доверия, когда дело доходит до коммуникации между пользователем и провайдером сервиса, хрупкость доверия всегда должна находиться под защитой. 

Akropolis потерял это доверие, и стал rekt.
