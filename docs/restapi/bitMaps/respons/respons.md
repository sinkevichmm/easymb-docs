# Разбор ответа

## **status**

Прищзнак успешного ответа на запрос

message: содержит служебные сообщения при **status** не "**ok**"

## **data**

Массив данных

----

### **actual**

Признак актуальность данных

----

### **value**

Ответа на запрос данных с устройства

----

### **bit**

Номер бита

----

### **idItem**

Значение из поля **links**[x].**devices**[x].**items**[x].**id**

----

### **text**

Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**on** при **value**=**true**
Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**off** при **value**=**false**

----

### **description**

Значение из поля **links**[x].**devices**[x].**items**[x].**bitMap**[x].**description**

----

### **lastResponse**

Время последнего ответа

Доступно при параметре запроса meta=true

----

### **lastChange**

Время последнего изменения значения поля value

----

### **tags**

Значение из поля **links**[x].**devices**[x].**items**[x].**tags**

----

### **properties**

Значение из поля **links**[x].**devices**[x].**items**[x].**properties**

----

### **buffer**

Хранит результыты прдидущих запросов

Доступно при значени поля **links**[x].**devices**[x].**items**[x].**type**=[**16bitXX**  **32bitXXXX**]

Заполняется при:

* **links**[x].**devices**[x].**items**[x].**buffer**.**enable**=**true**
* **links**[x].**devices**[x].**items**[x].bitMap[x].**buffer**.**enable**=**true**
* **links**[x].**devices**[x].**items**[x].bitMap[x].**buffer**.**size**>0 если поле существует, иначе, если **links**[x].**devices**[x].**items[**x].**buffer**.**size**>0