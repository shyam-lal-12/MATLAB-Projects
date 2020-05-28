# Smart Parking System

Using Simulink environment to develop and implement a Smart Parking System for vehicles that automatically lets in only the desired number of vehicles and prevents any additional vehicles that try to enter. 

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
   1. Servo Motor SG90
   2. LEDs - Green, Red
   3. LCD 1602 module + 220ohm + 10k potentiometer
   4. Bread Board
   5. Jumper wires
### 5. Arduino Board Pins:
   5V   :  LCD module and Servo motor.<br />
   GND  :  LCD module and Servo motor.<br />
   pin 9:  Red LED.<br />
   pin 8:  Green LED.<br />
   pin 2:  Control pin of Servo motor.<br />
   pin 13: Entry button.<br />
   pin 10: Exit button.<br />
   pin 6:  RS pin of LCD module.<br />
   pin 7:  En pin of LCD module. <br />
   pin 8:  D4 pin of LCD module.<br />
   pin 9:  D5 pin of LCD module.<br />
   pin 10: D6 pin of LCD module. <br />
   pin 11: D7 pin of LCD module.<br />
### 6. Functions Used:
   #### Main function:
   To control the entry and exit of vehicles by adjusting the servo arm to raise or lower with LEDs to indicate the entry and exit while maintaining the fixed parking vehicle count.
   1. Normally the Red LED glows indicating the entry is closed with the servo arm lowered.
   2. When the entry button is pressed (indicating a vehicle enters), the function checks for the available parking count and if available, raises the servo arm to let in the vehicle along with Green LED glowing indicating the entry is allowed. After entry, the arm closes and the Red LED light glows while decreasing the available parking count.
   3. When the exit button is pressed (indicating a vehicle exits), the function checks for the atleast 1 vehicle to be present inside the parking and if so, raises the servo arm and Green LED glows and increasing the available parking count. After exit, the arm closes and Red LED glows.
   
   #### LCD function:
   To display the status of the available parking count.
   1. Normally the available parking count will be displayed in the second line of the LCD Display while the first line displays the welcome message, "Welcome!". 
   2. During the entry/ exit button press, when the available parking count reduces, the corresponding count will be displayed in the second line.
