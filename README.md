<a href='https://play.google.com/store/apps/details?id=lav.watermeter&referrer=utm_source%3DGitHub'><img width="180" alt='Get it on Google Play' src='https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png'/></a>

[Habrahabr](https://habr.com/post/428844/)

## MetersReading
Данное устройство предназначено для сбора данных по расходу воды, электроэнергии, можно следить за датчиками протечки или использовать для чего-то другого, где необходимо отслеживать состояние выводов. Для хранения данных используется сервис [thingspeak](https://thingspeak.com/). В качестве основного модуля использовалась ESP-03. Прошивка модуля собрана при помощи [online-конструктора](http://nodemcu-build.com)

<img src="https://github.com/LukyanovAnatoliy/MetersReading/blob/master/image/scheme.png"/>

## Настройка
При старте устройство переходит в режим настройки. После этого, в списке доступных сетей должна появиться сеть ESP-???????, где вместо символов ? будет id вашего ESP. Пароль для подключения к сети "1234567890". После подключения, в браузере необходимо перейти по адресу 1.1.1.1. В данной версии скрипта доступно два режима: учет потребления воды и учет потребления электроэнергии

<img src="https://github.com/LukyanovAnatoliy/MetersReading/blob/master/image/setup1.png" width="400"/> <img src="https://github.com/LukyanovAnatoliy/MetersReading/blob/master/image/setup2.png" width="400"/>

После ввода всех настроек, необходимо нажать на кнопку "Сохранить". Если к устройству не подключаться, то через 60 секунд устройство перейдет в рабочий режим.

## Принцип работы
При работе с водосчетчиками устройство передает данные каждые 60 секукнд, при условии что были изменения. При работе с электросчетчиком данные передаются каждые 20 секунд.
Если необзходимо, скрипт можно доработать как нужно. Например одновременно подключить к устройству счетчики воды, датчик протечки и светодиод для индикации работы или 2 счетчика воды и 2 датчика протечки. Вариантов много.

## Приложение
Приложение работает с сервисом [thingspeak](https://thingspeak.com/) и ему не важно кто туда передает данные. 

<img src="https://github.com/LukyanovAnatoliy/MetersReading/blob/master/image/device1.jpg" />

<img src="https://github.com/LukyanovAnatoliy/MetersReading/blob/master/image/device2.jpg"/>
