# Endangered-fish-Aquarium-monitoring-system

An automated Endangered Fish Aquarium Monitoring System designed to continuously monitor water quality using various sensors. The system uses an ESP32 microcontroller to collect real-time data from turbidity, pH, TDS, and temperature sensors, and automates control of the water filtration system to maintain ideal conditions for fish, especially endangered species like the Napoleon Wrasse.

Table of Contents
1.Project Overview
2.Features
3.Hardware Components
4.Software Requirements
5.Installation and Setup
6.Usage
7.Bluetooth Commands
8.Contributing

Project Overview
This project is designed to monitor aquarium water conditions using an ESP32 microcontroller with Bluetooth capability. The system measures:

TDS (Total Dissolved Solids) to evaluate water purity.
Water temperature using the DS18B20 temperature sensor.
Water quality using an analog sensor.
The data is transmitted over Bluetooth to a mobile device, and the user receives alerts about the water quality. The ESP32 will indicate whether the water quality is GOOD, DIRTY, or BAD based on the analog sensor readings.

Features
Real-time monitoring of water temperature and TDS levels.
Bluetooth data transmission to any paired device.
Water quality assessment based on analog sensor readings.
User feedback through serial output and Bluetooth messages.


Here’s a README template specifically for the Aquarium Monitoring System that uses Bluetooth and temperature sensors, as described by your code. This README will guide users through the project, including installation, usage, and how to understand the output from the Bluetooth-enabled monitoring system.

Aquarium Monitoring System with Bluetooth
This project monitors water quality in an aquarium using a TDS sensor and a DS18B20 temperature sensor. It sends real-time water quality data to a Bluetooth-enabled device (such as a smartphone) using the ESP32 microcontroller. The system also checks water clarity using an analog sensor and provides water quality status.

Table of Contents
Project Overview
Features
Hardware Components
Software Requirements
Installation and Setup
Usage
Bluetooth Commands
Contributing
License
Project Overview
This project is designed to monitor aquarium water conditions using an ESP32 microcontroller with Bluetooth capability. The system measures:

TDS (Total Dissolved Solids) to evaluate water purity.
Water temperature using the DS18B20 temperature sensor.
Water quality using an analog sensor.
The data is transmitted over Bluetooth to a mobile device, and the user receives alerts about the water quality. The ESP32 will indicate whether the water quality is GOOD, DIRTY, or BAD based on the analog sensor readings.

Features:
Real-time monitoring of water temperature and TDS levels.
Bluetooth data transmission to any paired device.
Water quality assessment based on analog sensor readings.
User feedback through serial output and Bluetooth messages.

Hardware Components:
ESP32: The central microcontroller.
TDS Sensor: Measures the total dissolved solids (connected to analog pin 36).
DS18B20 Temperature Sensor: Monitors water temperature (connected via GPIO 2).
Analog Water Quality Sensor: Measures water clarity.
Bluetooth Serial Communication: Sends real-time data to a smartphone or other device.

Pin Connections:
Component	Pin Number on ESP32
TDS Sensor	-GPIO 36 (Analog)
Temperature Sensor	-GPIO 2 (OneWire)
Analog Water Sensor	-GPIO 35 (Analog) 

Software Requirements:
Arduino IDE: Download and install from here.
ESP32 Board Package: Follow this guide to add ESP32 support in the Arduino IDE.
BluetoothSerial Library: This comes built-in with the ESP32 board package.
OneWire and DallasTemperature Libraries:
Install from the Arduino Library Manager.

Installation and Setup:
Step 1: Set up the Hardware
Connect the TDS sensor to the ESP32's GPIO 36.
Connect the DS18B20 temperature sensor to GPIO 2.
Connect the analog water quality sensor to GPIO 35.
Power the ESP32 using a USB cable or an external power source.
Step 2: Install Libraries
Open the Arduino IDE.
Install the required libraries:
Open Library Manager (Sketch -> Include Library -> Manage Libraries...).
Search for and install OneWire.
Search for and install DallasTemperature.
Step 3: Upload the Code
Copy the provided code into the Arduino IDE.
Select your ESP32 board and the correct COM port (Tools -> Board -> ESP32 Dev Module and Tools -> Port).
Click Upload to flash the code onto the ESP32.
Step 4: Pair with Bluetooth
Open the Bluetooth settings on your smartphone or PC.
Search for and pair with the device named AQUACULTURE.
Use any Bluetooth terminal app (e.g., Serial Bluetooth Terminal) to receive real-time water quality data.
Usage
Once the ESP32 is powered on and connected via Bluetooth, it will start collecting and transmitting data from the sensors.

The TDS sensor data is displayed as TDS PPM.
The temperature sensor data is shown in degrees Celsius.
The analog water quality sensor value determines whether the water quality is GOOD, DIRTY, or BAD.

Water Quality Conditions:
Good: Sensor value between 1800 and 2200.
Dirty: Sensor value between 1000 and 1750.
Bad: Sensor value below 1000.
Bluetooth Commands
You can send commands or receive sensor data via any Bluetooth terminal app on your phone or computer.

Sample Data Sent via Bluetooth:
TDS PPM: Indicates the total dissolved solids in the water.
Temperature: Water temperature in degrees Celsius.
Water Quality: Either "GOOD", "DIRTY", or "BAD" based on the analog sensor's readings.


Here’s a README template specifically for the Aquarium Monitoring System that uses Bluetooth and temperature sensors, as described by your code. This README will guide users through the project, including installation, usage, and how to understand the output from the Bluetooth-enabled monitoring system.

Aquarium Monitoring System with Bluetooth
This project monitors water quality in an aquarium using a TDS sensor and a DS18B20 temperature sensor. It sends real-time water quality data to a Bluetooth-enabled device (such as a smartphone) using the ESP32 microcontroller. The system also checks water clarity using an analog sensor and provides water quality status.

Table of Contents
Project Overview
Features
Hardware Components
Software Requirements
Installation and Setup
Usage
Bluetooth Commands
Contributing
License
Project Overview
This project is designed to monitor aquarium water conditions using an ESP32 microcontroller with Bluetooth capability. The system measures:

TDS (Total Dissolved Solids) to evaluate water purity.
Water temperature using the DS18B20 temperature sensor.
Water quality using an analog sensor.
The data is transmitted over Bluetooth to a mobile device, and the user receives alerts about the water quality. The ESP32 will indicate whether the water quality is GOOD, DIRTY, or BAD based on the analog sensor readings.

Features
Real-time monitoring of water temperature and TDS levels.
Bluetooth data transmission to any paired device.
Water quality assessment based on analog sensor readings.
User feedback through serial output and Bluetooth messages.
Hardware Components
ESP32: The central microcontroller.
TDS Sensor: Measures the total dissolved solids (connected to analog pin 36).
DS18B20 Temperature Sensor: Monitors water temperature (connected via GPIO 2).
Analog Water Quality Sensor: Measures water clarity.
Bluetooth Serial Communication: Sends real-time data to a smartphone or other device.
Pin Connections
Component	Pin Number on ESP32
TDS Sensor	GPIO 36 (Analog)
Temperature Sensor	GPIO 2 (OneWire)
Analog Water Sensor	GPIO 35 (Analog)
Software Requirements
Arduino IDE: Download and install from here.
ESP32 Board Package: Follow this guide to add ESP32 support in the Arduino IDE.
BluetoothSerial Library: This comes built-in with the ESP32 board package.
OneWire and DallasTemperature Libraries:
Install from the Arduino Library Manager.
Installation and Setup
Step 1: Set up the Hardware
Connect the TDS sensor to the ESP32's GPIO 36.
Connect the DS18B20 temperature sensor to GPIO 2.
Connect the analog water quality sensor to GPIO 35.
Power the ESP32 using a USB cable or an external power source.
Step 2: Install Libraries
Open the Arduino IDE.
Install the required libraries:
Open Library Manager (Sketch -> Include Library -> Manage Libraries...).
Search for and install OneWire.
Search for and install DallasTemperature.
Step 3: Upload the Code
Copy the provided code into the Arduino IDE.
Select your ESP32 board and the correct COM port (Tools -> Board -> ESP32 Dev Module and Tools -> Port).
Click Upload to flash the code onto the ESP32.
Step 4: Pair with Bluetooth
Open the Bluetooth settings on your smartphone or PC.
Search for and pair with the device named AQUACULTURE.
Use any Bluetooth terminal app (e.g., Serial Bluetooth Terminal) to receive real-time water quality data.
Usage
Once the ESP32 is powered on and connected via Bluetooth, it will start collecting and transmitting data from the sensors.

The TDS sensor data is displayed as TDS PPM.
The temperature sensor data is shown in degrees Celsius.
The analog water quality sensor value determines whether the water quality is GOOD, DIRTY, or BAD.
Example Output via Bluetooth:
java
Copy code
TDS PPM = 560.49
Temperature: 25.68ºC
sensor = 1900
WATER QUALITY IS GOOD
This data is transmitted every 500 milliseconds to the paired Bluetooth device.

Water Quality Conditions:
Good: Sensor value between 1800 and 2200.
Dirty: Sensor value between 1000 and 1750.
Bad: Sensor value below 1000.
Bluetooth Commands
You can send commands or receive sensor data via any Bluetooth terminal app on your phone or computer.

Sample Data Sent via Bluetooth:
TDS PPM: Indicates the total dissolved solids in the water.
Temperature: Water temperature in degrees Celsius.
Water Quality: Either "GOOD", "DIRTY", or "BAD" based on the analog sensor's readings.

Contributing:
Contributions are welcome! If you have ideas to improve the project, feel free to open an issue or submit a pull request.
