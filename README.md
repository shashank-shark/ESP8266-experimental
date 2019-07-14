# ESP8266-experimental
--------------------------
 Experimental Projects using ESP8266 wifi chip and other open source electronics.

|  TOC |  Description | Link |
|---|---|---|
|  1.0 | Basic pin diagram |  [Click Here](#Pin-Connections-of-NodeMCU ) |
|  1.1 | How it looks ?  | [Click Here](#It-looks-like-the-one-below)  |
|  1.2 | LED Blink Code |  [Go to blink code](#Demo-code-for-blinking-LED-on-NodeMCU) |
| 1.3  | Find Hardware MAC  |  [Go to code](#Code-to-find-the-MAC-address-off-NodeMCU) |

 A basic pin diagram of the NodeMCU is given below.


 ## Pin Connections of NodeMCU ([back to TOC](#ESP8266-experimental))
 --------------------------------
 ![Pin connections of NodeMCU](https://firebasestorage.googleapis.com/v0/b/esp8266-experiments.appspot.com/o/esp8266-main%2Fpin-diargam-nodeMCU%2FNodeMCUpins.png?alt=media&token=797f5613-7b60-4379-b420-ac8b255fc37e)

 ## It looks like the one below. ([back to TOP](#ESP8266-experimental))
 ---------------------------------
<img src="https://firebasestorage.googleapis.com/v0/b/esp8266-experiments.appspot.com/o/esp8266-main%2Freal-images-nodemcu%2FNodemcu.jpg?alt=media&token=ef6f87da-c9b7-4411-9665-5e0cbc8d7669" heigh="200" width="450">

## Demo code for blinking LED on NodeMCU ([back to TOC](#ESP8266-experimental))
----------------------------------------
```c
/* setup function here */
void setup() {
  // Initialize the LED_BUILTIN pin as an output
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {

    /* Turn the LED on (Note that LOW is the voltage level
   but actually the LED is on; this is because
   it is active low on the ESP-01) */

  digitalWrite(LED_BUILTIN, LOW);

  // now give some delay for one second
  delay(1000);

  // Turn the LED off by making the voltage HIGH
  digitalWrite(LED_BUILTIN, HIGH);  

  // Wait for two seconds (to demonstrate the active low LED)
  delay(2000);
}
```

## Code to find the MAC address off NodeMCU ([back to TOC](#ESP8266-experimental))
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