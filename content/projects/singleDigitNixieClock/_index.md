---
title: "Single Digit Nixie Clock"
date: 2025-02-20
tags: ["ESP32", "Nixie", "Firmware", "Hardware"]
categories: ["Electronics", "Projects"]
summary: "A single-digit nixie clock combining ESP32, a vintage tube, KiCAD PCBs, and a 3D-printed carbon/brass enclosure."
description: "This project features a single-digit nixie clock that combines a vintage Soviet IN-14 nixie tube from the 1970s with modern electronics. Originally developed on the ESP8266 using the Arduino IDE, the project has been upgraded to the ESP32 platform with ESP-IDF for enhanced performance and stability. The clock is powered from USB type C connector and includes a Real-Time Clock (RTC) module for accurate timekeeping. It offers wireless configuration via a captive portal and synchronizes time using NTP."
cover:
  image: "cover.webp"
  alt: "Single Digit Nixie Clock cover image"
  relative: true
---

![Single Digit Nixie Clock](singleDigitNixieClock.gif)

The hardware design features a two-board stack: the control board integrates the ESP32 with a high-voltage boost converter and RTC, while the display board houses the nixie tube, a BCD-to-decimal decoder and a WS2812B RGB LED.

The enclosure is crafted from a 3D-printed base, overlaid with chopped carbon fiber and accented with brass hardware, drawing inspiration from automotive design.

The firmware is developed in C++ using the ESP-IDF framework.

For a detailed look at the schematics, PCB designs, and firmware, visit the [GitHub repository](https://github.com/Deni90/singleDigitNixieClock)

Below you’ll find project logs:
