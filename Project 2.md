**The pipeline of the project:**

Input from IMU's + Other Data ==> RL Model ==> Outputs - ( Motor values )  ==> Action is performed and validated ==> correct the RL Model ==> Inputs

This is a closed loop control system

*We need to figure out ways to connect 19 IMUs to the MCU (say Arduino UNO):*

**About MPU-6050**:

The IMU used is MPU-6050.
The IMU sensor works based on I2C communivation.

The sensor has VCC, GND, SCL (Serial Clock Line), SDA (Serial Data Address) and AD0 pin primarily.
The SCL pin on sensor is connected to the SCL pin on Arduino (which is the analog pin A5), SDA pin on sensor is connected to the SDA pin on Arduino (which is the analog pin A4).

Each type of an IMU sensor has an unique address, when AD0 pin is set to HIGH, it will have an I2C address of 0x69, whereas when the AD0 is set to LOW or when it is not connected, it will have an address of 0x68.

**The Problem : Connecting multiple I2C sensors with SAME address**

The solutions I have found so far:

* *Using different types of MCUs*:

This would solve the purpose as using different IMUs would give us different addresses, thus eliminating our problem. But, it is hard to find 19 different types of IMU sensors.

* *The trick*:

The trick is to put all the IMUs on the I2C bus, and connect IMU's AD0 pin to a seperate digital pin on the Arduino. The crux is, when you want to read from a specific IMU, set all AD0s to HIGH, except the one you want to read to LOW. All the IMUs with AD0s set to HIGH will have an address of 0x69, whereas the only one on LOW will have an address of 0x68. Thus, now we are able to differentiate the IMU from which we want to read values from, and the rest.

Now, this leads us to ONE MORE problem:

We will need 19 Arduino pins to connect to the  









