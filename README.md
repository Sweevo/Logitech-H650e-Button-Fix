# Logitech-H650e-Button-Fix
Fix for the Logitech H650e headset inline buttons - tested on Fedora 31

This headset has two main issues that I've found on Ubuntu Fedora:

Pressing the 'mic mute' button triggers the LED on the inline controls to illuminate, however the mic is not muted within the Operating System.
The volume buttons can sometimes trigger suprious volume dialog pop-ups to occur. As the inline volume controls appear to operate independently of the operating system, this change will prevent that behaviour.

To fix both issues:

Copy the 99-logitech-H650e.hwdb file to /usr/lib/udev/hwdb.d/. (using sudo)
Run sudo systemd-hwdb update to update the hwdb database.
Trigger the changes by running sudo udevadm trigger
