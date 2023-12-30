# c3i
Composite to CSI2 Camera Interface (aka CCCI aka c3i)

### Purpose
Add a readily-available composite video camera (sold as 'backup cameras') to Raspberry Pi over a MIPI CSI2 camera interface

### Basic function
The ADV7280-M chip does all the magic, automatically detecting the composite video format (NTSC or PAL) and converting that to YCrCb 4:2:2 video stream. The -M variant of this chip adds a MIPI CSI2 conversion block, providing a single lane output MIPI data stream. Raspberry Pi's have dual lane MIPI channels, but according to [this](https://forums.raspberrypi.com/viewtopic.php?p=1717572&sid=e0199da8a1beeaa71a4631e8f8f0ca87#p1717572) thread, using lane 0 alone will work. The ADV7280-M has 8 composite video inputs, selectable by writing over i2c to the input selector register. Other than a couple voltage regulators and passive components, I designed this interface nearly identical to the recommended/typical use shown in the [datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/ADV7280.PDF). 

Parts can be found at [Digikey](https://www.digikey.com/en/mylists/list/8FBMX8EIKW). At the time of writing, this cost me just shy of $20 before shipping in parts. With 


## ** Currently under development ** 
I haven't gotten this working yet. Still in early stages of development.
