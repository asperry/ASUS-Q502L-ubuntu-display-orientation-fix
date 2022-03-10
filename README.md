## Problem

When Ubuntu is installed on an ASUS Q502L laptop, the
orientation of the accelerometer mounted inside the
screen may not be configured correctly. This manifests as
the screen rotation always being in the wrong orientation
when rotation lock is off; it's as if the direction of
gravity is some direction other than downward.

This problem is fixed by overwritting the rotation
matrix that describes the orientation of the
accelerometer relative to the screen.

## How To Fix It

To fix this problem, add the `61-sensor-local.hwdb` file
in this repository to the `/etc/udev/hwdb.d/` directory
and restart the computer (you may need `sudo` privileges).

This sets the accelerometer orientation for `iio-sensor-proxy`.

## References

These references are where I learned how to fix this issue:

[Changing the way automatic screen rotation works in Gnome shell](https://unix.stackexchange.com/questions/361472/changing-the-way-automatic-screen-rotation-works-in-gnome-shell)

[Change iio-sensors data via custom ACCEL_MOUNT_MATRIX](https://unix.stackexchange.com/questions/410826/change-iio-sensors-data-via-custom-accel-mount-matrix)

[iio-sensor-proxy Repository](https://gitlab.freedesktop.org/hadess/iio-sensor-proxy/)

[60-sensor.hwdb from systemd Repository](https://github.com/systemd/systemd/blob/main/hwdb.d/60-sensor.hwdb)
