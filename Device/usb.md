# USB Device Configuration

Use the following commands to assign a fixed name to a USB device and establish a network connection through USB.

```bash
$ lsblk
# Bus 001 Device 034: ID aaaa:bbbb HMD Global Nokia 5.3

$ cat /etc/udev/rules.d/10-usb-net.rules
# SUBSYSTEM=="net", ACTION=="add", ATTRS{idVendor}=="aaaa", ATTRS{idProduct}=="bbbb", NAME="nokia_5.3_usb"

$ sudo udevadm control --reload-rules

$ nmcli con show
# | NAME                  | UUID            | TYPE      | DEVICE            |
# |-----------------------|-----------------|-----------|-------------------|
# | Panhong_5.3_USB_Net   | xxxxx           | ethernet  | nokia_5.3_usb     |
```

Use firejail to restrict the browser's routing.

**Unable to set up routing for wifi** because wifi requires a password. Therefore, routing must be specified for wired devices.

```bash
$ firejail --net=enp1s0 --ip=dhcp firefox
# Open https://whatismyipaddress.com/ to check if the IP is routed to a specific route.
```
