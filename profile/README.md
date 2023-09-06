# Conductivity Sensor Electronic - Read Me
Welcome to the Organization of my Bachelor's thesis. 

You can find a summary of the project [here](thesis-summary.pdf).

This project was made by Loris Zufferey.

(18.09.2023)
## Ressources
Documents relating to the work can be found:
  1. Source code [here](https://github.com/Bachelor-Work-Zufferey/programation).
  2. Schematic [here](https://github.com/Bachelor-Work-Zufferey/electronic).
  3. Report or other administrative [here](https://github.com/Bachelor-Work-Zufferey/administrative).
## How to use the test bench 
  1. Start the test bench by plugging the provided USB cable
     - Note: You must used this cable, or another one with a USB to TTL serial
  2. Pin 30 and 32 of devkit must be short-circuited
     - Note: This will short-circuit the follower OPAMP
![information2](https://github.com/Bachelor-Work-Zufferey/.github/assets/54267681/9f06b5da-e5b5-4741-bee4-51b29b572153)
  3. The reference sensor must be connected to a 24V voltage supply with the provided cable
  4. Now, data will be send every second to the Raspberry via e'Stream

## How to get and compile the application
  1. Install Zephyr invironment ([Getting started with Zephyr](https://docs.zephyrproject.org/latest/develop/getting_started/index.html) )
  2. Clone the "programmation" repository
  3. Implement your modification
  4. Go to path
````
/zephyrproject/modules/stm32l4xx/drivers/src/stm32l4xx_hal_dac.c
```` 
  6. Delete the lines **812 to 844** as follow:
     ![IMPORTANT_README](https://github.com/Bachelor-Work-Zufferey/.github/assets/54267681/8f7b09ba-82e3-45bb-b8ad-afb4b97a76c9)
  8. Compile your work using [west](https://docs.zephyrproject.org/latest/develop/west/index.html) command.

## Ways to improve measurement methods
  1. Get only the minimum values of the sine measured
  2. Improve calculation of conductivity
  3. Add an average method on the board, by doing the mean value of the N last measures
  4. Add an auto calibration method on the test bench


