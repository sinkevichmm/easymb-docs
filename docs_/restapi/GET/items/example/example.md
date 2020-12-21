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
                            "type": "float3412",
                            "direction": "in",
                            "tags": [
                                "tad1",
                                "second"
                            ],
                            "description": "тест флоат float3412",
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

> http://127.0.0.1:7283/api/items?idItem=543,5&meta=true&bitMap=true&buffer=true

## **Ответ**

```json
HTTP/1.1 200 OK
Content-Type: application/json; charset=UTF-8
Date: Fri, 27 Nov 2020 05:11:17 GMT
Connection: close
Transfer-Encoding: chunked

{
  "status": "ok",
  "message": "",
  "data": [
    {
      "actual": true,
      "addressDevice": 156,
      "addressItem": 41,
      "idItem": 543,
      "idLink": 2,
      "idDevice": 22,
      "direction": "in",
      "type": "float3412",
      "description": "тест флоат float3412",
      "value": "0.33333334",
      "lastResponse": "2020.11.27-12:11:17.249",
      "lastChange": "2020.11.27-12:11:17.149",
      "tags": [
        "tad1",
        "second"
      ],
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
      "buffer": [
      	...
        {
          "value": "0.33333334",
          "lastChange": "2020.11.27-12:11:17.149"
        },
        {
          "value": "-131.85715",
          "lastChange": "2020.11.27-12:11:16.158"
        },
        ...
        
      ]
    },
    {
      "actual": true,
      "addressDevice": 42,
      "addressItem": 41,
      "idItem": 5,
      "idLink": 3,
      "idDevice": 75,
      "direction": "in",
      "type": "32bit1234",
      "description": "тест 32bit1234",
      "value": "01111100000000000100011011101000",
      "lastResponse": "2020.11.27-12:11:17.152",
      "lastChange": "2020.11.27-12:11:17.152",
      "tags": [
        "1",
        "2",
        "3"
      ],
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
      "bitMap": [
        {
          "value": false,
          "bit": 0,
          "text": "Нет Авария ркс!",
          "description": "Авария ркс!",
          "lastChange": "2020.11.27-12.11.17.196",
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
            ...
            {
              "value": "1",
              "lastChange": "2020.11.27-12.11.16.196"
            },
            
            {
              "value": "0",
              "lastChange": "2020.11.27-12.11.13.196"
            },
            {
              "value": "1",
              "lastChange": "2020.11.27-12.11.10.196"
            },
            ...

          ]
        },
        ...
        {
          "value": false,
          "bit": 31,
          "text": "Нет Авария ркс!",
          "description": "Авария ркс!",
          "lastChange": "2020.11.27-12.11.17.196",
          "tags": [],
          "properties": []
        }
      ]
    }
  ]
}
```
