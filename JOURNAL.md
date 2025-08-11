---
title: "NexoBT"
author: "Giacomo Rossi - @giacomo"
description: "Bluetooth receiver based on an ESP, fitted on my own PCB design."
created_at: "2025-05-28"
---
# Preamble:

I started this project for Highway but I didn't have time to finish it.

It could be noted how scarce updates this is because I usually work for projects in your free time for a few minutes and therefore groups small progress in a single more full -bodied update
For the same reason, the hours I spent are approximate but to say socially no less than 36 hours spent on this project.

I hope that this does not cost me the exclusion from the Grant (it was a too tiring project to carry out so as not to present it anyway even if I know of these critical issues)

----------------------------------------------------------

# DAY 1 - 19/06/2025 6H
* Today I started creating the PCB, more specifically the power supply:
    It will be a diet with 2 voltages, one at 5v atraverse a connector to Barrell Jack, an interruption a status LED and several filter capacitors, the other at     3.3v useful for the ESP obtained at the time the use of an AMS 1117 - 3.3. (**2H**)
![Schematic with power supply](https://github.com/user-attachments/assets/98bbded4-5f5f-49db-a1bf-b35c552be6ee "power supply")
* I started thinking about that ESP 32 module to use, I think it is for one with SMA lactacco to use the external antenna. (**1.5H**)
* I decided that for the audio output I do not use the TRS or XLR connectors but of the bipolar connectors so that both types of peripheral can be connected like this: ![XLR / TRS 6mm bipolar conerger](https://github.com/user-attachments/assets/de2226ec-ffe9-4a9e-89d3-1a23ec07308a "XLR / TRS 6mm bipolar conerger")(**1.5H**)
* I evaluated the use of an DAC and I came to the conclusion that it is a necco but I still have to understand which one and how to choose it.(**1H**)

# DAY 2 - 29/06/2025 6H
* I continued by deciding which components to choose(**2H**):
    - Bluetooth processor / receiver-> ESP32-WROOM-32UE-N4
    - Dac anchor to choose from even if I think I choose the PCM 1793 or the PCM1794 
    - I have the doubt because I have to better understand how differential outputs (balanced) work with these chips. 
* I therefore started creating the schematic for the ESP chip: (**2.5H**)
![Schematic Esp Chip](https://github.com/user-attachments/assets/be129c30-39ea-482e-b6cd-d7e4ccb6a5a4 "Schematic Esp Chip")
* I also wired the audio outputs:(**1.5H**)
![Schematic Audio outputs](https://github.com/user-attachments/assets/c5bb6e6c-6190-4684-87f2-7314bb4e24eb "Schematic Audio outputs")

# DAY 3 - 04/07/2025 6H
Maybe I should continue this project more often I'm carrying out a little too little :/ 
* I completely changed my mind on the dac to be used (thanks to the advice of @AAVOJ :D) (**3H** to understand how it work) 
* I use a Max98357a very simple to use and incorporate an amplifier that greatly simplifies the design and makes the PCB cleaner
    - Use 2 chips one for each channel  (**2H**)
    - I prepared a selector for the gain that can be moved via a jumper (**1H**)
    - to select the Visogna channel, set the SD_Mode iìcon Pin a resistance on the right channel while the accident must be high
  ![Schematic MAX98357A](https://github.com/user-attachments/assets/11d15057-435d-42e2-ba1b-bf095407d9d4 "Schematic MAX98357A")
* with the ESP32 processor I still have to understand how I go ahead I'm still stopped 
* I am at a good point Yuppyyy I think the next few days I stop (I have an amnesty exam for the super important university :) ) but I promise it.
* Today the state of the schematic is as follows:
![Schematic_2025-07-04](https://github.com/user-attachments/assets/b6f8e213-8eab-4412-a293-efb934957c75)
* I'm assuming a screen but I don't know :/ 

# DAY 4 - 19/07/2025 6H
There is good news and bad news :)

* I finished the schematic definitively (Yuppie 🥳) (**3H**)
![Schematic_2025-07-19](https://github.com/user-attachments/assets/59e15a65-4536-4feb-9e84-6ba6b0ab8a4e)
* I change complity the elettric supply (**1H**)
* I included an OLED screen (**0.5H**)
* I purchased the necessary hardwere (cards with Max98357a, ESP S3 Devboard, screen) (**1H**)
* I started to create an Alpha version of the software. (**0.5H**)

Here the good news ends:/ (and the bad ones begin)

By creating the software version I planned the start screen and the status of the LEDs but I also discovered that the ESP32S3 chip does not support the Classic Bluethooth but only the BLE and guess the A2DP protocol that is used to transfer laudio between the device and the card is not compatible with the Bluetooth Low Energy but only with the classic.

Therefore:
* I have not finished the schematic (not yuppie)
* I have not ordered all the necessary hardware
* I can't make the final software from it all

But hey my grandfather would say that "è inutile piangere sul latte versato" (it is useless to cry on the spilled milk) , you have to learn from errors so now I change chip, I refer the schematic, I order the right chip and I finish this project!

(At least I hope ahaha)

# DAY 5 - 26/07/25 3H

Today is the turning day:

* I finished version 2.0 of the PCB (after soperto that lesp s3 was not good) (**2.5H**)
![SCH_NEXOBT_BOARD_1-P1_2025-07-26](https://github.com/user-attachments/assets/adf9ee2b-3472-4611-8261-a7dcd3d94f91).
* Now what should I do?
  - Select the physical components
  - Create the PCB
* I am well under July 31st I will have finished Yuppiiee 
* Here is the Nexo BT logothat I adapted: (**0.5H**)
  ![logo_nexobt](https://github.com/user-attachments/assets/31247463-d115-4a54-9664-ffdcb5320900)
* Here is a video of the animation for now is a prototype the one in which he is turning:

  https://github.com/user-attachments/assets/b4eb3508-a3bb-4f44-8b17-ce57ccbac2f7

# DAY 6 - 6/08/25 6H
Hi, how long has passed since the last update (I was in Rome for the young man's jubilee). But I went back to work on the schematic: 
* I suspended the MAX98357 with a PCM5102AP (**2H**)
* added negative voltage generator and two drivers that transform the signal into two counter -phase audio signals. (**2H**)
![Schematich 06-08-25](https://github.com/user-attachments/assets/4823440a-5964-481c-afe1-efd272693eb5)
![Schematich2 06-08-25](https://github.com/user-attachments/assets/55aab46b-aa77-48a4-a717-7992b12338c9)
* The schematic has changed a lot:
      -  I started positioning the components on the PCB and also started connecting the very first cables. (**2H**)
![PCB 06-08-25](https://github.com/user-attachments/assets/d44f8234-54a2-4e23-970d-52f1ea8b4215)

# DAY 7 - 9/08/25 3H
Here we are at the end 
Yesterday I finished drawing the PCB and today I nominated it for a Grounded voucher.
* I finished connecting the components (**2H**)
* I designed the mass plan and the 3.3v (A&B) labor pine pines (**0.5H**)
* I designed the polygons for the power line and checked that everything was correct (**0.5H**)
* I checked the price 136.60 euros wow

I Think That I SPEND SOMTHING LIKE 36H ON THIS PROJECT.
