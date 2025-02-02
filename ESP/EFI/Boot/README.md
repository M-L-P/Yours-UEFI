## ESP: /EFI/BOOT

- `BOOTX64.EFI` is what is `shimx64.efi` renamed;
- `fallback.efi` is what is `PreLoader.efi` renamed;
- `grubx64_real.efi` is linked to `Yours_x64.efi`;
- `MokManager.efi` is used to eroll the key;

### Working Principle
[Power On]=>[UEFI Firmware]=>[BOOTX64.EFI] `shimx64.efi` renamed =>[MokManager.efi] `PreLoader.efi` renamed =>[grubx64_real.efi] Linked to `Yours_x64.efi` =>[Yours_x64.efi]=>[Yours]