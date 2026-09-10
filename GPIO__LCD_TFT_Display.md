# GPIO - 3.5'' LCD TFT Display

----
### Official Elegoo Manual

For further details, download manual [here](https://github.com/kingston-hackSpace/Display__RaspberryPi/blob/main/35_tft.pdf)

----
# 3.5'' LCD TFT Display

See reference image [here](https://github.com/kingston-hackSpace/Display__RaspberryPi/blob/main/LCD_Elegoo_1.jpg)

The 3.5'' LCD TFT Display module was designed for use with Raspberry Pi boards. It offers a 480 × 320 pixel colour display with an integrated resistive touch panel, making it suitable for small graphical interfaces and DIY projects. The screen connects via the Pi’s GPIO pins using an SPI interface, so it doesn’t use HDMI and leaves most GPIO free for other hardware. It typically includes a simple touch stylus and requires a compatible driver to appear as the console display on the Pi.

----
### Features

  - Runs videos (.mov, .mp4) at low framerate and low resolution. Not suitable for smooth or high-quality video
    
  - Typical performance:
      
      - 5–15 FPS

      - Best at 320×240 or 480×32

----
### Wiring

Wiring reference image [here](https://github.com/kingston-hackSpace/Display__RaspberryPi/blob/main/LCD_Elegoo_3.png)

----
### Driver Installation Instructions:

If you are running this screen *for the first time* in your RPi, you will need to install a driver that allows communication between the devices.

  - Connect your RPi to a keyboard, mouse, and screen via HDMI.

  - Connect your RPi to Ethernet or WIFI (Eduroam might not work).

  - Turn on your RPi

  - Open the Terminal and type:

    ```
    sudo apt update
    sudo apt install git
    git clone https://github.com/goodtft/LCD-show.git
    cd LCD-show/
    sudo ./LCD35-show
    ```
  - The Pi will reboot automatically.

  - Turn off the Pi and unplug the HDMI cable to the main monitor.

  - Replug the Pi and wait until you see the Desktop on the LCD screen.


NOTE: The *LCD35-show* script works by reconfiguring the Pi's framebuffer/display config (editing /boot/config.txt and swapping in an SPI-based display driver) so the LCD becomes the primary console output instead of HDMI. It doesn't mirror or extend across both — it redirects the whole display pipeline to the SPI screen.







