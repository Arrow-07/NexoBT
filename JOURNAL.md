---
title: "NexoBT"
author: "Giacomo Rossi - @giacomo"
description: "Bluetooth receiver based on an ESP, fitted on my own PCB design."
created_at: "2025-05-28"
---

# DAY 1 - 19/06/2025
* Today I started creating the PCB, more specifically the power supply:
    It will be a diet with 2 voltages, one at 5v atraverse a connector to Barrell Jack, an interruption a status LED and several filter capacitors, the other at     3.3v useful for the ESP obtained at the time the use of an AMS 1117 - 3.3.
![Schematic with power supply](https://github.com/user-attachments/assets/98bbded4-5f5f-49db-a1bf-b35c552be6ee "power supply")
* I started thinking about that ESP 32 module to use, I think it is for one with SMA lactacco to use the external antenna.
* I decided that for the audio output I do not use the TRS or XLR connectors but of the bipolar connectors so that both types of peripheral can be connected like this: ![XLR / TRS 6mm bipolar conerger](https://github.com/user-attachments/assets/de2226ec-ffe9-4a9e-89d3-1a23ec07308a "XLR / TRS 6mm bipolar conerger")
* I evaluated the use of an DAC and I came to the conclusion that it is a necco but I still have to understand which one and how to choose it.

# DAY 2 - 29/06/2025
*I continued by deciding which components to choose:
    -Bluetooth processor / receiver-> ESP32-WROOM-32UE-N4
    -Dac anchor to choose from even if I think I choose the PCM 1793 or the PCM1794
        I have the doubt because I have to better understand how differential outputs (balanced) work with these chips.
*I therefore started creating the schematic for the ESP chip:
![Schematic Esp Chip](https://github.com/user-attachments/assets/be129c30-39ea-482e-b6cd-d7e4ccb6a5a4 "Schematic Esp Chip")
*I also wired the audio outputs:
![Schematic Audio outputs](https://github.com/user-attachments/assets/c5bb6e6c-6190-4684-87f2-7314bb4e24eb "Schematic Audio outputs")
