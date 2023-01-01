//Pisao: Djordje Kostic
/*
 * 3D Robotska ruka
 * 
 */
#include <Servo.h>

Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;

int joy1 = 0;
int joy2 = 1;
int joy3 = 2; 
int joy4 = 3;

int pot1;
int pot2;
int pot3;
int pot4;
void setup() {
  servo1.attach(3);
  servo2.attach(5);
  servo3.attach(9);
  servo4.attach(10);

}

void loop() {
  pot1 = analogRead(joy1);
  pot1 = map(pot1, 0, 1023, 0, 180);
  servo1.write(pot1);

  pot2 = analogRead(joy2);
  pot2 = map(pot2, 0, 1023, 0, 180);
  servo2.write(pot2);

  pot3 = analogRead(joy3);
  pot3 = map(pot3, 0, 1023, 0, 180);
  servo3.write(pot3);

  pot4 = analogRead(joy4);
  pot4 = map(pot4, 0, 1023, 0, 180);
  servo4.write(pot4);
}
