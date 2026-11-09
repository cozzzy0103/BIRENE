 #include <Servo.h>

Servo myServo;

const int switchPin = 8;
const int servoPin = 9;

void setup() {
  pinMode(switchPin, INPUT);
  myServo.attach(servoPin);
  myServo.write(0);
}

void loop() {
  if (digitalRead(switchPin) == HIGH) {
    myServo.write(90);
  } else {
    myServo.write(0);
  }
}
