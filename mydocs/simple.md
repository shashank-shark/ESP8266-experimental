```c
#include <ESP8266WiFi.h>

void setup () {
  Serial.begin (115200);
  delay (200);
}

void loop () {
  Serial.println ();
  Serial.print ("MAC : ");
  Serial.print (WiFi.macAddress());
}
```