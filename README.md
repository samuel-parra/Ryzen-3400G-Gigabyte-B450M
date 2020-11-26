# Ryzen-3400G-Gigabyte-B450M  

Ryzen 5 3400G Gigabyte B450M DS3H


# Configuration

## Sensor lm-sensors  

Configuration for sensors ITE IT8686E Super IO Sensors  

```
sudo modprobe --verbose it87 force_id=0x8733
```

create file /etc/modprobe.d/it87.conf  
```
options it87 force_id=0x8733  
```
Or add in rc.local  

## Grub
The Grub modificator for Ryzen
```
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"
GRUB_CMDLINE_LINUX="idle=nomwait acpi_enforce_resources=lax iommu=soft"
```

## Audio settings
### Modprobe
in modprobe add  for use dual codec and 7.1 sound

```
options snd-hda-intel model=dual-codecs index=1,0 enable=1
```
### Pulse Audio
in /etc/pulse/daemon.conf  change  
```
; default-sample-channels = 2  

```
to 
```
default-sample-channels = 6  
```