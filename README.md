# E-TOGBK
Arduino code for SpaceApp Challange-Nasa 2020 Create a Mascot category robot, namely E-TOG
This code can only be used for academic research. Any kind of usage for trading will be treated as "stealing" and by reading this note, you accept accusing.

#include <LiquidCrystal.h> 

LiquidCrystal lcd(12, 11, 10, 8, 9, 7); 

 
const int but_m=A0;  //mercury
const int but_v=A1;   //venus
const int but_e=A2;   //earth
const int but_ma=A3;  //mars
const int but_j=A4;   //jupiter
const int but_s=A5;   //saturn
const int but_u=2;    //uranus
const int but_n=3;    //neptune
const int but_sun=4;   //sun
int  mouth[2][16]={
{0,1,1,1,0,0,0,0,0,0,0,0,1,1,1,0},
{0,0,0,1,1,1,1,1,1,1,1,1,1,0,0,0}
};

void setup() {
  // put your setup code here, to run once:
pinMode(but_m,INPUT_PULLUP);
pinMode(but_v,INPUT_PULLUP);
pinMode(but_e,INPUT_PULLUP);
pinMode(but_ma,INPUT_PULLUP);
pinMode(but_j,INPUT_PULLUP);
pinMode(but_s,INPUT_PULLUP);
pinMode(but_u,INPUT_PULLUP);
pinMode(but_n,INPUT_PULLUP);
pinMode(but_sun,INPUT_PULLUP);
Serial.begin(9600);
lcd.begin(16, 2); 
lcd.print("hi");
delay(1000);

}

void loop() {

if(digitalRead(but_m)==LOW){
    lcd.clear();
  pinMode(but_m,OUTPUT);
  digitalWrite(but_m,HIGH);
  lcd.setCursor(0, 1);
  lcd.print("Mercury");
  delay(5000);
}
if(digitalRead(but_v)==LOW){
    lcd.clear();
  pinMode(but_v,OUTPUT);
  digitalWrite(but_v,HIGH);
  lcd.setCursor(0, 1);
  lcd.print("Venus");
  delay(5000);
}
if(digitalRead(but_e)==LOW){
    lcd.clear();
  pinMode(but_e,OUTPUT);
  digitalWrite(but_e,HIGH);
  lcd.setCursor(0, 1);
  lcd.print("Earth");
  delay(5000);
  
}
if(digitalRead(but_ma)==LOW){
  lcd.clear();
  pinMode(but_ma,OUTPUT);
  digitalWrite(but_ma,HIGH);
  lcd.setCursor(0, 1);
  lcd.print("Mars");
  delay(5000);
  
}
if(digitalRead(but_j)==LOW){
    lcd.clear();
  pinMode(but_j,OUTPUT);
  digitalWrite(but_j,HIGH);
  lcd.setCursor(0, 1);
  lcd.print("Jupiter");
  delay(5000);
  
}
if(digitalRead(but_s)==LOW){
    lcd.clear();
  pinMode(but_s,OUTPUT);
  digitalWrite(but_s,HIGH);
  lcd.setCursor(0, 1);
  lcd.print("Saturn");
  delay(5000);
  
}
if(digitalRead(but_u)==LOW){
    lcd.clear();
  pinMode(but_u,OUTPUT);
  digitalWrite(but_u,HIGH);
  lcd.setCursor(0, 1);
  lcd.print("Uranus");
  delay(5000);
  
}
if(digitalRead(but_n)==LOW){
    lcd.clear();
  pinMode(but_n,OUTPUT);
  digitalWrite(but_n,HIGH);
  lcd.setCursor(0, 1);
  lcd.print("Neptune");
  delay(5000);
  
}
if(digitalRead(but_sun)==LOW){
    lcd.clear();
  pinMode(but_sun,OUTPUT);
  digitalWrite(but_sun,HIGH);
  lcd.setCursor(0, 1);
  lcd.print("Sun");
  delay(5000);
  
}
else{
  
  lcd.clear();
  lcd.setCursor(0, 0);
  lcd.println("Press a button  ");
  lcd.setCursor(0,1);
  lcd.println("to explore space");
  delay(2000);
  lcd.clear();
  lcd.setCursor(0,0);
  for(int i=0;i<2;i++){
   for(int j=0; j<16;j++){
     lcd.setCursor(j, i);    
     if(mouth[i][j]==1){
       lcd.write(255);
     }
   }
  }
  delay(2000);
  lcd.clear();
}
clearout();
}

void clearout(){
  digitalWrite(but_m,LOW);
  digitalWrite(but_v,LOW);
  digitalWrite(but_e,LOW);
  digitalWrite(but_ma,LOW);
  digitalWrite(but_j,LOW);
  digitalWrite(but_s,LOW);
  digitalWrite(but_u,LOW);
  digitalWrite(but_n,LOW);
  digitalWrite(but_sun,LOW);
  pinMode(but_m,INPUT_PULLUP);
  pinMode(but_v,INPUT_PULLUP);
  pinMode(but_e,INPUT_PULLUP);
  pinMode(but_ma,INPUT_PULLUP);
  pinMode(but_j,INPUT_PULLUP);
  pinMode(but_s,INPUT_PULLUP);
  pinMode(but_u,INPUT_PULLUP);
  pinMode(but_n,INPUT_PULLUP);
  pinMode(but_sun,INPUT_PULLUP);

  
  
}
