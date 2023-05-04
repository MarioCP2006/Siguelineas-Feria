# Siguelineas-Feria
Feria de las Ciencias Jerez 2023

#PROGRAMACIÓN SIGUELÍNEAS:
int sensor1 = 2;
int sensor2 = 3;
int sensor3 = 4;
int sensor4 = 5;
int sensor5 = 6;


int motor1A = 11;
int motor1B = 10;
int motor2A = 9;
int motor2B = 8;

void setup() {
  
  pinMode(sensor1, INPUT);
  pinMode(sensor2, INPUT);
  pinMode(sensor3, INPUT);
  pinMode(sensor4, INPUT);
  pinMode(sensor5, INPUT);

 
  pinMode(motor1A, OUTPUT);
  pinMode(motor1B, OUTPUT);
  pinMode(motor2A, OUTPUT);
  pinMode(motor2B, OUTPUT);
}

void loop() {

  int lectura1 = digitalRead(sensor1);
  int lectura2 = digitalRead(sensor2);
  int lectura3 = digitalRead(sensor3);
  int lectura4 = digitalRead(sensor4);
  int lectura5 = digitalRead(sensor5);

  
  if (lectura2 == LOW && lectura3 == LOW) {
    digitalWrite(motor1A, HIGH);
    digitalWrite(motor1B, LOW);
    digitalWrite(motor2A, HIGH);
    digitalWrite(motor2B, LOW);
  }
  
  else if (lectura1 == LOW) {
    digitalWrite(motor1A, LOW);
    digitalWrite(motor1B, HIGH);
    digitalWrite(motor2A, HIGH);
    digitalWrite(motor2B, LOW);
  }

  else if (lectura5 == LOW) {
    digitalWrite(motor1A, HIGH);
    digitalWrite(motor1B, LOW);
    digitalWrite(motor2A, LOW);
    digitalWrite(motor2B, HIGH);
  }
}


