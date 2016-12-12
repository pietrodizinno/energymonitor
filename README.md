# Energy Monitor

![Alt completed](/images/2016-09-05%2017.05.03.jpg?raw=true)

This repository encapsulates one phase energy monitor for ThingSpeak based on ESP8266-01 module, current transformer and precision rectifier.

Because ESP8266-01 has only two digital I/O pins (and also for precision) is for A/D conversion used 18bit I2C A/D converter MCP3421
and fullwave precision rectifier realized via OZ LM258. For measuring current is used current transformer 30A SCT-013-030 which has already integrated shunt resistor (available through ebay).

For powering is used miniature 3.3V/600mA power supply from eBay such as http://www.ebay.com/itm/400761809788, but due to initial power requirements of ESP8266 i recomend 3.3V/1A power supply (is also available through this seller).

Repository contains Eagle schematic and PCB layout. Because i do not have equipment for handling SMDs (and also for use MCP3421 on breadboard) i created small DPS that holds MCP3421 and has standard DIP dimensions.

Arduino software can be uploaded to ESP8266 via Arduino IDE. For first 5 minutes after module startup is available WiFi AP "EnergyMonitor" with HTTP server at 192.168.4.1:80 behind it. On this URL is available simple configuration page for setting WiFi parameters, ThingSpeak channel/field with write-key, mains voltage and other tunning parameters. Configuration server is after startup also available on internal network at DHCP assigned IP address. Default parameters can be set in source file.

There is also OpenSCAD model for case.

I use module for several months at home and also on cottage. Public channels on ThingSpeak are:

https://thingspeak.com/channels/150525

https://thingspeak.com/channels/157732

Here are some project images:

### PCBs
![Alt pcbs](/images/2016-09-01%2017.50.18.jpg?raw=true)
### Mounted PCB
![Alt pcbs](/images/2016-09-02%2022.31.33.jpg?raw=true)
### 3D printed case
![Alt pcbs](/images/2016-09-04%2022.42.33.jpg?raw=true)
