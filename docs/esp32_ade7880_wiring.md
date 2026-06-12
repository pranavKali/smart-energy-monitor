## Isolation Layer

The ESP32 does not communicate directly with the ADE7880.

A digital isolator sits between the devices.

```text
ADE7880
   │
SPI
   │
Digital Isolator
   │
SPI
   │
ESP32
```

Purpose:

* Electrical isolation
* Improved safety
* Protection against ground potential differences
* Noise reduction

```
```
