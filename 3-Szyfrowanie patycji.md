1. Uruchom system z nośnika Live disk
2. Tworzenie szyfrowanej partycji i otworzenie jej

```bash
cryptsetup luksFormat /dev/sda4
cryptsetup luksOpen /dev/sda4 sda4_crypt

```

3. Tworzenie grupy woluminów i logicznych woluminów: (w tej instrukcji system jest na dwóch partycjach: / - główna, /home, bez partycji SWAP)

```bash
vgcreate systemvg /dev/mapper/sda4_crypt
lvcreate -n rootlv -L60G systemvg
lvcreate -n homelv -l100%FREE systemvg
```

**NIE URUCHAMIAJ PONOWNIE !!!**
