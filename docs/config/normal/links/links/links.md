
# **links**

описание настроек соединений с устройствами

|Свойство|Значение|
|----|---:|
|Тип|массив JSON|
|Обязательный|Да|

----

## **links**.**id**

Уникальный номер соединения

|Свойство|Значение|
|----|---:|
|Тип|int|
|Обязательный|Да|
|Значение|-2147483648...2147483647|

Должен быть уникальным в пределах проекта

----

## **links**.**name**

Имя соединения. Используется в режиме test и monitor

|Свойство|Значение|
|----|---:|
|Тип|string|
|Обязательный|Да|
|Значение|"Произвольная строка"|

----

## **links**.**description**

Описание соединения.  Служит в качестве meta информации

|Свойство|Значение|
|----|---:|
|Тип|string|
|Обязательный|Нет|
|Значение|"Произвольная строка"|

----

## **links**.**protocol**

Тип протокола передачи данных

|Свойство|Значение|
|----|---:|
|Тип|enum|
|Обязательный|Да|
|Значение|["mb-tcp" "mb-rtu"]|

для  **protocol**=**mb-tcp** пара **ip**:**port** должна быть уникальна
в пределах проекта

для  **protocol**=**mb-rtu** **port** должен быть уникальным
в пределах проекта

----

## **links**.**ip**

Адрес устройства

|Свойство|Значение|
|----|---:|
|Тип|string|
|Обязательный|Да|
|Значение|"ddd.ddd.ddd.ddd"|

----

## **links**.**port**

Порт для соединения с устройством

|Свойство|Значение|
|----|---:|
|Тип|string|
|Обязательный|Да|
|Значение для **protocol**=**mb-tcp**|"1"..."65535"|
|Значение для **protocol**=**mb-rtu**|строка типа ["COM1" "/dev/ttyUSB0"]|

----

## **links**.**baudRate**

Скорость передачи данных

|Свойство|Значение|
|----|---:|
|Тип|ENUM|
|Обязательный|Да для  **protocol**=**mb-rtu**|
|Значение|[50 75 110 134 150 200 300 600 1200 1800 2400 4800 9600 19200 38400 57600 115200 230400 460800 500000 576000 921600 1000000 1152000 1500000 2000000 2500000 3000000 3500000 4000000]|

----

## **links**.**dataBits**

Биты данных

|Свойство|Значение|
|----|---:|
|Тип|ENUM|
|Обязательный|Да для  **protocol**=**mb-rtu**|
|Значение|[5 6 7 8 ]|

----

## **links**.**parity**  

Бит чётности

|Свойство|Значение|
|----|---:|
|Тип|ENUM|
|Обязательный|Да для  **protocol**=**mb-rtu**|
|Значение|["N" "E" "O"]|

----

## **links**.**stopBits**  

Стоп-бит

|Свойство|Значение|
|----|---:|
|Тип|ENUM|
|Обязательный|Да для  **protocol**=**mb-rtu**|
|Значение|[1 2]|

----

## **links**.**timeoutMs**  

Таймаут запроса в миллисекундах

|Свойство|Значение|
|----|---:|
|Тип|int|
|Обязательный|Да|
|Значение|1...9223372036854775807|

----

## **links**.**requestMs**  

Пауза между запросами в миллисекундах

|Свойство|Значение|
|----|---:|
|Тип|int|
|Обязательный|Да|
|Значение|1...9223372036854775807|

----

## **links**.**devices**  

Описание настроек устройства

|Свойство|Значение|
|----|---:|
|Тип|массив JSON|
|Обязательный|Да|
