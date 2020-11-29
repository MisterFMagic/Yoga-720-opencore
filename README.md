# Yoga-720-opencore
OpenCore configuration for Lenovo Yoga 720-13IKB
- Core i7-8550U (Kaby Lake R)
- 16GB RAM
- 512GB SSD NVMe (Adata, replaced the shipped Samsung -> check the web, lots of trouble)
- UHD 620
- Internal 4K display
- Broadcom DW1820A (replaced the shipped WiFi card)

## Credits
- inspired by @dragonflylee and his Clover-based Yoga 730 config that worked quite fine with my 720:  https://github.com/dragonflylee/Yoga-730-hackintosh 

## State 
- [x] Catalina is working fine
- [ ] Big Sur is under investigation, due to 4K display stuff (-cdfon/enable-hdmi20 switch). Gets stuck in an endless reboot. 

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
(without this quirk, Big Sur installer won't start at all - although Catalina runs fine)
