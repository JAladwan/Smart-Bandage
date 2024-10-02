# Smart-Bandage Sensor System
*This is a project for a smart bandage that is designed to detect infections through sensor acquisition. It is currently a work in progress.* 

## Project Overview:
This project is a smart bandage designed to detect infections through continuous sensor data acquisition and will be sent via a WiFi module. 

### APDS9960: 
A color sensor used to measure clear, red, green, and blue light levels. These readings can indicate changes in skin color, which may signal an infection.
### TMP117: 
A high-precision temperature sensor that monitors skin temperature, detecting potential feverish symptoms, an early indicator of infection.
Currently, the code is optimized for testing and will be further refined as the product moves towards its final release. The project is in an early prototyping phase, focused on validating sensor functionality and data collection. Future iterations will integrate more advanced features and optimizations tailored for real-world use.

### Code Structure:
**Modular I2C Communication:** The program utilizes I2C communication via the STM32 HAL library to interact with both sensors, and includes mechanisms to switch between them efficiently during testing.

**UART Debugging:** Debugging is enabled via UART, allowing for easy monitoring and troubleshooting of sensor data during this testing phase.

**APDS9960 (Color Sensor):**
Functions to enable and disable the sensor to conserve power.
Acquires readings for clear, red, green, and blue light, which are processed for testing skin health metrics.

**TMP117 (Temperature Sensor):**
Continuously reads temperature data, converts the raw data into Celsius, and outputs it for further analysis.
Testing and Future Optimizations:
The code is structured to ensure effective testing and data validation during development. In this phase:

Sensor power management is implemented to test energy efficiency and the accuracy of sensor readings in different conditions.
The functionality of I2C communication between the MCU and sensors is a key focus, ensuring that both sensors can operate in tandem without conflict.
As development progresses, future optimizations will include more advanced error handling, sensor calibration, and energy-saving features for the final product. Additionally, threshold-based alerts will be integrated to signal potential infections based on sensor readings.

### Future Plans:
This repository will also include the PCB layout for the final smart bandage circuit, which is currently under design. The PCB will integrate both sensors (APDS9960 and TMP117) and the necessary microcontroller along with a chosen WiFI module. Once the final design is complete, the layout and BOM (Bill of Materials) will be added to the repository for reference.

The final product will be fine-tuned for performance and power efficiency, and adjustments will be made based on test results and feedback
