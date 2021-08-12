## Hi
I'm NIKHIL KJ  
  
### Expt 1:LED Blinking  
  
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
<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/MUQfKFzIOeU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->  
  
### Expt 2:Traffic Light
\
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
\
<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/MUQfKFzIOeU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
\
\
### Expt 3:LED Chasing Effect
\
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
\
<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/MUQfKFzIOeU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
\
\
### Expt 4:RGB LED
\
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

\
<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/MUQfKFzIOeU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
\
\
###Expt 5:Buzzer
\
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

\
<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/MUQfKFzIOeU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
\
\
### Expt :POTENTIOMETER
\
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
\
<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/MUQfKFzIOeU" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
\
\

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```


