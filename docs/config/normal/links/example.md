# Пример

```json
{
    "links": [
        {
            "id": 3,
            "name": "SerialConnection",
            "description": "usb1",
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
                    "description": "device name",
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
            "name": "TCPConnection",
            "description": "tcp502",
            "protocol": "mb-tcp",
            "port": "502",
            "ip": "192.168.22.132",
            "timeoutMs": 100,
            "reqestMs": 100,
            "devices": [
                {
                    "id": 22,
                    "address": 156,
                    "description": "device 2",
                    "groupRequest": "all",
                    "items": [
                        {
                            "id": 543,
                            "enable": true,
                            "address": 41,
                            "type": "float3412",
                            "direction": "in",
                            "tags": [
                                "t1",
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
                            "calculate": {
                                "multiplier": 0.6,
                                "offset": -7,
                                "round":{
                                    "enable": true,
                                    "precision":3
                                }
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
