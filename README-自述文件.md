<div align="center">

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/M-L-P/Yours-UEFI)](https://github.com/M-L-P/Yours-UEFI/releases/latest)
[![GitHub all releases](https://img.shields.io/github/downloads/M-L-P/Yours-UEFI/total)](https://github.com/M-L-P/Yours-UEFI/releases)
[![GitHub Discussions](https://img.shields.io/github/discussions/M-L-P/Yours-UEFI)](https://github.com/M-L-P/Yours-UEFI/discussions)
[![GitHub Repo stars](https://img.shields.io/github/stars/M-L-P/Yours-UEFI?style=social)](https://github.com/M-L-P/Yours-UEFI/stargazers)

</div>

[English](README.md)|[简体中文](README-自述文件.md)|[繁體中文](README-繁體中文.md)|...
--|--|--|--

<h1 align="center">Yours-UEFI</h1>

- [🖱️Click to Jump to Yours🖱️](https://github.com/M-L-P/rEFInd-theme-Yours)<br/>
[Y-o-u-r-s](https://github.com/M-L-P/rEFInd-theme-Yours),<br/>
Your own usual rEFInd's sign for UEFI firmware.<br/>
多亏了安全启动补丁，来自 [ValdikSS](https://github.com/ValdikSS) 的 [Super-UEFIinSecureBoot-Disk](https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk)，<br/>
终于能够在安全启动模式开启的情况下，加载 Clover 或 OpenCore 进而启动黑苹果，可以不用再关闭安全启动模式了。
#### 你的设备应该满足条件,
- 支持 64bit UEFI；
- GPU/vBIOS 支持 UEFI；
#### 工作原理
[Power On]=>[UEFI Firmware]=>[BOOTX64.EFI] `shimx64.efi` 重命名的 =>[grubx64.efi] `PreLoader.efi` 重命名的 =>[grubx64_real.efi] 链接到 `Yours_x64.efi` =>[Yours_x64.efi]=>[Yours]<br/>
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
- 删除文件夹 `ESP: ESP\EFI\Boot`；
- 复制文件夹 `zip: ESP\EFI\Yours` 到 `ESP: \EFI`；
- 复制文件夹 `zip: ESP\EFI\BOOT` 到 `ESP: \EFI`；
- 复制文件 `zip: ESP\startup.nsh` 到 `ESP: \`；
- 复制文件 `zip: ESP\ENROLL_THIS_KEY_IN_MOKMANAGER.cer` 到 `ESP: \`；

#### 若有 黑苹果
为了让
- 图形界面衔接得更加紧密，中途没有代码界面；
- 同时支持安全启动；

<details>
<summary>🖱️点击展开查看🖱️</summary>

文件名|所在目录|文件原理|文件功能
-|-|-|-
`GrubPreLoader_CLOVER.efi`|`EFI\Yours\efi`|链接到 `EFI\CLOVER\CLOVERX64.efi`|预启动 CloverBootloader
`GrubPreLoader_CLOVER.png`|`EFI\Yours\efi`|同名显示图标|用于显示 Clover 的启动图标
`GrubPreLoader_OC.efi`|`EFI\Yours\efi`|链接到 `EFI\OC\OpenCore.efi`|预启动 OpenCore
`GrubPreLoader_OC.png`|`EFI\Yours\efi`|同名显示图标|用于显示 OC 的启动图标

#### 若是 OpenCore
- 你应该编辑 `config.plist` 设置 `LauncherOption=System` ；

#### 若不用黑果
- 你可以选定 Clover 或 OC 的启动图标，按下【Delete】，隐藏对应的入口。
</details>

</details>

### 添加入口
<details>
<summary>🖱️点击展开查看🖱️</summary>
https://www.diskgenius.com/manual/set-uefi-bios-boot-entries.php

[<img src="https://github.com/M-L-P/Yours-UEFI/assets/69227436/df531a15-a171-49c3-8c8a-59447c2f396e">](https://www.diskgenius.com/manual/set-uefi-bios-boot-entries.php)

</details>

## 📝FAQ❓️
常见问题
### 安全启动
http://www.rodsbooks.com/refind/secureboot.html<br/>
https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk

## ⭐收藏🌟
如果你喜欢并且期待未来的更新，你可以点亮星星。💫

## 🎉来源🎊
- *Roderick W. Smith* 的 [rEFInd Boot Manager](http://www.rodsbooks.com/refind/)；
- [a1ive](https://github.com/a1ive) 的 [grub2-filemanager](https://github.com/a1ive/grub2-filemanager)；
- 安全启动补丁 来自 [ValdikSS](https://github.com/ValdikSS) 的 [Super-UEFIinSecureBoot-Disk](https://github.com/ValdikSS/Super-UEFIinSecureBoot-Disk)；

## [🧁请我吃块巧克力🍫](https://github.com/M-L-P/.github/blob/main/chocolate/chocolate.md)