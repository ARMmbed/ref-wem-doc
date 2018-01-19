
# Workplace Environmental Monitor Reference Deployment

![photo](IMG_1254.png)

This document contains the current information you need to configure your Workplace Environmental Monitor and set it up so you can demonstrate its functionality to a group.

The monitor has sensors for:

* Temperature
* Humidity
* Light brightness

To turn the device on/off locate power switch on the side of the device next to the micro USB port. When fully charged it can run for several hours on internal battery, or it can be connected to a power source via the micro USB port for power/charging.

When turned on, it connects to the Wi-Fi access point it was configured to. Because of this it will probably not be able to connect to the internet the first time you turn it on. You will have to follow the instructions below to flash the board with your mbed credentials and needed Wi-Fi access point and password.

The documentation on this page shows how to flash software onto the device and also how to do wireless updating of the firmware (also known as "firmware over the air" updates).

## Flashing a Firmware Image
You need to flash the firmware at least once because it's the only way to get your device associated with your mbed cloud account. We have a web page setup that compiles the image for you, so you will only need to drag-and-drop the file onto your device.

#### Required Hardware:

* Laptop with USB port (or dongles to provide a USB port)
* USB to Micro USB cable
* The environmental monitor device itself 

#### Required file:

* An mbed cloud certificate file. First visit https://portal.us-east-1.mbedcloud.com/signup to sign up if you haven't already.
To get an mbed cloud certificate file, first sign in at https://portal.us-east-1.mbedcloud.com/

Click "Device identity", then click on "Actions", then click on "Create a developer certificate":

![photo](mbed_create_cert.png)

Then click on the certificate, and then click the button "Download the developer C file":

![photo](mbed_cloud_cert_download.png)

#### Now that you have an mbed developer C file, follow the rest of these steps to flash your device:

1. Connect laptop via USB cable to the device. The laptop should automatically add a new drive, in this case named "DAPLINK". This is where you will drag-and-drop the firmware:

![photo](image3.jpeg)

1. Visit and clone the FOTA Demo repository: https://github.com/ARMmbed/fota-demo

1. Following the FOTA Demo instruction and build your firmware: https://github.com/ARMmbed/fota-demo/blob/dev/README.md 

1. Save that file to your computer, then drag-and-drop it into the drive for your device (see step #1).

That's it! Wait about a minute and the device is now flashed with your image.

## Using the command console on the device
![photo](ScreenShot2017-12-05at2.34.23PM.jpeg)

![photo](IMG_2039.jpg)

Connect your device to your laptop via a USB cable. Then you can use software such as PuTTy, Coolterm, or Minicom to connect to the device.



On macbook for example, you can type a command such as:
```
    minicom -D /dev/tty.usbmodem144142
```
To set the Wi-Fi configuration:

Press the ENTER key and you should see a prompt where you can type "help" to see all the available commands.
```
    set wifi.ssid NAME
    set wifi.key PASSWORD
    set wifi.encryption TYPE
```
You need to replace NAME with the displayed name of your access point and similiar with PASSWORD. The TYPE should be wither WPA2 or OPEN are the two most popular modes.

Type "reboot" to let the device boot up and attemp to connect to the Wi-Fi access point you specified.

## Firmware over-the-air update (FOTA)

Before starting the FOTA campaign we must increment the version of our application because we can't update to the same revision of the firmware.

In your cloned project folder open the file 'mbed_app.json' with the editor of your choice and increment the version number.

change from...
```
"version": {
    "help": "Display this version string on the device",
    "value": "\"1.0\""
},
```

to...
```
"version": {
    "help": "Display this version string on the device",
    "value": "\"1.1\""
},
```

Next open your shell to your project folder. 

```
make campaign
```

For a deeper understanding of FOTA please see:
https://cloud.mbed.com/docs/v1.2/updating-firmware/index.html 

For more details on building please see:
https://github.com/ARMmbed/fota-demo/blob/dev/README.md 

__Note__
To insure that FOTA will work after running 'make distclean' you must 1st run 'make certsave' so that your certs will pass to the new clean environment.

## Demo Script

#### Preparation (from a brand new board set)

1. Plug in the device to laptop, see if it show up as DAPLINK, if not, follow the instruction to update board firmware:  https://blackstoneengineering.github.io/DAPLink/
2. Copy "combined.bin" to board, wait for the board to flash.
3. Open board console (baudrate 115200). In console, enter "reset all" then "reboot".

#### Pre-Demo check

1. When power on the board, see the power LED on GREEN, LCD on, and first line is the "Version".
2. When the board is trying to connect Wi-Fi, see the Wi-Fi LED flashing YELLOW, and on LCD second line, the SSID of the Wi-Fi will be show in "Wi-Fi"
3. When the board is connected to the Wi-Fi, see the Wi-Fi LED on BLUE.
4. When the board is trying to connect to the mbed cloud, the cloud LED flashing YELLOW, and sensor LEDs on BLUE. Sensor data/Wi-Fi SSID/Label name should be paging on the second line of the LCD.
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
10. Make sure the device is registered with fota-portal 
    * http://ec2-34-229-249-172.compute-1.amazonaws.com/admin/livedevice/mbedcloudaccount/
    * Log into the site with - login: (contact the RED team for this)  password: (contact the RED team for this)
    * Registering your mbed cloud account API key generates a request to the mbed cloud portal to set your account's notification webhook to point to the Fota Portal webhook handler.
    * Mbed cloud account API keys can be created in your mbed cloud portal here:
        * https://portal.us-east-1.mbedcloud.com/access/keys

State Diagram detailing indicators in all states of the sales demo

#### Demo

* First Boot
    1. Turn on power to device
    2. Show LCD and say, "It's trying to connect to Wi-Fi, and then it will register with mbed cloud. Once this LED shows blue, it is all connected and registered."
    3. Once device connects, show LCD, "You can see sensor values shown here. Temperature, Humidity, and Light."
    4. Open web browser on laptop to  https://portal.us-east-1.mbedcloud.com/login
    5. Login with mbed credentials
    6. Click "Device directory", and click on the registered "Device ID". Say, "Here in mbed cloud, we can see the live sensor values."
    7. Click on the "Resources" tab and scroll down to "Object ID 3301" which contains "light_value".
    8. Click on the path next to "light_value". Say, "This is the light sensor. Let me cover it up."
    9. Cover light sensor with hand, and the value on mbed cloud should change within seconds.
    10. Open web browser tab to http://fotaportal.deploymbed.com/live-device/ "You don't have to login to mbed, cloud, you can create your own website. Here we've created an example. You can see Temperature, Light, and Humidity."
    11. Wait for applause.
* Location 
    1. With web browser still open to http://fotaportal.deploymbed.com/live-device/ click on "Find Device" link near top
    2. Zoom in on map to show location of device
    3. Say, "We can manually change this."
    4. Open web browser tab to  https://portal.us-east-1.mbedcloud.com/login
    5. Click on "Device Directory"
    6. Click on the correct "Device ID"
    7. Click on "Resources" tab
    8. Scroll down to "Object ID 3336"
    9. Click on link next to "Latitude" (Specifically "3336/0")
    10. Click "edit" type in a number (like 30) and click "Send" button
    11. Do similar steps for "Longitude" and "Uncertainty"
    12. Go back to map at http://fotaportal.deploymbed.com/live-device/find/
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
    10. Also show name changed on http://fotaportal.deploymbed.com/live-device/
* Firmware over-the-air updating.
    1. Open 'mbed_app.json'  and increment the version number.
    2. Open a shell
    3. CD to you project folder.
    4. Type 'make campaign'
    5. Talk about FOTA while waiting for update to begin.
 
