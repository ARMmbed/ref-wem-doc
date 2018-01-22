
## Workplace Environmental Monitor Reference Deployment

<span class="images">![](https://s3-us-west-2.amazonaws.com/mbed-os-docs-images/IMG_1254.png)<span>Photo</span></span>

This document contains the information you need to configure your Workplace Environmental Monitor and set it up, so you can demonstrate its functionality to a group.

The monitor has sensors for:

- Temperature.
- Humidity.
- Light brightness.

To turn the device on and off, locate the power switch on the side of the device next to the micro-USB port. When fully charged, the device can run for several hours on internal battery. You can also connect it to a power source through the micro-USB port for power and charging.

When turned on, the device connects to the Wi-Fi access point it was configured to. Because of this, the device probably will not connect to the internet the first time you turn it on. Follow the instructions below to flash the board. You need your Arm Mbed credentials, Wi-Fi access point and password.

The documentation on this page shows how to flash software onto the device and also how to wirelessly update the firmware (also known as "firmware over the air" updates).

You need to flash the firmware at least once because it's the only way to get your device associated with your Arm Mbed Cloud account. We have a web page set up that compiles the image for you, so you only need to drag and drop the file onto your device.

#### Required hardware:

- Laptop with USB port (or dongles to provide a USB port).
- USB to micro-USB cable.
- The environmental monitor device.

#### Required file:

- An Mbed Cloud certificate file. Visit https://portal.us-east-1.mbedcloud.com/signup to sign up if you haven't already.
To get an Mbed Cloud certificate file, sign in at https://portal.us-east-1.mbedcloud.com/

Click "Device identity", and then click on "Actions". Then click on "Create a developer certificate":

<span class="images">![](https://s3-us-west-2.amazonaws.com/mbed-os-docs-images/mbed_create_cert.png)<span>Photo</span></span>

Click on the certificate, and then click the button `Download the developer C file`:

<span class="images">![](https://s3-us-west-2.amazonaws.com/mbed-os-docs-images/mbed_cloud_cert_download.png)<span>Photo</span></span>

#### Now that you have an Arm Mbed developer C file, follow the these steps to flash your device:

1. Connect your laptop to the device with a USB cable. The laptop automatically adds a new drive, in this case named `DAPLINK`. This is where you drag and drop the firmware:


<span class="images">![](https://s3-us-west-2.amazonaws.com/mbed-os-docs-images/image3.jpeg)<span>Photo</span></span>

1. Visit and clone the firmware-over-the-air (FOTA) demo repository: https://github.com/ARMmbed/fota-demo

1. Follow the FOTA demo instructions to build your firmware: https://github.com/ARMmbed/fota-demo/blob/dev/README.md 

1. Save that file to your computer, and then drag and drop it into the drive for your device (see step #1).

That's it! Wait about a minute, and the device is now flashed with your image.

### Using the command console on the device

<span class="images">![](https://s3-us-west-2.amazonaws.com/mbed-os-docs-images/ScreenShot2017-12-05at2.34.23PM.jpeg)<span>Photo</span></span>

<span class="images">![](https://s3-us-west-2.amazonaws.com/mbed-os-docs-images/IMG_2039.jpg)<span>Photo</span></span>

Connect your device to your laptop with a USB cable. Then you can use software such as PuTTy, Coolterm or Minicom to connect to the device.

On Mac OS, for example, you can type a command such as:

```
    minicom -D /dev/tty.usbmodem144142
```

To set the Wi-Fi configuration:

Press the `ENTER` key, and you see a prompt where you can type `help` to see all the available commands.

```
    set wifi.ssid NAME
    set wifi.key PASSWORD
    set wifi.encryption TYPE
```

Replace `NAME` with the displayed name of your access point and similar with `PASSWORD`. The `TYPE` should be wither WPA2 or OPEN are the two most popular modes.

Type `reboot` to let the device boot up and connect to the Wi-Fi access point you specified.

### FOTA update

Before starting the FOTA campaign, you must increment the version of the application because you can't update to the same revision of the firmware.

In your cloned project folder, open the file `mbed_app.json` with the editor of your choice and increment the version number.

Change from:

```
"version": {
    "help": "Display this version string on the device",
    "value": "\"1.0\""
},
```

to:

```
"version": {
    "help": "Display this version string on the device",
    "value": "\"1.1\""
},
```

Next, open your shell to your project folder. 

```
make campaign
```

For a deeper understanding of FOTA, please see:
https://cloud.mbed.com/docs/v1.2/updating-firmware/index.html 

For more details on building, please see:
https://github.com/ARMmbed/fota-demo/blob/dev/README.md 

<span class="notes">**Note:** To ensure that FOTA works after running `make distclean`, you must first run `make certsave`, so your certs pass to the new clean environment.</span>

### Demo script

#### Preparation (from a brand new board set)

1. Plug the device into laptop. 
1. If the device does not show up as `DAPLINK`, follow the instruction to update board firmware:  https://blackstoneengineering.github.io/DAPLink/
1. Copy `combined.bin` to board, and wait for the board to flash.
1. Open the board console (baudrate 115200).
1. In the console, enter `reset all`.
1. Then, enter `reboot`.

#### Predemo check

1. When the board is on, the power LED is GREEN, the LCD is on and the first line is the "Version".
1. When the board is trying to connect to Wi-Fi, the Wi-Fi LED flashes YELLOW. On the second line of the LCD, the SSID of the Wi-Fi shows in `Wi-Fi`.
1. When the board is connected to the Wi-Fi, the Wi-Fi LED is BLUE.
1. When the board is trying to connect to Mbed Cloud, the cloud LED flashes YELLOW, and the sensor LEDs are BLUE. The sensor data, Wi-Fi SSID or label name is paging on the second line of the LCD.
1. When the board is connected and registered to Mbed Cloud, the cloud LED is BLUE, and the sensor and cloud LEDs flash GREEN in turn to show the sensor data uploaded.
1. Connect the account for the webapp hook. 
1. Open the webapp, and see the device updating sensor data on the page.
1. Create a campaign. When the board is trying to download firmware, the data and update LED flashes YELLOW, and the LCD shows `Downloading` with a progress bar.
1. After you have downloaded an image to the board and the board resets, all LEDs turn off. The power LED turns GREEN, the data and update LED flashes YELLOW and the LCD shows the 5 steps of the install progress: 
    - [1/5] CHK Flash.
    - [2/5] Erasing".
    - [3/5] Write HDR.
    - [4/5] Write FW.
    - [5/5] CHK Active.
1. After the installation finishes, the board restarts with the LCD showing the latest "Version".
1. Make sure the device is registered with FOTA portal:
    - http://ec2-34-229-249-172.compute-1.amazonaws.com/admin/livedevice/mbedcloudaccount/
    - Log into the site with `login: production` and `password: halarges`.
    - Registering your Mbed Cloud account API key generates a request to the Mbed Cloud portal to set your account's notification webhook to point to the Fota portal webhook handler.
    - You can create Mbed Cloud account API keys in your Mbed Cloud portal here: 
      https://portal.us-east-1.mbedcloud.com/access/keys


State Diagram detailing indicators in all states of the sales demo

#### Demo

- First boot
    1. Turn on power to device.
    2. Show the LCD, and say, "It's trying to connect to Wi-Fi, and then it will register with Mbed Cloud. Once this LED shows blue, it is all connected and registered."
    3. Once the device connects, show the LCD. "You can see sensor values shown here: temperature, humidity and light."
    4. Open a web browser on your laptop to https://portal.us-east-1.mbedcloud.com/login
    5. Log in with Mbed credentials.
    6. Click `Device directory`, and click on the registered `Device ID`. Say, "Here in Mbed cloud, we can see the live sensor values."
    7. Click on the `Resources` tab, and scroll down to `Object ID 3301`, which contains `light_value`.
    8. Click on the path next to `light_value`. Say, "This is the light sensor. Let me cover it up."
    9. Cover the light sensor with your hand, and the value on Mbed Cloud changes within seconds.
    10. Open a web browser tab to http://fotaportal.deploymbed.com/live-device/ "You don't have to log in to Mbed Cloud. You can create your own website. Here, we've created an example. You can see temperature, light and humidity."
    11. Wait for applause.
- Location 
    1. With the web browser still open to http://fotaportal.deploymbed.com/live-device/ click on the `Find Device` link near the top of the page.
    2. Zoom in on the map to show the location of the device.
    3. Say, "We can manually change this."
    4. Open the web browser tab to https://portal.us-east-1.mbedcloud.com/login
    5. Click on `Device Directory`.
    6. Click on the correct `Device ID`.
    7. Click on the `Resources` tab.
    8. Scroll down to `Object ID 3336`.
    9. Click on the link next to `Latitude` (specifically, `3336/0`).
    10. Click `edit`, type in a number (such as `30`) and click the `Send` button.
    11. Do similar steps for `Longitude` and `Uncertainty`.
    12. Go back to the map at http://fotaportal.deploymbed.com/live-device/find/
- Change the device label (name).
    1. Open a web browser tab to https://portal.us-east-1.mbedcloud.com/login
    2. Click `Device Directory`.
    3. Click the `Device ID`.
    4. Click the `Resources` tab.
    5. Scroll down to `Object /26241/0/1`.
    6. Click on the object.
    7. Click `Edit`, and change the value
    8. Click `Send`.
    9. Point to the device LCD, and show the device name changed there.
    10. Also show the name changed on http://fotaportal.deploymbed.com/live-device/
- Firmware over-the-air updating
    1. Open `mbed_app.json`, and increment the version number.
    2. Open a shell.
    3. In the command-line, use `cd` to get to your project folder.
    4. Type `make campaign`.
    5. Talk about FOTA while waiting for the update to begin.
 
