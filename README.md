# lab-03
# lab03
TO : Mark A. Yoder 

From: Team 11
      Pushpendra Kumar (B13132)
      Ankur Sardar (B13108)
      
Date: 06/09/15

Sub : Report on lab 03


Lab 03 was a very intresting lab. From this lab we leant how to use a potientiometer and a js fiddle software 
to control our led brightness and power


In lab 03 we use two LED's for following pusrpose:
1. To glow both the LED's: For this led we use 
2. To glow one LED's while another one fade away
3. To control the brightness of both the LED's using a poteniometer
4. Then we use fiddle to saw our code and make some changes in our code like we get values of potentiometer and a 
   button on screen to turn off and on the LED's.


CODE FOR blinking an led:

var b = require('bonescript');

var leds = ["USR0", "USR1", "USR2", "USR3", "P9_14"];

for(var i in leds) {
    b.pinMode(leds[i], b.OUTPUT);
}

var state = b.LOW;
for(var i in leds) {
    b.digitalWrite(leds[i], state);
}

setInterval(toggle, 1000);

function toggle() {
    if(state == b.LOW) state = b.HIGH;
    else state = b.LOW;
    for(var i in leds) {
        b.digitalWrite(leds[i], state);
    }
}







