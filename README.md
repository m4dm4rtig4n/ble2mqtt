# Service to export BLE devices to MQTT with Home Assistant discovery

## !!! It is a very early alpha release !!! Use this software at your own risk.

Default config should be located in `/etc/ble2mqtt.json` or 
can be overridden with `BLE2MQTT_CONFIG` environment variable.

Example run command:

```sh 
BLE2MQTT_CONFIG=./ble2mqtt.json python3 ble2mqtt.py
```

The configuration file is a JSON with the following content:

```json
{
    "mqtt_host": "localhost",
    "mqtt_port": 1883,
    "mqtt_user": "",
    "mqtt_password": "",
 	"devices": [
        {
            "address": "11:22:33:aa:bb:cc",
            "model": "RK-G213S",
            "type": "redmond200"
        }
    ]
}
```

For now only Redmond kettles G2xx are supported. 