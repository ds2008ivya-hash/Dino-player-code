# Dino-player-code
code for your new project GO IN README
SEE BELLOW

here is code copy from below line and paste in arduino ide,And please subscribe our channel. good luck and byyyyy.
#include <Servo.h>

Servo myservo;

int ldrPin = A0;
int ldrValue = 0;
int threshold = 500;   // adjust after testing

void setup() {
  myservo.attach(9);
  Serial.begin(9600);
}

void loop() {
  ldrValue = analogRead(ldrPin);
  Serial.println(ldrValue);

  if (ldrValue < threshold) {
    myservo.write(60);   // press space
    delay(200);
    myservo.write(0);    // release
    delay(300);
  }
}
