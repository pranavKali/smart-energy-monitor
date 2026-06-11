# ADE7880 Overview

## What is the ADE7880?

The ADE7880 is a specialized energy metering chip made by Analog Devices.

Its job is to measure electrical quantities from an AC power line and calculate useful information.

Instead of the ESP32 doing all of the complicated math itself, the ADE7880 performs the measurements and calculations internally.

## Measurements Provided

The ADE7880 can measure:

- RMS Voltage
- RMS Current
- Active Power
- Reactive Power
- Apparent Power
- Energy Consumption
- Frequency
- Power Factor

## Why We Are Using It

This project needs accurate energy measurements.

The ADE7880 is designed specifically for power monitoring applications and is much more accurate than trying to measure everything directly with an ESP32.

## Project Role

The ADE7880 will:

1. Receive voltage measurements
2. Receive current measurements
3. Calculate electrical parameters
4. Send measurement data to the ESP32

The ESP32 will then:

1. Read ADE7880 data
2. Connect to Wi-Fi
3. Send data to a dashboard

## Questions To Learn Next

- How does the ADE7880 communicate with a microcontroller?
- What pins are important?
- What is SPI?
- How do voltage sensors connect?
- How do current sensors connect?
