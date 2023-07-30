<div align="center">

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/M-L-P/Yours-UEFI)](https://github.com/M-L-P/Yours-UEFI/releases/latest)
[![GitHub all releases](https://img.shields.io/github/downloads/M-L-P/Yours-UEFI/total)](https://github.com/M-L-P/Yours-UEFI/releases)
[![GitHub Discussions](https://img.shields.io/github/discussions/M-L-P/Yours-UEFI)](https://github.com/M-L-P/Yours-UEFI/discussions)
[![GitHub Repo stars](https://img.shields.io/github/stars/M-L-P/Yours-UEFI?style=social)](https://github.com/M-L-P/Yours-UEFI/stargazers)

</div>

[English](README.md)|[简体中文](README-自述文件.md)|[繁體中文](README-繁體中文.md)|...
--|--|--|--

<h1 align="center">Yours-UEFI</h1>

🚩[🖱️Click to Jump to Yours🖱️](https://github.com/M-L-P/rEFInd-theme-Yours)<br/>
[Y-o-u-r-s](https://github.com/M-L-P/rEFInd-theme-Yours),<br/>
Your own usual rEFInd's sign for UEFI firmware.<br/>
Thank to Security bypass patches from [Super-UEFIinSecureBoot-Disk](https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk) of [ValdikSS](https://github.com/ValdikSS),<br/>
it can even load Clover or OpenCore to boot Hackintosh with SecureBoot enabled, not disabled anymore.
#### Your device should meet the requirements,
- 64bit UEFI supported;
- GPU/vBIOS UEFI supported;
#### Working Principle
[Power On]=>[UEFI Firmware]=>[BOOTX64.EFI] `shimx64.efi` renamed =>[grubx64.efi] `PreLoader.efi` renamed =>[grubx64_real.efi] Linked to `Yours_x64.efi` =>[Yours_x64.efi]=>[Yours]<br/>
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
- Copy the folder `zip: EFI\Yours` into `ESP: \EFI`;
- Delete the folder `ESP: EFI\Boot`;
- Copy the folder `zip: EFI\Boot` into `ESP: \EFI`;
- Copy the file `zip: startup.nsh` into `ESP: \`;

#### For Hackintosh
If you want,
- graphical interface is going to be not interrupted by codes;
- CloverBootloader does not conflict with Yours;

You need to perform the following steps.
<details>
<summary>🖱️Click to Unfold to see🖱️</summary>

##### For OpenCore
- Set `LauncherOption=System` by editing `config.plist`;
- Cut your EFI files into `ESP: \EFI\Yours\efi\OC`;
- Edit `refind.conf` to enable `include /EFI/Yours/Settings/menuentry/examples/OpenCore.conf` with `#` deleted;

##### For CloverBootloader
- Cut your EFI files into `ESP: \EFI\Yours\efi\CLOVER`;
- Edit `refind.conf` to enable `include /EFI/Yours/Settings/menuentry/examples/CLOVER.conf` with `#` deleted;
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

## 🧁Buy me a piece of chocolate🍫
<details>
<summary>🖱️Click to Unfold to see🖱️</summary>
I have no father; No man celebrates my birthday; No man buys me a cake🎂.<br/>
If you are willing, please treat me to a piece of chocolate🍫.<br/>
I need chocolate🍫 to help me release endorphins and dopamine to get rid of pain.<br/>
I would be very grateful to you, fairy lady🧚 or handsome knight🦸‍♂️.<br/>
<img src="https://github.com/M-L-P/Yours/assets/69227436/f094f056-9420-4dd5-beec-4ccecff20a1e" width="300px"><br/>
<img src="https://github.com/M-L-P/Yours/assets/69227436/8608e193-3c4d-4926-8171-7944e881d95f" width="300px">

[The List of Fairy Lady🧚 or Handsome kKnight🦸‍♂️](https://github.com/M-L-P/.github/blob/main/list/README.md)
</details>
