# Week 5

### Exercise 1: Control a Servo Motor
_(don't mind my well caffeinated hand)_

https://github.com/user-attachments/assets/b7d453be-0b2e-4f78-9bd9-7054d15977a5

### Exercise 2: Control a Servo with a Potentiometer

https://github.com/user-attachments/assets/4b7a94bb-2ca9-4d0a-9776-0695e60e81eb

Code:

```c++
#include <Servo.h>
Servo myservo;

const int pot = A0;
int potValue = 0;
int servoValue = 0;

void setup() {
  myservo.attach(9);
  Serial.begin(9600);
  pinMode(A0, INPUT);
}

void loop() {
  potValue = analogRead(A0);
  Serial.println(potValue);
  Serial.print(" ");
  servoValue = map(potValue, 0, 1023, 0, 180);
  Serial.println(servoValue);
  myservo.write(servoValue);
}
```

### Exercise 3: Joystick

Here I had a couple of struggles. In the code I came up with first I got confused with the digital and analogRead(). As it later turned out, I also put some cables in the wrong spot. 
Well... thank you for the help with the trouble shooting! 

### Exercise 4: Joystick + 2 Servos

As mentioned above, I had some struggles with the code regarding the reading of the joystick. Once that was fixed, we figured out how to move one servo, but the other one didn't 
want to react. We looked up some tutorials on controlling multiple servos online and found out that obviously only one servo was declared in the beginning, therefore only one could move..

Here is the code:

```c++
#include <Servo.h>
Servo myservo1;
Servo myservo2; // that's what I meant

const int servo1 = 8;
const int servo2 = 7;

const int X = A0;
const int Y = A1;
const int pin = 3;

int stateX = 0;
int stateY = 0;
int statePin = 0;

int servo1Value = 0;
int servo2Value = 0;

void setup() {
  Serial.begin(9600);
  pinMode(X, INPUT);
  pinMode(Y, INPUT);
  pinMode(pin, INPUT_PULLUP);
  myservo1.attach(8);
  myservo2.attach(7);
}

void loop() {
  stateX = analogRead(X);
  stateY = analogRead(Y);
  statePin = digitalRead(pin);

  Serial.print("X:");
  Serial.println(stateX);
  Serial.print("Y:");
  Serial.println(stateY);
  Serial.print("button:");
  Serial.println(statePin);
  Serial.print(" ");
  Serial.println(" ");

  servo1Value = map(stateX, 0, 1023, 0 , 180);
  servo2Value = map(stateY, 0, 1023, 0, 180);

  myservo1.write(servo1Value);
  myservo2.write(servo2Value);
}
```

And here is a super cool video of it!

https://github.com/user-attachments/assets/3a75325b-a6d4-401e-b55a-ef7a1ec48b2d

