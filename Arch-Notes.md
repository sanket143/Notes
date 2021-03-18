# Arch Linux Notes
fdisk /dev/sda
: g -> for GTP

EFI partition 500M
mkfs.fat - F32 /dev/sda1

Linux System 200G
mkfs.ext4 /dev/sda2

Linux System REST
mkfs.ext4 /dev/sda3

mount whichever to whichever
mount /dev/sda2 /mnt/root
mount /dev/sda3 /mnt/home

genfstab -U -p /mnt >> /mnt/etc/fstab

pacstrap -i /mnt base base-devel linux linux-firmware neovim openssh networkmanager 
systemctl enable NetworkManager

locale.gen en_US
```bash
$ locale-gen
$ passwd
$ useradd -m -g users -G wheel sanket143
$ passwd sanket143
$ pacman -S sudo
$ visudo # uncomment WHEEL
$ pacman -S grub efibootmgr dosfstools os-prober mtools
$ mkdir /boot/EFI
$ mount /dev/sda1 /boot/EFI
-- GRUB
$ grub-install --target=x86_64-efi --bootloader-id=grub_uefi --recheck
$ mkdir /boot/grub/locale
$ cp /usr/share/locale/en\@quot/LC_MESSAGES/grub.mo /boot/grub/locale/en.mo

$ grub-mkconfig -o /boot/grub/grub.cfg
$ reboot
```

