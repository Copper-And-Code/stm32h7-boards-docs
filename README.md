# STM32H743 Board Documentation

Photos, schematics, datasheets and demo videos for affordable STM32H743-based
boards supported by [lv_micropython](https://github.com/lvgl/lv_micropython)
(MicroPython with LVGL bindings).

These boards are commonly available on Aliexpress for around 60 EUR and
feature an STM32H743 MCU with external SDRAM, QSPI flash, USB, UART and
RGB display output via the LTDC peripheral.

## Boards

### DEV190806042

| Feature | Specification |
|---------|---------------|
| MCU | STM32H743IIT6 (480 MHz Cortex-M7) |
| SDRAM | 32 MB, 32-bit bus @ 120 MHz |
| QSPI Flash | 32 MB (W25Q256) |
| Display | RGB 24-bit via LTDC (Port I/J/K) |
| Touch | GT911 via SoftI2C |
| USB | Full-Speed CDC |
| SD Card | No |

### FK743M5-XIH6

| Feature | Specification |
|---------|---------------|
| MCU | STM32H743XIH6 (480 MHz Cortex-M7) |
| SDRAM | 32 MB, 16-bit bus @ 120 MHz |
| QSPI Flash | 8 MB (W25Q64) |
| Display | RGB 24-bit via LTDC (mixed ports) |
| Touch | GT911 via SoftI2C |
| USB | Full-Speed CDC |
| SD Card | Yes (SDMMC1) |

### STM32H7_CORE

Available in two hardware revisions with different pin assignments.

| Feature | V1.0 | V1.3 |
|---------|------|------|
| MCU | STM32H743IIT6 (480 MHz Cortex-M7) | same |
| SDRAM | 32 MB, 16-bit bus @ 120 MHz | same |
| QSPI Flash | 16 MB (W25Q128) | same |
| Display | RGB via LTDC (scattered pins) | RGB via LTDC (different pin mapping) |
| Touch | GT911 via HW I2C4 | GT911 via SoftI2C |
| USB | Full-Speed CDC | same |
| SD Card | Yes (SDMMC2) | Yes (SDMMC1) |
| User LED | PC13 | PB0 (red), PB1 (green) |
| User Button | No | PA1 |

## Repository structure

```
├── DEV190806042/
│   ├── photos/
│   └── docs/
│   
├── FK743M5-XIH6/
│   ├── photos/
│   └── docs/
├── STM32H7_CORE/
│   ├── V10/
│   │   ├── photos/
│   │   └── docs/
│   └── V13/
│       ├── photos/
│       └── docs/
└── videos/
```

## Related pull requests

- **Board definitions:** [lvgl/lv_micropython#TBD](https://github.com/lvgl/lv_micropython)
- **LTDC/Touch driver:** [lvgl/lv_binding_micropython#TBD](https://github.com/lvgl/lv_binding_micropython)

## Display panels tested

| Panel | Resolution | Interface | Touch |
|-------|-----------|-----------|-------|
| IPS 1024x600 | 1024 x 600 | RGB 24-bit | GT911 |
| RGB043M2 | 800 x 480 | RGB 24-bit | GT911 |

## License

Documentation and media files in this repository are provided for reference
purposes to support the upstream pull requests.
