# Smart Energy Monitor Data Flow

## Complete System Data Path

```text
Wall Electricity
      ↓
Current Transformer (CT)
Voltage Divider (VD)
      ↓
Tiny Analog Signals
      ↓
ADE7880 ADC
      ↓
Digital Numbers
      ↓
DSP
      ↓
RMS / Power Calculations
      ↓
Registers
      ↓
SPI
      ↓
ESP32
      ↓
WiFi
      ↓
Phone Dashboard
```

## Explanation

### Wall Electricity

The AC power we want to monitor.

### Current Transformer (CT)

Measures current without directly connecting the ADE7880 to high current.

### Voltage Divider (VD)

Scales the mains voltage down to a safe level.

### ADE7880 ADC

Converts analog voltage and current waveforms into digital samples.

### DSP

The Digital Signal Processor inside the ADE7880 analyzes the sampled waveforms.

### RMS / Power Calculations

The ADE7880 calculates:

- RMS Voltage
- RMS Current
- Active Power
- Reactive Power
- Apparent Power
- Energy Consumption

### Registers

Results are stored in internal ADE7880 registers.

### SPI

The ESP32 reads the register values using SPI communication.

### ESP32

Processes the data and sends it over Wi-Fi.

### Phone Dashboard

Displays energy usage information to the user.
```
