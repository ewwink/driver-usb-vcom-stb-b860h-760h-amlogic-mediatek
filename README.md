# Amlogic Usb Driver Signed
`libusb-win32` or `worldcup_device` Usb Driver adalah driver Windows 7/8/10 untuk perangkat Amlogic yang biasa digunakan untuk set-top-box (stb) Android seperti B760h, B860h dan lainnya. 

Untuk menginstall driver pada komputer dengan OS Windows diperlukan driver yg sudah bersertifikat akan tetapi sertifikat asli dari driver ini sudah kadaluarsa sehingga saat menginstallnya kita akan menemukan peringatan seperti dibawah dan itu artinya drivernya tidak akan berfungsi walaupun sudah terinstall.

![libusb-win32-unsigned-warning](https://user-images.githubusercontent.com/760764/43999813-25ae4390-9e3e-11e8-9b9b-fb723fd59cc1.png)

Hal tersebut bisa diatasi dengan mengaktifkan mode `Disable Driver Signature Enforcement or using our drivers` tapi kekurangannya dilayar monitor akan ada keterangan `Test Mode...` yg kurang enak dipandang bahkan memudahkan virus menginstall driver ke komputer kita.

![test-mode](https://user-images.githubusercontent.com/760764/59989993-a7a84280-966b-11e9-9f55-30b5936f965b.jpg)

Untuk itu daripada melakukan hal tersebut lebih baik kita membuat setifikatnya sendiri tapi itu lumayan rumit jadi lebih baik pakai yg sudah jadi diatas.

## Cara Install
- Download dan extract [amilogic_usb_drivers.zip](https://raw.githubusercontent.com/ewwink/amlogic-usb-world-cup-driver-signed/master/amilogic_usb_drivers.zip)
- install sertifikat `libusb-win32.cer` dengan cara double-klik kemudian tekan tombol "Install Certificate.."
- Install drivernya seperti biasa atau dengan cara `Add legacy hardware` or `Update` drivers dari **Device Manager** kemudian arahkan ke folder tempat drivernya.

**Hardware Ids** 

 - USB\VID_1B8E&PID_C003&REV_0007
 - USB\VID_1B8E&PID_C003
