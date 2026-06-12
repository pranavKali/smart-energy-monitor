# Digital Isolation

## Purpose

The smart energy monitor uses digital isolation between the ADE7880 and the ESP32.

The isolation barrier separates the energy metering circuitry from the microcontroller circuitry while still allowing data communication.

## System Architecture

```text
Wall Electricity
      ↓
Current Transformer (CT)
Voltage Sensing Circuit
      ↓
ADE7880
      ↓
SPI
      ↓
Digital Isolator
      ↓
SPI
      ↓
ESP32
      ↓
Wi-Fi
      ↓
Dashboard
```

## Why Isolation Is Needed

The ADE7880 is connected to circuits that measure mains electricity.

To improve safety and robustness, communication between the ADE7880 and ESP32 passes through a digital isolator.

Benefits include:

* Electrical isolation
* Improved safety
* Reduced noise coupling
* Protection against voltage differences between circuit domains
* More reliable communication

## Signals Crossing the Isolation Barrier

The following SPI signals pass through the isolator:

```text
ESP32                Isolator                ADE7880

MOSI   ----------->  Isolated Channel -----> MOSI

MISO   <-----------  Isolated Channel <----- MISO

SCLK   ----------->  Isolated Channel -----> SCLK

CS     ----------->  Isolated Channel -----> SS
```

Ground and power are handled according to the isolator design and are not directly shared across the isolation barrier.

## Firmware Impact

The firmware does not need to know that an isolator exists.

From the ESP32's perspective:

```text
ESP32 SPI Driver
        ↓
ADE7880 Registers
```

The isolator is transparent to software.

## Project Responsibility

### Hardware Team

* Isolator selection
* Schematic design
* PCB implementation
* Signal integrity verification

### Firmware Team

* SPI driver development
* ADE7880 register access
* Measurement acquisition
* Data transmission

## Status

Isolation architecture implemented in hardware schematic.

Firmware development will communicate with the ADE7880 through the isolated SPI interface.
