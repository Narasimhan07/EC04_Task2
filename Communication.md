# External Sensor Communication    
We have chosen our external sensor as a VL6180X/VL53L0X ToF sensor. We require a means to receive data from this sensor. The sensors within the pen are connected through wiring.   
## Possible modes of connection: Wired or Wireless   
### Wired mode of connection:     
If we go for a wired mode of connection between the ToF sensor and the microcontroller, we will require only one microcontroller. The controller is present within the pen and the 
communication is through I2C protocol. So, we will have multiple wired connections between the microcontroller and the ToF sensor. We could group the wires together and use 
extensible wires to make writing comfortable for the user (the wires will be similar to the wires we see in landline connections).             
<img src="https://sc01.alicdn.com/kf/HTB1I1KTKbSYBuNjSspfq6AZCpXaR/Direct-selling-automatic-spring-cable-coiled-electrical.jpg_350x350.jpg" width=30% height=30%>      
Advantages and disadvantages:    
It makes connections straightforward, merges the pen and the ToF sensor module into a single unit and makes the entire digital pen an I2C protocol run system.     
One issue is the availability of these wires.     
#### Choice of Microcontroller: 
We need a microchip which supports I2C, has digital/analog read options, and 5V and Ground pins. I feel the best choice is, microcontroller based on SAMD21.    
<img src="https://images-na.ssl-images-amazon.com/images/I/514Y1ToFnbL._AC_.jpg" width=40% height=40%>     
https://www.amazon.com/Seeeduino-Smallest-Microcontroller-Interfaces-Compatible/dp/B08745JBRP/ref=sr_1_4?dchild=1&keywords=microcontroller&qid=1625550349&sr=8-4    
### Wireless mode of connection:    
I tried to find an easy to implement method for wireless communication. Here are few of them:
#### Bluetooth module:   
There were a lot of projects in the internet that showed how to set up bluetooth module HC-05 using an arduino. The arduino output line is controlled using a bluetooth arduino app on an android device. The HC-05 communicates using UART. https://electrosome.com/interfacing-hc-05-bluetooth-module-arduino-uno/#:~:text=Interfacing%20HC-05%20Bluetooth%20Module%20with%20Arduino%20Uno%201,6%20Practical%20Implementation%207%20Video%208%20Conclusion.%20   
The bluetooth modules like HC-05 are used to control a microcontroller's output line. I don't think we can send data from the ToF sensor to the microchip using this technology.  
#### IR communication:    
As  the name suggests, we transfer data from the ToF device to the controller in the pen using IR sensors. We need two microcontrollers here. One placed outside the pen. This one will input data from the sensor, and transfer it to the controller within the pen. I feel IR sensors make the entire setup bulky, hard to carry around and use.     
#### Zigbee technology:    
This uses a set of high-level protocols for data transfer.     
**This along with IR and maybe other wireless comms demand more from the microcontroller. It might not be easy to continue with a small controller like the ATTiny85 model.**      
https://en.wikipedia.org/wiki/ZigBee#:~:text=Zigbee%20is%20an%20IEEE%20802.15.4-based%20specification%20for%20a,by%20the%20Zigbee%20specification%20is%20intended%20to%20be   

