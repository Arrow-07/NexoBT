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
* I continued by deciding which components to choose:
    - Bluetooth processor / receiver-> ESP32-WROOM-32UE-N4
    - Dac anchor to choose from even if I think I choose the PCM 1793 or the PCM1794
    - I have the doubt because I have to better understand how differential outputs (balanced) work with these chips.
* I therefore started creating the schematic for the ESP chip:
![Schematic Esp Chip](https://github.com/user-attachments/assets/be129c30-39ea-482e-b6cd-d7e4ccb6a5a4 "Schematic Esp Chip")
* I also wired the audio outputs:
![Schematic Audio outputs](https://github.com/user-attachments/assets/c5bb6e6c-6190-4684-87f2-7314bb4e24eb "Schematic Audio outputs")

# DAY 3 - 04/07/2025
Maybe I should continue this project more often I'm carrying out a little too little :/
* I completely changed my mind on the dac to be used (thanks to the advice of @AAVOJ :D)
* I use a Max98357a very simple to use and incorporate an amplifier that greatly simplifies the design and makes the PCB cleaner
    - Use 2 chips one for each channel
    - I prepared a selector for the gain that can be moved via a jumper
    - to select the Visogna channel, set the SD_Mode iìcon Pin a resistance on the right channel while the accident must be high
  ![Schematic MAX98357A](https://github.com/user-attachments/assets/11d15057-435d-42e2-ba1b-bf095407d9d4 "Schematic MAX98357A")
* with the ESP32 processor I still have to understand how I go ahead I'm still stopped 
* I am at a good point Yuppyyy I think the next few days I stop (I have an amnesty exam for the super important university :) ) but I promise it.
* Today the state of the schematic is as follows:
![Schematic_2025-07-04](https://github.com/user-attachments/assets/b6f8e213-8eab-4412-a293-efb934957c75)
*I'm assuming a screen but I don't know :/
