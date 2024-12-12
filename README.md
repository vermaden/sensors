# sensors
```
                                                   __ ____ __
                                                  / //    \\ \
   _____ _____   ____  _____ ____   _  ___ _____ / //  /  / \ \
  /  __//  _  \ /    \/  __//    \ / \/ _//  __// / \     \ / /
  \__  \\  ___//  /  /\__  \\  \  \\   /  \__  \\ \ /  /  // /
 /_____/ \___//__/__//_____/ \____/ \__\ /_____/ \_\\____//_/
```

The **sensors(8)** is script that displays temperatures and other power related information on FreeBSD.

Its inspired by the **sensors(8)** command from the **lm-sensors** Linux package.

### Instalation

```
mkdir -p ~/bin
fetch -o ~/bin/sensors https://raw.githubusercontent.com/vermaden/sensors/master/sensors
chmod +x ~/bin/sensors
```

### Usage

Below you will see examples of **sensors(8)** usage.

![sensors(8) Server Example](https://github.com/vermaden/sensors/raw/master/sensors.server.png)

![sensors(8) Laptop Example](https://github.com/vermaden/sensors/raw/master/sensors.laptop.png)

For comparison here is how the original Linux `sensors(8)` output looks like.

```
[root@rhidm ~]# sensors

coretemp-isa-0000
Adapter: ISA adapter
Core 0:       +35.0°C  (crit = +105.0°C)
Core 1:       +32.0°C  (crit = +105.0°C)

w83l771-i2c-0-4c
Adapter: SMBus nForce2 adapter at 4d00
temp1:        +28.0°C  (low  = -40.0°C, high = +70.0°C)
                       (crit = +85.0°C, hyst = +75.0°C)
temp2:        +37.4°C  (low  = -40.0°C, high = +70.0°C)
                       (crit = +110.0°C, hyst = +100.0°C)
```

... and mine FreeBSD `sensors(8)` output.

```
FreeBSD # sensors

            BATTERY/AC/TIME/FAN/SPEED
 ------------------------------------
               dev.cpu.0.cx_supported: C1/1/1 C2/2/400
                   dev.cpu.0.cx_usage: 0.00% 0.00% last 1000000us
                       dev.cpu.0.freq: 1550
                hw.acpi.cpu.cx_lowest: C1
                powerd(8)/powerdxx(8): disabled

                  SYSTEM/TEMPERATURES
 ------------------------------------
                dev.cpu.0.temperature: 39.7C
                dev.cpu.1.temperature: 39.7C
               dev.cpu.10.temperature: 39.7C
               dev.cpu.11.temperature: 39.7C
               dev.cpu.12.temperature: 39.7C
               dev.cpu.13.temperature: 39.7C
               dev.cpu.14.temperature: 39.7C
               dev.cpu.15.temperature: 39.7C
                dev.cpu.2.temperature: 39.7C
                dev.cpu.3.temperature: 39.7C
                dev.cpu.4.temperature: 39.7C
                dev.cpu.5.temperature: 39.7C
                dev.cpu.6.temperature: 39.7C
                dev.cpu.7.temperature: 39.7C
                dev.cpu.8.temperature: 39.7C
                dev.cpu.9.temperature: 39.7C

                   DISKS/TEMPERATURES
 ------------------------------------
       smart.ada0.temperature_celsius: 40.0C
              smart.nvme0.temperature: 42.0C
```



