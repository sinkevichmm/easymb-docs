# **items**

PUT запрос типа:

> PUT "/items/:id"

```json
body:

content-type: application/json

{
    "value":"43.1"
}
```

Установит значение **links**[x].**devices**[x].**items**[x].**value** переменной **links**[x].**devices**[x].**items**[x].**id**=**:id**

Актуален при **links**[x].**devices**[x].**items**[x].**type**=[**uintXX** **intXX** **ulongXXXX** **longXXXX**] и **links**[x].**devices**[x].**items**[x].**direction**=**out**
