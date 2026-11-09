# Week 2

Hi, it is the end of week 4 and I forgot to save most of the files for the exercises (the code) and didn't do any videos so far. Great.
So I will redo it at home..

### Exercise 1: Series Circuit
![Series Circuit](images/serial_circuit.jpeg)
(struggling to upload images, will ad later)

### Exercise 2: Parallel Circuit

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
