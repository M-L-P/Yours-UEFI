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
- 復製文件夾 `zip: EFI\Yours` 到 `ESP: \EFI`；
- 刪除文件夾 `ESP: EFI\Boot`；
- 復製文件夾 `zip: EFI\Boot` 到 `ESP: \EFI`；
- 復製文件 `zip: startup.nsh` 到 `ESP: \`；

#### 若有 Hackintosh
如果你想要，
- 讓圖形界面銜接得更加緊密，中途沒有代碼界面；
- CloverBootloader 不與 Yours 發生沖突；

你需要執行以下步驟。
<details>
<summary>🖱️點擊展開查看🖱️</summary>

##### 若是 OpenCore
- 編輯 `config.plist` 設置 `LauncherOption=System` ；
- 剪切 EFI 相關文件，粘貼到 `EFI\Yours\efi\OC` ；
- 編輯 `refind.conf` ，刪除 位於`include /EFI/Yours/Settings/menuentry/examples/OpenCore.conf` 前面的 `#`；

##### 若是 CloverBootloader
- 剪切 EFI 相關文件，粘貼到 `EFI\Yours\efi\CLOVER` ；
- 編輯 `refind.conf` ，刪除 位於 `include /EFI/Yours/Settings/menuentry/examples/CLOVER.conf` 前面的 `#`；
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

## 🧁請我吃塊巧克力🍫
<details>
<summary>🖱️點擊展開查看🖱️</summary>
我沒有父親；沒人給我過生日；沒人為我買蛋糕🎂。<br/>
如果你願意，請我吃塊巧克力🍫。<br/>
我需要巧克力🍫幫助我釋放內啡肽與多巴胺來緩解痛苦。<br/>
我將會非常感謝您，仙女姐姐🧚‍ 或 玉樹豪俠🦸‍♂️。<br/>
<img src="https://github.com/M-L-P/Yours/assets/69227436/f094f056-9420-4dd5-beec-4ccecff20a1e" width="300px"><br/>
<img src="https://github.com/M-L-P/Yours/assets/69227436/8608e193-3c4d-4926-8171-7944e881d95f" width="300px">

[🧚仙女豪俠🦸‍♂️ 名单](https://github.com/M-L-P/.github/blob/main/list/README.md)
</details>