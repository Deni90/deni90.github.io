---
title: "Hardware - Control board [v1]"
date: 2025-01-03
categories: ["Hardware", "Electronics", "NixieClock"]
tags: ["ESP8266", "DS3231", "NCH8200HV", "PCB"]
summary: "Description for the first version of control board"
---

For proof of concept NodeMCU was connected with a DS3231 RTC module on a breadboard. This was enough to start working the firmware. Later, a PCB was created. The PCB is basically a re-packaged NodeMCU design connected with DS3231 and NCH8200HV high voltage boost module board.
![Progression of the Nixie clock control board from protoboard to final PCB](nixie-clock-control-board-progression.gif)

## Schematic
![ESP8266-based control board schematic for single-digit Nixie clock](nixie-clock-control-board-schematic.png)

## PCB
![ESP8266-based control board PCB for single-digit Nixie clock](nixie-clock-control-board-pcb.webp)