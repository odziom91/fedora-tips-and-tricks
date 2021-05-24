# 2.5 fstab - obsługa montowania dysków

Montowanie partycji na dyskach twardych odbywa się przy pomocy pliku fstab.
```
/etc/fstab
```
Aby dodać własny wpis należy wykonać kilka kroków.
### Wyciąganie UUID
UUID jest potrzebne do identyfikacji dysków.

Aby wypisać listę partycji na dyskach użyj komendy:
```
lsblk
```
Aby wypisać rozpiskę identyfikatorów dysków i partycji użyj:
```
sudo blkid
```

### Utworzenie katalogów do zamontowania dysków:
Utwórz katalogi poleceniem:
```
sudo mkdir -p /mnt/<twoj_nowy_folder>
```
## Edycja fstab
Aby wyedytować plik z punktami montowania należy użyć edytora tekstu z uprawnieniami administratora:
```
sudo nano /etc/fstab
```

### Wpis konfiguracyjny dla EXT4:
```
UUID=<UUID_partycji> /mnt/<twój_punkt_montowania>    ext4    defaults        0 2
```

### Wpis konfiguracyjny dla NTFS:
```
UUID=<UUID_partycji> /mnt/<twój_punkt_montowania>	    ntfs-3g defaults	0	0
```

Po zapisaniu pliku punkty montowania można odświeżyć przy pomocy komendy:
```
sudo mount -a
```
