# Irrigation-Timer
Timer based irrigation controller.

This project is to demonstrate a timer based irrigation system using a Raspberry Pi, Arduino uno / Mega and a proprietary backplane with irrigation controller boards.

The Raspberry Pi handles the network, user interface and the higher level program functions.

The Arduino serves as a dedicated hardware controller for the sensors, the backplane and irrigation controller boards.

Communications between the Raspberry Pi and Arduino are interrupt driven, eliminating the need to poll a pin in Arduino.  Raspberry Pi do not support hardware interrupts, so we will still be required to poll the interrupt pin.

All interrupts are dedicated or not shared.

Real Time Clock will be a DS1307, DS3231 or compatitable model to maintain an accurate system time.

Microcontroller temp will be read from internal temperature sensor.

System temperature will be read from onboard temperature sensor.

