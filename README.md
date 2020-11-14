# Ryzen-3400G-Gigabyte-B450M
Ryzen 5 3400G Gigabyte B450M DS3H


# Configuration

## Sensor lm-sensors  

Configuration for sensors ITE IT8686E Super IO Sensors  

```
sudo modprobe --verbose it87 force_id=0x8733
```
create file /etc/modprobe.d/it87.conf
´´´
options it87 force_id=0x8733  

´´´