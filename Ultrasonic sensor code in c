#define TRIG 9
#define ECHO 10
#define LED 7
#define BUZZER 6

long duration;
int distance;

void setup()
{
  pinMode(TRIG, OUTPUT);
  pinMode(ECHO, INPUT);
  pinMode(LED, OUTPUT);
  pinMode(BUZZER, OUTPUT);
  
  Serial.begin(9600);
}

void loop()
{
  digitalWrite(TRIG, LOW);
  delayMicroseconds(2);
  
  digitalWrite(TRIG, HIGH);
  delayMicroseconds(10);
  digitalWrite(TRIG, LOW);
  duration = pulseIn(ECHO, HIGH);
  distance = duration * 0.034 / 2;

  Serial.print("Distance: ");
  Serial.print(distance);
  Serial.println(" cm");

  if(distance <= 10)
  {
    digitalWrite(LED, HIGH);
    digitalWrite(BUZZER, HIGH);
    delay(100);
    digitalWrite(LED, LOW);
    digitalWrite(BUZZER, LOW);
    delay(100);
  }
  else if(distance <= 20)
  {
    digitalWrite(LED, HIGH);
    digitalWrite(BUZZER, HIGH);
    delay(300);
    digitalWrite(LED, LOW);
    digitalWrite(BUZZER, LOW);
    delay(300);
  }
  else if(distance <= 30)
  {
    digitalWrite(LED, HIGH);
    digitalWrite(BUZZER, HIGH);
    delay(600);
    digitalWrite(LED, LOW);
    digitalWrite(BUZZER, LOW);
    delay(600);
  }
  else
  {
    digitalWrite(LED, LOW);
    digitalWrite(BUZZER, LOW);
  }
}