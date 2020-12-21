# Параметры запроса

> api/items?k=v"

## Параметры

Поиск соответствий ведется по узлу **links**[x].**devices**[x].**items**[x]

----

## **actual**

|Свойство|Значение|
|----|---:|
|Тип|bool|
|Значение|true/false|

Признак запроса актуальных данных

----

## **addressDevice**

|Свойство|Значение|
|----|---:|
|Тип|массив int|
|Разделитель|"**,**"|
|конкатенация|"ИЛИ"|

----

## **addressItem**

|Свойство|Значение|
|----|---:|
|Тип|массив int|
|Разделитель|"**,**"|
|конкатенация|"ИЛИ"|

----

## **idItem**

|Свойство|Значение|
|----|---:|
|Тип|массив int|
|Разделитель|"**,**"|
|конкатенация|"ИЛИ"|

----

## **idLink**

|Свойство|Значение|
|----|---:|
|Тип|массив int|
|Разделитель|"**,**"|
|конкатенация|"ИЛИ"|

----

## **idDevice**

|Свойство|Значение|
|----|---:|
|Тип|массив int|
|Разделитель|"**,**"|
|конкатенация|"ИЛИ"|

----

## **direction**

|Свойство|Значение|
|----|---:|
|Тип|ENUM|
|Значение|["in" "out"]|

----

## **type**

|Свойство|Значение|
|----|---:|
|Тип|массив ENUM|
|Разделитель|"**,**"|
|конкатенация|"ИЛИ"|
|Пример|"bool,float4321"|

массив строк состоящий из строки с резделителем значенией ","

----

## **description**

|Свойство|Значение|
|----|---:|
|Тип|string|

## **tag**

----

|Свойство|Значение|
|----|---:|
|Тип|массив string|
|Разделитель|"**,**"|
|конкатенация|"И"|
|Пример|"alarm,low level"|

массив строк состоящий из строки с резделителем значенией ","

## **property**

----

|Свойство|Значение|
|----|---:|
|Тип|массив string|
|Разделитель|"**,**"|
|конкатенация|"И"|
|Пример|"prop1:val1,engine:started"|

массив строк состоящий из строки с резделителем значенией "," и разделителем пар ключ:значение ":"

## **buffer**

----

|Свойство|Значение|
|----|---:|
|Тип|bool|
|Значение|true/false|

Признак запроса исторических данных

## **meta**

----

|Свойство|Значение|
|----|---:|
|Тип|bool|
|Значение|true/false|

Признак отображения вспомогоательной информации

## **bitMap**

----

|Свойство|Значение|
|----|---:|
|Тип|bool|
|Значение|true/false|

Признак отображения информации побитно для переменных типа  **links**[x].**devices**[x].**items**[x].**type**=[**16BitXX** **32bitXXXX**]