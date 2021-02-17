# -073-ESP8266-BLYNK-Arduino
#073 Непростой Терморегулятор ESP8266 + BLYNK Arduino.

  В чем суть скетча
 
   Мониторинг и контроль температуры.
   Датчики:
    1)Есть датчик для улицы (просто контроль температуры, влажности, давления)
    2)Есть датчик температуры воздуха в помещении и датчик температуры теплых полов.
    
   Исполнительные механизмы (Есть два нагревателя):
    1)Тепловая пушка (Условно назовем ее так, для того что бы в случае чего резко нагреть помещение)
    2)Теплый пол
    
   Логика "Тепловой пушки": 
     Задаем температуру Старт и температуру Стоп нагрев. 
     Если температура стала ниже старт то включится нагрев и будет греть пока температура не
     станет выше Стоп. Нагрев включится опять толь тогда когда температура станет опять ниже Старт.
   Логика "Теплого пола"
     Есть 4 таймера(Сутки разбиты на 4 части). Каждый таймер включает свою уставку Температуры.

Видео https://youtu.be/K6YWA9vz61c
     
 
  Скетч собран по материалам сайта http://docs.blynk.cc/
 
  Модули в составе проекта
  ESP8266 - 12E WIFI RobotDyn (3.68 $) https://goo.gl/k6TRUz
  ESP8266 - 12E WIFI GREAT WALL (3.44 $) https://goo.gl/DcqYMg
   
  Датчики для улицы:
   DHT 11 (1.00 $) https://goo.gl/sCBn3d  Тут дешево но долго шло
   DHT 11 (3.11 $) https://goo.gl/rBFbBD  Тут дороже но дойдет быстрее
   Желательно брать этот, скоро будет вариант и с ним.
   GY-BME280-3.3 (3.78 $) https://goo.gl/1eyGmg
   
  Модуль часов реального времени
   DS3231 Модуль RTC (1.95 $) https://goo.gl/3jMusY
   RTC DS3231 (часы реального времени)RobotDyn + аккумулятор (2.90 $) https://goo.gl/gGMRak
   
  Датчики температуры в помещении и в полу
   DS18B20 Датчик на плате (2.11 $) https://goo.gl/T4AmmR
   DS18B20 Датчик температуры в корпусе (2.07 $) https://goo.gl/HmbgWM
   
  Реле (выбор реле зависит от мощности нагрузки) 
   1-канальное реле с управлением Высоким и Низким уровнем 10Ампер (0,99 $) https://goo.gl/SnFuXY
   1-канальное реле с управлением Высоким и Низким уровнем 30Ампер (3.96 $) https://goo.gl/PW1uYL
  
 
  Библиотеки
 
  BLYNK   
     https://github.com/blynkkk/blynk-library/releases/tag/v0.5.0
     
  OTA Видео об этом https://youtu.be/AyGs8ptdZJc   
     Для возможности прошивки по сетевому порту,
     необходимо установить последнюю версию python 
     Скачать по ссылке: https://www.python.org/downloads/
    
     Ссылка на библиотеку Aduino OTA.
     https://github.com/esp8266/Arduino/tree/master/libraries/ArduinoOTA
     Ссылка которые стоит посетить. Там море инфы об беспроводной прошивке.
     http://esp8266.github.io/Arduino/versions/2.0.0/doc/ota_updates/ota_updates.html
  
  EEPROM
     EEPROMAnything Видео о Библиотеке https://youtu.be/xBHor5iW5OE
     Материалы к бибилиотеки из видео https://yadi.sk/d/BAYkOBHM3RXA7P
 
  Ссылки на библиотеки для модулей
     DHT (Температура и Влажность)
       https://github.com/adafruit/Adafruit_Sensor
       https://github.com/adafruit/DHT-sensor-library
     BME280 (Температура, Влажность и Давление)
       https://github.com/adafruit/Adafruit_BME280_Library.git
     DS18B20 (Термомитер)
       https://github.com/milesburton/Arduino-Temperature-Control-Library.git
     RTC DS3231 (Часы реального времени)
       https://github.com/rodan/ds3231.git
