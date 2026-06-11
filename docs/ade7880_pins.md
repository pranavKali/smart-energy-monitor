# ADE7880 Important Pins

As a beginner, there are thousands of details in the ADE7880 datasheet.

For now, we only care about 5 important pins.

## 1. VDD

VDD provides power to the ADE7880.

Think of it as the chip's food supply.

## 2. GND

Ground is the return path for electricity.

Every circuit needs a ground connection.

## 3. SCLK

SCLK stands for Serial Clock.

The clock keeps the ADE7880 and ESP32 synchronized while communicating.

Think of it like a metronome keeping two musicians on the same beat.

## 4. MOSI

MOSI stands for:

Master Out Slave In

The ESP32 sends commands to the ADE7880 through this line.

Example:

ESP32 → "Give me the voltage measurement."

## 5. MISO

MISO stands for:

Master In Slave Out

The ADE7880 sends data back to the ESP32 through this line.

Example:

ADE7880 → "Voltage = 230V RMS"

---

## Communication Diagram

```text
ESP32                         ADE7880

MOSI  --------------------->

MISO  <---------------------

SCLK  --------------------->

GND   ----------------------

VDD   ----------------------
```

## What Happens?

1. ESP32 sends a request through MOSI.
2. ESP32 provides clock pulses through SCLK.
3. ADE7880 responds through MISO.
4. ESP32 receives the measurement.
5. ESP32 sends the measurement over Wi-Fi.
