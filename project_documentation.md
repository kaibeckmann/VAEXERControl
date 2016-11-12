# Project documentation

## Devices

### Type list

* Microchip TC74 I2C temperatur sensor [Datasheet](http://ww1.microchip.com/downloads/en/DeviceDoc/21462c.pdf)
* Maxim DS18B20 1-Wire temperatur sensor [Datasheet](http://datasheets.maximintegrated.com/en/ds/DS18B20.pdf)
* PTC heater element 12v, 50 grad, 2-8W
* Raspberry Pi Explorer Hat [Link](https://shop.pimoroni.com/products/explorer-hat) [github](https://github.com/pimoroni/explorer-hat)
* Raspberry Pi Zero [Link](https://www.raspberrypi.org/products/pi-zero/)
* peristaltic pump 12V, [aliexpress]()
* L298N h-bridge breakout 12V []()
* 4x relay break out, 5V []()
* Sharp GP2Y0A51SK0F Analog Distance Sensor 2-15cm [datasheet]https://www.pololu.com/file/0J845/GP2Y0A41SK0F.pdf.pdf)
* todo light, illumination sensor (ir, visible, uv?) i2c
* todo barometer sensor i2c
* todo humidity sensor i2c
* liqid level sensor
 * TI FDC1004 [site](http://www.ti.com/product/fdc1004) [datasheet](http://www.ti.com/lit/ds/symlink/fdc1004.pdf)
 * TI FDC2214 [site](http://www.ti.com/product/FDC2214) [datasheet]()
 * TI app note liqid level sensor [pdf[(http://www.ti.com/lit/ug/tidu736a/tidu736a.pdf)

## Raspberry Pi Pinout 

| GPIO    | Alt0    | Function      | used by     | function      | hydro connected       |
| :-----: | ------- | ------------- | ----------- | ------------- | -----------------     | 
| BCM  0  | SDA     | i2c ID bus0?  | hydro       | i2c 2         | TC74_1, FDC_1         |
| BCM  1  | SCL     | i2c ID bus0?  | hydro       | i2c 2         | TC74_1, FDC_1         |
| BCM  2  | SDA     | i2c bus 1?    | hydro, expl | i2c 1         | Analog, TC74_2, FDC_2 |
| BCM  3  | SCL     | i2c bus 1?    | hydro, expl | i2c 1         | Analog, TC74_2, FDC_2 |
| BCM  4  | GPCLK0  | general clock | hydro       | 1-wire        | T_1, T_2              |
| BCM  5  | GPIO    |               | hydro       | h-bridge in1  | pump_1                |
| BCM  6  | GPIO    |               | Explorer    | Output 1      | Light_1               |
| BCM  7  | CE1     |               | hydro       | h-bridge in2  | pump_1                |
| BCM  8  | CE0     |               | hydro       | h-bridge in3  | pump_2                |
| BCM  9  | MISO    | SPI           |             |               |                       |
| BCM 10  | MOSI    | SPI           |             |               |                       |
| BCM 11  | SCLK    | SPI           |             |               |                       |
| BCM 12  | GPIO    |               | Exporer     | Output 2      | Light_2
| BCM 13  | GPIO    |               | Explorer    | Output 3      | Heater_1
| BCM 14  | TXD     | UART          | hydro       | serial tx     |
| BCM 15  | RXD     | UART          | hydro       | serial rx     |
| BCM 16  | GPIO    |               | Explorer    | Output 4      | Heater_2
| BCM 17  | GPIO    |               | hydro       | h-bridge in4  | pump_2
| BCM 18  | PWM0    | HW PWM        |             |               |
| BCM 19  | GPIO    |               | Explorer    | Motor 1 +     | Fan_1
| BCM 20  | GPIO    |               | Explorer    | Motor 1 -     | Fan_1
| BCM 21  | GPIO    |               | Explorer    | Motor 2 +     | Fan_2
| BCM 22  | GPIO    |               | Exlorer     | Input 2       |
| BCM 23  | GPIO    |               | Exlorer     | Input 1       |
| BCM 24  | GPIO    |               | Exlorer     | Input 3       |
| BCM 25  | GPIO    |               | Exlorer     | Input 4       |
| BCM 26  | GPIO    |               | Explorer    | Motor 2 -     | Fan_2
| BCM 27  | GPIO    |               |             |               |

