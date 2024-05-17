# Monitoring-light-intensity-using-LDR-and-uploading-the-data-in-the-cloud-using-an-IoT-controller-.

# AIM:
To monitor and upload the light intensity value in the Things mate using Arduino controller.

# Apparatus required:
Arduino Controller  </br>
Indoor gateway</br>
LoRaWAN shield </br>
LDR </br>
Power supply </br>
Connecting wires </br>
Bread board </br>

# PROCEDURE:

### Procedure for gateway setup
	Go to the link http://172.31.255.254:8000 </br>
	Type the user name password </br>
	Go to LoRa and set the frequency plan 865 Mhz </br>
	In LoRa WAN configurations enter the Gate EUI and server address </br>
	Enable the Internet </br>
	Select the Wifi access point </br>
	Type the ssid and password in wifi LAN setting </br>
	Select the internet and IoT service and provide the details. </br>
	Check all the green colour tick marks in gate way and proceed </br>
### Procedure for gateway registration in The thingsMate LoRaWAN Management </br>
	Login https://iot.saveetha.in:4433 and provide the user id and password </br>
	Go to overview and select application server </br>
	Go to gateway and add new gateway </br>
	Enter the gateway id, name, EUI and select frequency plan </br>
	Open Arduino IDE and type the program for the given application </br>
	Compile the program if no error uploads the program in the controller </br>
	Go to gateways in things mate and check the live data </br>
	Create channel by giving channel name and ID </br>
	Add end device and enter the frequency plan, DevEUI, AppEUI, APP key, Select LoRaWAN version </br>
	Enter payload formatters </br>
	Go to the option query and give the new query name </br>
	Go to the option Dashboard and verify the output.</br>  

# THEORY:

### What is IoT?

Internet of Things (IoT) describes an emerging trend where a large number of embedded devices (things) are connected to the Internet. These connected devices communicate with people and other things and often provide sensor data to cloud storage and cloud computing resources where the data is processed and analyzed to gain important insights. Cheap cloud computing power and increased device connectivity is enabling this trend.IoT solutions are built for many vertical applications such as environmental monitoring and control, health monitoring, vehicle fleet monitoring, industrial monitoring and control, and home automation

![image](https://user-images.githubusercontent.com/71547910/235334044-c01d4261-d46f-4f62-b07f-72a7b6fce5d5.png)

### LDR

LDR (Light Dependent Resistor) as the name states is a special type of resistor that works on the photoconductivity principle means that resistance changes according to the intensity of light. Its resistance decreases with an increase in the intensity of light.It is often used as a light sensor, light meter, Automatic street light, and in areas where we need to have light sensitivity. LDR is also known as a Light Sensor. LDR are usually available in 5mm, 8mm, 12mm, and 25mm dimensions.

The Light-dependent resistors made with photosensitive semiconductor materials like Cadmium Sulphides (CdS), lead sulfide, lead selenide, indium antimonide, or cadmium selenide and they are placed in a Zig-Zag shape.Two metal contacts are placed on both ends of the Zig-Zag shape these metal contacts help in creating a connection with the LDRs.Now, a transparent coating is applied on the top so that the zig-zag-shaped photosensitive material gets protected and as the coating is transparent the LDR will be able to capture light from the outer environment for its working.

![image](https://github.com/anishkumar-Embedded/Monitoring-light-intensity-using-LDR-and-uploading-the-data-in-the-cloud-using-an-IoT-controller-./assets/71547910/26a0e210-5d9d-40c6-955d-89c637d38265)

#### LDR Working Principle

It works on the principle of photoconductivity whenever the light falls on its photoconductive material, it absorbs its energy and the electrons of that photoconductive material in the valence band get excited and go to the conduction band and thus increasing the conductivity as per the increase in light intensity.Also, the energy in incident light should be greater than the bandgap gap energy so that the electrons from the valence band got excited and go to the conduction band.The LDR has the highest resistance in dark around 1012 Ohm and this resistance decreases with the increase in Light.As per the property of LDRs, the amount of light entering the LDR the inversely proportional to the resistance of the sensor, and the graph is hyperbolic in nature.

![image](https://github.com/anishkumar-Embedded/Monitoring-light-intensity-using-LDR-and-uploading-the-data-in-the-cloud-using-an-IoT-controller-./assets/71547910/e7c513a2-8aca-4f6a-bf20-32e1eeff3e17)


### What is LoRaWAN

The LoRaWAN® specification is a Low Power, Wide Area (LPWA) networking protocol designed to wirelessly connect battery operated ‘things’ to the internet in regional, national or global networks, and targets key Internet of Things (IoT) requirements such as bi-directional communication, end-to-end security, mobility and localization services.LoRaWAN® network architecture is deployed in a star-of-stars topology in which gateways relay messages between end-devices and a central network server. The gateways are connected to the network server via standard IP connections and act as a transparent bridge, simply converting RF packets to IP packets and vice versa. The wireless communication takes advantage of the Long Range characteristics of the LoRaÒ physical layer, allowing a single-hop link between the end-device and one or many gateways. All modes are capable of bi-directional communication, and there is support for multicast addressing groups to make efficient use of spectrum during tasks such as Firmware Over-The-Air (FOTA) upgrades or other mass distribution messages.

The specification defines the device-to-infrastructure (LoRa®) physical layer parameters & (LoRaWAN®) protocol and so provides seamless interoperability between manufacturers, as demonstrated via the device certification program.While the specification defines the technical implementation, it does not define any commercial model or type of deployment (public, shared, private, enterprise) and so offers the industry the freedom to innovate and differentiate how it is used.The LoRaWAN® specification is developed and maintained by the LoRa Alliance®: an open association of collaborating members.

![image](https://github.com/anishkumar-Embedded/Update-the-Ultrasonic-sensor-value-in-cloud/assets/71547910/c63c4edd-3b95-4a69-b9c2-4862afb335c3)

### Characteristics of LoRaWAN technology
Long range communication up to 10 miles in line of sight.
Long battery duration of up to 10 years. For enhanced battery life, you can operate your devices in class A or class B mode, which requires increased downlink latency.
Low cost for devices and maintenance.
License-free radio spectrum but region-specific regulations apply.
Low power but has a limited payload size of 51 bytes to 241 bytes depending on the data rate. The data rate can be 0,3 Kbit/s – 27 Kbit/s data rate with a 222 maximal payload size.

### The Things Mate - IoT Cloud Platform

IoT cloud platforms play a pivotal role in the development and deployment of Internet of Things (IoT) applications, connecting devices and enabling seamless data management and analysis. These platforms typically offer a comprehensive suite of services, including device provisioning, secure connectivity, data storage, and advanced analytics.Leading IoT cloud platforms, such as AWS IoT, Azure IoT, and Google Cloud IoT, provide scalable and reliable infrastructure to accommodate diverse IoT deployments. They facilitate device management, allowing users to monitor, update, and control connected devices remotely. Security features are integral, ensuring data integrity and safeguarding against potential threats.

Analytics capabilities enable organizations to derive meaningful insights from the vast amounts of data generated by IoT devices. Machine learning and artificial intelligence integrations further enhance predictive analytics, enabling proactive decision-making.These platforms often offer APIs for seamless integration with other cloud services, supporting a wide range of industries and applications, from smart homes to industrial automation. As the IoT landscape evolves, cloud platforms continue to innovate, contributing to the growth and sophistication of IoT ecosystems worldwide. Choosing the right IoT cloud platform involves considering factors such as scalability, security, and compatibility with specific use cases.

# PROGRAM:
```
#include <SoftwareSerial.h>
#include <Adafruit_Sensor.h>

/*

*/
 
//#define ldrpin  A1 // This is our input pin

int ldrpin=A0;
int ldr_value=0; 

String inputString = "";         // a String to hold incoming data
bool stringComplete = false;     // whether the string is complete

long old_time=millis();
long new_time;

long uplink_interval=30000;      //ms

bool time_to_at_recvb=false;
bool get_LA66_data_status=false;

bool network_joined_status=false;

float DHT11_temp;
float DHT11_hum;

SoftwareSerial ss(10, 11);       // Arduino RX, TX ,

char rxbuff[128];
uint8_t rxbuff_index=0;

void setup() {
  // initialize serial
  
  //pinMode(LED, OUTPUT); // put onboard LED as output
  pinMode(ldrpin, INPUT); //ldr sensor should be input as it is giving data
  Serial.begin(9600); //begin Serial communication

  ss.begin(9600);
  ss.listen();
  
  // reserve 200 bytes for the inputString:
  inputString.reserve(200);

 
  ss.println("ATZ");//reset LA66
}

void loop() {

  new_time = millis();

  if((new_time-old_time>=uplink_interval)&&(network_joined_status==1)){
    old_time = new_time;
    get_LA66_data_status=false;

    //LDR SENSOR INTERFACING // Flame Sensor Module
LDR();    

 
    
    char sensor_data_buff[128]="\0";

    //confirm status,Fport,payload length,payload(HEX)

    //--------------perfectly worked for  LDR SENSOR  -------------


    snprintf(sensor_data_buff,128,"AT+SENDB=%d,%d,%d,%02X%02X",0,2,2,(short)(ldr_value),(short)(ldrpin));
    ss.println(sensor_data_buff);
  }

  if(time_to_at_recvb==true){
    time_to_at_recvb=false;
    get_LA66_data_status=true;
    delay(1000);
    
    ss.println("AT+CFG");    
  }

    while ( ss.available()) {
    // get the new byte:
    char inChar = (char) ss.read();
    // add it to the inputString:
    inputString += inChar;

    rxbuff[rxbuff_index++]=inChar;

    if(rxbuff_index>128)
    break;
    
    // if the incoming character is a newline, set a flag so the main loop can
    // do something about it:
    if (inChar == '\n' || inChar == '\r') {
      stringComplete = true;
      rxbuff[rxbuff_index]='\0';
       
      if(strncmp(rxbuff,"JOINED",6)==0){
        network_joined_status=1;
      }

      if(strncmp(rxbuff,"Dragino LA66 Device",19)==0){
        network_joined_status=0;
      }

      if(strncmp(rxbuff,"Run AT+RECVB=? to see detail",28)==0){
        time_to_at_recvb=true;
        stringComplete=false;
        inputString = "\0";
      }

      if(strncmp(rxbuff,"AT+RECVB=",9)==0){       
        stringComplete=false;
        inputString = "\0";
        Serial.print("\r\nGet downlink data(FPort & Payload) ");
        Serial.println(&rxbuff[9]);
      }
      
      rxbuff_index=0;

      if(get_LA66_data_status==true){
        stringComplete=false;
        inputString = "\0";
      }
    }
  }

   while ( Serial.available()) {
    // get the new byte:
    char inChar = (char) Serial.read();
    // add it to the inputString:
    inputString += inChar;
    // if the incoming character is a newline, set a flag so the main loop can
    // do something about it:
    if (inChar == '\n' || inChar == '\r') {
      ss.print(inputString);
      inputString = "\0";
    }
  }
  
  // print the string when a newline arrives:
  if (stringComplete) {
    Serial.print(inputString);
    
    // clear the string:
    inputString = "\0";
    stringComplete = false;
  }
}



void LDR() {
  int ldr_value= analogRead(ldrpin);      //assign value of LDR sensor to a temporary variable
  Serial.println("Intensity="); //print on serial monitor using ""
  Serial.println(ldr_value);         //display output on serial monitor
  delay(300);
  }
```
# CIRCUIT DIAGRAM:

![image](https://github.com/dinesh2068/Monitoring-light-intensity-using-LDR-and-uploading-the-data-in-the-cloud-using-an-IoT-controller-./assets/151390189/6d2cc3f0-fd43-44dc-8101-a62f851f9388)

# OUTPUT:

![WhatsApp Image 2024-05-15 at 22 04 08_b91563ac](https://github.com/dinesh2068/Monitoring-light-intensity-using-LDR-and-uploading-the-data-in-the-cloud-using-an-IoT-controller-./assets/151390189/01b6fee6-bdae-4598-8474-d43465e8d14e)
![WhatsApp Image 2024-05-15 at 22 04 08_352f997a](https://github.com/dinesh2068/Monitoring-light-intensity-using-LDR-and-uploading-the-data-in-the-cloud-using-an-IoT-controller-./assets/151390189/68075b15-334c-41fb-9ed8-04934be84e8b)

# RESULT:

Thus the light intensity valve is uploaded in the Things mate using Arduino controller.
