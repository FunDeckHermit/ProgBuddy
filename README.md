# ProgBuddy

ProgBuddy is a compact USB 2.0 hub and power-monitoring board designed for practical bench use and embedded USB debugging. It combines a high-side current sensing front end, USB PD passthrough switching, a web interface over USB CDC/NCM, and a small user-facing display for live system status.

## Features

- USB 2.0 hub function with configurable upstream/downstream swap capability
- Accurate current sensing for downstream ports and total hub current
- INA229-based voltage and energy monitoring
- USB PD passthrough with CC-line switching and port control
- Web interface exposed over USB communication device class (CDC/NCM)
- LCD display for live voltages, power, and status information
- Flexible board layout for USB upstream/downstream swapping and reconfiguration

## Design goals

This project is intended to make USB power and debugging data visible and controllable in a single tool. The board is useful for:

- measuring real-time current draw from USB devices
- validating USB PD behavior and pass-through routing
- monitoring port voltage and energy usage
- debugging USB device behavior from a simple web dashboard
- presenting live status on a local panel without needing a separate host tool

## Hardware overview

The system integrates several key functions:

- USB 2.0 hub switching and port routing
- accurate current measurement using dedicated sensing hardware
- bus voltage and energy calculations with the INA229
- USB-C PD passthrough handling with CC switching
- configurable USB upstream/downstream connection options
- local display and status indication

## Firmware and interface

The project exposes a browser-based interface over USB CDC/NCM, allowing inspection and control without a traditional serial adapter stack. This makes it convenient for lab, prototype, and dev-board workflows where a clean USB-connected control path is valuable.

## Typical use cases

- USB port power auditing
- USB device validation and debugging
- PD-aware hub testing
- Bench monitoring for USB-powered electronics
- Controlled power and signal routing in prototypes

## Notes

This repository contains the design files and project documentation for the hardware and embedded firmware work. The board is intended to be configurable and practical, with emphasis on measurement accuracy, USB signal integrity, and operational flexibility.

## Status

This project is an active hardware and firmware design, with emphasis on USB hub functionality, power monitoring, and USB PD passthrough behavior.
