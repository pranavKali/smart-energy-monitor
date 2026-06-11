# Voltage Divider

## What is a Voltage Divider?

A voltage divider is a simple circuit made from resistors.

Its purpose is to reduce a large voltage into a smaller voltage.

## Why We Need It

Wall electricity is dangerous.

The ADE7880 cannot directly accept mains voltage.

We need to scale the voltage down to a safe level before it reaches the ADE7880.

## Simple Idea

```text
230V AC
   ↓
Voltage Divider
   ↓
Small Analog Signal
   ↓
ADE7880
```

## Role in This Project

The voltage divider creates a scaled version of the AC waveform.

The ADE7880 uses this waveform to calculate:

- RMS Voltage
- Power
- Energy Usage
- Frequency

## Beginner Summary

The voltage divider is like a translator.

It converts a large voltage into a small safe voltage that the ADE7880 can measure.
