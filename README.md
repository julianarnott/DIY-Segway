# DIY-Segway
Diy Segway using an Arduino Uno, MPU6050, Sabertooth 2x25A and a pair of mobility scooter motors

Schematics and the sketch included. 

You also need to connect the Aref pin to 3.3v

The pots need to be linear (marked with a 'B'). The two trimmer pots either side of the steering pot are just to make life easier to centre the steering column and are not strictly necessary. I used 20 turn trim pots for those.

The value of the pots are not crucial as they just swing the analogue pin between 0 and 3.3v and this is mapped in the code to give the range. Just make sure they're linear. 

When you test it, the mpu6050 should be with the IC facing up. 

The engage switch needs to be on before you power up the Arduino, and the kill cord switch needs to be open circuit. 

Make sure the Arduino is connected up and earthed before powering on the Sabertooth or you can fry the TX pin on the Arduino. 

Make sure the wheels are off the ground before starting it fir the first time and don't upload code to the Arduino whilst the Sabertooth is powered on or the motors go crazy. 

It's kinder to voltage regulator on the Arduino if you don't power it directly from one of the 12v batteries. 

I've used a 9v regulator (7809) here. The 5v output from the Sabertooth is not enough to power the Arduino.

The Sabertooth is using the simplified serial library at 9600 baud rate.

That's the Sabertooth switches set to: 
1 on
2 off
3 on
4 off
5 on
6 on

Check all your wiring before powering on!

I will fork this code once I have completed the latest version utilising a PID algorithm, but for practical reasons I need to test the new code on a small model first.
