# ESP32 Pin Map

## SPI Connections

| ESP32 Pin | Purpose | ADE7880 Pin |
|------------|----------|-------------|
| GPIO18 | SPI Clock (SCLK) | SCLK |
| GPIO19 | SPI MISO | MISO |
| GPIO23 | SPI MOSI | MOSI |
| GND | Ground | GND |
| 3.3V | Power | VDD |

## Notes

These connections are for the initial prototype.

The final design may change after reviewing the ADE7880 datasheet and hardware requirements.

## Data Flow

```text
ESP32 GPIO23 (MOSI)
          │
          ▼
      ADE7880

ESP32 GPIO19 (MISO)
          ▲
          │
      ADE7880

ESP32 GPIO18 (SCLK)
          │
          ▼
      ADE7880
```
