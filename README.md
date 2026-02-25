### Machine Info
- Name: LG Gram 15Z980
- CPU: i5-8250u
- iGPU: intel 620
- RAM: 16GB 2400Mhz
- Internal Storage: NVME 512GB + NVME 256GB
- External Storage: 512GB HDD in USB 3.0 enclosure

I Installed my hackintosh in External Storage hahhaha. I will not use this OS as my daily driver since I am using Ubuntu x Windows (Dualboot setup). I only did this project for the reason that I want to install cracked products in MacOS. I tied OSX-KVM project for running MAcOS in VM days ago but it has performance issue, it doesnt use iGPU (maybe my skill use). Cracked software exists in MacOS!!!.

## Project Details
### Added Kexts
- Itlwm.kext - fixed slow wireless internet
- ECEnabler.kext - for fixing battery display/ detection (ACPI SSDT files in z980 series doesn't work)

### Disabled in kernel tab at OCAT_Mac.dmg
- Airportltlwm.kext - this is built-in ACPI driver but struggles in getting internet speed (Wi-Fi). So I replaced it with Itlwm.kext. They belong to the same project
- Itlwm works well compared to Airportltlwm.kext but still struggles, not consistent.
- If connected to a phone's hotspot with the same router it can spike.
- 
### Working
- iGPU
- FN Keys (brightness, volume, backlight KB)
- Command/ windows Key
- Numpad
- Sleep and wake
- Battery Display
- Bluetooth

#### I used Hardwaresniffer to view and automate hardware report generation (.json file) for customized ACPI patch but there are still hardware that are not working properly or totaly not working. 
### Not Working
- PrtSc key
- Right 2nd USB slot (beside 3.5 Jack)
- Type-C cant detect phone storage but can provide power. 
- SD Card Slot (Detects my SD card after it stays in the slot for an hour)
- Airdrop (expected)
- FingerPrint

Note: if hackintosh is not booting when you remove the external storage holding EFI, replace your boot .efi file with OpenCore.efi and rename it "BOOTx64.efi" (if you are using Windows boot Manager) same situation if your using GRUB for linux but dont delete your original bootloader, save it as backup. I also uploaded the BOOTLOADER here together with my OC file, you can Copy & Paste it in your EFI partition. 

Note (2): I did this project on Feb 5, 2026 and created this README in Feb 25, 2026, I forgot some of the details, I am now thinking if I write this correctly hahaha. Its important to study more and read different repo, maybe ill modify this readme if I will go back in this project

if someone is reading this, thanks for visiting my repo and please leave a star hahaha




