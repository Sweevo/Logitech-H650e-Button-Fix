# Fix for the Logitech H650e headset inline buttons #
Tested on Fedora 31

This headset has two main issues that I've found on Fedora:

- Pressing the 'mic mute' button triggers the LED on the inline controls to illuminate, however the mic is not muted within the Operating System.
- The volume buttons can sometimes trigger suprious volume dialog pop-ups to occur. As the inline volume controls appear to operate independently of the operating system, this change will prevent that behaviour.

To address both issues:

1. Copy the **99-logitech-H650e.hwdb** file to **/usr/lib/udev/hwdb.d/.** (using sudo)
2. Run ```sudo systemd-hwdb update``` to update the hwdb database.
3. Trigger the changes by running ```sudo udevadm trigger```
