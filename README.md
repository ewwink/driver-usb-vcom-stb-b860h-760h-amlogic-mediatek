# Signed USB Driver STB Android B760h, B860h (Amlogic)
Untuk menghubungkan perangkat STB Android B760h, B860h atau yg mempunyai chipset Amlogic ke Windows 7/8/10 melalui USB dibutuhkan driver  `libusb-win32`, `worldcup_device`, atau  `MediaTek Preloader USB VCOM`  akan tetapi sertifikat asli dari driver ini sudah **kadaluwarsa** sehingga saat menginstallnya kita akan menemukan peringatan seperti dibawah dan itu artinya drivernya tidak akan berfungsi walaupun sudah terinstall.

![libusb-win32-unsigned-warning](https://user-images.githubusercontent.com/760764/43999813-25ae4390-9e3e-11e8-9b9b-fb723fd59cc1.png)

Hal tersebut bisa diatasi dengan mengaktifkan mode `Disable Driver Signature Enforcement or using our drivers` tapi kekurangannya dilayar monitor akan ada keterangan `Test Mode...` yg kurang enak dipandang bahkan memudahkan virus menginstall driver ke komputer kita.

![windows testmode](https://user-images.githubusercontent.com/760764/59989993-a7a84280-966b-11e9-9f55-30b5936f965b.jpg)

Untuk itu daripada melakukan hal tersebut yg lumayan ribet caranya lebih baik kita memakai self signing certificate.

## Cara Install

### 1. Install Sertifikat driver
- Download dan extract [amilogic_usb_drivers.zip](https://raw.githubusercontent.com/ewwink/amlogic-usb-world-cup-driver-signed/master/amilogic_usb_drivers.zip)
- install sertifikat `libusb-win32.cer` dengan cara double-klik file-nya kemudian tekan tombol "Install Certificate.."
 
![libusb-win32.cer](https://user-images.githubusercontent.com/760764/89237853-8069c600-d61e-11ea-9c36-d6aeb842ff38.jpg)

- di `Store Location` pilih `Local Machine` kemudian klik Next

![Certificate wizard](https://user-images.githubusercontent.com/760764/89237865-8a8bc480-d61e-11ea-966f-ed5a19e27bd3.jpg)

- klik `Place All certificate....` kemudian tombol `Browse` dan pilih `Trusted Publisher` dan `OK`

![add certificate trusted publisher](https://user-images.githubusercontent.com/760764/89237866-8b245b00-d61e-11ea-8530-609687f292a1.jpg)

- Klik `Finish` dan sertifikat driver terinstall di komputer kamu.

![4](https://user-images.githubusercontent.com/760764/89237869-8bbcf180-d61e-11ea-9503-8a5746c39d56.jpg)

Untuk verifikasi bisa buka **`certmgr`** seperrti dibawah

![Certificate manager windows](https://user-images.githubusercontent.com/760764/89237870-8bbcf180-d61e-11ea-9bc4-a4765ec9103e.jpg)

### 2. Install Driver
- Buka `Device Manager` kemudian Di Menu `Action` klik `Add legacy hardware`
- Setelah itu klik `Next` =>  `Install The Hardware That.....` => `Next` => `Have a disk` => `Browse` dan cari lokasi `WorldCup_Device.inf` yg tadi kamu extract
- Selesai, nanti pas kedetek saat `Download` atau `Readback` di SP Flash Tool di Device manage akan ada perangkat seperti digambar berikut:

  **B760H:** `MediaTek Preloader USB VCOM (Android)`
  
  ![MediaTek Preloader USB VCOM (Android)](https://user-images.githubusercontent.com/760764/89237861-895a9780-d61e-11ea-9fb2-94a87a36d788.jpg)

  **B860H:** `libusb win32 usb device Worldcup Device`
  
  ![libusb win32 usb device Worldcup Device](https://user-images.githubusercontent.com/760764/89240988-e9097080-d627-11ea-9faf-2086c0f60291.jpg)

**Hardware Ids** 

 - USB\VID_1B8E&PID_C003&REV_0007
 - USB\VID_1B8E&PID_C003
