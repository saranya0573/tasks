#include <SoftwareSerial.h>
SoftwareSerial blt(8,9);

int light =2;
int fan   =3;

void setup()
{
  pinMode(light, OUTPUT);
  pinMode(fan,   OUTPUT);
  blt.begin(9600);
}

void loop()
{
  if(blt.available())
{
  char data =blt. read ();
  digitalWrite(light, HIGH);
  digitalWrite(fan,   LOW);
  digitalWrite(light, HIGH);
  digitalWrite(fan,   LOW);
  delay(1000);
}
}

