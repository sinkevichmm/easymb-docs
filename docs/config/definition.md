# **Понятия и определения**

## **Modbus**

### **Область памяти**

Modbus имееет 4 области памяти в которых хранятся регистры данных

* Discrete Inputs
* Coils
* Input Registers
* Holding Registers

Для доступа к регистрам через EasyMB можно воспользоватся таблицей соответствия для  **links**[x].**devices**[x].**items**[x]:

|**type**|**direction**|modbus bank|
|----|---|---|
|**bool**|**in**|Discrete Inputs|
|**bool**|**out**|Coils|
|**other**|**in**|Input Registers|
|**other**|**out**|Holding Registers|
