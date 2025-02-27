## DFRobot_EC Library 
---------------------------------------------------------
This is the sample code for Gravity: Analog Electrical Conductivity Sensor / Meter Kit V2 (K=1.0), SKU: DFR0300.
## Table of Contents

* [Methods](#methods)
* [Compatibility](#Compatibility)
* [History](#history)
* [Credits](#credits)
<snippet>
<content>

## Methods

```C++

/*
 * @brief Init The Analog Electrical Conductivity Sensor
 */
void begin();

/*
 * @brief Convert voltage to EC with temperature compensation
 *
 * @param voltage     : Voltage value
 *        temperature : Ambient temperature
 *
 * @return The EC value
 */
float readEC(float voltage, float temperature);

/*
 * @brief Calibrate the calibration data
 *
 * @param voltage     : Voltage value
 *        temperature : Ambient temperature
 *        cmd         : enterec -> enter the EC calibration mode
 *                      calec   -> calibrate with the standard buffer solution, two buffer solutions(1413us/cm and 12.88ms/cm) will be automaticlly recognized
 *                      exitec  -> save the calibrated parameters and exit from EC calibration mode
 */
void calibration(float voltage, float temperature, char* cmd);

```

## Compatibility

MCU                | Work Well | Work Wrong | Untested  | Remarks
------------------ | :----------: | :----------: | :---------: | -----
Arduino Uno  |      √       |             |            | 
Leonardo  |      √       |             |            | 
Meag2560 |      √       |             |            | 

## History

- date 2018-11-6
- version V1.0

## Credits

Written by Jiawei Zhang(Welcome to our [website](https://www.dfrobot.com/))
  
My notes: 
Follow intruction below to use wifi module
https://robotdyn.com/uno-wifi-r3-atmega328p-esp8266-32mb-flash-usb-ttl-ch340g-micro-usb.html

http://arduino.esp8266.com/stable/package_esp8266com_index.json
  
Error to upload code to esp8266
https://forum.arduino.cc/t/esp-8266-timed-out-waiting-for-packet-header/597634/44
