# Getting Started

## Bill of Materials

* Trinket 5V
* 3 wires, 1 red, 1 yellow, and 1 black
* Neopixel Stick with 8 neopixels
* MicroUSB cable

## Step 1. Install the IDE

1. Download and install [arduino ide 1.6.10](https://www.arduino.cc/en/Main/Software)

## Step 2. Make Adafruit boards available

1. Start the Arduino IDE
2. Navigate to `Arduino->preferences`
   ![menus to navigate to preferences](https://raw.githubusercontent.com/stainlessio/intro-to-neopixels/master/images/preferences.png)
3. Click the double window button next to `Additional Boards Manager Url`
   ![preferences dialog box](https://raw.githubusercontent.com/stainlessio/intro-to-neopixels/master/images/preferences-dialog.png)
4. Add `https://adafruit.github.io/arduino-board-index/package_adafruit_index.json` into the text box
   ![additional boards url](https://raw.githubusercontent.com/stainlessio/intro-to-neopixels/master/images/board-url.png)
5. Click `Ok` to dismiss the two dialog boxes

## Step 3. Add Adafruit boards

1. Start the Arduino IDE
2. Navigate to `tools->board->board manager`
   ![menus to navigate to board manager](https://raw.githubusercontent.com/stainlessio/intro-to-neopixels/master/images/board-manager.png)
3. Find `adafruit avr boards` and click install.
   ![board manager with adafruit avr boards](https://raw.githubusercontent.com/stainlessio/intro-to-neopixels/master/images/add-boards.png)
4. Close the board manager

## Step 4. Load the Adafruit Neopixel Library

1. Navigate to `sketch->include library->Manage Libraries...`
   ![menus to navigate to library manager](https://raw.githubusercontent.com/stainlessio/intro-to-neopixels/master/images/library-manager.png)
2. Find `adafruit neopixel` and click install
   ![library manager with adafruit neopixel library](https://raw.githubusercontent.com/stainlessio/intro-to-neopixels/master/images/load-library.png)
3. Close the library manager

## Step 4.5. Install Drivers (Windows Online)

1. Download the drivers from [adafruit](http://bit.ly/2ac9S3m)
2. Install the drivers

## Step 5. Connecting the board and leds

1. Connect the yellow wire to `DIN` on the neopixel
2. Connect the yellow wire to `#0` on the trinket
3. Connect the red wire to `5v` on the neopixel and trinket
5. Connect the black wire to GND on the neopixel and trinket

## Step 6. Prep the firmware

1. Open `strandtest` by going to `file->sketchbook->libraries->Adafruit_Neopixel->standtest`
   ![menus showing where to find strandtest](https://raw.githubusercontent.com/stainlessio/intro-to-neopixels/master/images/standtest.png)
2. Find the `#define PIN` line and change the number to `0`
3. Find the line that contains `strip = Adafruit_Neopixel` and set the first argument to `8`
   ![where the find the code changes](https://raw.githubusercontent.com/stainlessio/intro-to-neopixels/master/images/code-changes.png)
4. Save the file, you will be prompted to save it to a new location

## Step 7. Upload the firmware to the trinket

0. Under `tools->board` select `Trinket 8Mhz` under the `adafruit boards` section
1. Under `tools->programmer` select `USBTinyISP`
1. Click the `compile` button which looks like a checkmark
2. Once the compile is done, plug the trinket into your usb cable
3. Wait for the red light to "breath"
4. Click the `upload` button
5. If everything worked correct, the leds should come to life.

# Next Steps

* Try changing the firmware to create other effects.
* Try to get a cylon effect
* Try to get a knight rider effect
* Try to get random flashes

# Troubleshooting

### Not "breathing" before upload

* Try the reset button
* Try unplugging for 30 seconds and then plugging it back in
* Try a different USB port
* Bootloader might need to be reburned.  (see instructor)

### Verification Errors

* Make sure the right board is selected under the `tools->board` menu
* Bootloader might need to be reburned (see instructor)

### Leds aren't light up

* Verify wiring
