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

