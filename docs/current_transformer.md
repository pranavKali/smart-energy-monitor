# Current Transformer

## What is a Current Transformer?

A Current Transformer, or CT, is a sensor used to measure AC current.

It lets us measure current without putting the ESP32 or ADE7880 directly in the main power path.

## Why We Need It

Wall electricity can have high current.

The ADE7880 cannot safely measure large current directly.

The CT converts large AC current into a much smaller signal that the ADE7880 can read.

## Simple Idea

```text
Large AC Current
      ↓
Current Transformer
      ↓
Small Analog Signal
      ↓
ADE7880
