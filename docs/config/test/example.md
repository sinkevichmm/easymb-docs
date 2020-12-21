# **Пример**

## **Файл конфигурации**

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
                    "address": 156,
                    "items": [
                        {
                            "address": 2
                        },
                        {
                            "address": 4
                        },
                        {
                            "address": 6
                        },
                        {
                            "address": 12
                        }
                    ]
                },
                {
                    "address": 157,
                    "items": [
                        {
                            "address": 0
                        },
                        {
                            "address": 2
                        },
                        {
                            "address": 4
                        },
                        {
                            "address": 6
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
                    "address": 1,
                    "items": [
                        {
                            "address": 0
                        },
                        {
                            "address": 17
                        },
                        {
                            "address": 6
                        }
                    ]
                },
                {
                    "address": 39,
                    "items": [
                        {
                            "address": 2
                        },
                        {
                            "address": 4
                        },
                        {
                            "address": 0
                        }
                    ]
                }
            ]
        }
    ]
}
```
