The pipeline of the project:

Input from IMU's + Other Data ==> RL Model ==> Outputs - ( Motor values )  ==> Action is performed and validated ==> correct the RL Model ==> Inputs

This is a closed loop control system

We need to figure out ways to connect 19 IMUs to the MCU (say Arduino UNO)

The IMU sensor works based on I2C communivation.


