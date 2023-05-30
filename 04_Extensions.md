<!--
author:   André Dietrich

version:  0.0.1

language: fr

narrator: US English Female

comment:  Try to write a short comment about
          your course, multiline is also okay.

@bold: __@0__

@test: Hello world @0 ... @1

import: https://raw.githubusercontent.com/liaTemplates/AVR8js/main/README.md

import: https://raw.githubusercontent.com/LiaTemplates/aframe/0.0.6/README.md

-->

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://LiaScript.github.io/course/?https://raw.githubusercontent.com/LiaPlayground/LiaScript_Tutorial_Dakar/main/04_Extensions.md)

Toggle Preview : alt+l

Update Preview : Ctrl+s

# New Course

Who ist the author?

@bold(@author)

@test(WWWWWWWWWWWWWWWWWWWWW,dont know)

## Upload an image

## Write a Macro

## Extensions

https://github.com/topics/liascript-template

```html @AFRAME.scene
<a-scene>
  <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
  <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
  <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
  <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
  <a-sky color="#ECECEC"></a-sky>
</a-scene>
```

``` cpp
void setup() {
  Serial.begin(9600);
}

void loop() {
   while (Serial.available() > 0 ) {

     String str = Serial.readString();

     if (str.equals("send")) {
        Serial.println("identified");
     } else {
        Serial.println("unknown");
     }
   }
}
```
@AVR8js.sketch


<div id="example">
<wokwi-led color="red"   pin="13" label="13"></wokwi-led>
<wokwi-led color="green" pin="12" label="12"></wokwi-led>
<wokwi-led color="blue"  pin="11" label="11"></wokwi-led>
<wokwi-led color="blue"  pin="10" label="10"></wokwi-led>
<span id="simulation-time"></span>
</div>

``` cpp
byte leds[] = {13, 12, 11, 10};
void setup() {
  Serial.begin(115200);
  for (byte i = 0; i < sizeof(leds); i++) {
    pinMode(leds[i], OUTPUT);
  }
}

int i = 0;
void loop() {
  Serial.print("LED: ");
  Serial.println(i);
  digitalWrite(leds[i], HIGH);
  delay(250);
  digitalWrite(leds[i], LOW);
  i = (i + 1) % sizeof(leds);
}
```
@AVR8js.sketch(example)