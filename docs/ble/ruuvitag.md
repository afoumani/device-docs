# RuuviTag BLE Advertising Format

## Overview

This document describes the BLE advertising data format used by RuuviTag.

## Manufacturer Data

RuuviTag uses manufacturer-specific data in the BLE advertising packet.

Example:

```text
99 04 05 12 FC 53 94 C3 7C 00 04 FF FC 04 0C AC 36 42 00 CD CB B8 33 4C 88 4F

| Byte Offset | Field                | Description                    |
| ----------: | -------------------- | ------------------------------ |
|         0-1 | Manufacturer ID      | Ruuvi manufacturer identifier  |
|           2 | Data Format          | Format identifier              |
|         3-4 | Temperature          | Encoded temperature value      |
|         5-6 | Humidity             | Encoded humidity value         |
|         7-8 | Pressure             | Encoded air pressure value     |
|        9-14 | Acceleration         | X, Y and Z acceleration values |
|       15-16 | Battery + TX Power   | Battery voltage and TX power   |
|          17 | Movement Counter     | Movement counter               |
|       18-19 | Measurement Sequence | Measurement sequence number    |
|       20-25 | MAC Address          | Device MAC address             |
