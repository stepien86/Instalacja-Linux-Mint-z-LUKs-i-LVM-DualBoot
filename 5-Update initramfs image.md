1. Zaloguj na konto root

```bash
sudo su -
```

2. chroot nowej instalacji

```bash
mount /dev/systemvg/rootlv /target
mount /dev/sda2 /target/boot
mount -o bind /proc /target/proc
mount -o bind /dev /target/dev
mount -o bind /sys /target/sys
chroot /target
```

3. Wskaż używaną przez Ciebie szyfrowaną partycję

```bash
blkid /dev/sda4
```

Ważny jest dla Ciebie UUID partycji!

```bash

echo sda4_crypt UUID=aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee none luks > /etc/crypttab
update-initramfs -k all -c
```

4. Exit chroot
5. Reboot
