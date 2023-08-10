# servo-motor
The servo motor is a motor that comes with a gearbox and a Shaft transmission that gives the movement greater torque and great accuracy, and this motor can turn 180 degrees and in some types 360 degrees. 
## Explanation of the mechanism of action
Black: satisfied.

Red: power source (5V).

Yellow: control, it outputs PWM pulses at a fixed frequency of 50HZ.

![servo](https://github.com/shaikhahObaid/servo-motor/assets/111530370/7770d88d-a1fc-4c47-9d89-c1228c0cdc70)

### controls a specific direction.

A group of pulses with a frequency of 50Hz and the width of the pulse is therefore 20ms total pulse width.

 Very High + Low = 20ms

 
Clockwise: give a high pulse for (0.7 - 1) ms and a low pulse for 19 ms.


Anticlockwise direction: give a high pulse of (1.7 - 2) ms and a low pulse (18 - 18.3).


To reset to position 0: give a high pulse for 1.5ms and a low pulse for 18.5ms

![servo work ](https://github.com/shaikhahObaid/servo-motor/assets/111530370/31c2b14b-a3f2-473c-bc1b-4f2485a1db3a)
## Practical example - servo motor arduino
### Circuit view and simulation 
 ![cir ser](https://github.com/shaikhahObaid/servo-motor/assets/111530370/c7ae493d-80c7-4f5c-a0dc-c5cb5d42da79)
https://www.tinkercad.com/things/4nPLcGSWUz7-neat-maimu/editel?sharecode=OClHN9V2js0XBD4WaJuRQoR1Y-j-2OtsrpVvKvqAOjk

### the code 

#include <Servo.h> // Incluimos la librería para Servo

Servo servoBase;//Asigno un nombre específico

void setup() {


   servoBase.attach(A1);//Pin a utilizar para servo

   
   servoBase.write(0);  //asigno 0 al servo motor
   
}

void loop() {

  for(int i=0; i<=180; i=i+10)
  
  {
  
   servoBase.write(i);

   delay(2000);
   
  }
  
 }
 
