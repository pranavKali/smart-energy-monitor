# ESP32 to ADE7880 Wiring

## Basic SPI Connections

```text
ESP32                    ADE7880

3.3V   ----------------> VDD

GND    ----------------> GND

SCLK   ----------------> SCLK

MOSI   ----------------> MOSI

MISO   <---------------- MISO
```

## Purpose of Each Wire

### 3.3V

Provides power to the ADE7880.

### GND

Provides a common electrical reference.

### SCLK

The ESP32 generates clock pulses.

These pulses tell both chips when to send and receive data.

### MOSI

Commands travel from the ESP32 to the ADE7880.

Example:

Read RMS Voltage

### MISO

Measurement data travels from the ADE7880 to the ESP32.

Example:

230.4 Volts RMS

## Data Flow

```text
ESP32
  │
  │ Request Voltage
  ▼
ADE7880
  │
  │ Calculate Measurement
  ▼
ESP32
  │
  │ Send over Wi-Fi
  ▼
Phone Dashboard
```

## Important Note

This is a simplified wiring diagram used for learning.

The real ADE7880 circuit will contain many additional pins and components that we will learn later.
