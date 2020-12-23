# Ответ

## **status**

Признак успешного ответа на запрос

message: содержит служебные сообщения при **status** не "**ok**"

## **data**

Массив данных

----

### **value**

Значение поля **links**[x].**devices**[x].**items**[x].**properties**[x].**value** для **key** указанного в параметре запроса **main**

----

## **groups**

Массив данных сгруппированных по **links**[x].**devices**[x].**items**[x].**properties**[x].**key** указанных в параметре запроса **sub**

----

### **groups**.**value**

Значение из поля **links**[x].**devices**[x].**items**[x].**address**.  Доступно при параметре запроса **meta**=**true**

----

### **groups**.**items**

Представление данных переменных для **links**[x].**devices**[x].**items**[x].**type**=[**bool** **intXX**  **uintXX**  **longXXX** **ulongXXXX** **floatXXXX**]

----

#### **items**.**actual**

Признак актуальность данных

----

#### **items**.**idItem**

Значение из поля **links**[x].**devices**[x].**items**[x].**id**.  

----

#### **items**.**value**

Значение переменной

----

#### **items**.**direction**

Значение из поля **links**[x].**devices**[x].**items**[x].**direction** Доступно при параметре запроса **meta**=**true**

----

#### **items**.**lastResponse**

Время последнего ответа

Доступно при параметре запроса **meta**=**true**

----

#### **items**.**lastChange**

Время последнего изменения значения поля **value**

----

#### **items**.**tags**

Значение из поля **links**[x].**devices**[x].**items**[x].**tags**

----

#### **items**.**properties**

Значение из поля **links**[x].**devices**[x].**items**[x].**properties**

----

#### **items**.**buffer**

Хранит результаты предыдущих запросов

Доступно при значени поля **links**[x].**devices**[x].**items**[x].**type**=[**bool** **intXX**  **uintXX**  **longXXX** **ulongXXXX** **floatXXXX**]

Заполняется при:

* **links**[x].**devices**[x].**items**[x].**buffer**.**enable**=**true**

----

##### **buffer**.**value**

Архивное значение

----

##### **buffer**.**lastChange**

Дата изменения значение

----

### **groups**.**bitMap**

Представление данных переменных для **links**[x].**devices**[x].**items**[x].**type**=[**16bitXX** **32bitXXXX**]

----

#### **bitMap**.**bit**

Номер бита. Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**bit**

----

#### **bitMap**.**value**

Значение бита

----

#### **bitMap**.**text**

Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**on** при **value**=**true**
Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**off** при **value**=**false**

----

#### **bitMap**.**description**

Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**description**

----

#### **bitMap**.**lastChange**

Время последнего изменения значения поля **value**

----

#### **bitMap**.**tags**

Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**tags**

----

#### **bitMap**.**properties**

Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**properties**

----

#### **bitMap**.**buffer**

Хранит результаты предыдущих запросов

Доступно при значени поля **links**[x].**devices**[x].**items**[x].**type**=[**16bitXX**  **32bitXXXX**]

Заполняется при:

* **links**[x].**devices**[x].**items**[x].**buffer**.**enable**=**true**
* **links**[x].**devices**[x].**items**[x].bitMap[x].**buffer**.**enable**=**true**
* **links**[x].**devices**[x].**items**[x].bitMap[x].**buffer**.**size**>0 если поле существует, иначе, если **links**[x].**devices**[x].**items[**x].**buffer**.**size**>0

----

##### **bitMap**.**buffer**.**value**

Архивное значение

----

##### **bitMap**.**buffer**.**lastChange**

Дата изменения значение
