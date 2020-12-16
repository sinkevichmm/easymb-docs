# Пример

```json
"restapi": {
        "port": 7283,
        "enable": true,
        "accessList": [
            {
                "ip": "127.0.0.1",
                "read": true,
                "write": true
            },{
                "ip": "127.0.0.2",
                "read": true,
                "write": false
            }
        ],
        "publicFolder": {
            "enable": true,
            "path": "path/to/public/folder"
        }
    }
```
