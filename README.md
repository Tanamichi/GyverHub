[![latest](https://img.shields.io/github/v/release/GyverLibs/GyverHUB.svg?color=brightgreen)](https://github.com/GyverLibs/GyverHUB/releases/latest/download/GyverHUB.zip)
[![Foo](https://img.shields.io/badge/Website-AlexGyver.ru-blue.svg?style=flat-square)](https://alexgyver.ru/)
[![Foo](https://img.shields.io/badge/%E2%82%BD$%E2%82%AC%20%D0%9D%D0%B0%20%D0%BF%D0%B8%D0%B2%D0%BE-%D1%81%20%D1%80%D1%8B%D0%B1%D0%BA%D0%BE%D0%B9-orange.svg?style=flat-square)](https://alexgyver.ru/support_alex/)
[![Foo](https://img.shields.io/badge/README-ENGLISH-blueviolet.svg?style=flat-square)](https://github-com.translate.goog/GyverLibs/GyverHUB?_x_tr_sl=ru&_x_tr_tl=en)  

[![Foo](https://img.shields.io/badge/ПОДПИСАТЬСЯ-НА%20ОБНОВЛЕНИЯ-brightgreen.svg?style=social&logo=telegram&color=blue)](https://t.me/GyverLibs)

# GyverHUB
Панель управления для esp8266, esp32 и других Arduino. Конструктор интерфейса, интеграция в умный дом

> <br>**Документация находится в [Wiki репозитория](https://github.com/GyverLibs/GyverHUB/wiki). English docs - [translate](https://github-com.translate.goog/GyverLibs/GyverHUB/wiki?_x_tr_sl=ru&_x_tr_tl=en)**<br><br>

|⚠️⚠️⚠️<br>**Бета-версия! Проект пока что тестируется, следите за коммитами. Известные проблемы, особенности версии, обсуждение, предложения, баги - всё [вот тут](https://github.com/GyverLibs/GyverHUB/issues/3)**<br>⚠️⚠️⚠️|
| --- |

|☕☕☕<br>**Библиотека разработана благодаря народной поддержке [на Boosty](https://boosty.to/alexgyvershow). Также есть [другие способы](https://alexgyver.ru/support_alex/) поддержать автора**<br>☕☕☕|
| --- |

![promo](/docs/promo.jpg)

GyverHUB - это программный комплекс, включающий в себя библиотеку для микроконтроллеров и программу для управления. Программа написана на JavaScript и по сути является сайтом, который доступен:
- С официального сайта [hub.gyver.ru](http://hub.gyver.ru/)
- Сайт можно [установить](https://github.com/GyverLibs/GyverHUB/wiki/%D0%9D%D0%B0%D1%87%D0%B0%D0%BB%D0%BE-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B#%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-%D0%B2%D0%B5%D0%B1-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F) как веб-приложение (PWA) на любое устройство (Android/iOS/Windows...)
- Локально с компьютера, для этого нужно [скачать сайт](https://github.com/GyverLibs/GyverHUB/raw/main/web/local/local.zip) из папки `web/local`
- Из памяти ESP8266/32, см. [документацию](https://github.com/GyverLibs/GyverHUB/wiki/5.-%D0%94%D0%BE%D0%BF%D0%BE%D0%BB%D0%BD%D0%B8%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE#%D0%B7%D0%B0%D0%BF%D1%83%D1%81%D0%BA-%D0%B8%D0%B7-%D0%BF%D0%B0%D0%BC%D1%8F%D1%82%D0%B8-esp)
- Из [Телеграм-бота](https://t.me/GyverHUB_bot)
- Отдельное Android приложение (в разработке)

Микроконтроллер и приложение обмениваются данными по своему протоколу (см. [API](https://github.com/GyverLibs/GyverHUB/wiki#api)) через различные интерфейсы связи: 
- MQTT (через Интернет)
- WebSocket (в локальной сети)
- Serial (в разработке)
- Bluetooth (в разработке)

Основные моменты:
- Приложение может обнаруживать устройства в своей "сети"
- В программе для микроконтроллера "собирается" графический интерфейс, который отправляется в приложение
- Можно управлять микроконтроллером с полученного интерфейса в приложении или с сайта
- В случае с ESP8266/ESP32 это работает через Интернет
- Библиотека реализована таким образом, что помимо использования в паре с родным приложением можно очень просто и быстро интегрировать свою самоделку в любую систему умного дома, которая поддерживает MQTT (Алиса, Home Assistant...)

Особенности:
- Библиотека невероятно проста в использовании
- Стильный дизайн ;) светлая и тёмная темы, несколько цветовых схем
- Удобный парсинг действий с приложения/сайта или сервера умного дома
- Более 20 активных компонентов интерфейса (кнопки, слайдеры, выбор...) + блоки оформления и навигации
- Настраиваемые модули: загрузка и скачивание файлов, информация о плате, OTA обновление, защита паролем, интерфейс командной строки...
- 1000 FontAwesome иконок оформления для кнопок и списка устройств
- Библиотека асинхронная (опционально для ESP8266/ESP32)
- Оптимальное использование памяти для работы на слабых МК

Аналоги:
- Приложение RemoteXY
- Сервис Blynk

В отличие от них GyverHUB полностью бесплатный, безопасный, не имеет ограничений и не нуждается в локальном сервере

### Совместимость
Все Arduino
- **НЕ РАБОТАЕТ НА ESP32 SDK 2.0.8**

## Установка
- Зависимости: [Stamp](https://github.com/GyverLibs/Stamp), [PubSubClient](https://github.com/knolleary/pubsubclient), [arduinoWebSockets](https://github.com/Links2004/arduinoWebSockets), [ESPAsyncWebServer](https://github.com/me-no-dev/ESPAsyncWebServer), [ESPAsyncTCP](https://github.com/me-no-dev/ESPAsyncTCP), [AsyncTCP](https://github.com/me-no-dev/AsyncTCP), [async-mqtt-client](https://github.com/marvinroger/async-mqtt-client)
- Подробнее читай [в документации](https://github.com/GyverLibs/GyverHUB/wiki/%D0%9D%D0%B0%D1%87%D0%B0%D0%BB%D0%BE-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%8B)

### Обновление
- Рекомендую всегда обновлять библиотеку: в новых версиях исправляются ошибки и баги, а также проводится оптимизация и добавляются новые фичи
- Через менеджер библиотек IDE: найти библиотеку как при установке и нажать "Обновить"
- Вручную: **удалить папку со старой версией**, а затем положить на её место новую. "Замену" делать нельзя: иногда в новых версиях удаляются файлы, которые останутся при замене и могут привести к ошибкам!

## Версии
- v1.0

## Баги и обратная связь
При нахождении багов создавайте **Issue**, а лучше сразу пишите на почту [alex@alexgyver.ru](mailto:alex@alexgyver.ru)  
Библиотека открыта для доработки и ваших **Pull Request**'ов!

При сообщении о багах или некорректной работе библиотеки нужно обязательно указывать:
- Версия библиотеки
- Какой используется МК
- Версия SDK (для ESP)
- Версия Arduino IDE
- Корректно ли работают ли встроенные примеры, в которых используются функции и конструкции, приводящие к багу в вашем коде
- Какой код загружался, какая работа от него ожидалась и как он работает в реальности
- В идеале приложить минимальный код, в котором наблюдается баг. Не полотно из тысячи строк, а минимальный код
