1. Uruchom instalator systemu Mint
2. Wybierz inne rozwiązanie dla instalacji
3. Ustaw "/dev/mapper/datavg-homelv"  
   System plików: ext4  
   Punkt montowania /home  
   Format: on (jeżeli wybierzesz off nic się nie stanie)
4. Set "/dev/mapper/systemvg-rootlv"  
   System plików:: ext4  
   Punkt montowania: /  
   Format: on (jeżeli wybierzesz off nic się nie stanie)
5. Set "dev/sda2"  
   System plików: ext4  
   Punkt montowania: /boot  
   **Format: off**
6. Wybierz urządzenie dla instalacji bootloadera:  
   /dev/sda (bez numeru, ponieważ należy wskazać dysk a nie partycję)
7. Zainstaluj  
   Zignoruj ostrzeżenie z powodu brakującej flagi formatu dla partycji startowej
8. Po zakończeniu instalacji "Kontynuuj testowanie"  
   **NIE RESTARTUJ!!!**
