# Amlogic Usb Driver Signed
Self signed `libusb-win32` or `worldcup_device` Usb Driver for Amlogic or other compatible devices.

Certificate for signing `libusb-win32` was expired on 2014 if you install the driver on Windows 7/8/10 you will see this error:

![libusb-win32-unsigned-warning](https://user-images.githubusercontent.com/760764/43999813-25ae4390-9e3e-11e8-9b9b-fb723fd59cc1.png)

**Solution:** Disable Driver Signature Enforcement or using our drivers

## Installation
- install certificate `libusb-win32.cer` to your Computer
- `Add legacy hardware` or `Update` drivers from **Device Manager**

**Hardware Ids** 

 - USB\VID_1B8E&PID_C003&REV_0007
 - USB\VID_1B8E&PID_C003
