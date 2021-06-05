detailed report
---------------------------------
Here we need to use 2types of sensor and magnetic locking circuit.

 MAGNET CONTACT
 ---------------------
 ![image](https://user-images.githubusercontent.com/66949546/120879923-7c168c80-c5e4-11eb-8991-0ab72ee5331a.png)

(0 for MAGNET circuit BREAK) (1 for MAGNET circuit contact) 
WHICH COINTAINS THE 2 PINS as normal led light connect the 2 wires to the port1.1 & port1.2
make port1.0 '0' for door closing
make port1.0 '1' for door opening and after certain time make this automatically goes low '0'.
Signal Reception from PIR sensor to detect the human.

PIR SENSOR
---------------
PIR sensors are more complicated than many of the other sensors explained in these tutorials (like photocells, FSRs and tilt switches) because there are multiple variables that affect the sensors input and output. To begin explaining how a basic sensor works, we'll use this rather nice diagram
The PIR sensor itself has two slots in it, each slot is made of a special material that is sensitive to IR. The lens used here is not really doing much and so we see that the two slots can 'see' out past some distance (basically the sensitivity of the sensor). When the sensor is idle, both slots detect the same amount of IR, the ambient amount radiated from the room or walls or outdoors. When a warm body like a human or animal passes by, it first intercepts one half of the PIR sensor, which causes a positive differential change between the two halves. When the warm body leaves the sensing area, the reverse happens, whereby the sensor generates a negative differential change. These change pulses are what is detected.

![image](https://user-images.githubusercontent.com/66949546/120879847-00b4db00-c5e4-11eb-9727-45d9e1f3cb05.png)

PIR sensor consists of 3 pin 
VCC (+ve power supply)
GND (-ve power supply)
DO (goes high when detected) (will be at rest of the condition)


when the "DO" goes high it should send the signals to the magnetic to make low so that the contact will break and door opens.
At the rest of the condition the MC should check for the "DO" pin regularly. DO PIN IS CONNECTED PO PIN P0.1
For manual operation door DO is connected to the external power supply with the switch.

IR SENSOR 
----------
R technology is used in daily life and also in industries for different purposes. For example, TVs use an IR sensor to understand the signals which are transmitted from a remote control. The main benefits of IR sensors are low power usage, their simple design & their convenient features. IR signals are not noticeable by the human eye. The IR radiation in the electromagnetic spectrum can be found in the regions of the visible & microwave. Usually, the wavelengths of these waves range from 0.7 µm 5 to 1000µm. The IR spectrum can be divided into three regions like near-infrared, mid, and far-infrared. The near IR region’s wavelength ranges from 0.75 – 3µm, the mid-infrared region’s wavelength ranges from 3 to 6µm & the far IR region’s infrared radiation’s wavelength is higher than 6µm.
![image](https://user-images.githubusercontent.com/66949546/120879986-e6c7c800-c5e4-11eb-8c52-2af66f272ed2.png)


(0 FOR NO FIRE FOUND), (1 FOR FIRE FOUND)
creat the interrupt when the IR sensor goes high and open the door permanently.
to do this send the high signal to the port P0.2 '1'  continuisly.
