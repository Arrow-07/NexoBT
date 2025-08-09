# NexoBT
*Nexo* - in Latin connection - *BT* - Bluetooth. is a bluetooth receiver born from the need to connect a bluetooth audio receiver to a professional audio system with XLR outputs; something that is not very common on the market and so I decided to create it myself.

# Hpw it work?
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
The software is still being developed but it will be made available on Github:
I already develop the initial animation for the display (check on juornal.md )
