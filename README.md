# xvc-esp8266
Xilinx Virtual Cable Implementation based on ESP8266

# Compiling

Please set the CPU frequency to 160MHz and lwIP variant to "v2 Higher bandwidth" in Arduino IDE for better performance.

# Pinout

JTAG A, TCP port 2542

|GPIO|JTAG|
|-|-|
|GPIO4|TCK|
|GPIO5|TDO|
|GPIO10|TDI|
|GPIO9|TMS|

JTAG B, TCP port 2543

|GPIO|JTAG|
|-|-|
|GPIO14|TCK|
|GPIO12|TDO|
|GPIO13|TDI|
|GPIO2|TMS|

UART, TCP port 2544

|GPIO|UART|
|-|-|
|TX0 (GPIO1)|TX|
|RX0 (GPIO3)|RX|

## Note:
Don't use GPIO pin 16. It's controlled by a different register and it's very slow to toggle, at least 2x slower than other GPIO pins.
