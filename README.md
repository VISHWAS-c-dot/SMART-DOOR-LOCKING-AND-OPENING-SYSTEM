#SMART DOOR LOCKING SYSTEM USING 8051 MICRO CONTROLLER:
============================================================

#Operations It Can:
------------------------------------------
1st - human detection and open the  door
2nd - Open for emergency exit (eg. at the case of fire)
3rd - overwriting manual when the automatic fails
4th - manual lock the door at emergeny.


#Working and Architecture:
---------------------------------
Here we need to use 2types of sensor and magnetic locking circuit.

 MAGNET CONTACT
(0 for MAGNET circuit BREAK) (1 for MAGNET circuit contact) 
WHICH COINTAINS THE 2 PINS as normal led light connect the 2 wires to the port1.1 & port1.2
make port1.0 '0' for door closing
make port1.0 '1' for door opening and after certain time make this automatically goes low '0'.
Signal Reception from PIR sensor to detect the human.
PIR sensor consists of 3 pin 
VCC (+ve power supply)
GND (-ve power supply)
DO (goes high when detected) (will be at rest of the condition)

when the "DO" goes high it should send the signals to the magnetic to make low so that the contact will break and door opens.
At the rest of the condition the MC should check for the "DO" pin regularly. DO PIN IS CONNECTED PO PIN P0.1
For manual operation door DO is connected to the external power supply with the switch.

IR SENSOR (0 FOR NO FIRE FOUND), (1 FOR FIRE FOUND)
creat the interrupt when the IR sensor goes high and open the door permanently.
to do this send the high signal to the port P0.2 '1'  continuisly.

#APPLICATION
-----------------------
The automatic door opening systems are used in commercial buildings, shopping malls, theaters, etc. These systems are used to open and close the door when a person comes near to the entry of the door and close it after the person entered into the door and it also activate automatically at the time of fire emergencies.

if you have any doubt fell free to mail me @ <pre><code>vishwas@varzsecurity.com</code></pre>
