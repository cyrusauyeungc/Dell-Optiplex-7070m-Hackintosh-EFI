# Dell-Optiplex-7070m-Hackintosh-EFI

Credits/Reference:  
Thanks @[liaoyudong](https://github.com/liaoyudong2/Dell-7070-mff-hackintosh) for guiding me through my very first Hackintosh build. 

---

## Hackintosh macOS Big Sur 11.1 Build 20C69 at Dell Optiplex 7070 Micro Form Factor

![](https://user-images.githubusercontent.com/69232468/107194292-d20a6780-6a2a-11eb-96c8-e15f43806466.png)

![](https://user-images.githubusercontent.com/69232468/107194426-fcf4bb80-6a2a-11eb-84b2-c56a7b35933d.png)

### Specifications

*   Processor : Intel Core i5 9500T
*   IGPU : Intel UHD 630
*   RAM : 16GB DDR4 2666Mhz
*   Storage : 256gb Toshiba m.2 NVMe ssd
*   Wifi : Broadcom94352z
*   Audio : Realtek ALC255
*   Bootloader : OpenCore 0.6.3

### What's working?

*   Airdrop/Handoff/Continuity
*   Restart, Sleep, Wakeup and Shutdown
*   Internal Speaker, 3.5mm Audio Output
*   Wifi
*   Display Port Output
*   All USB Port
*   Boot Chime

### Not Work/ Pending for testing

*   (Pending) Unlock with Apple Watch
*   (Pending) Microphone Jack
*   (Pending) Display Port Audio Out
*   (Not Working) DRM Content on Safari
*   (Not Working) Wake on Wi-Fi (only wake on ethernet is available in power settings)

### Steps (Always refer to OpenCore Install Guide [here](https://dortania.github.io/OpenCore-Install-Guide/))

1.  Format your USB Drive to MacOS Journaled / GUID Partition
2.  Install Big Sur Installer
3.  Mount with ESP Mounter Pro to access EFI
4.  Extract the "EFI-Shell.zip" to your USB Drive with EFI folder in the first level
5.  Boot with the bootx64.efi (2.5mb)
6.  Execute the 2 statement in Shell as noted in the `setup_var.txt` without the #comment
7.  Rename the EFI folder to EFI-Setupvar (to prevent system booting from it, or you can remove the whole EFI folder)
8.  Copy the "Boot" and "OC" from `After Setup_Var` folder to the EFI, and start the installation!

### Point to Note

*   [x] Please add your own SystemSerialNumber / SystemUUID / MLB with [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
