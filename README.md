# 8Bit/16Bit Parallel TFT Library for WiringPi

This is library for RaspberryPi/OrangePi.   
You can use a TFT Shield for UNO R3.   
This library can show a chart to TFT Shield.   

Supported TFT controllers:   
8bit Parallel ILI9325   
8bit Parallel ILI9327   
8bit Parallel ILI9341   
8bit Parallel ILI9342   
8bit Parallel ILI9481   
8bit Parallel SPFD5408   
8bit Parallel S6D1121   
8bit Parallel R61505U   
8bit Parallel R61509V   
8bit Parallel ST7781   
16bit Parallel ILI9341   

![2 4tft-1](https://cloud.githubusercontent.com/assets/6020549/24932714/bff42314-1f4d-11e7-8c13-28a6c4652992.JPG)

![2 4tft-2](https://cloud.githubusercontent.com/assets/6020549/24932732/d45d7080-1f4d-11e7-95d8-a34c0cb901b3.JPG)

Primarily, these TFT Shiled is the one for Arduino.   

----

# Wirering for 8Bit Parallel   

|TFT||Rpi/Opi|
|:-:|:-:|:-:|
|LCD_RST|--|Pin#7|
|LCD_CS|--|Pin#3|
|LCD_RS|--|Pin#5|
|LCD_WR|--|Pin#26|
|LCD_RD|--|Pin#28|
|LCD_D0|--|Pin#29|
|LCD_D1|--|Pin#31|
|LCD_D2|--|Pin#33|
|LCD_D3|--|Pin#35|
|LCD_D4|--|Pin#37|
|LCD_D5|--|Pin#32|
|LCD_D6|--|Pin#36|
|LCD_D7|--|Pin#38|
|5V|--|5V(*)|
|3.3V|--|3.3V(*)|
|GND|--|GND|

\*When a regulator(It's often AMS1117) is mounted on the back, it's operated 5V.   
\*When a regulator is NOT mounted on the back, it's operated 3.3V.   

You can change any pin.   
Pin define is "pin.conf".   

----

# Build   

for ILI9325   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9325   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9325   

for ILI9327   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9327   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9327   

for ILI9341   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9341   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9341   

for ILI9342   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9342   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9342   

for ILI9481   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9481   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9481   

for SPFD5408   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DSPFD5408   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DSPFD5408   

for S6D1121   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DS6D1121   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DS6D1121   

for R61505U   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DR61505U   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DR61505U   

for R61509B   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DR61509V   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DR61509V   

for ST7781   
cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DST7781   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DST7781   

----

# How to get your TFT controller CHIP_ID   

You can use this tool.   
https://github.com/nopnop2002/lcd_id

----

# Start Auto Demo   
./demo   

![ILI9341-10](https://user-images.githubusercontent.com/6020549/59558184-52df4900-9027-11e9-8e80-7c85fdb4213c.JPG)
![ILI9341-11](https://user-images.githubusercontent.com/6020549/59558185-52df4900-9027-11e9-84d6-cf6e69051ce8.JPG)
![ILI9341-12](https://user-images.githubusercontent.com/6020549/59558186-5377df80-9027-11e9-88a8-4c8c4df9a830.JPG)
![ILI9341-13](https://user-images.githubusercontent.com/6020549/59558187-5377df80-9027-11e9-8f72-a7ebbbe57c0b.JPG)
![ILI9341-14](https://user-images.githubusercontent.com/6020549/59558188-5377df80-9027-11e9-99f7-de3c8b1878dd.JPG)
![ILI9341-15](https://user-images.githubusercontent.com/6020549/59558189-54107600-9027-11e9-89eb-39e8f2cbeab2.JPG)
![ILI9341-16](https://user-images.githubusercontent.com/6020549/59558190-54107600-9027-11e9-9d23-d71c3997a3d0.JPG)
![ILI9341-17](https://user-images.githubusercontent.com/6020549/59558191-54107600-9027-11e9-888c-a1485758e943.JPG)
![ILI9341-18](https://user-images.githubusercontent.com/6020549/59558192-54107600-9027-11e9-946c-39443ae83053.JPG)
![ILI9341-19](https://user-images.githubusercontent.com/6020549/59558183-52df4900-9027-11e9-9a79-8969d47f902e.JPG)

----

# Start Interpreter mode   

./draw draw1.txt   
./draw draw2.txt   

cc -o rgb2color rgb2color.c   
bash ./me.sh   

You can change draw1.txt & draw2.txt & me.sh   

![me_sh](https://user-images.githubusercontent.com/6020549/42207927-f32ae206-7ee5-11e8-80a0-f5cb81d76747.JPG)

----

# Wirering for 16Bit Parallel   
|TFT||Rpi/Opi|
|:-:|:-:|:-:|
|LCD_RST|--|Pin#7|
|LCD_CS|--|Pin#3|
|LCD_RS|--|Pin#5|
|LCD_WR|--|Pin#26|
|LCD_RD|--|Pin#28|
|LCD_D0|--|Pin#29|
|LCD_D1|--|Pin#31|
|LCD_D2|--|Pin#33|
|LCD_D3|--|Pin#35|
|LCD_D4|--|Pin#37|
|LCD_D5|--|Pin#32|
|LCD_D6|--|Pin#36|
|LCD_D7|--|Pin#38|
|LCD_D8|--|Pin#13|
|LCD_D9|--|Pin#15|
|LCD_D10|--|Pin#16|
|LCD_D11|--|Pin#18|
|LCD_D12|--|Pin#8|
|LCD_D13|--|Pin#10|
|LCD_D14|--|Pin#40|
|LCD_D15|--|Pin#27|
|5V|--|5V(*)|
|3.3V|--|3.3V(*)|
|GND|--|GND|

\*When a regulator(It's often AMS1117) is mounted on the back, it's operated 5V.   
\*When a regulator is NOT mounted on the back, it's operated 3.3V.   

You can change any pin.   
Pin define is "pin.conf".   

----

# Build   

cc -o demo demo.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9341 -DP16BIT   
cc -o draw draw.c fontx.c ili93xx.c -lwiringPi -lm -lpthread -DILI9341 -DP16BIT   

----

# Start Auto Demo   
./demo   

![ili9341-16bit-1](https://user-images.githubusercontent.com/6020549/42122957-c62b7b66-7c84-11e8-8619-5c4ab0d624f5.JPG)

![ili9341-16bit-2](https://user-images.githubusercontent.com/6020549/42122960-c92f25e2-7c84-11e8-970b-11f0f08a88cd.JPG)

----

This module has SPI-Touch Sensor.   
So you can read touch position.   
Please make SPI effective first.

Wirering for SPI-Touch sensor   

|TFT||Rpi/Opi|
|:-:|:-:|:-:|
|PEN|--|Pin#22(\*\*)|
|T_CS|--|Pin#24(\*\*)|
|MOSI|--|Pin#19(\*\*\*)|
|MISO|--|Pin#21(\*\*\*)|
|CLK|--|Pin#23(\*\*\*)|


\*\*It's defined in the source cord.   
#define SPI_CHANNEL 0 // /dev/spidev0.0  
//#define SPI_CHANNEL 1 // /dev/spidev0.1  
#define GPIO_PEN 6   

\*\*\*Can't change   


cc -o xpt xpt.c xpt2046.c -lwiringPi -lm -lpthread   
sudo ./xpt   

![touch-1](https://user-images.githubusercontent.com/6020549/42130602-8710a000-7d24-11e8-9b8e-b1819301bc0f.jpg)


And you can operate Pi using touch sensor.  

cc -o touch touch.c fontx.c ili93xx.c xpt2046.c -lwiringPi -lm -lpthread -DILI9341 -DP16BIT   
sudo ./touch   


![touch-2](https://user-images.githubusercontent.com/6020549/42130606-8b7c0ed6-7d24-11e8-97e8-41f7cf18d4bc.JPG)

