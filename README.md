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

### Expt 4:Button Controlled LED

<br/>

```c

int readPIN = 8;
int ledPIN  = 12;

void setup() {
  //pinMode(readPIN,INPUT_PULLUP);
  pinMode(readPIN,INPUT);
  pinMode(ledPIN,OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int readVal;
  readVal = digitalRead(readPIN);
  Serial.println(readVal);
  if(readVal)
    digitalWrite(ledPIN,HIGH);
  else
    digitalWrite(ledPIN,LOW);
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

### Expt 6:RGB LED
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

### Expt 8: Flame Sensor

<br/>

```c
int Flame = A0;
int Buzzer =8;

void setup() {
  pinMode(Flame,INPUT);
  pinMode(Buzzer,OUTPUT);
  Serial.begin(9600);
}

void loop() {
  
  int flameVAL = analogRead(Flame);
  Serial.println(flameVAL);
  if(flameVAL> 600)
    digitalWrite(Buzzer,HIGH);
  else
    digitalWrite(Buzzer,0);
  delay(500);

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

### Expt 9:Temperature Sensor LM35

<br/>

```c
int temp = A0;

void setup() {
  pinMode(temp,INPUT);
  Serial.begin(9600);
}

void loop() {
  
  int val = analogRead(temp);
  int dat;// define variable
  val=analogRead(0);
  // read the analog value of the sensor and assign it to val
  dat=(125*val)>>8;// temperature calculation formula
  Serial.print("Temp ");// output and display characters beginning with Tep
  Serial.print(dat);// output and display value of dat
  Serial.println(" C");// display “C” characters
  delay(500);// wait for 0.5 second;
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

### Expt #:Toggle Switch
<br/>

```c

int readPIN = 8;
int ledPIN  = 12;

void setup() {
  //pinMode(readPIN,INPUT_PULLUP);//press =0
  pinMode(readPIN,INPUT);
  pinMode(ledPIN,OUTPUT);
  Serial.begin(9600);
}


bool prevVal = HIGH; 
bool prev_readVal;
void loop() {
  bool readVal;
  readVal = digitalRead(readPIN);
  delay(50);
  if(readVal & !prev_readVal){ // 0 to 1 transition
     digitalWrite(ledPIN, prevVal);
     prevVal = !prevVal;
    }
  prev_readVal=readVal;   
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

### Expt #: Button Controlled dimmable LED

<br/>

```c
int readPIN_up = 11;
int readPIN_down = 12;
int ledPIN  = 9;

int BrightVal=0;

void setup() {
  pinMode(readPIN_up,INPUT_PULLUP);
  pinMode(readPIN_down,INPUT_PULLUP);
  pinMode(ledPIN,OUTPUT);
  Serial.begin(9600);
}


void loop() {

  int dt =50;
  
  int readVal_up;
  readVal_up=digitalRead(readPIN_up);
  delay(dt);
  
  int readVal_down;
  readVal_down=digitalRead(readPIN_down);
  delay(dt);
  
  if(!readVal_up){
    if(BrightVal != 255){
      BrightVal += 17;
      Serial.println(BrightVal);
      analogWrite(ledPIN,BrightVal);
    }
  }
  
  if(!readVal_down){
    if(BrightVal != 0){
      BrightVal-= 17;
      Serial.println(BrightVal);
      analogWrite(ledPIN,BrightVal);
    }
  }
  
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

