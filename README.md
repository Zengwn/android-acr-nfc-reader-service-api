android-acr-nfc-reader-service-api
==================================
This project hosts the API for interacting with the [ACS NFC Reader Service](https://play.google.com/store/apps/details?id=com.skjolberg.acs) found at Google Play. 
It contains
 * Java API files for integration via broadcasts, and an
 * Android client which demonstrates actual usage

Supported readers
=================
Currently the readers
 * [ACR 122U](http://www.acs.com.hk/index.php?pid=product&id=ACR122U) 
 * [ACR 1222L](http://www.acs.com.hk/index.php?pid=product&id=ACR1222L)
 * [ACR 1251](http://www.acs.com.hk/en/products/218/acr1251-usb-nfc-reader-ii/)
 
are supported and must be connected to your Android device via an On-The-Go (OTG) USB cable.

Supported tag technology
========================
Mifare Ultralight and Mifare Classic tags are supported. NTAG203 also work. I recommend Mifare Ultralights or NTAG203. Desfire EV1 tags are detected but there is no NDEF support. If you need some tags, get some at [RapidNFC](http://rapidnfc.com/r/1372).

Note: For ACR 122U the Mifare Classic support is experimental.

API
===
The API defines actions and Intent extras for interaction with the service.
 * Service started/stopped 
 * ACR NFC Reader opened / closed - triggered by connects / disconnects via USB
 * NFC Tag scans 

Demo client
===========
The demo client keeps track of the service states and displays NDEF messages from tags scanned by the ACR NFC Reader.

Free features
===========
Detecting tag presence, type and id are free features.

Premium features
===========
Reading and writing NDEF messages are premium features. This API should speed up NFC development considerably, so consider going premium. A more advanced API is available upon request, which also includes direct reader commands. I offer pay-once licenses both for source and/or compiled library. Having the library will save you anywhere between 1 and 3 months of work.

Troubleshooting
===========
Does the ACR reader not light up when connected to your device, even after the service asks for USB permissions? The ACR reader shuts down if there is not enough battery, so try charging your battery more. Please report any issues to skjolber@gmail.com.

Related apps
============
You might be interested in
 * [ACR 1222L USB NFC Reader Utils](https://play.google.com/store/apps/details?id=com.skjolberg.acr1222) 
 * [ACR 122 USB NFC Reader Utils](https://play.google.com/store/apps/details?id=com.skjolberg.acr122u)

for configuration of your reader.

Need help?
===========
If you need professional assistance with an NFC project, get in touch. I also do

 * Host Card Emulation for Android
 * Desfire EV1 tags (with encryption)
 * Smart card related workflows and integrations

Check out my professional profile and connect with me on [LinkedIn](http://lnkd.in/r7PWDz).
