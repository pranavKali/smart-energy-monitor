## System Architecture

```text
Wall Electricity
      ↓
Current Transformer (CT)
Voltage Sensing Circuit
      ↓
Analog Front End
      ↓
ADE7880
      ↓
SPI
      ↓
Digital Isolator
      ↓
ESP32
      ↓
Wi-Fi
      ↓
Cloud / Dashboard
```

### Team Responsibilities

#### Analog Hardware

* Current transformer interface
* Voltage sensing circuit
* Input filtering
* Isolation circuitry
* ADE7880 hardware design

#### Firmware

* ESP32 firmware
* SPI communication
* ADE7880 register access
* Data acquisition
* Wi-Fi connectivity
* Dashboard integration

```
```
