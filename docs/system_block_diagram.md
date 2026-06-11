# Smart Energy Monitor System Diagram

```text
Wall Outlet
     │
     ▼
Voltage Sensor
     │
     ▼
 ADE7880  ◄──── Current Sensor
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

## Explanation

### Wall Outlet

This is the AC electricity we want to monitor.

### Voltage Sensor

Measures the voltage from the power line and sends a safe signal to the ADE7880.

### Current Sensor

Measures how much current is flowing through the wire and sends a signal to the ADE7880.

### ADE7880

Calculates:

- RMS Voltage
- RMS Current
- Power
- Energy Usage
- Frequency

### ESP32

Reads measurements from the ADE7880 and sends them over Wi-Fi.

### Phone Dashboard

Displays the electrical data to the user.
