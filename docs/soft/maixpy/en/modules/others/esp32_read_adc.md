---
title: ESP32 ADC
keywords: maixpy, k210, AIOT, edge computing
desc: maixpy  ESP32 ADC
---

## How to use ESP32 to get ADC analog

Since K210 does not have the function of ADC to read analog quantity, this function can only be obtained from hardware such as ESP32 and ESP82XX. The most basic purpose of ADC is to realize a touchable button contact.

### ESP32 sample code

```python
# Uasge see readme.md
# from network_esp32 import wifi

import time, network
from Maix import GPIO
from fpioa_manager import fm

class wifi():
    # IO map for ESP32 on Maixduino
    fm.register(25,fm.fpioa.GPIOHS10)#cs
    fm.register(8,fm.fpioa.GPIOHS11)#rst
    fm.register(9,fm.fpioa.GPIOHS12)#rdy
    print("Use Hareware SPI for other maixduino")
    fm.register(28,fm.fpioa.SPI1_D0, force=True)#mosi
    fm.register(26,fm.fpioa.SPI1_D1, force=True)#miso
    fm.register(27,fm.fpioa.SPI1_SCLK, force=True)#sclk
    nic = network.ESP32_SPI(cs=fm.fpioa.GPIOHS10, rst=fm.fpioa.GPIOHS11, rdy=fm.fpioa.GPIOHS12, spi=1)

print("ESP32_SPI firmware version:", wifi.nic.version())

# get ADC0 ADC1 ADC2
adc = wifi.nic.adc((0,1,2))
print(adc)

while True:
    try:
        # get ADC0~5
        adc = wifi.nic.adc()
    except Exception as e:
        print(e)
        continue
    for v in adc:
        print("%04d" %(v), end=" ")
    print(': adc')

'''
    MicroPython v0.5.1-136-g039f72b6c-dirty on 2020-11-18; Sipeed_M1 with kendryte-k210
    Type "help()" for more information.
    >>>
    raw REPL; CTRL-B to exit
    >OK
    (2370, 3102, 3071)
    2017 2753 0977 2709 0963 0855: adc
    0617 0757 0150 0095 0133 0153: adc
    1319 1478 0955 0939 0698 0619: adc
    2403 3231 3299 3298 1483 0779: adc
    1119 1815 1274 1315 0230 0255: adc
    0951 0951 0295 0283 0319 0399: adc
    2175 2769 2576 2579 1487 1104: adc
    1995 2846 2647 2699 0839 0441: adc
'''
```


### OSError: Get version fail

Just try again, usually esp32 has not been initialized successfully.

```shell
Traceback (most recent call last):
  File "<stdin>", line 15, in <module>
  File "<stdin>", line 24, in wifi
OSError: Get version fail
>
```

### ESP82XX implementation ideas

> The document does not explain this part of the content.

Query the ADC value through AT+SYSADC. In Espressif's ESP82XX AT firmware, the default is GPIO12.

Read the value directly to use.
