Fork of the Adafruit Stepper Motor Shield V2 Library, with the 'quickstep()' function implemented, as suggested by "Adafruit Support Bill" over on their forum. This function is similar to the 'onestep()' function, but always functions in the DOUBLE motor mode, and removes the bloat of the microstepping PWM code. This yields a little bit of extra motor speed out of the Shield. Speeds are still pretty limited, but this gives you a little bit more. 

If you are using the AccelStepper library, simply use 'quickstep(FORWARD)' and 'quickstep(BACKWARD)' in place of the 'onestep()' functions when setting up the motor calls. 

Also suggested to increase your I2C bus speed to communicate with the motors faster, you should be able to increase the bus up to 500Khz by adding the line " Wire.setClock(500000L);" to your code after you call 'begin();'

Read more: https://forums.adafruit.com/viewtopic.php?f=31&t=57041&p=292119#p292119
