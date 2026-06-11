# ESP32 Overview

## What is the ESP32?

The ESP32 is a microcontroller.

A microcontroller is a tiny computer on a chip.

Just like your laptop has a CPU, memory, and input/output connections, the ESP32 contains those things in a much smaller form.

## What Will the ESP32 Do?

In this project the ESP32 will:

1. Talk to the ADE7880
2. Read energy measurements
3. Connect to Wi-Fi
4. Send data to a dashboard

## Why Not Use Only the ESP32?

The ESP32 is good at:

- Running code
- Communicating
- Wi-Fi
- Bluetooth

The ADE7880 is good at:

- Measuring electricity
- Calculating power
- Calculating energy usage

Using both chips gives us the best solution.

## Inputs and Outputs

The ESP32 has pins.

Pins can:

- Send signals
- Receive signals
- Communicate with sensors
- Communicate with chips

## Project Role

```text
ADE7880
    │
    ▼
ESP32
    │
    ▼
Wi-Fi
    │
    ▼
Phone Dashboard
```

The ESP32 acts as the bridge between the ADE7880 and the internet.

## Future Tasks

- Learn ESP32 pins
- Learn SPI communication
- Write firmware
- Connect to Wi-Fi
