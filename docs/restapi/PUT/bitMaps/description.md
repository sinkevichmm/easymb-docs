# **bitmaps**

PUT запрос типа:

> PUT "/bitmaps/:id"

```json
body:

content-type: application/json

{
    "value":
        [
            {
                "bit": 0,
                "value": true
            },
            {
                "bit": 31,
                "value": false
            }
        ]
}
```

Установит значения битов **links**[x].**devices**[x].**items**[x].**bitMap**[x].**value** переменной **links**[x].**devices**[x].**items**[x].**id**=**:id**

Актуален при **links**[x].**devices**[x].**items**[x].**type** [**16bitXX**  **32bitXXXX**] и **links**[x].**devices**[x].**items**[x].**direction**=**out**
