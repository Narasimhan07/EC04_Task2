# Pressure and Force sensors Comparison   
### BMP180 Pressure Sensor
Pressure sensors are available in different shapes and sizes. The BMP180 pressure sensor, which was mentioned in the previous year's ideation, is used extensively to measure 
atmospheric temperature and pressure. The BMP180 sensor board is very small and can be a possible candidate for our project, but it is not possible to determine pressure on the
nib using the BMP180 sensor.      
<img src="https://www.circuitbasics.com/wp-content/uploads/2017/05/Arduino-Pressure-Sensor-Tutorial-BMP180-Pin-Diagram.png" width=30% height=30%>      
https://www.circuitbasics.com/set-bmp180-barometric-pressure-sensor-arduino/ - here the working of this sensor is mentioned along with a program to measure barometric pressure and
temperature using the same.     
### Other pressure sensors      
https://www.omega.co.uk/technical-learning/sensor-theory-of-operation.html     
I was able to find a few other type of pressure sensors in the internet. But many of them were expensive and required some sort of USB connection directly to a PC to give an
output (accurate pressure value). Our project needs a sensor to mainly detect pressure. Hence, I feel that this level of accuracy or complicated circuitry/component is not 
required.      
### Force Sensor   
A force sensor consists of a 5V input line and an output line which outputs some analog value (between 0-1023). It has a sensing area which is made of a material whose resistance 
changes with force applied on the sensing area. So, basically it acts like a potentiometer with the applied force being the potentiometer "knob". In our project, the nib must be
connected to the sensing area. This way, any force on the nib can be detected.     
<img src="https://th.bing.com/th/id/R.97912d2f3beab99308be862534169ba3?rik=UaUsupiXlO9Q9g&riu=http%3a%2f%2ftinkersphere.com%2f2265-thickbox_default%2ffsr-force-sensor-pressure-sensor-arduino-compatible.jpg&ehk=RpCjVQNBs1ibsMZ3%2fOfz3gA98VU5LGQWO76kC2O%2fo8g%3d&risl=&pid=ImgRaw" width=30% height=30%>      
This sensor is available in the market. The cost might not be very less compared to a few other components, but it is pretty cheap compared to pressure sensors discussed above and
also solves the purpose.       
Here is a simple example showing the working of the force sensor:    
#### Circuitry     
<img src="https://github.com/Narasimhan07/EC04_Task2/blob/af97291d442b3f0db37edc620a0cda19bcb83d86/simple%20force%20sensor.png" width=100% height=100%>               
#### code    
```
int inputpin=A0;
int pressure_analog;
int no_pressure=400;
void setup()
{
  pinMode(A0,INPUT);
  Serial.begin(9600);
}

void loop()
{
  pressure_analog=analogRead(inputpin);
  Serial.println(pressure_analog);
  if(pressure_analog>400)
  {
    Serial.println("significant force bro");
  }
  delay(500);
}
```
