# qidi-tech-1-dual-extruder-backup
Backups from my qidi tech one dual extruder

This is a Replicator Makerbot dual extruder clone.
The mainboard has 2 Atmel chips on it 

Original dumps were created using a USBtiny ISP

I reached out to qidi tech to get copies of these, however they responded telling me the original DEV team has let the company and they no longer have this data.
Also ths printer is long out of support.

one is an ATmega8u2 (USB pass through) Read via port 8u2 ICSP 8 pin header

avrdude -c usbtiny -p m8u2 -P usb -b 5608 -U flash:r:"ATmega8u2-Flash.hex":i

avrdude -c usbtiny -p m8u2 -P usb -b 5608 -U flash:r:"ATmega8u2-EEPROM.hex":i

avrdude -c usbtiny -p m8u2 -P usb -b 5608 -U flash:r:"ATmega8u2-Flash.bin":r

avrdude -c usbtiny -p m8u2 -P usb -b 5608 -U flash:r:"ATmega8u2-EEPROM.bin":r

Fuses and lock bit read as:

lfuse: 0xFF

hfuse: 0xD9

efuse: 0xF4

Lock bits: 0xCF




The main chip is an ATmega2560 Read via 1280 ICSP 8 pin header

avrdude -c usbtiny -p m2560 -P usb -b 5600 -U flash:r:"ATmega2560-Flash.hex":i

avrdude -c usbtiny -p m2560 -P usb -b 5600 -U flash:r:"ATmega2560-EEPROM.hex":i

avrdude -c usbtiny -p m2560 -P usb -b 5600 -U flash:r:"ATmega2560-Flash.bin":r

avrdude -c usbtiny -p m2560 -P usb -b 5600 -U flash:r:"ATmega2560-EEPROM.bin":r

Fuses and lock bit read as:

lfuse: 0xFF

hfuse: 0xD8

efuse: 0xFD

Lock bits: 0xCF
