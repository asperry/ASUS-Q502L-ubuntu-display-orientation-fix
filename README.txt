To fix the screen orientation problem on ASUS Q502L, add
the 61-sensor-local.hwdb file to the /etc/udev/hwdb.d
directory and restart the computer.

This sets the accelerometer orientation for iio-sensor-proxy

References where I learned how to fix this issue:

https://unix.stackexchange.com/quest...in-gnome-shell

https://unix.stackexchange.com/quest...l-mount-matrix

https://gitlab.freedesktop.org/hadess/iio-sensor-proxy/

https://github.com/systemd/systemd/b...60-sensor.hwdb
