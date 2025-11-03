## Using the Arduino IDE

1. Go to https://docs.m5stack.com/en/arduino/arduino_development follow the instructions under heading "Boards Manager"
2. Open tallyarbiter-m5atom.ino in Arduino IDE
3. In Library Manager install FastLED, arduinoWebSockets, Arduino_JSON, WebSockets version 2.3.4, WifiManager (by tzapu) and MultiButton
4. Plug your board into the computer.
5. In the IDE go to Sketch -> Upload.
   Make sure you have selected the **right serial port** and the **right board type**.

Done! Now your board is running the latest listener client firmware version. Go to the _"Setup your device"_ sections to connect the board to the Tally Arbiter server.

The code base is compiled for **M5StickC-Plus2** based on the configured **M5Stack Arduino** version in **Board** in Arduino IDE. Only one can be enabled at at time:
- M5Stack Arduino -> M5StickC-Plus2

It is possible to manually select what board type to build for if the wanted board type in the ino file, e.g., when not using Arduino IDE.

TALLY_EXTRA_OUTPUT can be used for extra tally info. The internal led is used for program. Preview and aux is available on external ports by default.

# Setup your device

1. Plug the device in a power source
2. Wait for the boot up to finish, if there is no saved AP it will startup an Access Point where you can configure one.
3. Connect to the 'm5StickC-XXXXXX' Access Point via phone and go to 192.168.4.1 (or wait a bit, a captive portal page should open). NB: The portal times out after 120 sec of inactivity.
4. Set your Tally Arbiter server ip by going to _"Setup"_ page.
5. Go back, then go to the "Configure WiFi" page and set your WiFi credentials. The board should reboot.
6. If the connection is successful a settings page will shown. If not, reconnect to 'm5StickC-XXXXXX' Access Point.

Button A (M5):
Single click - Switch between settings screen and device name (the device name is from Tally Arbiter server).
Long press 5 seconds - reset WiFi credentials.

Button B:
Single click - Increase screen brightness

NB: The captive portal page is accessible on the device when the settings screen is shown.
