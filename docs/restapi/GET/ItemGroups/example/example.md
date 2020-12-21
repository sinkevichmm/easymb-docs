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
                            "id": 1,
                            "enable": true,
                            "address": 17,
                            "type": "int12",
                            "direction": "in",
                            "description": "M01 Температура1",
                            "buffer": {
                                "enable": true,
                                "size": 30
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true
                                }
                            },
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M01"
                                },
                                {
                                    "key": "temperature",
                                    "value": "t1"
                                }
                            ]
                        },
                        {
                            "id": 2,
                            "enable": true,
                            "address": 18,
                            "type": "int12",
                            "direction": "in",
                            "description": "M01 Температура2",
                            "buffer": {
                                "enable": true,
                                "size": 30
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true
                                }
                            },
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M01"
                                },
                                {
                                    "key": "temperature",
                                    "value": "t2"
                                }
                            ]
                        },
                        {
                            "id": 3,
                            "enable": true,
                            "address": 19,
                            "type": "int12",
                            "direction": "in",
                            "description": "M02 Температура1",
                            "buffer": {
                                "enable": true,
                                "size": 30
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true
                                }
                            },
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M02"
                                },
                                {
                                    "key": "temperature",
                                    "value": "t1"
                                }
                            ]
                        },
                        {
                            "id": 4,
                            "enable": true,
                            "address": 24,
                            "type": "int12",
                            "direction": "in",
                            "description": "M02 Температура2",
                            "buffer": {
                                "enable": true,
                                "size": 30
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true
                                }
                            },
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M02"
                                },
                                {
                                    "key": "temperature",
                                    "value": "t2"
                                }
                            ]
                        },
                        {
                            "id": 5,
                            "enable": true,
                            "address": 41,
                            "type": "float3412",
                            "direction": "in",
                            "description": "M01 Давление1",
                            "buffer": {
                                "enable": true,
                                "size": 30
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true
                                }
                            },
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M01"
                                },
                                {
                                    "key": "pressure",
                                    "value": "p1"
                                }
                            ]
                        },
                        {
                            "id": 6,
                            "enable": true,
                            "address": 43,
                            "type": "float3412",
                            "direction": "in",
                            "description": "M01 Давление2",
                            "buffer": {
                                "enable": true,
                                "size": 30
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true
                                }
                            },
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M01"
                                },
                                {
                                    "key": "pressure",
                                    "value": "p2"
                                }
                            ]
                        },
                        {
                            "id": 7,
                            "enable": true,
                            "address": 45,
                            "type": "float3412",
                            "direction": "in",
                            "description": "M02 Давление1",
                            "buffer": {
                                "enable": true,
                                "size": 30
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true
                                }
                            },
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M02"
                                },
                                {
                                    "key": "pressure",
                                    "value": "p1"
                                }
                            ]
                        },
                        {
                            "id": 8,
                            "enable": true,
                            "address": 48,
                            "type": "float3412",
                            "direction": "in",
                            "description": "M02 Давление2",
                            "buffer": {
                                "enable": true,
                                "size": 30
                            },
                            "remoteAccess": {
                                "restapi": {
                                    "enable": true
                                }
                            },
                            "properties": [
                                {
                                    "key": "mech",
                                    "value": "M02"
                                },
                                {
                                    "key": "pressure",
                                    "value": "p2"
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
                            "address": 26,
                            "type": "32bit3412",
                            "direction": "in",
                            "description": "Дискретные данные",
                            "buffer": {
                                "enable": true,
                                "size": 30
                            },
                            "bitMap": [
                                {
                                    "bit": 0,
                                    "description": "РКС1",
                                    "on": "",
                                    "off": "",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M01"
                                        },
                                        {
                                            "key": "DescritInput",
                                            "value": "RKS1"
                                        }
                                    ]
                                },
                                {
                                    "bit": 1,
                                    "description": "РКС2",
                                    "on": "",
                                    "off": "",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M01"
                                        },
                                        {
                                            "key": "DescritInput",
                                            "value": "RKS2"
                                        }
                                    ]
                                },
                                {
                                    "bit": 2,
                                    "description": "КФ1",
                                    "on": "",
                                    "off": "М01 НЕТ КФ1",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M01"
                                        },
                                        {
                                            "key": "DescritInput",
                                            "value": "KF1"
                                        }
                                    ]
                                },
                                {
                                    "bit": 3,
                                    "description": "КФ2",
                                    "on": "",
                                    "off": "М01 НЕТ КФ2",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M01"
                                        },
                                        {
                                            "key": "DescritInput",
                                            "value": "KF2"
                                        }
                                    ]
                                },
                                {
                                    "bit": 4,
                                    "description": "РКС1",
                                    "on": "",
                                    "off": "",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M02"
                                        },
                                        {
                                            "key": "DescritInput",
                                            "value": "RKS1"
                                        }
                                    ]
                                },
                                {
                                    "bit": 5,
                                    "description": "РКС2",
                                    "on": "",
                                    "off": "",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M02"
                                        },
                                        {
                                            "key": "DescritInput",
                                            "value": "RKS2"
                                        }
                                    ]
                                },
                                {
                                    "bit": 6,
                                    "description": "КФ1",
                                    "on": "",
                                    "off": "М02 НЕТ КФ1",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M02"
                                        },
                                        {
                                            "key": "DescritInput",
                                            "value": "KF1"
                                        }
                                    ]
                                },
                                {
                                    "bit": 7,
                                    "description": "КФ2",
                                    "on": "",
                                    "off": "М01 НЕТ КФ2",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M02"
                                        },
                                        {
                                            "key": "DescritInput",
                                            "value": "KF2"
                                        }
                                    ]
                                },
                                {
                                    "bit": 8,
                                    "description": "M01 Авария РКС1",
                                    "on": "АВАРИЯ РКС1",
                                    "off": "",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M01"
                                        },
                                        {
                                            "key": "Alarms",
                                            "value": "RKS"
                                        }
                                    ]
                                },
                                {
                                    "bit": 9,
                                    "description": "M01 Авария РКС2",
                                    "on": "АВАРИЯ РКС2",
                                    "off": "",
                                    "buffer": {
                                        "enable": true
                                    },
                                    "properties": [
                                        {
                                            "key": "mech",
                                            "value": "M01"
                                        },
                                        {
                                            "key": "Alarms",
                                            "value": "RKS"
                                        }
                                    ]
                                }
                            ],
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

> http://127.0.0.1:7283/api/itemgroups?main=mech&sub=temperature,pressure,DescritInput,Alarms&meta=true

## **Ответ**

```json
HTTP/1.1 200 OK
Content-Type: application/json; charset=UTF-8
Date: Tue, 01 Dec 2020 03:56:20 GMT
Connection: close
Transfer-Encoding: chunked

{
  "status": "ok",
  "message": "",
  "data": [
    {
      "value": "M01",
      "groups": [
        {
          "value": "temperature",
          "items": [
            {
              "actual": true,
              "idItem": 2,
              "value": "16914",
              "description": "M01 Температура2",
              "lastResponse": "2020.12.01-10:56:20.929",
              "lastchange": "2020.12.01-10:56:20.929",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "temperature",
                  "value": "t2"
                }
              ],
              "buffer": [
                {
                  "value": "16914",
                  "lastChange": "2020.12.01-10:56:20.929"
                },
                ...
              ]
            },
            {
              "actual": true,
              "idItem": 1,
              "value": "-15282",
              "description": "M01 Температура1",
              "lastResponse": "2020.12.01-10:56:20.929",
              "lastchange": "2020.12.01-10:56:20.929",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "temperature",
                  "value": "t1"
                }
              ],
              "buffer": [
                {
                  "value": "-15282",
                  "lastChange": "2020.12.01-10:56:20.929"
                },
                ...
              ]
            }
          ],
          "bitMap": []
        },
        {
          "value": "pressure",
          "items": [
            {
              "actual": true,
              "idItem": 6,
              "value": "226.25",
              "description": "M01 Давление2",
              "lastResponse": "2020.12.01-10:56:20.929",
              "lastchange": "2020.12.01-10:56:20.929",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "pressure",
                  "value": "p2"
                }
              ],
              "buffer": [
                {
                  "value": "226.25",
                  "lastChange": "2020.12.01-10:56:20.929"
                },
                ...
              ]
            },
            {
              "actual": true,
              "idItem": 5,
              "value": "4783",
              "description": "M01 Давление1",
              "lastResponse": "2020.12.01-10:56:20.929",
              "lastchange": "2020.12.01-10:56:20.929",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "pressure",
                  "value": "p1"
                }
              ],
              "buffer": [
                {
                  "value": "4783",
                  "lastChange": "2020.12.01-10:56:20.929"
                },
                ...
              ]
            }
          ],
          "bitMap": []
        },
        {
          "value": "DescritInput",
          "items": [],
          "bitMap": [
            {
              "bit": 1,
              "actual": true,
              "value": true,
              "idItem": 543,
              "text": "",
              "description": "РКС2",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.19.650",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "DescritInput",
                  "value": "RKS2"
                }
              ],
              "buffer": [
                {
                  "value": "1",
                  "lastChange": "2020.12.01-10.56.19.650"
                },
                ...
              ]
            },
            {
              "bit": 2,
              "actual": true,
              "value": false,
              "idItem": 543,
              "text": "М01 НЕТ КФ1",
              "description": "КФ1",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.20.995",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "DescritInput",
                  "value": "KF1"
                }
              ],
              "buffer": [
                {
                  "value": "0",
                  "lastChange": "2020.12.01-10.56.20.995"
                },
                ...
              ]
            },
            {
              "bit": 3,
              "actual": true,
              "value": false,
              "idItem": 543,
              "text": "М01 НЕТ КФ2",
              "description": "КФ2",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.20.995",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "DescritInput",
                  "value": "KF2"
                }
              ],
              "buffer": [
                {
                  "value": "0",
                  "lastChange": "2020.12.01-10.56.20.995"
                },
                ...
              ]
            },
            {
              "bit": 0,
              "actual": true,
              "value": true,
              "idItem": 543,
              "text": "",
              "description": "РКС1",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.20.995",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "DescritInput",
                  "value": "RKS1"
                }
              ],
              "buffer": [
                {
                  "value": "1",
                  "lastChange": "2020.12.01-10.56.20.995"
                },
                ...
              ]
            }
          ]
        },
        {
          "value": "Alarms",
          "items": [],
          "bitMap": [
            {
              "bit": 9,
              "actual": true,
              "value": true,
              "idItem": 543,
              "text": "АВАРИЯ РКС2",
              "description": "M01 Авария РКС2",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.20.995",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "Alarms",
                  "value": "RKS"
                }
              ],
              "buffer": [
                {
                  "value": "1",
                  "lastChange": "2020.12.01-10.56.20.995"
                },
                ...
              ]
            },
            {
              "bit": 8,
              "actual": true,
              "value": true,
              "idItem": 543,
              "text": "АВАРИЯ РКС1",
              "description": "M01 Авария РКС1",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.19.650",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M01"
                },
                {
                  "key": "Alarms",
                  "value": "RKS"
                }
              ],
              "buffer": [
                {
                  "value": "1",
                  "lastChange": "2020.12.01-10.56.19.650"
                },
                ...
              ]
            }
          ]
        }
      ]
    },
    {
      "value": "M02",
      "groups": [
        {
          "value": "temperature",
          "items": [
            {
              "actual": true,
              "idItem": 3,
              "value": "30626",
              "description": "M02 Температура1",
              "lastResponse": "2020.12.01-10:56:20.929",
              "lastchange": "2020.12.01-10:56:20.929",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M02"
                },
                {
                  "key": "temperature",
                  "value": "t1"
                }
              ],
              "buffer": [
                {
                  "value": "30626",
                  "lastChange": "2020.12.01-10:56:20.929"
                },
                ...
              ]
            },
            {
              "actual": true,
              "idItem": 4,
              "value": "27657",
              "description": "M02 Температура2",
              "lastResponse": "2020.12.01-10:56:20.929",
              "lastchange": "2020.12.01-10:56:20.929",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M02"
                },
                {
                  "key": "temperature",
                  "value": "t2"
                }
              ],
              "buffer": [
                {
                  "value": "27657",
                  "lastChange": "2020.12.01-10:56:20.929"
                },
                ...
              ]
            }
          ],
          "bitMap": []
        },
        {
          "value": "pressure",
          "items": [
            {
              "actual": true,
              "idItem": 7,
              "value": "9.444445",
              "description": "M02 Давление1",
              "lastResponse": "2020.12.01-10:56:20.929",
              "lastchange": "2020.12.01-10:56:20.929",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M02"
                },
                {
                  "key": "pressure",
                  "value": "p1"
                }
              ],
              "buffer": [
                {
                  "value": "9.444445",
                  "lastChange": "2020.12.01-10:56:20.929"
                },
                ...
              ]
            },
            {
              "actual": true,
              "idItem": 8,
              "value": "0",
              "description": "M02 Давление2",
              "lastResponse": "2020.12.01-10:56:20.929",
              "lastchange": "2020.12.01-10:56:20.629",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M02"
                },
                {
                  "key": "pressure",
                  "value": "p2"
                }
              ],
              "buffer": [
                {
                  "value": "0",
                  "lastChange": "2020.12.01-10:56:20.629"
                },
                ...
              ]
            }
          ],
          "bitMap": []
        },
        {
          "value": "DescritInput",
          "items": [],
          "bitMap": [
            {
              "bit": 7,
              "actual": true,
              "value": false,
              "idItem": 543,
              "text": "М01 НЕТ КФ2",
              "description": "КФ2",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.20.650",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M02"
                },
                {
                  "key": "DescritInput",
                  "value": "KF2"
                }
              ],
              "buffer": [
                {
                  "value": "0",
                  "lastChange": "2020.12.01-10.56.20.650"
                },
                ...
              ]
            },
            {
              "bit": 6,
              "actual": true,
              "value": false,
              "idItem": 543,
              "text": "М02 НЕТ КФ1",
              "description": "КФ1",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.19.650",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M02"
                },
                {
                  "key": "DescritInput",
                  "value": "KF1"
                }
              ],
              "buffer": [
                {
                  "value": "0",
                  "lastChange": "2020.12.01-10.56.19.650"
                },
                ...
              ]
            },
            {
              "bit": 5,
              "actual": true,
              "value": true,
              "idItem": 543,
              "text": "",
              "description": "РКС2",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.19.650",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M02"
                },
                {
                  "key": "DescritInput",
                  "value": "RKS2"
                }
              ],
              "buffer": [
                {
                  "value": "1",
                  "lastChange": "2020.12.01-10.56.19.650"
                },
                ...
              ]
            },
            {
              "bit": 4,
              "actual": true,
              "value": true,
              "idItem": 543,
              "text": "",
              "description": "РКС1",
              "lastResponse": "2020.12.01-10:56:20.984",
              "lastchange": "2020.12.01-10.56.20.995",
              "tags": [],
              "properties": [
                {
                  "key": "mech",
                  "value": "M02"
                },
                {
                  "key": "DescritInput",
                  "value": "RKS1"
                }
              ],
              "buffer": [
                {
                  "value": "1",
                  "lastChange": "2020.12.01-10.56.20.995"
                },
                ...
              ]
            }
          ]
        },
        {
          "value": "Alarms",
          "items": [],
          "bitMap": []
        }
      ]
    }
  ]
}
```
