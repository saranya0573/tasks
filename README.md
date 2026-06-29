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

task2

#include <SoftwareSerial.h>
SoftwareSerial blt(10,11);
int gaspin =A2

void setup()
{
Serial.begin(9600);
blt.begin(9600);
}

void loop()
{
int gasvalue = analogRead(gaspin);
blt.print("gas value:");
Serial.println(gasvalue);
blt.println(gasvalue);
delay(1000);
}

task 3

#include <bluetoothSerial.h>
bluetoothSerial blt;
int led = 2;

void setup()
{
  pinMode(led, OUTPUT);
  Serial.begin(115200);
  blt.begin("ESP32");
}

void loop()
{
  if(blt.available))
  {
   data = blt.read();
   Serial.println(data);
   }
  if(data=='A')
  {
  digitalWrite(led, HIGH);
  }
  if(data=='B')
  {
  digitalWrite(led, LOW);
}
}

task 4
#include <BluetoothSerial.h>

BluetoothSerial blt;

int flame = 4;

void setup()
{
  pinMode(flame, INPUT);
  Serial.begin(9600);
  blt.begin("ESP32");
}

void loop()
{
  if (digitalRead(flame) == LOW)
  {
    Serial.println("Flame Detected");
    blt.println("Flame Detected");
  }
  else
  {
    Serial.println("No Flame");
    blt.println("No Flame");
  }

  delay(1000);
}


