# Temperature_Control_System
This Project is to design temperature control system using two ATMega32 microcontrollers with the help of platformio and proteus.

- Uses SPI communication protocol
- Uses LM35 Temperature Sensor for measurement of temperature
- 16×2 LCD is used to display temperature set point and controls temperature by turning on and off the heater or cooler
- Show warning if the temperature is in the bad state
- Analyze the waveform of motors signal using oscilloscope

# Master Chip
- Receives Actual temperature value (A) from LM35 sensors
- converts the analog value of (A) to digital using ADC
- Prints the digital value of (A) on a 16x2 alphanumeric LCD
- Takes the optimum degree (B) from LCD
- Send digital value of (A) to the slave with the optimum degree (B) through SPI communication protocol

# Slave Chip
- Receives the temperature value from the master through SPI communication protocol
- Turn on the cooler motor for temperatures between (optimum degree (B)+5) and (optimum degree (B)+10) degrees (starting with a
duty cycle of 50% plus 10% for every additional 5 degrees)
- Turn on the heater when the temperature is lower than (optimum-5) degrees and turn on the cooler motor (starting with a
duty cycle of 50% plus 10% for every additional 5 degrees)
- Red warning LED blink when the temperature is higher than (optimum degree (B)+10) degrees and 
- When one motor is on, the other motor should be off

# Design
![GP1](https://github.com/waelmarwan7/TEMPERATURE_CONTROL_SYSTEM/assets/91396631/19d7ce7e-fc26-4e21-b32c-abdc22da5c37)
![GP](https://github.com/AbdelrahmanAbdel-Aal/Temperature_Control_System/assets/87050373/f81f3b27-9392-44d4-9be9-c026356a9c13)

