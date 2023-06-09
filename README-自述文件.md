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
Your own usual rEFInd's sign for UEFI firmware.
#### 你的设备应该满足条件,
- 支持 64bit UEFI；
- GPU/vBIOS 支持 UEFI；
#### 工作原理
[Power On]=>[UEFI Firmware]=>[bootx64.efi]=>[Yours]<br/>
or<br/>
[Power On]=>[UEFI Firmware]=>[Yours_x64.efi]=>[Yours]<br/>
#### 文件结构树状图
<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours-UEFI/Yours-UEFI.png">

-----------------------------------------------------------------------------------------------------------------------------------
## 💻️预览👀

<details>
<summary>🖱️点击展开查看🖱️</summary>

<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours-UEFI/about.real.png">
<img src="https://raw.githubusercontent.com/M-L-P/.github/main/screenshots/Yours/1080p.M.big.png">
</details>

## 🧭指南⬇️

### 调整 ESP 分区
<details>
<summary>🖱️点击展开查看🖱️</summary>

#### 复制到 ESP 分区
- 复制文件夹 `zip: EFI\Yours` 到 `ESP: \EFI`；
- 删除文件夹 `ESP: EFI\Boot`；
- 复制文件夹 `zip: EFI\Boot` 到 `ESP: \EFI`；
- 复制文件 `zip: startup.nsh` 到 `ESP: \`；

#### 若有 黑苹果
如果你想要，
- 让图形界面衔接得更加紧密，中途没有代码界面；
- CloverBootloader 不与 Yours 发生冲突；

你需要执行以下步骤。
<details>
<summary>🖱️点击展开查看🖱️</summary>

##### 若是 OpenCore
- 编辑 `config.plist` 设置 `LauncherOption=System` ；
- 剪切 EFI 相关文件，粘贴到 `EFI\Yours\efi\OC` ；
- 编辑 `refind.conf` ，删除 位于`include /EFI/Yours/Settings/menuentry/examples/OpenCore.conf` 前面的 `#`；

##### 若是 CloverBootloader
- 剪切 EFI 相关文件，粘贴到 `EFI\Yours\efi\CLOVER` ；
- 编辑 `refind.conf` ，删除 位于 `include /EFI/Yours/Settings/menuentry/examples/CLOVER.conf` 前面的 `#`；
</details>

</details>

### 添加入口
<details>
<summary>🖱️点击展开查看🖱️</summary>
https://www.diskgenius.com/manual/set-uefi-bios-boot-entries.php

[<img src="https://github.com/M-L-P/Yours-UEFI/assets/69227436/2f7cc14d-e8c0-434e-bd8b-1a6d51f4ac57">](https://www.diskgenius.com/manual/set-uefi-bios-boot-entries.php)

</details>

## 📝FAQ❓️
常见问题
### 安全启动
http://www.rodsbooks.com/refind/secureboot.html

## ⭐收藏🌟
如果你喜欢并且期待未来的更新，你可以点亮星星。💫

## 🎉来源🎊
- *Roderick W. Smith* 的 [rEFInd Boot Manager](http://www.rodsbooks.com/refind/)；
- [a1ive](https://github.com/a1ive) 的 [grub2-filemanager](https://github.com/a1ive/grub2-filemanager)；

## 🧁请我吃块巧克力🍫
<details>
<summary>🖱️点击展开查看🖱️</summary>
我没有父亲；没人给我过生日；没人为我买蛋糕🎂。<br/>
如果你愿意，请我吃块巧克力🍫。<br/>
我需要巧克力🍫帮助我释放内啡肽与多巴胺来缓解痛苦。<br/>
我将会非常感谢您，仙女姐姐🧚‍ 或 玉树豪侠🦸‍♂️。<br/>
<img src="https://github.com/M-L-P/Yours/assets/69227436/f094f056-9420-4dd5-beec-4ccecff20a1e" width="300px"><br/>
<img src="https://github.com/M-L-P/Yours/assets/69227436/8608e193-3c4d-4926-8171-7944e881d95f" width="300px">

[🧚仙女豪侠🦸‍♂️ 名单](https://github.com/M-L-P/.github/blob/main/list/README.md)
</details>