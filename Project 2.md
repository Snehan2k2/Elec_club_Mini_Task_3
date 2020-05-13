**The pipeline of the project:**

Input from IMU's + Other Data ==> RL Model ==> Outputs - ( Motor values )  ==> Action is performed and validated ==> correct the RL Model ==> Inputs

This is a closed loop control system

*We need to figure out ways to connect 19 IMUs to the MCU (say Arduino UNO):*

The IMU used is MPU-6050.
The IMU sensor works based on I2C communivation.

The sensor has VCC, GND, SCL (Serial Clock Line), SDA (Serial Data Address) and AD0 pin primarily.
The SCL pin on sensor is connected to the SCL pin on Arduino (which is the analog pin A5), SDA pin on sensor is connected to the SDA pin on Arduino (which is the analog pin A4).

Each type of an IMU sensor has an unique address, when AD0 pin is set to HIGH, it will have an I2C address of 0x69, whereas when the AD0 is set to LOW, it will have an address of 0x68.







