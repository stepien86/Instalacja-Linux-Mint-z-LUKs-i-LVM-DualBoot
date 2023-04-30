1. Uruchom system z nośnika Live Disk
2. Partycjonowanie dysków:
3. Dysk główny dla rozruchu (boot) i głównego (root)
   1. Utwórz podstawową partycję (FAT32) ~500MB (e.g. sda1) (dla EFI filesystem)
   2. Utwórz podstawową partycję (ext4) ~1GB (e.g. sda2) (boot dla partycji /boot)
   3. Utwórz partycję dla pozostałej powierzchni (e.g. sda3) (dla partycji /, /home, )
   4. Apply changes
   5. Ustaw flagę boot i esp dla pierwszej partycji (sda1)
