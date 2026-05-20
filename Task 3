const int happyFSR = A0;
const int sadFSR = A1;
const int winFSR = A2;

const int buzzer = 10;

const int happyLed = 2;
const int sadLed = 3;

void setup() {
  pinMode(happyFSR, INPUT);
  pinMode(sadFSR, INPUT);
  pinMode(winFSR, INPUT);
  pinMode(buzzer, OUTPUT);

  pinMode(happyLed, OUTPUT);
  pinMode(sadLed, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int input1 = analogRead(happyFSR);
  int input2 = analogRead(sadFSR);
  int input3 = analogRead(winFSR);

  if (input1 > 100){
    digitalWrite(happyLed, HIGH);
    happySound();
    delay(2000);
    digitalWrite(happyLed, LOW);
    delay(1000);
  }
  Serial.println(input1);

  if (input2 > 100){
    digitalWrite(sadLed, HIGH);
    sadSound();
    delay(2000);
    digitalWrite(sadLed, LOW);
    delay(1000);
  }
  Serial.println(input2);

  if (input3 > 100){
    winSound();
  }
  Serial.println(input3);

}

void happySound() {
  tone(buzzer, 523);
  delay(150);

  tone(buzzer, 659);
  delay(150);

  tone(buzzer, 784);
  delay(150);

  tone(buzzer, 1047);
  delay(300);

  noTone(buzzer);
  delay(100);
}

void sadSound() {
  tone(buzzer, 392);
  delay(300);

  tone(buzzer, 349);
  delay(300);

  tone(buzzer, 294);
  delay(500);


  noTone(buzzer);
  delay(100);
}


void winSound() {
  tone(buzzer, 523);
  delay(150);

  tone(buzzer, 659);
  delay(150);

  tone(buzzer, 784);
  delay(150);

  tone(buzzer, 1047);
  delay(300);

  tone(buzzer, 784);
  delay(150);

  tone(buzzer, 1047);
  delay(500);

  noTone(buzzer);
}
