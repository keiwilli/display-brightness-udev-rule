# display-brightness-udev-rule
udev rule file for Fedora for the Adjust Display Brightness Gnome Extension https://extensions.gnome.org/extension/4652/adjust-display-brightness/

By default, Fedora 35 does not allow the extension the ability to talk to the i2c devices which prevents the extension from being able to find any displays. Fedora does not have the i2c group that Debian has for handling access. This udev rule sets file permissions for all i2c devices for all users (666). It is recommended that a user sets only the permissions for the required i2c devices.

Place file in /lib/udev/rules.d with root privileges 
