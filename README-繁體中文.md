- [🖱️點擊跳轉查看🖱️](https://github.com/M-L-P/rEFInd-theme-Yours)<br/>

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
多虧了安全啟動補丁，來自 [ValdikSS](https://github.com/ValdikSS) 的 [Super-UEFIinSecureBoot-Disk](https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk)，<br/>
終於能夠在安全啟動模式開啟的情況下，加載 Clover 或 OpenCore 進而啟動黑蘋果，可以不用再關閉安全啟動模式了。
#### 你的設備應該滿足條件,
- 支持 64bit UEFI；
- GPU/vBIOS 支持 UEFI；
#### 工作原理
[Power On]=>[UEFI Firmware]=>[BOOTX64.EFI] `shimx64.efi` 重命名的 =>[grubx64.efi] `PreLoader.efi` 重命名的 =>[grubx64_real.efi] 鏈接到 `Yours_x64.efi` =>[Yours_x64.efi]=>[Yours]<br/>
#### 文件結構樹狀圖
<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours-UEFI/Yours-UEFI.png">

-----------------------------------------------------------------------------------------------------------------------------------
## 💻️預覽👀

<details>
<summary>🖱️點擊展開查看🖱️</summary>

<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours-UEFI/about.real.png">
<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours/1080p.M.big.png">
</details>

## 🧭指南⬇️

### 調整 ESP 分區
<details>
<summary>🖱️點擊展開查看🖱️</summary>

#### 復製到 ESP 分區
- 刪除文件夾 `ESP: ESP\EFI\Boot`；
- 復製文件夾 `zip: ESP\EFI\Yours` 到 `ESP: \EFI`；
- 復製文件夾 `zip: ESP\EFI\BOOT` 到 `ESP: \EFI`；
- 復製文件 `zip: ESP\startup.nsh` 到 `ESP: \`；
- 復製文件 `zip: ESP\ENROLL_THIS_KEY_IN_MOKMANAGER.cer` 到 `ESP: \`；

#### 若有 Hackintosh
為了讓
- 圖形界面銜接得更加緊密，中途沒有代碼界面；
- 同時支持安全啟動；

<details>
<summary>🖱️點擊展開查看🖱️</summary>

文件名|所在目錄|文件原理|文件功能
-|-|-|-
`GrubPreLoader_CLOVER.efi`|`EFI\Yours\efi`|鏈接到 `EFI\CLOVER\CLOVERX64.efi`|預啟動 CloverBootloader
`GrubPreLoader_CLOVER.png`|`EFI\Yours\efi`|同名顯示圖標|用於顯示 Clover 的啟動圖標
`GrubPreLoader_OC.efi`|`EFI\Yours\efi`|鏈接到 `EFI\OC\OpenCore.efi`|預啟動 OpenCore
`GrubPreLoader_OC.png`|`EFI\Yours\efi`|同名顯示圖標|用於顯示 OC 的啟動圖標

#### 若是 OpenCore
- 你應該編輯 `config.plist` 設置 `LauncherOption=System` ；

#### 若不用黑果
- 你可以選定 Clover 或 OC 的啟動圖標，按下【Delete】，隱藏對應的入口。
</details>

</details>

### 添加入口
<details>
<summary>🖱️點擊展開查看🖱️</summary>
https://www.diskgenius.com/manual/set-uefi-bios-boot-entries.php

[<img src="https://github.com/M-L-P/Yours-UEFI/assets/69227436/df531a15-a171-49c3-8c8a-59447c2f396e">](https://www.diskgenius.com/manual/set-uefi-bios-boot-entries.php)

</details>

## 📝FAQ❓️
常見問題
### 安全啟動
http://www.rodsbooks.com/refind/secureboot.html<br/>
https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk

## ⭐收藏🌟
如果你喜歡並且期待未來的更新，你可以點亮星星。💫

## 🎉來源🎊
- *Roderick W. Smith* 的 [rEFInd Boot Manager](http://www.rodsbooks.com/refind/)；
- [a1ive](https://github.com/a1ive) 的 [grub2-filemanager](https://github.com/a1ive/grub2-filemanager)；
- 安全啟動補丁來自 [ValdikSS](https://github.com/ValdikSS) 的 [Super-UEFIinSecureBoot-Disk](https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk);

## [🧁請我吃塊巧克力🍫](https://github.com/M-L-P/.github/blob/main/chocolate/chocolate.md)