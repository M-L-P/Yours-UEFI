[icons](https://github.com/M-L-P/icons)|[rEFInd-theme-Yours](https://github.com/M-L-P/rEFInd-theme-Yours)|[Yours-LegacyBIOS](https://github.com/M-L-P/Yours-LegacyBIOS)|[Yours-UEFI](https://github.com/M-L-P/Yours-UEFI)
-|-|-|-

<div align="center">

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/M-L-P/Yours-UEFI)](https://github.com/M-L-P/Yours-UEFI/releases/latest)
[![GitHub all releases](https://img.shields.io/github/downloads/M-L-P/Yours-UEFI/total)](https://github.com/M-L-P/Yours-UEFI/releases)
[![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/M-L-P/Yours-UEFI/%E6%89%93%E5%8C%85.yml)](https://github.com/M-L-P/Yours-UEFI/actions)
[![GitHub Discussions](https://img.shields.io/github/discussions/M-L-P/Yours-UEFI)](https://github.com/M-L-P/Yours-UEFI/discussions)
[![GitHub Repo stars](https://img.shields.io/github/stars/M-L-P/Yours-UEFI?style=social)](https://github.com/M-L-P/Yours-UEFI/stargazers)

</div>

[English](README.md)|[简体中文](README-自述文件.md)|[繁體中文](README-繁體中文.md)|...
--|--|--|--

<h1 align="center">Yours-UEFI</h1>

[Y-o-u-r-s](https://github.com/M-L-P/rEFInd-theme-Yours),<br/>
Your own usual rEFInd's sign for UEFI firmware.<br/>
多虧了安全啟動補丁，來自 [ValdikSS](https://github.com/ValdikSS) 的 [Super-UEFIinSecureBoot-Disk](https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk)，<br/>
終於能夠在安全啟動模式開啟的情況下，載入 Clover 或 OpenCore 進而啟動黑蘋果，可以不用再關閉安全啟動模式了。
#### 你的裝置應該滿足條件,
- 支援 64bit UEFI；
- GPU/vBIOS 支援 UEFI；
#### 工作原理
[Power On]=>[UEFI Firmware]=>[Bootx64.efi] `shimx64.efi` 重新命名的 =>[MokManager.efi] `PreLoader.efi` 重新命名的 =>[grubx64_real.efi] 連結到 `Yours_x64.efi` =>[Yours_x64.efi]=>[Yours]<br/>
#### 檔案結構樹狀圖
<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours-UEFI/Yours-UEFI.png">

-----------------------------------------------------------------------------------------------------------------------------------
## 💻️預覽👀

<details>
<summary>🖱️點選展開檢視🖱️</summary>

<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours-UEFI/about.real.png">
<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours/1080p.M.big.png">
</details>

## 🧭指南⬇️

### 調整 ESP 分割槽
<details>
<summary>🖱️點選展開檢視🖱️</summary>

#### 複製到 ESP 分割槽
- 刪除資料夾 `ESP: ESP\EFI\Boot`；
- 複製資料夾 `zip: ESP\EFI\Yours` 到 `ESP: \EFI`；
- 複製資料夾 `zip: ESP\EFI\Boot` 到 `ESP: \EFI`；
- 複製檔案 `zip: ESP\startup.nsh` 到 `ESP: \`；
- 複製檔案 `zip: ESP\ENROLL_THIS_KEY_IN_MOKMANAGER.cer` 到 `ESP: \`；

#### 若有 黑蘋果
為了讓
- 圖形介面銜接得更加緊密，中途沒有程式碼介面；
- 同時支援安全啟動；

<details>
<summary>🖱️點選展開檢視🖱️</summary>

檔名|所在目錄|檔案原理|檔案功能
-|-|-|-
`GRUB_PreLoader_CLOVER.efi`|`EFI\Yours\efi\Hackintosh`|連結到 `EFI\CLOVER\CLOVERX64.efi`|預啟動 CloverBootloader
`GRUB_PreLoader_CLOVER.png`|`EFI\Yours\efi\Hackintosh`|同名顯示圖示|用於顯示 Clover 的啟動圖示
`GRUB_PreLoader_OC.efi`|`EFI\Yours\efi\Hackintosh`|連結到 `EFI\OC\OpenCore.efi`|預啟動 OpenCore
`GRUB_PreLoader_OC.png`|`EFI\Yours\efi\Hackintosh`|同名顯示圖示|用於顯示 OC 的啟動圖示

#### 若是 OpenCore
- 你應該編輯 `config.plist` 設定 `LauncherOption=System` ；

#### 若不用黑果
- 你可以選定 Clover 或 OC 的啟動圖示，按下【Delete】，隱藏對應的入口。
</details>

</details>

### 新增入口
<details>
<summary>🖱️點選展開檢視🖱️</summary>
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
- 安全啟動補丁 來自 [ValdikSS](https://github.com/ValdikSS) 的 [Super-UEFIinSecureBoot-Disk](https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk)；

## [🧁請我吃塊巧克力🍫](https://github.com/M-L-P/.github/blob/main/profile/chocolate/README.md)
