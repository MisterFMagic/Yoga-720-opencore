# Yoga-720-opencore
OpenCore 0.95 configuration for Lenovo Yoga 720-13IKB
- Core i7-8550U (Kaby Lake R)
- 16GB RAM
- 1024GB SSD NVMe (replaced the shipped Samsung -> check the web, lots of trouble)
- UHD 620
- Internal 4K display (uses -igfxmpc instead of -cdfon/enable-hdmi20 to get it running with Big Sur)
- Using the shipped Intel WiFi / BT card
- Support for Broadcom Cards included, but Kexts disabled
- Uses MacBookPro15,4 instead of 14,1 to be ready for Sonoma

## Credits
- inspired by @dragonflylee and his Clover-based Yoga 730 config that worked quite fine with my 720:  https://github.com/dragonflylee/Yoga-730-hackintosh 

## State 
- runs Ventura 13.6 fine! 
- preparing for Sonoma (switch to Intel Wifi/BT and waiting for airportitlwm being ready for the upgrade)
- (a branch for Big Sur is available in this repository as well (although OC and Kexts are outdated))

## BIOS/Firmware settings
- Virtualization on
- Intel SGX off
- Secure Boot off
- SATA to AHCI

## Some details

### Bluetooth working again 
Due to this modification: https://osxlatitude.com/forums/topic/18225-enable-bluetooth-in-macos-ventura-134-for-broadcom-intel-bluetooth-intel-bluetooth-fix/

### DW1820A 
Followed this thread to get rid of the freezes: https://osxlatitude.com/forums/topic/11322-broadcom-bcm4350-cards-under-high-sierramojavecatalina/
-> works! 

### Devirtualise MMIO
activated, working whithelist contained 
(without this quirk, Big Sur installer won't start at all - although Catalina runs fine without)

### enable-max-pixel-override / WhateverGreen
see this:
https://github.com/acidanthera/WhateverGreen/commit/978cb8c7a744ac189074225fd8eb2f16feb5a4c0

