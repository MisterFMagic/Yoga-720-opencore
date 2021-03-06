# Yoga-720-opencore
OpenCore 0.65 configuration for Lenovo Yoga 720-13IKB
- Core i7-8550U (Kaby Lake R)
- 16GB RAM
- 512GB SSD NVMe (Adata, replaced the shipped Samsung -> check the web, lots of trouble)
- UHD 620
- Internal 4K display (uses -igfxmpc instead of -cdfon/enable-hdmi20 to get it running with Big Sur)
- Broadcom DW1820A (replaced the shipped WiFi card)

## Credits
- inspired by @dragonflylee and his Clover-based Yoga 730 config that worked quite fine with my 720:  https://github.com/dragonflylee/Yoga-730-hackintosh 

## State 
- [x] Catalina is working fine
- [x] Big Sur: installer gets stuck in a reboot loop at stage 2. 
               But: using a preinstalled volume (e.g. by another Mac/OC-Hack) works fine with this configuration! 
               Any hints welcome

## BIOS/Firmware settings
- Virtualization on
- Intel SGX off
- Secure Boot off
- SATA to AHCI

## Some details

### DW1820A 
Followed this thread to get rid of the freezes: https://osxlatitude.com/forums/topic/11322-broadcom-bcm4350-cards-under-high-sierramojavecatalina/
-> works! 

### Devirtualise MMIO
activated, working whithelist contained 
(without this quirk, Big Sur installer won't start at all - although Catalina runs fine without)

### enable-max-pixel-override / WhateverGreen
see this:
https://github.com/acidanthera/WhateverGreen/commit/978cb8c7a744ac189074225fd8eb2f16feb5a4c0

