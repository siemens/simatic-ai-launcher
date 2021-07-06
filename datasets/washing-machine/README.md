


# Washing-machine dataset

This folder contains multi-variate time series measurements, which are compatible with and can be used in AI Designer. 

All measurements contain a dataset showing energy consumption and motion data of a washing machine during different washing programs. Each measurement is stored both as raw and preprocessed data in different file formats.

## File naming convention

The filenames are encoding the base length (real length is variable due to the variable weight of the load), the temperature of the washing program, and if the file contains raw or preprocessed data. For example 240m60d-raw.* file contains the raw data of a 240 minutes base length, 60 celsius washing program, while 45m30d-ts.* contains the preprocessed (time shifted) data of a 45 minutes base length 30 celsius washing program.

### File Formats

All measurements are stored in 2 different file formats:
- **.csv**: comma separated values in a simple text file, edible for humans, and can be imported to more advanced tools, like Excel.
- **.parquet**: a binary format storing all data and meta data including data types. This can be read and used in data processing libraries like *Pandas*. 

### Data Columns

The following variables are stored as columns in every file:
- **DateTime**: timestamp showing when the data was recorded
- **temperature**: inner temperature of a power meter device 
- **power**: showing how much power is used by the machine in kW. It is updated at least every 30 seconds, or more often if there are significant changes in the measured value. 
- **energy**: showing how much power is used by the plugged in device in kWh. It was not set to zero after measurements, thus, it is not always starting with 0.0.
- **aX, aY, aZ**: accelerometer data read periodically (roughly twice a second)
- **gX, gY, gZ**: gyroscope data read periodically (roughly twice a second)
All but the timestamp data is stored as floats in the .parquet files.

### Raw Data and Preprocessed Data

The raw data (&ast;-raw.&ast;) contains one measurement in each row, because the data was collected by using an MQTT subscription (which updated one MQTT topic at once). This means, that the data can be represented as a large sparse matrix. For this reason, we implemented a simple time shift preprocessing. This process takes the data read most rarely (which is the power consumption, a dynamically read property), and at every update of it's value a full row is created by using the maximum absolute values of every other measurement since the latest update. This results in a much smaller, dense representation stored in the preprocessed data files (&ast;-ts.&ast;).

## How to reproduce measurements

### Hardware

All data used are collected by one of the following devices:

1. [Shelly Plug S](https://shelly.cloud/products/shelly-plug-s-smart-home-automation-device/): It is a WiFi enabled smart plug, able to report energy usage data. The *power*, *energy*, and *temperature* values are collected by this device to an MQTT server running on a PC. (As mentioned before, temperature is the inner temperature of this device, not the washing temperature of the washing machine.) All of the measurements are reported at least once every 30 seconds, or more often, when the *power* value changes significantly.
2. [MPU6050 module](https://components101.com/sensors/mpu6050-module): It is a 3-axis accelerometer and gyroscope module able to report data through I2C communication. An [Arduino Uno](https://store.arduino.cc/arduino-uno-rev3) receives this data and forwards it to a PC through a USB cable, which then sends it to the MQTT server

### Software

- A [Mosquitto MQTT](https://mosquitto.org/) server was used to collect all data. The server was running on a PC, while different devices and python scripts reported all the measurements as MQTT clients.
- The Arduino Uno was programmed in the Arduino Development environment. The algorithm is simply reading all available data from the MPU6050 unit periodically using the *MPU6050_tockn* and *Wire* libraries, does some formatting and sends it to the PC using serial communication in a single string roughly twice a second.
- A python script was written to read the serial data received from the Arduino Uno, parse it, and send it to the MQTT server using [paho-mqtt](https://pypi.org/project/paho-mqtt/) library.
- A python based MQTT client was written to subscribe all possible variables using [paho-mqtt](https://pypi.org/project/paho-mqtt/). This subscriber uses a DataFrame from the [pandas](https://pandas.pydata.org/) library to collect the data, preprocess it, and export both the raw data and a time shifted data into *.parquet* and *.csv* files.

# Legal information

This content may contain hyperlinks to the web pages of third parties. Siemens shall have no liability for the contents of such web pages and does not make representations about or endorse such web pages or their contents as its own, as Siemens does not control the information on such web pages and is not responsible for the contents and information given thereon. The use of such web pages shall be at the sole risk of the user.
