int buzzer= 4;
int high_led=12;
int medium_led=14;
int low_led=27;
#define trig 22
#define echo 23
long duration;
float distance;

void setup(){
  Serial.begin(115200);
  pinMode(high_led, OUTPUT);
  pinMode(medium_led, OUTPUT);
  pinMode(low_led, OUTPUT);
  pinMode(buzzer, OUTPUT);
  pinMode(trig, OUTPUT);
  pinMode(echo, INPUT);
}

void loop(){
  digitalWrite(trig, LOW);
  delayMicroseconds(2);
  digitalWrite(trig, HIGH);
  delayMicroseconds(10);
  digitalWrite(trig, LOW);

  duration=pulseIn(echo,HIGH);
  distance=duration*0.034/2;
  
  Serial.println("Distance: ");
  Serial.println(distance);
  Serial.println(" Cm");

  if(distance>20) {
    digitalWrite(low_led,HIGH);
    digitalWrite(buzzer, LOW);
    Serial.println("water Level: Low ");  
  }
  else if (distance<10){
    digitalWrite(medium_led, HIGH);
    digitalWrite(buzzer, LOW);
    Serial.println("Water Level: Medium ");
  }
  else{
    digitalWrite(high_led, HIGH);
    digitalWrite(buzzer, HIGH);
    delay(500);
    Serial.println("Water Level: High ");
  
  }
  delay(2000);
}
