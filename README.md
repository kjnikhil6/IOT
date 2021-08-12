## Hi
I'm NIKHIL KJ,Undergraduate @ GEC PKD
<br/>
<br/>
### Expt 1:LED Blinking
<br/>

```c
int ledPin = 4;
void setup() {
  pinMode(ledPin,OUTPUT);
}

void loop() {
  digitalWrite(ledPin,HIGH);
  delay(1000);
  digitalWrite(ledPin,LOW);
  delay(1000);
}
```

<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/JToYQKcGWNk" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->

<br/>
<br/>

### Expt 2:Traffic Light

<br/>
<br/>

```c
int rLED = 13;
int yLED = 8;
int gLED = 2;
int i;
void setup() {
  pinMode(rLED,OUTPUT);
  pinMode(yLED,OUTPUT);
  pinMode(gLED,OUTPUT);
}

void loop() {
  digitalWrite(gLED,HIGH);
  delay(5000);
  digitalWrite(gLED,LOW);
  
  for(i=0;i<3;i++){
    delay(500);
    digitalWrite(yLED,HIGH);
    delay(500);
    digitalWrite(yLED,LOW);
  }
  delay(500);
  digitalWrite(rLED,HIGH);
  delay(5000);
  digitalWrite(rLED,LOW);
  
}
```
<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/Wa89EvzFB1U" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
<br/>
<br/>

### Expt 3:LED Chasing Effect
<br/>

```c
int BASE =2;
int NUM =5;
int dTime=200;

void CHASING(int POWER){
  for(int i =BASE;i<BASE+NUM;i++){
    digitalWrite(i,POWER);
    delay(dTime);
  }
}
void setup() {
  // put your setup code here, to run once:
  for(int i =BASE;i<BASE+NUM;i++){
    pinMode(i,OUTPUT);
  }
}

void loop() {
  // put your main code here, to run repeatedly:
  
  CHASING(HIGH);
  CHASING(LOW);

}
```
<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/sk6itZsqzhE" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
<br/>
<br/>

### Expt 4:RGB LED
<br/>

```c
String color;
int RedL=3;
int GreenL=6;
int  BlueL=9;
String msg ="Enter the color:";

void RGB(int R, int G , int B){
   analogWrite(RedL,R);
   analogWrite(GreenL,G);
   analogWrite(BlueL,B);
   delay(1200);
}
void setup() {
pinMode(RedL,OUTPUT);
pinMode(GreenL,OUTPUT);
pinMode(BlueL,OUTPUT);
Serial.begin(9600);
}

void loop() {
  //RED
  RGB(255,0,0);
  //GREEN
  RGB(0,255,0);
  //BLUE
  RGB(0,0,255);
  //CYAN
  RGB(0,255,255);
  //YELLOW
  RGB(255,255,0);
  //magenta
  RGB(255,0,255);
  //WHITE
  RGB(255,255,255);
  //
  RGB(125,255,10);
  //
  RGB(170,200,50);
}
```
<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/NKEFPGZ-0GU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
<br/>
<br/>

### Expt 5:Buzzer

<br/>

```c
int buzzPin = 12;
void setup() {
  pinMode(buzzPin,OUTPUT);
}

void loop() {
  digitalWrite(buzzPin,HIGH);
  delayMicroseconds(1000);
  digitalWrite(buzzPin,LOW);
  delayMicroseconds(1000);
}
```
<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->

<br/>
<br/>

### Expt #:POTENTIOMETER
<br/>

```c
int potVal;
int potPin=A0;
int ledPin=11;
float ledV;
float ledVal;

float potV2ledV(int potV){
  ledV=(255./1023.)*potV;
  return ledV;
}
void setup() {
  Serial.begin(9600);
  pinMode(potPin,INPUT);
  pinMode(ledPin,OUTPUT);
}
void loop() {
  potVal=analogRead(potPin);
  Serial.println(potVal);
  ledVal = potV2ledV(potVal);
  Serial.println(ledVal);
  Serial.println("--------------");
  analogWrite(ledPin,ledVal);  
}
```
<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/dhxAwZ74s28" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->

<br/>
<br/>

### Expt #:LDR
<br/>


```c
int LDrPin=8;
int ledPin=12;
int buzzPin= 7;

void setup() {
  Serial.begin(9600);
  pinMode(LDrPin,INPUT);
  pinMode(ledPin,OUTPUT);
  pinMode(buzzPin,OUTPUT);
}

void loop() {

  int LDrVal;
  digitalWrite(ledPin,LOW);
  int dt=155;
  LDrVal=digitalRead(LDrPin);
  Serial.println(LDrVal);

  while(LDrVal){
    digitalWrite(ledPin,HIGH);
    
    digitalWrite(buzzPin,HIGH);
    delay(dt);
    digitalWrite(buzzPin,LOW);
    delay(dt);
    LDrVal=digitalRead(LDrPin);
  }
  
  
}
```

<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/QuOpklLrG78" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->

<br/>
<br/>

