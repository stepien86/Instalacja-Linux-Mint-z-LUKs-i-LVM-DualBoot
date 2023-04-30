1. Zaloguj się na konto root

```bash
sudo su -
```

2. Pobierz signed grub (opcjonalnie, jeżeli twoja wersja systemu Live nie posiada tego pakietu)

```bash
sudo apt install grub-efi-amd64-signed
```

3. Zamontuj boot oraz efi

```bash
mount /dev/sda2 /mnt
mkdir /mnt/boot
mkdir /mnt/boot/efi
mount /dev/sda1 /mnt/boot/efi
```

4. Zainstaluj grub

```bash
grub-install --uefi-secure-boot --recheck --no-floppy --root-directory=/ --boot-directory=/mnt/boot --efi-directory=/mnt/boot/efi /dev/sda
```

5. Reboot
