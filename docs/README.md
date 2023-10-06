[icons](https://github.com/M-L-P/icons)|[rEFInd-theme-Yours](https://github.com/M-L-P/rEFInd-theme-Yours)|[Yours-LegacyBIOS](https://github.com/M-L-P/Yours-LegacyBIOS)|[Yours-UEFI](https://github.com/M-L-P/Yours-UEFI)
-|-|-|-

<div align="center">

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/M-L-P/Yours-UEFI)](https://github.com/M-L-P/Yours-UEFI/releases/latest)
[![GitHub all releases](https://img.shields.io/github/downloads/M-L-P/Yours-UEFI/total)](https://github.com/M-L-P/Yours-UEFI/releases)
[![GitHub Discussions](https://img.shields.io/github/discussions/M-L-P/Yours-UEFI)](https://github.com/M-L-P/Yours-UEFI/discussions)
[![GitHub Repo stars](https://img.shields.io/github/stars/M-L-P/Yours-UEFI?style=social)](https://github.com/M-L-P/Yours-UEFI/stargazers)

</div>

[English](README.md)|[简体中文](README-自述文件.md)|[繁體中文](README-繁體中文.md)|...
--|--|--|--

<h1 align="center">Yours-UEFI</h1>

[Y-o-u-r-s](https://github.com/M-L-P/rEFInd-theme-Yours),<br/>
Your own usual rEFInd's sign for UEFI firmware.<br/>
Thank to Security bypass patches from [Super-UEFIinSecureBoot-Disk](https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk) of [ValdikSS](https://github.com/ValdikSS),<br/>
it can even load Clover or OpenCore to boot Hackintosh with Secure Boot enabled, not disabled anymore.
#### Your device should meet the requirements,
- 64bit UEFI supported;
- GPU/vBIOS UEFI supported;
#### Working Principle
[Power On]=>[UEFI Firmware]=>[BOOTX64.EFI] `shimx64.efi` renamed =>[fbx64.efi] `PreLoader.efi` renamed =>[grubx64_real.efi] Linked to `Yours_x64.efi` =>[Yours_x64.efi]=>[Yours]<br/>
#### File Tree
<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours-UEFI/Yours-UEFI.png">

-----------------------------------------------------------------------------------------------------------------------------------
## 💻️Preview👀

<details>
<summary>🖱️Click to Unfold to see🖱️</summary>

<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours-UEFI/about.real.png">
<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours/1080p.M.big.png">
</details>

## 🧭Guide⬇️

### Manage ESP
<details>
<summary>🖱️Click to Unfold to see🖱️</summary>

#### Copy in ESP
- Delete the folder `ESP: ESP\EFI\Boot`;
- Copy the folder `zip: ESP\EFI\Yours` into `ESP: \EFI`;
- Copy the folder `zip: ESP\EFI\BOOT` into `ESP: \EFI`;
- Copy the file `zip: ESP\startup.nsh` into `ESP: \`;
- Copy the file `zip: ESP\ENROLL_THIS_KEY_IN_MOKMANAGER.cer` into `ESP: \`;

#### For Hackintosh
In order to ensure 
- that the graphical interface is NOT going to be interrupted by codes;
- that it will support Secure Boot;

<details>
<summary>🖱️Click to Unfold to see🖱️</summary>

File Name|Directory|Principle|Function
-|-|-|-
`GRUB_PreLoader_CLOVER.efi`|`EFI\Yours\efi\Hackintosh`|Linked to `EFI\CLOVER\CLOVERX64.efi`|PreLoader CloverBootloader
`GRUB_PreLoader_CLOVER.png`|`EFI\Yours\efi\Hackintosh`|To display icon with the same name|Used to display icon of Clover
`GRUB_PreLoader_OC.efi`|`EFI\Yours\efi\Hackintosh`|Linked to `EFI\OC\OpenCore.efi`|PreLoader OpenCore
`GRUB_PreLoader_OC.png`|`EFI\Yours\efi\Hackintosh`|To display icon with the same name|Used to display icon of OC

#### For OpenCore
- Set `LauncherOption=System` by editing `config.plist`;

#### Without Hackintosh
- You can select the icon of Clover or OC, press [Delete], and hide the corresponding entry.
</details>

</details>

### Add Entry
<details>
<summary>🖱️Click to Unfold to see🖱️</summary>
https://www.diskgenius.com/manual/set-uefi-bios-boot-entries.php

[<img src="https://github.com/M-L-P/Yours-UEFI/assets/69227436/df531a15-a171-49c3-8c8a-59447c2f396e">](https://www.diskgenius.com/manual/set-uefi-bios-boot-entries.php)

</details>

## 📝FAQ❓️
Frequently asked question
### Secure Boot
http://www.rodsbooks.com/refind/secureboot.html<br/>
https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk

## ⭐Star🌟
If you like it and are looking forward to the coming update, you can star it.💫

## 🎉Credit🎊
- [rEFInd Boot Manager](http://www.rodsbooks.com/refind/) of *Roderick W. Smith*;
- [grub2-filemanager](https://github.com/a1ive/grub2-filemanager) of [a1ive](https://github.com/a1ive);
- Security bypass patches from [Super-UEFIinSecureBoot-Disk](https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk) of [ValdikSS](https://github.com/ValdikSS);

## [🧁Buy me a piece of chocolate🍫](https://github.com/M-L-P/.github/blob/main/profile/chocolate/README.md)