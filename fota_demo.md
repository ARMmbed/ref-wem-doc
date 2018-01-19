# License Status

| Name | Repository | License | Trademark/Copyright | Patent | 3PIP | OSS | Approval Date | Approved SHA | Changes Requiring Review | Service Now Ticket | Created by RED | Publicly Accessible | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| fota-demo	| http://github.com/armmbed/fota-demo.git | Apache License 2.0 | Approved | Approved | Requested | Requested | | | | RITM0035447 | Y | N | Sales Tool Demo - FOTA |
| fota-hardware | http://github.com/armmbed/fota-hardware.git | Solderpad License v0.51 | Approved	|	Requested	|Requested | | | | | RITM0035447	| Y | N	| Sales Tool Demo - FOTA |
| fotaportal | http://github.com/armmbed/fotaportal.git | Apache License 2.0 | Approved | Approved	Requested | Requested | | | | | RITM0035447 | Y |	N | Sales Tool Demo - FOTA |
|DHT|http://github.com/armmbed/dht.git|Apache License 2.0|Approved| |Requested|Requested| |f6cd0c6| |RITM0035447||C|N|
|fota-demo-bootloader|http://github.com/armmbed/fota-demo-bootloader.git|Apache License 2.0|Approved| |Requested|Requested| | | | |C|N|No longer used. A patch will be maintained which will be applied to the mbed-bootloader-restricted repository.|
|ws2801|http://github.com/armmbed/ws2801.git|Apache License 2.0|Approved| |Requested|Requested| |9706013| |RITM0035447|C|N|
|Sht31|https://mbed.org/users/andcor02/code/Sht31|BSD License| | | | | |c84a603| | |N|Y
|TSL2591| | | | | | | | | | |C|N|Files may have been pulled from mbed Developer website with NO specific license mentioned|https://os.mbed.com/users/12104404/code/TSL2591/ |
|PCA995xA|https://github.com/ARMmbed/PCA995xA.git|Apache License 2.0| | | | | |66241d8| | |C|N|
|TextLCD|https://github.com/ARMmbed/TextLCD|MIT License| | | | | |9e7940c| | |C|N
|ESP8266|https://github.com/armmbed/esp8266-driver|Apache License 2.0| | | | | ||fdb44a4| | |N|Y
|SPI Flash|https://github.com/ARMmbed/spif-driver|Apache License 2.0| | | | | |c46b2a7| | |N|Y
|SD Driver|https://github.com/ARMmbed/sd-driver|Apache License 2.0| | | | | |1cb007f| | |N|Y
|RapidJson|https://github.com/miloyip/rapidjson|MIT License| | | | | |f05edc9| | |N|Y||mbed OS|https://github.com/ARMmbed/mbed-os|Apache License 2.0| | | | | |6e0d01c| | |N|Y
|mbed Cloud Update CLI|https://github.com/ARMmbed/mbed-cloud-update-cli| 497567c| | |N|N|Created by us, no License currently exists|
|mbed Cloud Client|https://github.com/ARMmbed/mbed-cloud-client-sources-internal|ARM Proprietary| | | | | |5412d5c| | |N|N|
|mbed Bootloader|https://github.com/armmbed/mbed-bootloader-internal|2cc3ad9| | |N|N|No License?|


# Links

* JIRA: 
    * *http://us-aus-igor.austin.arm.com:8080/secure/RapidBoard.jspa?rapidView=1&projectKey=RED
* Github:
    * https://github.com/ARMmbed/fota-demo
    * https://github.com/ARMmbed/fota-hardware
    * https://github.com/armmbed/fotaportal
    * https://github.com/armmbed/fota-demo-bootloader
    * https://github.com/ARMmbed/red-web-docs
* Jenkins: https://jenkins-internal.mbed.com/view/RedTeam/job/RedFotaDemo/
* 3d Printer Webcam: http://10.118.14.54:8080/?action=stream
* Cloud Webhook: http://ec2-34-229-249-172.compute-1.amazonaws.com/live-device/mbed-cloud-webhook/
* Staging Cloud Webhook: http://staging.fotaportal.red.mbed.fattuba.com/live-device/mbed-cloud-webhook/
* Staging Document Website: http://test.deploymbed.com:5000/

# Demo Videos
* https://youtu.be/lzeMOiA2W_Y
* https://youtu.be/AVaQs_Vno0o
* https://youtu.be/UlDpxea2mRo
* https://youtu.be/K7ORvPeTZE0
* Sprint 5
    * user-configured geolocation: https://youtu.be/JKSWBP-V2dQ
    * network recovery: http://www.youtube.com/watch?v=ctsBVZ8ce44
* Sprint 6
    * Live data on the Reference Design webapp:  https://youtu.be/iAD0eB8nPkg
    * Fota-demo on Ublox EVK-ODIN-W2: https://youtu.be/A6-nTCSTAPM
    * Reference Deployments Website: https://youtu.be/xX1V5CjNsGM
* Sprint 7
    * Using python project for upcoming workshop:  https://youtu.be/kdmHD2R4-hU


# Fota Portal

On staging, to connect your device to the Fota Portal so that telemetry data is graphed on the Live Device page, add your mbed cloud account API key here:

 http://staging.fotaportal.red.mbed.fattuba.com/admin/livedevice/mbedcloudaccount/

login: staging
password: foobar


...and on production:

http://ec2-34-229-249-172.compute-1.amazonaws.com/admin/livedevice/mbedcloudaccount/

login: production
password: halarges
Registering your mbed cloud account API key generates a request to the mbed cloud portal to set your account's notification webhook to point to the Fota Portal webhook handler.

Mbed cloud account API keys can be created in your mbed cloud portal here:

https://portal.us-east-1.mbedcloud.com/access/keys

Once you've saved your Mbed cloud api key, you'll need to click "Start long poll".

|Deliverable|Product Status|Product (Hardware)|Has Been Delivered|Instructions|QRCode|Status|Certificates|Who Has It?|
|---|---|---|---|---|---|---|---|---|
|Starter Kit 1 (Earwig)| | | | | [QR Code](./qrcode_0.svg "Title")|Completed||
|Starter Kit 2 (Earwig)| | | | | [QR Code](./qrcode_1.svg "Title")|Completed FW: v1.9.1 FOTA: PASS Label: starter-kit2|Sales Tool Demo - FOTA| |
|Starter Kit 3 (Earwig)| | | | |qrcode_2.svg|Waiting on plastics FW: v1.9.1 FOTA: PASS Label: starter-kit|Sales Tool Demo - FOTA|
|Starter Kit 4 (?)     | | | | |qrcode_4.svg|?||

# Hardware
## Component Catalog
|Category|Component|Rev B (Bumblebee)|Rev C (Centipede)|Rev D (Dragonfly)|Notes|
|---|---|---|---|---|---|
|Main board|FRDM-K64F|X|X|X|  Info:  https://developer.mbed.org/platforms/FRDM-K64F/  Buy:  http://www.mouser.com/ProductDetail/NXP/FRDM-K64F/
|Main board|Base Shield V2|X|X|X|Info/Buy:  https://www.seeedstudio.com/Base%20Shield%20V2-p-1378.html
|Storage|MicroSD card| |X|X|Info:  https://www.sandisk.com/home/memory-cards/microsd-cards/sandisk-microsd <br/>Buy:  https://www.amazon.com/SanDisk-Memory-Frustration-Free-Packaging-SDSDQ-008G-AFFP/dp/B007KFXICK
|WiFi|ESP8266 UART|X|X|X|Info/Buy:  https://www.seeedstudio.com/Grove-Uart-Wifi-p-2495.html
|WiFi|ODIN-W262||||Info/Buy:   https://www.u-blox.com/en/product/odin-w2-series
|LED|WS2801 strip (5x LEDs)|X|||Info:controller: WS2801  https://cdn-shop.adafruit.com/datasheets/WS2801.pdf <br/>LED: 5050 SMD RGB, Smalite SL-C25050-AL http://www.chinaseniorsupplier.com/Lights_Lighting/Other_Lights_Lighting_Products/516189574/LED_smd_RGB_epistar_chip_for_LED_lights.html <br/>Buy:  https://www.amazon.com/NooElec-Addressable-Waterproof-Connectors-Pre-Soldered/dp/B008F05N54
|LED|WS2801 string (7x LEDs)| |X|X|Info: controller: WS2801  https://cdn-shop.adafruit.com/datasheets/WS2801.pdf <br/>Buy:  https://www.amazon.com/dp/B073QLVTB9
|LCD|16x2 I2C character display|X|X|X|Info:LCD DM-LCD1602-402:  https://drive.google.com/file/d/0B5lkVYnewKTGalhWazNhOGxVbUE/view?usp=sharing <br/>display driver SPLC780D:https://drive.google.com/file/d/0BxCL-uXywP6wQXlvMnRIaFN6UVU/view?usp=sharing<br/>cross ref product info:  https://www.displaymodule.com/products/dm-lcd1602-402 <br/>cross ref product info:  https://www.amazon.com/Qunqi-Serial-Backlight-Arduino-MEGA2560/dp/B01E4YUT3K <br/>Buy:  https://www.amazon.com/gp/product/B01LC7ECAS <br/>Note: This component requires the Grove Shield to be set to VCC=5V
|Power supply|XL6009-based buck-boost voltage regulator|X|X||Info:XL6009 regulator chip:  http://www.haoyuelectronics.com/Attachment/XL6009/XL6009-DC-DC-Converter-Datasheet.pdf <br/>DSN6000AUD board <br/>Buy:  https://www.amazon.com/adjustable-Converter-XL6009-Module-Voltage/dp/B01JCN7XDM
|Power supply|LM2596/LM2577 buck-boost voltage regulator||||Info/Buy:  https://www.amazon.com/SMAKN-Adjustable-converter-LM2596-LM2577/dp/B00FIYOK5O
|Power supply|PowerBoost 1000 Charger 5V/1A LiPo USB| | |X|Info/Buy: https://www.adafruit.com/product/2465
|Power supply|Lithium Ion Battery Pack 3.7V/4400mAh||||Info/Buy: https://www.adafruit.com/product/354
|Power supply|LiPo Battery Pack 3.7V/2500mAh| | |X|Info/Buy: https://www.adafruit.com/product/328
|Cable|Low profile angled microUSB cable|X|X||Buy:  https://www.amazon.com/CablesOnline-Micro-B-Position-Extension-AD-U44/dp/B00JSXUJ7Y/ <br>Buy:  https://www.amazon.com/gp/product/B01LZFKVDP
|Cable|USB extension cable|X|||Buy:  https://www.amazon.com/gp/product/B06XXL2H6F
|Cable|microUSB cable angled up| | |X|Buy:  https://www.amazon.com/CablesOnline-Micro-B-Position-Extension-AD-U44/dp/B00JSXUJ7Y/
|Connector|microUSB female| | | |Info/Buy: http://www.mouser.com/Search/ProductDetail.aspx?qs=1Nn7v2rJFSJs6IftS%252bmZAw%3d%3d?
|Power switch|1P2T SPDT slide switch| | |X|Info/Buy: https://www.amazon.com/gp/product/B007QAJMHO
|Filter|Thermwell 15X24x3/16 Open Cell Foam F1524 Air Conditioner Filter|X|X|X|Buy:  https://www.amazon.com/gp/product/B000BO68BU
|Filter|Stainless steel woven wire mesh 0.038mm aperture| | | |Buy:   https://www.amazon.com/gp/product/B01N5SZRS8
|Sensor (light, analog)|Grove Light Sensor (P) v1.1| |X|X|Info/Buy: https://www.seeedstudio.com/Grove-Light-Sensor-%28P%29-v1.1-p-2693.html
|Sensor (sound, analog)|Grove Loudness Sensor| | | |Info/Buy: https://www.seeedstudio.com/Grove-Loudness-Sensor-p-1382.html
|Sensor (temperature, analog)| | |X|
|Sensor (temp & humidity, digital)|Grove Temperature&Humidity Sensor Pro| |X|X|Info/Buy:  https://www.seeedstudio.com/grove-temperaturehumidity-sensor-pro-p-838.html
|Battery contacts|(4x) Keystone 288 dual leaf spring battery contact|X|X||Buy:  https://www.amazon.com/gp/product/B00QZE4YAM

# Enclosure

### Prototype A (Aardvark)
Description: off the shelf enclosure
Info/Buy:  https://www.okwenclosures.com/en/Synergy/ER126059.htm

### Prototype B (Bumblebee)
Description: custom design, 3D printed on a cartesian FDM printer, 0.1mm layer height, finished with metallic paint and acrylic disc light pipe
Preliminary model preview:
TinkerCAD concept  https://www.tinkercad.com/things/2Yf9L3Xwajp-sales-tool-device-wip/editv2?sharecode=l5UYDPa3LTG5JpMvsD18oKAgj9v4-I8xtR5Nlx7OA5M=
After sanding and painting:

### Materials:
PolyMax PLA 1.75mm  https://www.amazon.com/Polymaker-PolyMax-Filament-Jam-Free-Stronger/dp/B01I4SDE70
Acrylic sheet 0.8mm  https://www.amazon.com/dp/B01N7MLF3D
XTC-3D High Performance Self Leveling Epoxy  https://www.amazon.com/XTC-3D-High-Performance-Print-Coating/dp/B00PFXK4JY
primer - Dupli-Color Primer Filler  https://www.amazon.com/Dupli-Color-FP101-General-Purpose-Sandable/dp/B000B6DG7C
paint - Testors Graphite Gray Metallic 1253  https://www.amazon.com/Graphite-Metallic-Spray-Enamel-Paint/dp/B00NQCHTHG
Prototype C (Centipede)
Description: custom design, 3D printed on a cartesian FDM printer, 0.1-0.4mm layer height, finished with metallic paint and silicone embedded 3D printed light pipes
LED order (1 = closest to the connector):

|1|2|3|4|5|6|7|
|-|-|-|-|-|-|-|
|power|wifi|cloud|update/FOTA|light sensor|temp/humidity sensor|LCD / future sound sensor

### Materials:
PolyMax PLA 1.75mm  https://www.amazon.com/Polymaker-PolyMax-Filament-Jam-Free-Stronger/dp/B01I4SDE70
XTC-3D High Performance Self Leveling Epoxy  https://www.amazon.com/XTC-3D-High-Performance-Print-Coating/dp/B00PFXK4JY
primer - TBD
paint - TBD
Assembly:


## Finished look:


### Prototype D (Dragonfly)
Description: custom design, same manufacturing and finish as Rev C; powered by a LiPo flat pack and a battery charging power circuit, with a microUSB female connector and a power switch exposed on the lower part of the enclosure

LED order is the same as Rev C

Materials are the same as Rev C

### Finished look:


### Prototype E (Earwig)
Description: custom design, downsized from Rev D, fitted with a custom design PCB and intended for external manufacturing and finish due to high demand; reworked locking mechanism acts as ventilation slots when fully locked; top has symmetrical vents positioned to facilitate convection; battery holder fits both the 2500mAh flat pack used in Rev D, as well as a 4400mAh dual 18650 round pack

LED order is the same as Rev C

Design images
Rendered images:

### Finished look:

# External manufacturing:
### Manufacturing Plastics

||FDM|SLA|PolyJet|SLS|CNC|Sanding|Painting|Anodizing|Injection molding|Mold casting|Notes|
|---|---|---|---|---|---|---|---|---|---|---|---|
|Fictiv.com|$104.23|-|$363 ($2500 mentioned for 15 units)|-|$1308|$50/hour|$100|TBD|-|-|Dual material for FDM and PolyJet Est. manual finishing cost $350-$500
|Goengineer.com|$170|-|$250|-|-|-|-|-|-|-|Dual material for PolyJet only, no finishing Shipping $25
|Ponoko.com|-|-|-|-|-|-|-|-|-|-|Laser cutting and engraving only
|Protocase.com|-|-|-|-|TBD| | |TBD They offer volume production as well
|Protolabs.com| | | | | | | | | | |TBD
|Sculpteo.com|$198.84|$479.98|$367.59|$226.42 Carbonmide $138.38 Alumide $1042.39 Aluminum $176.48 Ni plated steel|-|$10.43 (FDM)|TBD|-|-|-|Also offer hand polishing for SLA, price TBD
|Seeedstudio.com|-|-|-|-|-|-|-|-|$6k-$12k|$6k-$16k
|Shapeways.com|$46.68 PLA $140.57 polished metallic plastic $87.70 strong&flexible|$241.81 Acrylic $151.56 Frosted Ultra|-|$416.01 polished Ni steel|$1095.75|$1 (s&f)|-|-|-|-|Estimates unavailable with light pipes separated from the top
|UPS.com|$148, 3 days|-|-|-|-|-|-|-|-|-|No finishing, single material only

### Manufacturing choices:
Due to the fact that the top part has built-in light channels, manufacturing choices are split in two categories. First, printing the top part without light channels and adding them in-house, either via translucent material pouring (e.g. epoxy or silicone gel) or via press-fitting acrylic cut parts. Both variants are difficult and are likely to yield low quality results (e.g. uneven surfaces or gaps). Second, printing the top part with a dual material process. This is the recommended action, even though it comes with a severe limitation in manufacturing processes. Only FDM and PolyJet are able to embed translucent material into a part. Of the two, FDM is the most cost effective, and PolyJet is the better looking. The exact difference in unfinished quality will vary with the manufacturer. The recommended course of action is to get one unit with each of the two processes, and pick one to move forward based on visual inspection.

### Finishing choices:
For our in-house production we have used manual sanding and painting for the best results. Manufacturing houses all want to avoid this, because of the high and non-scalable cost. Some houses offer automatic sanding and some mention the ability to paint, but without specific pricing. The recommendation is to manufacture the parts with no finish or with only automatic sanding, and see whether the outcome looks satisfactory enough.

# Manufacturing Electronics

|Manufacturer|5 boards PCB|5 boards assembly|30 boards PCB|30 boards assembly|Tooling|Notes|
|---|---|---|---|---|---|---|
|Eagle Circuits (Dallas) | \$155.53 5 days <br> \$137.58 10 days |||| \$1075 |	Recommended by Charles Dittmer <br> They would make 5 boards first and 25 upon our approval
|LTEK (Slovenia)|EUR 210.21 including most of the BOM (see notes) || EUR 77.40	||EUR 612.40 |Recommended by Chris Styles <br> Quote does not include the Odin part, they told us they couldn't source it
|Advanced Circuits (CO/AZ/MN)|\$178.67 1 day <br> \$76.37 3 days | \$408.95 2 days <br> 227.20 10 days| \$31.96 1 day <br> \$14.91 3 days | \$106.55 2 days <br> \$59.20 10 days | \$0? 
|Screaming Circuits (Oregon)|N/A|\$292.41 2 days <br> \$207.09 10 days |  N/A | \$107.90 2 days <br> \$65.35 10 days |	$0|	Partner of Sunstone Circuits for assembly
|Sunstone Circuits (Oregon)|\$156.74 1 day <br> \$50.28 21 days | \$175 unknown lead time	| \$41.87 1 day <br> \$13.96 21 days | \$49.80 unknown lead time | \$0?
|ExpressPCB (Oregon) | \$41.50 2 days <br> \$25.41 1 day | N/A | N/A | N/A	|\$0|ProtoPro (batch of 4 boards only)
|Smart Prototyping (Hong Kong)|\$6.67 4 days | N/A | $2.34 4 days | N/A | $0 | +\$28 for 2 day orders <br> +\$50 for 1 day orders
|Seeed Studio (China) |TBD|TBD|TBD|TBD|TBD
|PCBCart (China) | \$9.51 4 days <br> \$8.50 5 days <br> \$18.73 8 days <br> \$18.21 12 days| available, price NA <br> available, price NA|\$5.24 4 days <br> \$4.23 5 days <br> \$5.10 8 days <br> \$4.92 12 days | available, price NA  | \$0 for PCB, unknown for assembly <br> \$37 for PCB, unknown assembly| Prototype Quality <br> <br> Regular Quality
|Elecrow (China) |\$42 2-3 weeks | |TBD |TBD|TDB|A lot of components (R,C mostly) in their internal catalog are provided for free.The Odin part is \$75, BOM comes to \$130.
|PCBTrain (UK)|£36.38 5 days <br> £27.78 10 days | £135.59 7 days <br> £112.01 15 days |£14.87 5 days<br>£11.58 10 days | £57.92 15 days| \$0? 


\* Listed cost is per board; tooling cost is always included in the board cost even though it may be listed separately as well; quotes do not include BOM price unless otherwise indicated

\*\* Mfg recommendation thread

BOM cost (DigiKey): $120 for one board, $548 for 5 boards, $2778 for 30 boards
Additional components (LiPo + Molex cable): $20.03 for one board, $92.70 for 5 boards, $537.96 for 30 boards

## Prototype F (Firefly)
Description: complete rework - The PCB is now a single board design and has a modified shape. Test points are present for future test fixture and factory provisioning purposes. Enclosure parts are modular for more versatility and for cheaper and better printing. The locking mechanism is on the top half now, to allow inserting the new PCB at assembly time. Exposed microUSB connector, sliding power switch, charging LED, and a button, all on the upper rim of the enclosure. The bottom side of the enclosure is used only for the battery now, which is larger than in the previous revisions (4400mAh 18650x2 instead of 2500mAh flat pack). The light sensor has its own window, to maximize response to environment changes. The temp/humidity sensor is placed in a thermal relief area on the PCB and positioned directly under an air vent, to make readings more accurate and more responsive. Light pipes are joined together to facilitate future press fit manufacturing. Locking clips and clamps are used throughout, to eliminate the need for hot gluing during assembly.

LED order and face plate looks are the same as Rev E

Required and suggested PCB fixes from revision E:

|Item|Required? (O=Optional)|Comment|Action|
|---|---|---|---|
|Schematic|O|	Remove text crossing wires or overlapping other text
|Schematic|O|Pins C6-C13 are labeled as reserved in the data sheet, but there may be a SPI interface behind those pins that the general data sheet does not show.
|Schematic|N|LED8 not lit when battery is disconnected
|Schematic|Y|U11 pin 5 (OE) needs to be grounded (instead of pulled up to +3.3V), or connected to an I2C bus controller's OE line|Done as of Oct 20th 2017.
|Schematic|N|Temperature sensor RESET line (U9 pin 6) needs to be tied to an available GPIO pin on the STM32F4xx for sinking (still need the pull up resistor to VDD)
|Schematic|N|PCA9956B PWM driver (U11) needs the RESET line (pin 35) tied to an available GPIO pin on the STM32F4xx for sinking (still need the pull up resistor to VDD)
|PCB|N|Rotate Molex connector on bottom board by 180 degrees
|PCB|Y|Mount microUSB connector on the underside of the PCB (same side as the power switch)|Done as of Oct 20th 2017.
|PCB|Y|Height clearance: move L1 and C30 away from arc edge (radially inward) by dR=3 mm|Done as of Oct 20th 2017.
|PCB|Y|Move light sensor 4.2mm to the left (towards the USB connector)|Done as of Oct 20th 2017.
|PCB|O|Rotate LED8 so that it is perpendicular to the board edge's tangent
|PCB|O|More stitching vias on the smaller board between the top and bottom ground planes
|PCB|O|Better decoupling can be achieved between C1/C2/C3 by placing the smallest value capacitor closest to the power pin
|PCB|Y|If using the ODIN integrated antenna we need to trim back the ground plane on that side of the module to improve RF performance. The integration guide indicates the module should be at the edge of the board: |https://www.u-blox.com/sites/default/files/ODIN-W2_SIM_%28UBX-14040040%29.pdf
|PCB|O|Silkscreen over pads of some footprints may cause problems with assembly (e.g. U14 outline and C30)
|PCB Mfg|Y|U10 was populated wrong (needs to be rotated 180 degrees)
|PCB Mfg|Y|LED8 was populated upside down (keep orientation, flip 180 degrees)
|Hardware| |Should an additional sensor be placed on the board for developer experience?
|Hardware| |Need an external power adapter or cord for out-of-box experience.
|Firmware| |Need to ensure that the correct DAPLink firmware has been flashed on the board. Currently the board comes up with "CRP_DISABLD" which indicates that DAPLink has no firmware.
|Software| |Mbed Cloud Starter Kit software downloaded from Apple App Store or Google Play Store?
|Software| |Updates to the FOTA demo software for new hardware (SHT library for temperature, PWM driver, light sensor, etc.)
|Miscellaneous| |Need an "attractive" box for the device, power cable, and instruction manual.
|Miscellaneous| |Need auto-generated cloud credentials that can be provided in the instructions so that user can get started immediately.
|Miscellaneous| |Need an instruction manual for getting started and a QR code which links to the instruction manual in case the physical one is lost.
|Miscellaneous| |A USB micro cable for serial debugging and flashing the device



## Bringup
1. Plug the board in. Make sure it enumerates as "CRP DISABLD". On a Mac, this will be under /Volumes.
2. Run this command: `rm /Volumes/CRP\ DISABLD/*; cp -X lpc11u35_mbed_cloud_connect_if_crc.bin /Volumes/CRP\ DISABLD/`
3. Wait for DAPLink to be flashed (depending on your machine, between 7 and ~70 seconds)
4. Turn the board off and then back on. Make sure it now enumerates as "DAPLINK". If it still enumerates as before, you didn't wait enough - go back to step 2.
5. Hold the Reset button down, and while keeping it down, run this command: `touch /Volumes/DAPLINK/auto_rst.cfg`
6. Let go of the Reset button. Wait for the board to reboot. Flash firmware. Profit.

## Assembly
1. Flush cut the leads at the edge of the PCB, so they fit under the enclosure rim.
2. Sand the light pipes, to make them diffuse.
3. Fill out the inside of the cloud icon with black marker or paint, to prevent the LED from shining through. Make sure you do not cross the cloud edge (where the light pipe is).
4. Remove the left half of the bottom clip, to help the PCB go in easier.
5. Assemble top plate with upper ring, with the USB hole at the bottom (below the LCD cutout). Push the pins down gently with a tool, don't push the ring itself or the pins will break. Make sure the plate is flush with the ring and no gaps are showing. Optionally, hot glue the pins in place to provide more durability.
6. Insert light guides (don't glue them) and adjust top of the marked tab to be even height.
7. Using a dab of glue (hot glue), put the tiny cylindrical light pipe in.
8. Assemble bottom plate with lower ring the same way as top plate in step 5.
9. Place battery in battery holder and assemble the holder onto the bottom plate.
10. Remove the LCD's protective sheet and insert PCB into top half of the enclosure. This is the trickiest step, as the fit is tight. Align the connectors to the holes first, then slide it in and seat it into the guide. The PCB is correctly inserted when there is no space between the LCD and the top plate of the enclosure. Bonus points if you avoid putting fingerprints on the LCD.
11. Insert the two round PCB clips and twist each of them 90 degrees clockwise to lock the PCB in place.
12. Connect battery to the PCB and twist lock the two enclosure halves. Test basic functions and ship it.

# Pinouts
## Base Shield:

||Aardvark|Bumblebee|Centipede|Dragonfly|
|---|---|---|---|---|
|A0|||	Grove - Light Sensor (P) v1.1|Grove - Light Sensor (P) v1.1
|A1||| 	[obsolete] Analog Temperature Sensor (reworked all units to DHT on D4)|N/C
|A2|||N/C|N/C
|A3|||N/C|N/C
|UART|||ESP8266 WiFi|ESP8266 WiFi
|D2|||WS2801 LED Controller (D2=data, D3=clock)	|WS2801 LED Controller (D2=data, D3=clock)
|D3|||N/C <br> (DO NOT USE THIS CONNECTOR - data line is taken by the WS2801 LED controller) |N/C <br>(DO NOT USE THIS CONNECTOR - data line is taken by the WS2801 LED controller)
|D4|||Grove - Temperature&Humidity Sensor Pro|Grove - Temperature&Humidity Sensor Pro
|D5|||N/C|N/C
|D6|||N/C|N/C
|D7|||N/C|N/C
|D8|||N/C|N/C
|I2C|||16x2 I2C LCD character display|16x2 I2C LCD character display
|I2C|||N/C|N/C
|I2C|||N/C|N/C
|I2C|||N/C|N/C

## Thermal

#### Design #1

- FRDM-K64F
- 1x Grove Seeed LED
- 1x WiFi ESP8266
- Cardboard enclosure
- Wall power

|Test|Description|0|1|2|3|4|5|10|15|30|45|60|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|1|Idle|83.4|83.4|85.1|86.6|86.5|86.1|85.4|85.7|85.3|86.4|84.7
|2|continuous wifi download <br>sha256 on downloaded data<br>LED on constant bright white|81.6|81.6|81.8|84.7|88.7|93.2|94.5|97.7|97.7|97.7|101.3


The plastic used for Bumblebee (PLA) has a melting point of 190C/374F and starts to deform (soften) at 60C/140F.

### Electric
The device uses [ TODO ] when fully powered (all LEDs to full brightness on white, WiFi connected and communicating, the LCD on at full contrast, and the MCU running a tight loop).

|Component|Hardware Revision|typical|max|notes|
|-|-|-|-|-|
|Complete device|Bumblebee|280mA|330mA|Normal operation: three LEDs on a primary color, WiFi connected, LCD on at normal contrast, sending data to the cloud periodically
||Centipede|340mA|400mA
|K64F+shield|
|voltage regulator|||90%|Efficiency
|WiFi||80mA|105mA|observed values
|LCD 16x2|| 24.5mA
|RGB LED||10mA|60mA|It uses up to 20mA per primary color, 60mA when white at full brightness.
|96x96 Seeed OLED|||77mA|Current usage varies with the number of lit pixels.


The 96x96 OLED display uses 77mA.

Each LED uses up to 20mA per color (60mA when white at full brightness).

### LED Color State Matrix
|LED Name|In Progress|Good|Bad|
|-|-|-|-|
|Power|Blink Green|Green|Red
|WI-FI|Blink Yellow|Blue|Red
|Cloud|Blink Yellow|Blue|Red
|Firmware Update (Download in progress)|Blink Yellow|Blue (on download completion)|Red
|Firmware Update (Perform verifications and write to flash)|Blue|Off (on flash completion, system rebooted) |Red

### Assembly instructions
Warning: DO NOT POWER the device until you have adjusted the voltage regulator! They can output 7 times more voltage than the board takes, and ship in an undefined initial state.

Assembly instructions for the Bumblebee prototype sent to Cambridge:  Assembly Instructions - Bumblebee.pdf

# Demo Script
#### Preparation (from a brand new board set)

1. Plug in the device to laptop, see if it show up as DAPLINK, if not, follow the instruction to update board firmware:  https://blackstoneengineering.github.io/DAPLink/
2. Copy "combined.bin" to board, wait for the board to flash.
3. Open board console (baudrate 115200). In console, enter "reset all" then "reboot".

#### Pre-Demo check

1. When power on the board, see the power LED on GREEN, LCD on, and first line is the "Version".
2. When the board is trying to connect wifi, see the wifi LED flashing YELLOW, and on LCD second line, the SSID of the wifi will be show in "WiFi"
3. When the board is connected to the wifi, see the wifi LED on BLUE.
4. When the board is trying to connect to the mbed cloud, the cloud LED flashing YELLOW, and sensor LEDs on BLUE. Sensor data/WiFi SSID/Label name should be paging on the second line of the LCD.
5. When the board is connected and registered to the mbed cloud, the cloud LED on BLUE, and the sensor and cloud LEDs will flash GREEN in turn to show the sensor data uploaded.
6. Connect account to webapp hook. Open the webapp, see the device updating sensor data on the page.
7. Create campaign. When the board is trying to download firmware, see the data/update LED flashing YELLOW, LCD show "Downloading" with progress bar.
8. After image been downloaded to the board and board resets, all LEDs turn off, then the power LED back on GREEN, the data/update LED flashing YELLOW, while LCD show the 5 steps of the install progress: 
    * [1/5] CHK Flash 
    * [2/5] Erasing"
    * [3/5] Write HDR
    * [4/5] Write FW
    * [5/5] CHK Active
9. After install finishes, board will restart with LCD shows the latest "Version".

State Diagram detailing indicators in all states of the sales demo


#### Demo script

* First Boot
    1. Turn on power to device
    2. Show LCD and say, "It's trying to connect to Wifi, and then it will register with mbed cloud. Once this LED shows blue, it is all connected and registered."
    3. Once device connects, show LCD, "You can see sensor values shown here. Temperature, Humidity, and Light."
    4. Open web browser on laptop to  https://portal.us-east-1.mbedcloud.com/login
    5. Login with mbed credentials
    6. Click "Device directory", and click on the registered "Device ID". Say, "Here in mbed cloud, we can see the live sensor values."
    7. Click on the "Resources" tab and scroll down to "Object ID 3301" which contains "light_value".
    8. Click on the path next to "light_value". Say, "This is the light sensor. Let me cover it up."
    9. Cover light sensor with hand, and the value on mbed cloud should change within seconds.
    10. Open web browser tab to http://staging.fotaportal.deploymbed.com/live-device/ "You don't have to login to mbed, cloud, you can create your own website. Here we've created an example. You can see Temperature, Light, and Humidity."
    11. Wait for applause.
* Location 
    1. With web browser still open to http://staging.fotaportal.deploymbed.com/live-device/ click on "Find Device" link near top
    2. Zoom in on map to show location of device
    3. Say, "We can manually change this."
    4. Open web browser tab to  https://portal.us-east-1.mbedcloud.com/login
    5. Click on "Device Directory"
    6. Click on the correct "Device ID"
    7. Click on "Resources" tab
    8. Scroll down to "Object ID 3336"
    9. Click on link next to "Latitutde" (Specifically "3336/0")
    10. Click "edit" type in a number (like 30) and click "Send" button
    11. Do similar steps for "Longitude" and "Uncertainty"
    12. Go back to map at http://staging.fotaportal.deploymbed.com/live-device/find/
* Change device label (name)
    1. Open web browser tab to  https://portal.us-east-1.mbedcloud.com/login
    2. Click "Device Directory"
    3. Click the "Device ID"
    4. Click "Resources" tab
    5. Scroll down to "Object /26241/0/1"
    6. Click on the object
    7. Click Edit and change value
    8. Click "Send"
    9. Point to device LCD and show the device name changed there
    10. Also show name changed on http://staging.fotaportal.deploymbed.com/live-device/
* Firmware over-the-air updating.
    1. Open web browser tab back to mbed cloud portal
    2. Click on "Device directory"
    3. Click "Create new filter"
    4. Click "Add attribute"
    5. Click "Device ID"
    6. Copy-paste Device ID into the text field
    7. Click "Save filter"
    8. Type in a name and click "Save"
    9. Click on "Update firmware"
    10. Click on "Images"
    11. Click button, "Upload new images"
    12. Type in a name, then click "Choose file" and select file on your computer "fota-demo.bin" (not the combined.bin file!)
    13. Click on "Manifests"
    14. Click button, "Upload new manifest" and fill out the form.
    15. Click on "Update campaigns"
    16. Click on "Create campaign"
    17. Type in a name, select "Manifest" and select "Devices" filter
    18. Click "Save"
    19. Say, "Now I will update my devices". Click "Start".
    20. Device will update and reboot, displaying the new "version" name.

### FOTA / Recovery / Flashing a Firmware Image manually
See Workplace Environmental Monitor Reference Deployment

### Clang-format
You can use clang-format to easily comply with mbed coding style:  https://developer.mbed.org/teams/SDK-Development/wiki/mbed-sdk-coding-style



1. Installation
    * macOS: brew install clang-format
    * Ubuntu: apt-get install clang-format

2. Usage
    * clang-format -i *.cpp *.h
##### note: -i means in-place reformatting of files
3. IDE integration
    * VS code: set C_Cpp.clang_format_path to the path to clang-format.  Press shift+cmd+p and search for the command "format document"
    * Vim:  https://clang.llvm.org/docs/ClangFormat.html#vim-integration
    * Emacs:  https://clang.llvm.org/docs/ClangFormat.html#emacs-integration
    * Sublime Text:  https://github.com/rosshemsley/SublimeClangFormat

## Other Platforms

#### u-blox EVK-ODIN-W2
An initial port to the EVK-ODIN-W2 platform is available from fota-demo v1.6.0.

The high-level changes to the fota-demo app are as follows.  For more detail, please see the fota-demo git repo.

1. Replace ESP8266 WiFi driver with OdinWiFiInterface.  This was simple and just required a change to the class of wifi interface instantiated on startup.  The WiFiInterface API abstraction was otherwise sufficient and required no other modification.
2. LCD pin names changed.  The odin header file that defines pin names (PinNames.h) does not define I2C_SDA and I2C_SCL unlike the PinNames.h included for the K64F.  Equivalent pins exist for I2C on the EVK-ODIN-W2, but the pin names are different.
3. LEDs are removed.  On the K64F, the LEDs are connected to pins D2 and D3.  However, on the EVK-ODIN-W2, pin D2 is also connected to UART-1 RX which causes the serial console to be unable to receive user input from an attached terminal, thus breaking the Commander CLI.  Removing the LEDs from pins D2 and D3 fixed the serial console.
4. The EVK-ODIN-W2 includes pre-built binary images for the WiFi and Bluetooth driver and inclusion of these pre-built images into the final firmware image causes a significant increase in firmware image size.  This is a problem in particular for the bootloader which has a size constraint of 0x20000 (131072) bytes common across many platforms and becomes too large when combined with the LCD driver for bootloader status messages.  The issue was addressed by increasing the bootloader size and app offsets, a change which had to be replicated in 3 places: the bootloader build configuration file mbed-bootloader/mbed_app.json, the application build configuration file mbed_app.json, and parameters supplied to the combine_bootloader_with_app.py script which combines the bootloader and app into a final firmware image.  The bootloader size constraint was changed to 0x28000 (163840) bytes, an increase of 32768 bytes.

#### What works:
* bootloader boots
* app boots
* WiFi connects to network
* sensors (temp, humidity, light) initialize and begin to sample data
* LCD status messages appear to be correct in app and in bootloader
* Commander CLI
    * keystore (get,set,del) works
    * reboot
    * reset (all,keys,certs)
* App label R/W from mbed portal
* User Geo R/W from mbed portal
* M2M sensor data available in the mbed portal
* LEDs
* Auto Geo
* FOTA

#### What doesn't work:
* FotaPortal: The Mbed cloud portal does not forward sensor data and manual geo location to the webapp fota portal.  The Odin board data is pushed and can be verified in the mbed cloud portal, but the data doesn't seem to make it all the way to the webapp through the webhook.  Note the same issue was observed on a K64F at the same time, so this may not be an Odin specific issue.
* Also noticed, odin board will de-register after few minutes up and running. And for a long run, board sometimes hang.

### How to build:

NOTE: If you are on Windows you may have to install the ST-Link Debug driver from here, or directly from here if you don't want to send e-mail information.

A Base Shield in a Dragonfly configuration should plugged into the Odin board, with the exception that the LEDs attached to port D2 and the ESP8266 WiFi module attached to port UART must be removed.  Make sure to install a freshly formatted SD card.

Odin support has been merged into the dev branch of fota-demo.  Build the firmware image as normal, but change the target to UBLOX_EVK_ODIN_W2.  If you are re-using a build environment, make sure to run 'make distclean' first.

$ git clone git@github.com:armmbed/fota-demo.git
$ cd fota-demo
$ cp <path/to/mbed_cloud_dev_credentials.c> .
$ mbed config ROOT .
$ mbed target UBLOX_EVK_ODIN_W2
$ mbed toolchain GCC_ARM
$ make


https://github.com/ARMmbed/sd-driver

Factory Configurator
Requirements
You need the ability to upload certificates on your Mbed Cloud account.  Contact  Birbhadra.Dhungana@arm.com
K64F-based sales-tool.  This may work on other boards too, with minor modifications.
SD card in the K64F
Python 3
pip3
Linux PC or Windows PC
On Windows, you need to execute these steps in a Linux virtual machine.
On Macs, closing the serial port causes a board reboot.
You can work around this by using TCP, or by using a separate firmware for erasing and provisioning, among other methods.  Those steps are not included here.
Mbed CLI
ARM GCC
Recommended: a Vagrant Box has been created with all software requirements.  https://github.com/ARMmbed/fcu-vagrant

Steps
Build and flash the example FC client.
git clone https://github.com/ARMmbed/factory-configurator-client-example-restricted
cd factory-configurator-client-example-restricted
bash build-mbed-os.sh --toolchain=GCC_ARM --platform=K64F --iface=FCE_SERIAL_INTERFACE
Copy ./BUILD/k64f/GCC_ARM/factory-configurator-client-example.bin to the K64F over DAPLINK.

Connect a serial console to the K64F.

Reboot the K64F.  You should see the following
[INFO][fcc ]: factory_configurator_client.c:117:fcc_storage_delete:===>
[INFO][esfs]: esfs_reset - enter
[INFO][esfs]: esfs_finalize - enter
[INFO][esfs]: esfs_init - enter
[ERR ][PAL ]: Failed to open/create file, was the storage properly initialized?
[INFO][fcc ]: factory_configurator_client.c:129:fcc_storage_delete:<=== Factory flow begins...

Log into the Mbed Cloud portal.   https://portal.us-east-1.mbedcloud.com/identity/factorytools
Click "Download"
Unzip the file you just downloaded.
Hint: if you're using Vagrant, use the shared directory "work/" to copy the file into the virtual machine, then run "unzip factory_configurator_utility.zip -d fcu"

Read the documentation inside the zip file, under "docs/index.html".
Install the factory configurator utility
Make a virtual environment if you prefer
pip3 install fcu/fcu-1.2.4.227-py3-none-any.whl
pip3 install -r ft_demo/sources/requirements.txt
if this failed with a permission error, try with --user
Run the factory configurator demo
Modify config/fcu.yml.  Fill out the info.  For an example, see the documentations under "Factory tool demo".  I've also attached a sample.  Key sections are:
device-certificate
certificate-authority
device-info
update-auth-cert
The UUIDs under here are also needed.  Generate random UUIDs.
python3 ft_demo/sources/ft_demo.py setup
python3 ft_demo/sources/ft_demo.py -c config/fcu.yml inject --endpoint-name=<ENDPOINT_NAME> --serial-number=<SERIAL_NUMBER> serial --port=<SERIAL_PORT> --baud=115200 --connection-timeout=10

Hint: SERIAL_PORT should be /dev/ttyS1 if using Vagrant.
This writes the factory provisioning info to the device.  Don't reboot the board or the FC info will be erased.
Modify the dev branch main.cpp of fota-demo, such that it doesn't call fcc_developer_flow()
Before
After
Before
After
static int init_fcc(void)
{
    fcc_status_e ret;

#if MBED_CONF_APP_FCC_WIPE
    ret = fcc_storage_delete();
    if (ret != FCC_STATUS_SUCCESS) {
        cmd.printf("ERROR: fcc delete failed: %d\n", ret);
    }
#endif

    ret = fcc_init();
    if (ret != FCC_STATUS_SUCCESS) {
        cmd.printf("ERROR: fcc init failed: %d\n", ret);
        return ret;
    }

    ret = fcc_developer_flow();
    if (ret == FCC_STATUS_KCM_FILE_EXIST_ERROR) {
        cmd.printf("fcc: developer credentials already exists\n");
    } else if (ret != FCC_STATUS_SUCCESS) {
        cmd.printf("ERROR: fcc failed to load developer credentials\n");
        return ret;
    }

    ret = fcc_verify_device_configured_4mbed_cloud();
    if (ret != FCC_STATUS_SUCCESS) {
        cmd.printf("ERROR: fcc device not configured for mbed cloud\n");
        return ret;
    }

    return 0;
}
static int init_fcc(void)
{
    fcc_status_e ret;

#if MBED_CONF_APP_FCC_WIPE
    ret = fcc_storage_delete();
    if (ret != FCC_STATUS_SUCCESS) {
        cmd.printf("ERROR: fcc delete failed: %d\n", ret);
    }
#endif

    ret = fcc_init();
    if (ret != FCC_STATUS_SUCCESS) {
        cmd.printf("ERROR: fcc init failed: %d\n", ret);
        return ret;
    }

#if 0
    ret = fcc_developer_flow();
    if (ret == FCC_STATUS_KCM_FILE_EXIST_ERROR) {
        cmd.printf("fcc: developer credentials already exists\n");
    } else if (ret != FCC_STATUS_SUCCESS) {
        cmd.printf("ERROR: fcc failed to load developer credentials\n");
        return ret;
    }
#endif

    ret = fcc_verify_device_configured_4mbed_cloud();
    if (ret != FCC_STATUS_SUCCESS) {
        cmd.printf("ERROR: fcc device not configured for mbed cloud\n");
        return ret;
    }

    return 0;
}
Build and flash the fota-demo to the board, and finally reboot.
You should see the board connect to Mbed Cloud under your account.
Firmware Releases
The 'dev' branch is the main development branch and is where all new commits are merged.  'master' is the stable branch from which firmware releases are tagged and generated.  At the end of a sprint, or as needed for hot-fixes, 'dev' is merged into 'master' and a new release version is tagged.

Here is the process for merging 'dev' into 'master':

git clone git@github.com:armmbed/fota-demo.git
cd fota-demo
git remote add <fork> git@github.com:<fork>/fota-demo.git
add your private fork as a remote so that you have a place to temporarily push the merged master branch to generate a Pull Request for code review.
git checkout -b master origin/master
git merge origin/dev --no-ff
make sure to specify --no-ff so that the git-log clearly shows when releases were made.
the git commit title should be the new release version number of the format "vX.YY.Z", such as "v1.12.2".  The second number (12 in the example) is incremented at the end of each sprint and the third number (2 in the example) increments for intra-sprint hot-fix releases.
the git commit message should contain a short summary of the differences between this release and the previous release
git push <fork> master
push the merged commits to your fork to make it available for code review.
Create the pull request, making sure to specify the 'master' branch in the PR.  NOTE: the default branch for this repo is 'dev', so double-check that you are issuing a PR against 'master'.
Address any comments in the PR.
Once the PR passes build verification and receives approval, continue to the next step.
git tag -a "vX.YY.Z"
tag the build, making sure to use the same version number specified in the merge commit.
git push origin master --tags
requires admin privileges on the repo
git checkout -b dev origin/dev
git merge origin/master
git push origin dev
requires admin privileges on the repo
this keeps the 'dev' branch history the same as 'master'#document