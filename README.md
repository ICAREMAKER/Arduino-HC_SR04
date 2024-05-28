# Arduino-HC_SR04 ![arduinoThumb](https://github.com/ICAREMAKER/Arduino-HC_SR04/assets/107696317/bb841dbb-29c7-422d-b47c-a2a599ede986) ![C++-Logo wine](https://github.com/ICAREMAKER/Arduino-HC_SR04/assets/107696317/a405d046-5961-4827-bcb3-4f0c21265742)

## Preview
![HCSR04](https://github.com/ICAREMAKER/Arduino-HC_SR04/assets/107696317/6c0422e0-ac34-4e65-92c6-ac16043b499f)

## Code
```C
int duration, trigPin = 6, echoPin = 7;

void setup() {
  Serial.begin(9600);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);;
  delay(5000);
}

void loop() {
    EchoSonic();
    Serial.println(cm);
```

```C
void EchoSonic() {
  digitalWrite(trigPin, LOW);
  delayMicroseconds(5);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(15);
  digitalWrite(trigPin, LOW);
  duration = pulseIn(echoPin, HIGH);
  cm = duration / 58;
```
