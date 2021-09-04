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
src="https://www.youtube.com/embed/T9m9NT8zQqs" 
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

### Expt 7:LDR

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
src="https://www.youtube.com/embed/zzLf0j56xfw" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
<br/>
<br/>

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
  dat=(125*val)>>8;// temperature calculation formula
  Serial.print("Temp ");
  Serial.print(dat);
  Serial.println(" C");
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

<br/>
<br/>

### Expt 10: IR Remote

<br/>

```c
#include <IRremote.h>
int RECV_PIN = 3;
int LED1 = 8;
int LED2 = 9;
int LED3 = 10;
int LED4 = 11;

const unsigned long LED1_IR = 0x00C0006D;
const unsigned long LED2_IR = 0xC0006E;
const unsigned long LED3_IR = 0xC0006F;
const unsigned long LED4_IR = 0xC00070;
const unsigned long TOGGLE_IR = 0xC0000C;

IRrecv irrecv(RECV_PIN);
decode_results results;

void dump(decode_results results) {
  switch (results.decode_type) {
    case NEC:
      Serial.println("NEC");
      break;
    case SONY:
      Serial.println("SONY");
      break;
    case RC5:
      Serial.println("RC5");
      break;
    case RC6:
      Serial.print("RC6:");
      break;
    case DISH:
      Serial.print("DISH:");
      break;
    case SHARP:
      Serial.print("SHARP:");
      break;
    case JVC:
      Serial.print("JVC:");
      break;
    case SANYO:
      Serial.print("SANYO:");
      break;
    case MITSUBISHI:
      Serial.print("MITSUBISHI:");
      break;
    case SAMSUNG:
      Serial.print("SAMSUNG:");
      break;
    case LG:
      Serial.print("LG:");
      break;
    case WHYNTER:
      Serial.print("WHYNTER:");
      break;
    case AIWA_RC_T501:
      Serial.print("AIWA_RC_T501:");
      break;
    case PANASONIC:
      Serial.print("PANASONIC:");
      break;
    case DENON:
      Serial.print("DENON:");
      break;
    default:
    case UNKNOWN:
      Serial.print("UNKNOWN:");
      break;
  }
  Serial.print(results.value, HEX);
  Serial.print(" (");
  Serial.print(results.bits, DEC);
  Serial.println(" bits)");
}

void lights(int a,int b,int c,int d){
  digitalWrite(LED1,a);
  digitalWrite(LED2,b);
  digitalWrite(LED3,c);
  digitalWrite(LED4,d);
}

void setup()
{
  pinMode(RECV_PIN, INPUT);
  pinMode(LED1, OUTPUT);
  pinMode(LED2, OUTPUT);
  pinMode(LED3, OUTPUT);
  pinMode(LED4, OUTPUT);
  pinMode(13, OUTPUT);
  Serial.begin(9600);
  irrecv.enableIRIn(); // Start the receiver
}
int on = 0;
unsigned long last = millis();
void loop()
{
  if (irrecv.decode(&results))
  {
    // If it's been at least 1/4 second since the last
    // IR received, toggle the relay
    if (millis() - last > 250)
    {
      on = !on;
      digitalWrite(13, on ? HIGH : LOW);
      dump(results);
    }
    

    switch (results.value){
      case LED1_IR :
            Serial.print(results.value);
            lights(1,0,0,0);
            break;
      case LED2_IR :
            lights(0,1,0,0);
            break;
      case LED3_IR :
            lights(0,0,1,0);
            break;
      case LED4_IR :
            lights(0,0,0,1);
            break;
      case TOGGLE_IR :
            lights(on,on,on,on);
            break;
            
    }



    last = millis();
    irrecv.resume(); // Receive the next value
  }
}
```
<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/S8j5t4o1oxc" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->
<br/>
<br/>

### Expt 11:POTENTIOMETER
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



### Expt 12: 7 Segment Display

<br/>

```c
// C++ code
//
int g = 12;
int f = 11;
int e = 10;
int d = 9;
int c = 8;
int b = 7;
int a = 6;
int dp = 5;


void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void)
{// display number 1
digitalWrite(a,LOW);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,LOW);
digitalWrite(e,LOW);
digitalWrite(f,LOW);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=12;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{
 digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{
 digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=6;j<=8;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=9;j<=12;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=6;j<=12;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
  int i;// set variable
  for(i=5;i<=12;i++)
  pinMode(i,OUTPUT);// set pin 5-12 as “output”
}

void loop()
{
while(1)
{
digital_0();
delay(1000);
digital_1();
delay(1000);
digital_2();
delay(1000);
digital_3();
delay(1000); 
digital_4();
delay(1000); 
digital_5();
delay(1000); 
digital_6();
delay(1000); 
digital_7();
delay(1000);
digital_8();
delay(1000); 
digital_9();
delay(1000); 
}}

```
<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/OtOnRjMkYkE" 
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

### ASSIGNMENT 1 : THERMOMETER

<br/>

```c
int temp = A0;
int LED1=8;
int LED6=13;
void setup() {
  pinMode(temp,INPUT);
  for(int i=LED1;i<=LED6;++i){
    pinMode(i,OUTPUT);
  }
  Serial.begin(9600);
}

void ledOn(int led){
   for(int i=LED1;i<=LED1+led;++i){
   digitalWrite(i,HIGH);
  }
}

void thermometerScale(float temp){
 if(temp<-13.32)
    ledOn(0);
  else if(temp<20.68)
    ledOn(1);
  else if(temp<47.48)
    ledOn(2);
  else if(temp<81.64)
    ledOn(3);
  else if(temp<115.80)
    ledOn(4);
  else if(temp<149)
    ledOn(5);
  else 
    ledOn(6);
    
}


void loop() {
  
  int val = analogRead(temp);
  float dat;// define variable
  val=analogRead(0);
  dat=(125*val)>>8;// temperature calculation formula
  Serial.print("Temp ");
  Serial.print(dat);
  Serial.println(" C");
  thermometerScale(dat);
  delay(5000);
}
```
<br/>

<!-- blank line -->
![Thermometer.jpg](/IMG_20210828_161604_1~2.jpg "Thermometer")
<!-- blank line -->

<br/>
<br/>

### ASSIGNMENT 2 : DIGITAL DICE
<br/>

```c

int buttonPin = 7;
int LED1=8;
int LED6=13;

void rolling(){//CHASING EFFECT
   for(int pin=LED1;pin<=LED6;++pin){
   digitalWrite(pin,HIGH);
   delay(100);
  }
  for(int pin=LED6;pin>=LED1;--pin){
   digitalWrite(pin,LOW);
   delay(100);
  }
}

void displayResult(int number){
  for(int i=LED1;i<LED1+number;++i){
    digitalWrite(i,HIGH);
    delay(50);
  }
}

void setup() {
  for (int i=LED1;i<=LED6;++i){
    pinMode(i,OUTPUT);
  }
  pinMode(buttonPin,INPUT_PULLUP);
  Serial.begin(9600);
  randomSeed(analogRead(0));
}
void loop() { 
  if(!digitalRead(buttonPin)){//IF THE BUTTON IS PRESSED
    
    for(int i=0;i<=3;++i){    // ROLLING EFFECT
      rolling();            
    }
    displayResult(random(1,7)); //DISPLAY RESULT
  } 
}
```

<br/>

<!-- blank line -->
<iframe width="560" height="315"
src="https://www.youtube.com/embed/KFgrftnXKk8" 
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
<!-- blank line -->

<br/>
<br/>


