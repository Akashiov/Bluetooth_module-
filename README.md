# Bluetooth_module-
#include<SoftwareSerial.h>
String b;
void setup() {
Serial.begin(9600);
pinMode(4,OUTPUT);// define the pin 
}

void loop() {
if(Serial.available())
{

  b=Serial.readString();
  Serial.println(b);
}
if(b=="on")
{
  digitalWrite(4,1);
}
else if(b=="off")



{
  digitalWrite(4,0);
}
}
