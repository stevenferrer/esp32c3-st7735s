# esp32c3-st7735s

Fork of [nopnop2002/esp-idf-m5stickC](https://github.com/nopnop2002/esp-idf-m5stickC) (with minimal change) that uses ESP32-C3-mini-1 and 1.8 TFT display.

## Requirements

- [esp-idf](https://github.com/espressif/esp-idf) v5.x

## How to build and flash

```sh
idf.py set-target esp32c3
idf.py -p PORT flash
```

## TFT display

- 1.8 TFT 128x160 LCD display (ST7735)

![tft display](tft-1-8-st7735s.png)

## Tested on the following boards

- ESP32-C3-mini-1

![esp32-c3-mini-1](esp32-c3-mini-1.png)

## Connections

- ESP32-C3, see [1] and [2].

| 1.8 TFT           | ESP32-C3 |
|-------------------|----------|
| LED / Backlight   | 3.3v     |
| SCK / SPI clock   | IO6      |
| SDA / SPI data    | IO7      |
| A0 / Data command | IO4      |
| Reset             | RST      |
| CS / Chip select  | IO10     |
| GND / Ground      | Ground   |
| VCC               | 3.3v     |

## Original README

See [README-m5stickc.md](./README-m5stickc.md).

## References

[1]: Espressif, _ESP32-C3-mini-1 datasheet_, version 2.0, page 11, section 3.2, _Pin Description_, _Table 3: Pin Definitions_, [pdf](https://www.espressif.com/sites/default/files/documentation/esp32-c3-mini-1_datasheet_en.pdf)

[2]: Espressif, _ESP32-C3 reference manual_, version 1.3, page 611, section 27.5.2, _FSPI Bus Signal Mapping_, [pdf](https://www.espressif.com/sites/default/files/documentation/esp32-c3_technical_reference_manual_en.pdf)
