<img width="1181" height="728" alt="Nuovo progetto (1)" src="https://github.com/user-attachments/assets/95ea478e-064b-4774-b370-29bfe3cfee88" />

# NexoBT
*Nexo* - in Latin connection - *BT* - Bluetooth. is a bluetooth receiver born from the need to connect a bluetooth audio receiver to a professional audio system with XLR outputs; something that is not very common on the market and so I decided to create it myself.

# How it work?
The project is governed by an ESP32 module (ESP32-WROOM-32UE-N8) which, as A2DP Sink, receives music from a device via Bluetooth and sends it via the I2S protocol to an DAC PCM5102APWR which returns two stereo audio signals.

To obtain the balanced audio signal, a differential driver such as DRV135UA/2K5,
After that the signal is sent to the XLR connector (in this case hybrid because a 6mm TRS connector can also be used)

# Componets:
* ESP32-WROOM-32UE-N8
* DAC PCM5102APW
* Differntial driver DRV135UA/2K5
* predisposition for an i2c OLED display
* 2 LEDs to report the state of nutrition (dual in order to isolate the analogous part from the digital part)
* 1 RGB LED
* Barrel-Jack connector and a switch to choose whether to use the USB-C or the Jack as a power supply.
* A negative voltage generator (ICL7660m/TR) for differential drivers
* A connector to use the remaining pins of the ESP 32 module in the future
* EXTERNAL 2.4GHZ ANTENNA
* protection from static electric discharges on XLR outputs

# Software code
The software is available on Github in code file
I edit one of lybriry that i use.
Also I set the partition scheme to HUGE APP.
----------------------------------------------------

#Render - and photos:
* 3D render from the top
<img width="1176" height="725" alt="immagine_2025-08-09_162942723" src="https://github.com/user-attachments/assets/aa51afb1-a69e-4b4e-8b7d-b5d09f865607" />

* 3D render from the bottom
<img width="1177" height="723" alt="image" src="https://github.com/user-attachments/assets/628735bc-3410-462d-ae27-7cebdb145b95" />

* schematich (Digital parts)
<img width="1287" height="894" alt="image" src="https://github.com/user-attachments/assets/98a15c6a-8336-4dd8-9d1b-6b2b710c9b0c" />

* schematich (Analogic parts)
<img width="1272" height="902" alt="image" src="https://github.com/user-attachments/assets/b1e5b60f-4d16-40d9-92b1-3d58f3a55d48" />
