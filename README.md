# EXP-02-INTERFACING-DIGITAL-INPUT-SENSOR-WITH-ARDUINO-PUSH-BUTTON

AIM:  To interface a digital input (push button) and blink and LED upon activation.

COMPONENTS REQUIRED:
1.	1 KΩ Resistor 
2.	Arduino Uno 
3.	Bread board 
4.	USB Interfacing cable 
5.	Jumper wires 
6.	LED of choice 

THEORY :

Arduino UNO - 
 	  The Uno is a microcontroller board based on the ATmega328P. It has 14 digital input/output pins (of which 6 can be used as PWM outputs), 6 analog inputs, a 16 MHz quartz crystal, a USB connection, a power jack, an ICSP header and a reset button. It contains everything needed to support the microcontroller; simply connect it to a computer with a USB cable or power it with a AC-to-DC adapter or battery to get started.
	  
Technical specifications of Arduino UNO :

a.Microcontroller	ATmega168/328
b.Microcontroller	ATmega168/328
c.Operating Voltage	5V
d.Input Voltage (recommended)	7-12V
e.Input Voltage (limits)	6-20V
f.Digital I/O Pins	14 (of which 6 provide PWM output)
g.Analog Input Pins	6
h.DC Current per I/O Pin	40 mA
i.DC Current for 3.3V Pin	50 mA
j.Flash Memory	16 KB (ATmega168) or 32 KB (ATmega328) of which 2 KB used by boot loader
k.SRAM	1 KB (ATmega168) or 2 KB (ATmega328)
l.EEPROM	512 bytes (ATmega168) or 1 KB (ATmega328)
m.Clock Speed	16 MHz

PIN DIAGRAM FOR ATMEGA 328
 
![image](https://user-images.githubusercontent.com/36288975/163530394-115baee4-7ed1-49fe-9cce-d7b625e11e85.png)

FIGURE-01

![image](https://user-images.githubusercontent.com/36288975/163530431-4d390e98-0942-42d8-95b8-f57d348e6ad8.png)

PROCEDURE:

Open tinker cad account 
1.	Select Arduino uno , bread board , digital input and digital output 
2.	Connect the circuit as given in the figure 
3.	Develop the program and compile it for any errors 
4.	 .Execute the program 
5.	Check the simulation 

CIRCUIT DIAGRAM:

![image](https://user-images.githubusercontent.com/36288975/163530437-87a0afbd-b3c9-44ad-b907-5de63486fb9d.png)

FIGURE -02
![exp2](https://user-images.githubusercontent.com/75234588/166475881-f6264750-49a5-42ca-a0a1-bf54d6b7109e.png)



PROGRAM:
```c
const int BUTTON = 2;
const int LED = 6;
int BUTTONstate = 0;
void setup()
{
  pinMode(BUTTON, INPUT);
  pinMode(LED, OUTPUT);
}
void loop()
{
  BUTTONstate = digitalRead(BUTTON);
  if(BUTTONstate == HIGH)
  {
    digitalWrite(LED, HIGH);
  }
  else{
    digitalWrite(LED, LOW);
  }
}
```

Output of the simulation :
![exp2](https://user-images.githubusercontent.com/75234588/166475900-3f13ed34-0f64-467b-97d8-8c904c1fbcd9.png)



Result:

Thus, we have interfaced a digital input (push button) and blink of LED upon activation.

