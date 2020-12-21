# Пример

----

## Файл конфигурации

```json
{
    "restapi": {
        "port": 7283,
        "enable": true,
        "accessList": [
            {
                "ip": "127.0.0.1",
                "read": true
            }
        ]
    },
    "links": [
        {
            "id": 3,
            "name": "SMH2G",
            "description": "",
            "protocol": "mb-rtu",
            "port": "/dev/ttyUSB1",
            "baudRate": 115200,
            "dataBits": 8,
            "parity": "N",
            "stopBits": 2,
            "timeoutMs": 100,
            "reqestMs": 100,
            "devices": [
                {
                    "id": 75,
                    "address": 42,
                    "description": "smh4",
                    "groupRequest": "all",
                    "items": [
                        {
                            "id": 5,
                            "enable": true,
                            "address": 41,
                            "type": "32bit1234",
                            "direction": "in",
                            "description": "тест 32bit1234",
                            "buffer": {
                                "enable": true,
                                "size": 23
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true
                                }
                            },
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M34"
                                },
                                {
                                    "key": "proj",
                                    "value": "demo-1212"
                                }
                            ],
                            "tags": [
                                "1",
                                "2",
                                "3"
                            ],
                            "bitMap": [
                                {
                                    "bit": 0,
                                    "description": "Авария ркс!",
                                    "on": "Авария ркс!",
                                    "off": "Нет Авария ркс!",
                                    "tags": [
                                        "11",
                                        "22",
                                        "33"
                                    ],
                                    "buffer": {
                                        "enable": true,
                                        "size": 17
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "m1"
                                        },
                                        {
                                            "key": "DescritInput",
                                            "value": "RKS"
                                        }
                                    ]
                                }
                            ]
                        }
                    ]
                }
            ]
        },
        {
            "id": 2,
            "name": "Pixel3",
            "description": "Pixel",
            "protocol": "mb-tcp",
            "port": "502",
            "ip": "192.168.22.132",
            "timeoutMs": 100,
            "reqestMs": 100,
            "devices": [
                {
                    "id": 22,
                    "address": 156,
                    "description": "smh4",
                    "groupRequest": "all",
                    "items": [
                        {
                            "id": 543,
                            "enable": true,
                            "address": 41,
                            "type": "16bit12",
                            "direction": "in",
                            "tags": [
                                "tad1",
                                "second"
                            ],
                            "description": "тест флоат 16bit12",
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M34"
                                },
                                {
                                    "key": "proj",
                                    "value": "demo-1212"
                                }
                            ],
                            "buffer": {
                                "enable": true,
                                "size": 100
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true,
                                    "accessList": [
                                        {
                                            "ip": "127.0.0.1",
                                            "read": true
                                        }
                                    ]
                                }
                            }
                        }
                    ]
                }
            ]
        }
    ]
}
```

## **Запрос**

> http://127.0.0.1:7283/api/bitmaps?meta=true&buffer=true

## **Ответ**

```json
HTTP/1.1 200 OK
Content-Type: application/json; charset=UTF-8
Date: Mon, 30 Nov 2020 04:11:10 GMT
Connection: close
Transfer-Encoding: chunked

{
  "status": "ok",
  "message": "",
  "data": [
    ...
    {
      "actual": true,
      "value": false,
      "bit": 2,
      "idItem": 543,
      "text": "",
      "description": "",
      "lastResponse": "2020.11.30-11:11:10.170",
      "lastChange": "2020.11.30-11.11.08.258",
      "tags": [],
      "properties": []
    },
    {
      "actual": true,
      "value": true,
      "bit": 3,
      "idItem": 543,
      "text": "",
      "description": "",
      "lastResponse": "2020.11.30-11:11:10.170",
      "lastChange": "2020.11.30-11.11.10.173",
      "tags": [],
      "properties": []
    },
    ...
    {
      "actual": true,
      "value": true,
      "bit": 15,
      "idItem": 543,
      "description": "",
      "lastResponse": "2020.11.30-11:11:10.170",
      "lastChange": "2020.11.30-11.11.09.258",
      "tags": [],
      "properties": []
    },
    {
      "actual": true,
      "value": false,
      "bit": 0,
      "idItem": 5,
      "text": "Нет Авария ркс!",
      "description": "Авария ркс!",
      "lastResponse": "2020.11.30-11:11:10.075",
      "lastChange": "2020.11.30-11.11.10.173",
      "tags": [
        "11",
        "22",
        "33"
      ],
      "properties": [
        {
          "key": "mech",
          "value": "m1"
        },
        {
          "key": "DescritInput",
          "value": "RKS"
        }
      ],
      "buffer": [
        {
          "value": "0",
          "lastChange": "2020.11.30-11.11.10.173"
        },
        {
          "value": "1",
          "lastChange": "2020.11.30-11.11.07.258"
        },
        ...
      ]
    },
    {
      "actual": true,
      "value": true,
      "bit": 1,
      "idItem": 5,
      "text": "",
      "description": "",
      "lastResponse": "2020.11.30-11:11:10.075",
      "lastChange": "2020.11.30-11.11.09.258",
      "tags": [],
      "properties": []
    },
    ...
    {
      "actual": true,
      "value": true,
      "bit": 31,
      "idItem": 5,
      "text": "",
      "description": "",
      "lastResponse": "2020.11.30-11:11:10.075",
      "lastChange": "2020.11.30-11.11.10.173",
      "tags": [],
      "properties": []
    }
  ]
}
```
