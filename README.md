# Temperature_Control_System
This Project is to design temperature control system using two ATMega32 microcontrollers with the help of platformio and proteus.

- Uses SPI communication protocol
- Uses LM35 Temperature Sensor for measurement of temperature
- 16×2 LCD is used to display temperature set point
- It controls temperature by turning on and off the heater or cooler
- Show warning if the temperature is in the bad state
- Analyze the waveform of motors signal using oscilloscope

# Master Chip
- Receives two temperature values A and B from LM35 sensors
- Compares the two values using AC
- As long as A is higher than B, converts the analog value of A to digital using ADC
- Prints the digital value of A on a 16x2 alphanumeric LCD
- Sends the digital value of A to the slave

# Slave Chip
- Receives the temperature value from the master
- Turn on the cooler motor for temperatures between 25 and 55 degrees (starting with a
duty cycle of 50% plus 10% for every additional 5 degrees)
- Turn on the heater when the temperature is lower than 20 degrees
- Red warning LED blink when the temperature is higher than 55 degrees
- When one motor is on, the other motor should be off

# Design
![GP1](https://github.com/waelmarwan7/TEMPERATURE_CONTROL_SYSTEM/assets/91396631/19d7ce7e-fc26-4e21-b32c-abdc22da5c37)
![GP](https://github.com/AbdelrahmanAbdel-Aal/Temperature_Control_System/assets/87050373/f81f3b27-9392-44d4-9be9-c026356a9c13)

