# How to perform an action on a specific device with adb

If you have more than one device connected to your machine but want
to perform an adb action on a specific device.

```bash
adb devices
// list of devices and its unique ID...

adb -s "<deviceIDfromlist>" install "<path-to-apk>"

```

[source](https://stackoverflow.com/a/7186322)