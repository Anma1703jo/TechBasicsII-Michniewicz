# Week 2

Hi, it is the end of week 4 and I forgot to save most of the files for the exercises (the code) and didn't do any videos so far. Great.
So I will redo it at home..

### Exercise 1: Series Circuit
<img width="302" height="403" alt="Image" src="https://github.com/user-attachments/assets/04b24b7a-d1c4-463c-b08f-7af39a5a4102" />

### Exercise 2: Parallel Circuit
<img width="403" height="302" alt="Image" src="https://github.com/user-attachments/assets/5a8cd31b-e66d-4b73-b141-50b7aeb66e67" />

### Exercise 3: Traffic Light
### a: simultaneously
https://github.com/user-attachments/assets/b719e9f5-7a7b-4a19-ac63-13c46a648cfe

Code:

const int RED = 4;
const int YELLOW = 3;
const int GREEN = 2;

void setup() {
  pinMode(RED, OUTPUT);
  pinMode(YELLOW, OUTPUT);
  pinMode(GREEN, OUTPUT);
}

void loop() {
  digitalWrite(RED, HIGH);
  digitalWrite(GREEN, HIGH);
  digitalWrite(YELLOW, HIGH);
  delay(500);
  digitalWrite(RED, LOW);
  digitalWrite(GREEN, LOW);
  digitalWrite(YELLOW, LOW);
  delay(500);
}


### b: in sequence
https://github.com/user-attachments/assets/bc2a5e14-7299-4f8f-be86-0c4ddb8a7b6e

Code:

const int RED = 4;
const int YELLOW = 3;
const int GREEN = 2;

void setup() {
  pinMode(RED, OUTPUT);
  pinMode(YELLOW, OUTPUT);
  pinMode(GREEN, OUTPUT);
}

void loop() {
  digitalWrite(RED, HIGH);
  delay(250);
  digitalWrite(YELLOW, HIGH);
  delay(250);
  digitalWrite(GREEN, HIGH);
  delay(500);
  digitalWrite(RED, LOW);
  delay(250);
  digitalWrite(YELLOW, LOW);
  delay(250);
  digitalWrite(GREEN, LOW);
  delay(500);
}

### Exercise 4

