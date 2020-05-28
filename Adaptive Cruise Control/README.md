# Adaptive Cruise Control

Using Simulink environment to develop and implement an adaptive cruise control system for vehicles that automatically adjusts the vehicle speed to maintain a safe distance from vehicles ahead. 

### 1. MATLAB version: 
2019a
### 2. Arduino Board: 
Uno R3
### 3. Add-ons Used:
   1. MATLAB Support Package for Arduino Hardware
   2. Simulink Support Package for Arduino Hardware
   3. Arduino_Engineering_Kit_Hardware_Support
   4. Simulink library for Arduino Liquid Crystal Display
### 4. Hardware Components Used:
   1. Ultrasonic Sensor 
   2. Buttons - 5
   3. LCD 1602 module + 220ohm + 10k potentiometer
   4. Bread Board
   5. Jumper wires
### 5. Arduino Board Pins:
   5V   :  Supply for ultrasonic sensor, LCD module.<br />
   GND  :  Ground for ultrasonic sensor, LCD module.<br />
   pin 2:  Trigger for ultrasonic sensor.<br />
   pin 3:  Echo for ultrasonic sensor.<br />
   pin 4:  Button_1 for Cruise Mode.<br />
   pin 12: Button_2 for Increasing Speed.<br />
   pin 13: Button_3 for Decreasing Speed.<br />
   pin 3:  Button_4 for Adaptive Mode (Analog pin).<br />
   pin 5:  Button_5 for Cancel Modes.<br />
   pin 6:  RS pin of LCD module.<br />
   pin 7:  En pin of LCD module. <br />
   pin 8:  D4 pin of LCD module.<br />
   pin 9:  D5 pin of LCD module.<br />
   pin 10: D6 pin of LCD module. <br />
   pin 11: D7 pin of LCD module.<br />
   pin 12: Control pin of Servo motor.<br />
   pin 13: LED pin.<br />
### 6. Functions Used:
   #### Main function:
   Controls and Adjusts the speed of the vehicle based on the obstacle in front along with normal cruise mode(maintaining a constant speed)
   1. When not in any specific modes and wihout pressing the increase or decrease speed buttons, it sends the current speed to the display unit.
   2. When increase/ decrease speed buttons are pressed the function adjusts the current speed accordingly and sends it to the display unit and when the button press is released, the speed slowly decreases to 0.
   3. When Cruise button is pressed, the current speed at the moment is locked and is maintained till the cancel button is pressed while provinding the ability to increase/ decrease the speed using the increase/ decrease buttons and the speed value is sent to the display unit. 
   4. When the Adaptive Cruise button is pressed, the current speed is locked and the ultrasonic sensor starts sensing the obstacles in front of it. When the obstacle is at a distance of 20cm to 10 cm from the vehicle, the speed decreases and if the obstacle is less than 10cm from to the vehicle, the speed decreases faster while continuesly sending the speeds to the display unit.
   
   #### LCD function:
   To display the status of the vehicle speed during different modes of driving.
   1. When in Adaptive Cruise mode the display shows the speed of the vehicle in the second line and displays "ACC Speed:" in the first line while the screen blinks indicating the Adaptive Cruise mode.
   2. When in normal Cruise mode the display shows the speed of the vehicle in the second line while displaying "Cruise Speed:" in the first line.
   3. When not in any specfic modes, the first line displays "Speed:" in the first line and displays the speed of the vehicle in the second line of the display.
