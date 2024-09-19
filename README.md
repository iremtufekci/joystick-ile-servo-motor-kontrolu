# joystick-ile-servo-motor-kontrolu

#include <Servo.h>
Servo motor;
int deger;
int derece;

void setup() {
  // put your setup code here, to run once:
motor.attach(3);
}

void loop() {
  // put your main code here, to run repeatedly:
deger=analogRead(A0);
derece=map(deger,0,1023,0,180);
motor.write(derece);

}
