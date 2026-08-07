---
title: "TinyPPS"
date: 2026-02-08
tags: ["RP2040", "USB", "PD", "PPS", "Firmware", "Hardware", "power supply"]
categories: ["Electronics", "Projects"]
summary: "A pocket-sized programmable power supply built on USB-C PD and PPS protocols to transform a standard charger into a versatile, programmable bench power supply."
description: "TinyPPS is a pocket-sized programmable power supply built on the USB Power Delivery (PD) standard and the USB Programmable Power Supply (PPS) feature. It transforms a standard USB-C PD charger into a flexible bench-style power source by negotiating selectable output voltages and current limits directly with the charger."
cover:
  image: "cover.webp"
  alt: "TinyPPS cover image"
  relative: true
---

![TinyPPS](fixes_improvements_and_new_features/tinyPPS.webp)

## Key features

TinyPPS now takes advantage of pin-compatible USB PD sink ICs (AP33772 and AP33772S), providing two feature sets within a single firmware, depending on the selected IC:

| Feature | With AP33772s | With AP33772 |
| - | - | - |
| Supported PDO profiles | fixed PDO, PPS | fixed PDO, PPS |
| Output voltage range | 3.3 - 21V | 3.3 - 21V |
| Max output current* | 5A | 5A |
| PPS voltage step size | 100mV/Step | 20mV/Step |
| Programmable current limit | 250mA/Step | 50mA/Step |
| User-switchable output | ✅ | ✅ |
| Over Voltage Protection (OVP) | ✅ → Hard Reset and Auto Restart | ✅ → Auto Restart |
| Over Current Protection (OCP) | ✅ → Output Disable | ✅ → Auto Restart |
| Under Voltage Protection (UVP) | ✅ → Output Disable | ❌ |
| Over temperature protection (OTP)** | ✅ → Output Disable | ✅ → Output Disable |
| Short-Circuit Protection (SCP) | ✅ → Output Disable | ✅ → Output Disable |

**charger and cable dependent*

***OTP is set to 85°C*

For a detailed look at the schematics, PCB design and firmware, visit the [GitHub repository](https://github.com/Deni90/tinyPPS).

## Sponsor time

Huge thank you to **[PCBWay](https://www.pcbway.com)** for providing me PCBs and SMD stencil for free.
![TinyPPS PCB & SMD stencil](tinypps-pcbs-and-smd-stencil.webp)

PCBWay offers high-quality PCBs at affordable prices. The boards are ready to solder straight out of the box, with no leftover tabs that need to be sanded down.
Ordering is super easy: just upload the Gerber files and select the desired parameters.

What I like most is their customer support. They are quick to review orders and don’t just point out issues - they provide detailed explanations on how to address them. Whether it is about a missing Gerber file or out of capabilies issue. At the end, the outcome is always positive.

## Project logs
