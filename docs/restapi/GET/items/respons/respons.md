# Ответ

## **status**

Признак успешного ответа на запрос

message: содержит служебные сообщения при **status** не "**ok**"

## **data**

Массив данных

----

### **actual**

Признак актуальность данных

----

### **addressDevice**

Значение из поля **links**[x].**devices**[x].**address**. Доступно при параметре запроса **meta**=**true**

----

### **addressItem**

Значение из поля **links**[x].**devices**[x].**items**[x].**address**.  Доступно при параметре запроса **meta**=**true**

----

### **idItem**

Значение из поля **links**[x].**devices**[x].**items**[x].**id**.  

----

### **idLink**

Значение из поля **links**[x].**id**. Доступно при параметре запроса **meta**=**true**

----

### **idDevice**

Значение из поля **links**[x].**devices**[x].**id**. Доступно при параметре запроса **meta**=**true**

----

### **direction**

Значение из поля **links**[x].**devices**[x].**items**[x].**direction** Доступно при параметре запроса **meta**=**true**

----

### **type**

Значение из поля **links**[x].**devices**[x].**items**[x].**type** Доступно при параметре запроса **meta**=**true**

### **description**

Значение из поля **links**[x].**devices**[x].**items**[x].**description**

----

### **value**

Значение переменной

----

### **lastResponse**

Время последнего ответа

Доступно при параметре запроса **meta**=**true**

----

### **lastChange**

Время последнего изменения значения поля **value**

----

### **tags**

Значение из поля **links**[x].**devices**[x].**items**[x].**tags**

----

### **properties**

Значение из поля **links**[x].**devices**[x].**items**[x].**properties**

----

### **buffer**

Хранит результаты предыдущих запросов

Доступно при значени поля **links**[x].**devices**[x].**items**[x].**type**=[**bool** **intXX**  **uintXX**  **longXXX** **ulongXXXX** **floatXXXX**]

Заполняется при:

* **links**[x].**devices**[x].**items**[x].**buffer**.**enable**=**true**

----

#### **buffer**.**value**

Архивное значение

----

#### **buffer**.**lastChange**

Дата изменения значение

----

### **bitMap**

Доступно при значени поля **links**[x].**devices**[x].**items**[x].**type** [**16bitXX**  **32bitXXXX**]

#### **bitMap**.**bit**

Номер бита. Номер бита. Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**bit**

----

#### **bitMap**.**value**

Значение бита

----

#### **bitMap**.**text**

Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**on** при **value**=**true**
Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**off** при **value**=**false**

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
