The components used in the bot are:

**Microcontroller** : Arduino UNO

**Power** : 9V battery

**Chassis** : Made from General Purpose Circuit Board

**Wiring** : Jumpers ( both male to male and male to female )

**Sensors** : 3 Ultrasonic sensors HC-SR 04 (One in the front and two on the sides)

The sensor detects the presence of wall in the three directions

**Motors** : 12V DC motors are used

**Motor driver** : L298N dual H-bridge motor controller (This is used to control both the motors)

The motor driver has ENA and ENB pins (which is used to control the speed of the two motors) which are connected to the PWM pins of Arduino, and 4 IN pins (which is used to turn the two motors clockwise or anti-clockwise) are connected to the digital pins of Arduino.

The 5V pin on the driver is connected to the Vin pin of Arduino, which powers it.




