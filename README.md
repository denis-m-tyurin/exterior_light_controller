# exterior_light_controller
Exterior light controller based on Nucleo L073RZ board

Purpose of this project is to create an automatic building light controller which will turn exterior lights on at the sunset time and off at sunrise. 
- It is based on Nucleo L073RZ board with additional LCD display for user interaction.
- An external back-up battery is connected to the board to keep RTC running in case of electricity black-out. 
- A power MOSFET is used to control an external load. PWM is used to soft ramp-up and ramp-down.
- A sunset and sunrise look-up table for a specific region (Nizhny Novgorod, Russia) is hardcoded in this project, which can be easily adjusted for other regions.

Main use case scenario:
1) Connect all parts all together
2) Turn controller on and enter actual date and time
3) Controller will turn external lights on at sunset
4) Controller will turn external lights off at sunrise
5) Controller will show current mode, date and time on its LCD
6) In a case of black-out, controller will be turned off, however RTC will keep runing on the back-up battery. Once electricity is restored, controller will return to normal operations.
