# An RC script for Home Assistant Core in a Python virtual environment on FreeBSD

This rc script assumes that you have installed Home Assistant Core in a Python virtual environment.
See these instructions for an example of how to do this: https://blog.brendans-bits.com/posts/2024/upgradable-home-assistant-in-a-freebsd-jail/

This script was developed to make it easy to change Python virtual environments as Home Assistant Core is upgraded between releases.
For example: to upgrade from HA Core 2024.2 to 2024.3, you would create a new python virtual environment where you install the new version of HA.
To begin using the new version of HA, you change the path in the `homeassistant_environment` variable in `/etc/rc.conf` to point to the new python virtual environment and then restart the `homeassistant` service.

The script also includes a custom `status` method that shows you which versions of Python and of Home Assistant Core are running.

Suggestions and contributions welcomed.