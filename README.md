# SoftwareWire_TCS34725
Using Adafruit's TCS34725 with SoftwareWire to use two sensors on the same microcontroller.

To run this you should also use [SoftwareWire](https://github.com/Testato/SoftwareWire) as one of your Arduino Libraries.

## Usage

### Constructor

To create your instance of SoftwareWire_TCS34725 use the constructor `SoftwareWire_TCS34725`

```c
SoftwareWire_TCS34725(int sda, int scl, soft_tcs34725IntegrationTime_t = SOFT_TCS34725_INTEGRATIONTIME_2_4MS, soft_tcs34725Gain_t = SOFT_TCS34725_GAIN_1X);
```
 * `sda` - Virtual SDA pin
 * `scl` - Virtual SCL pin
 * `SOFT_TCS34725_INTEGRATIONTIME_2_4MS` - Time sampling the sensor pin, default is ```2.4 ms```
 * `SOFT_TCS34725_GAIN_1X` - Gain Applied to the sensor readings, default is ```1x```
 
| Values for Integration time       | Number of cycles | Max Value |      Gain Values     | 
| --------------------------------- |:----------------:|:---------:|----------------------|
|SOFT_TCS34725_INTEGRATIONTIME_2_4MS|      1 cycles    |    1024   |SOFT_TCS34725_GAIN_1X |
|SOFT_TCS34725_INTEGRATIONTIME_24MS |     10 cycles    |   10240   |SOFT_TCS34725_GAIN_4X |
|SOFT_TCS34725_INTEGRATIONTIME_50MS |     20 cycles    |   20480   |SOFT_TCS34725_GAIN_16X|
|SOFT_TCS34725_INTEGRATIONTIME_101MS|     42 cycles    |   43008   |SOFT_TCS34725_GAIN_60X|
|SOFT_TCS34725_INTEGRATIONTIME_154MS|     64 cycles    |   65535   ||
|SOFT_TCS34725_INTEGRATIONTIME_700MS|    256 cycles    |   65535   ||
