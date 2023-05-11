[English](README.md)|[简体中文](自述文件.md)|[繁體中文](繁體中文.md)
--|--|--

# Yours-UEFI
Your own usual rEFInd's sign for UEFI.
#### Your device should meet the requirements,
- 64bit UEFI supported;
- GPU/vBIOS UEFI supported;
#### Working Principle
[Power On]=>[UEFI Firmware]=>[bootx64.efi]=>[Yours]<br/>
or<br/>
[Power On]=>[UEFI Firmware]=>[Yours_x64.efi]=>[Yours]<br/>
#### File Tree
<img src="README/Yours-UEFI.png">

## 💻️Preview👀

<details>
<summary>🖱️Click to Unfold to see🖱️</summary>

<img src="README/about.real.png">
</details>

## 🧭Guide⬇️

<details>
<summary>🖱️Click to Unfold to see🖱️</summary>

### Manage ESP
<details>
<summary>🖱️Click to Unfold to see🖱️</summary>

#### Copy in ESP

#### For Hackintosh
If you want,
- graphical interface is going to be not interrupted by codes;
- CloverBootloader does not conflict with Yours;

You need to perform the following steps.
<details>
<summary>🖱️Click to Unfold to see🖱️</summary>

##### For OpenCore
- Set `LauncherOption=System` by editing `config.plist`;
- Cut your EFI files into `EFI\Yours\efi\OC`;
- Edit `refind.conf` to enable `include /EFI/Yours/Settings/menuentry/examples/OpenCore.conf` with `#` deleted;

##### For CloverBootloader
- Cut your EFI files into `EFI\Yours\efi\CLOVER`;
- Edit `refind.conf` to enable `include /EFI/Yours/Settings/menuentry/examples/CLOVER.conf` with `#` deleted;
</details>

</details>

### Add Entry
<details>
<summary>🖱️Click to Unfold to see🖱️</summary>

</details>

</details>

## ⭐Star🌟
If you like it and are looking forward to the coming update, you can star it.💫

## 🎉Credit🎊
- 
