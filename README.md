# Lenovo Ideapad Fan Control
Fan control indicator for Ubuntu's Unity desktop.

Provided as-is without support, guarantees or warranty. Use entirely at your own risk.
Developed for a Lenovo z570 running Ubuntu 14.10 w/ Unity. May work on other Lenovo Ideapad systems - see the 'Set up' section.

This my first Python project - the best structure and conventions may not be adhered to while I'm still learning!

## Setup
This script should auto detect the `'fan_mode'` file used by your operating system to set the fan speeds. Toggle it on/off by setting `autoDetectEnabled` in fileWriter to either True or False. If false, it will revert to the path stored in `FAN_MODE_FULLPATH`.

`FAN_MODE_FULLPATH` in fileWriter.py may need to be altered to point to the location of your fan_mode file. This can be found by running the following command in a terminal:

`find /sys/devices -name "fan_mode"`

Copy and paste the file path into the `FAN_MODE_FULLPATH` variable and then run fanControl.py. Ensure fileWriter.py is in the same location.
 
## Requirements
* python 2.7 (`sudo apt-get install python`)
* python-gobject package installed (`sudo apt-get install python-gobject`)
* gksudo package (`sudo apt-get install gksu`)
* Desktop environment w/ support for Appindicators (e.g Unity)
