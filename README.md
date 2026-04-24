# Portable GPS System

A MicroPython-based GNSS display system that parses NMEA data and displays real-time navigation information on an SH1106 OLED screen.

## Features
- **Multi-Constellation Support:** Parses `$GN` and `$GP` sentences for GPS, GLONASS, and Galileo.
- **Real-time Data:** Displays Latitude/Longitude, Altitude, Satellite count, UTC Time, and Speed.
- **Interactive UI:** 5 main pages with specific sub-pages accessible via hardware buttons.
- **Smart Parsing:** - Converts NMEA coordinates to decimal degrees.
  - Calculates continent and hemisphere based on coordinates.
  - Includes an "Everest Comparison" for altitude.

## Hardware Components
- **Microcontroller:** Raspberry Pi Pico (or similar MicroPython board).
- **GPS Module:** Connected via UART (TX: Pin 4, RX: Pin 5).
- **Display:** SH1106 128x64 OLED (I2C: SDA Pin 0, SCL Pin 1).
- **Buttons:** - **Button A (Pin 14):** Change main pages.
  - **Button B (Pin 15):** Enter/Exit sub-pages.

## Software Requirements
- `sh1106.py` library for the OLED display.
- MicroPython firmware installed on the microcontroller.
