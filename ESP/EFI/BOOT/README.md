## ESP: /EFI/BOOT

- `BOOTX64.EFI` is what is `shimx64.efi` renamed;
- `grubx64.efi` is what is `PreLoader.efi` renamed;
- `grubx64_real.efi` is linked to `Yours_x64.efi`;
- `mmx64.efi` is used to eroll the key;

### Working Principle
[Power On]=>[UEFI Firmware]=>[BOOTX64.EFI] `shimx64.efi` renamed =>[grubx64.efi] `PreLoader.efi` renamed =>[grubx64_real.efi] Linked to `Yours_x64.efi` =>[Yours_x64.efi]=>[Yours]