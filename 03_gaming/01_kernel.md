# 3.1 Niestandardowy Kernel
Instalacja niestandardowego kernela w systemie **nie jest obowiązkowa**. Domyślny zawiera zaimplementowany patch esync, który znacząco zwiększa wydajność w grach. Jeśli jednak potrzebujesz wyższej wydajności, bądź chcesz uruchomić grę, która **wymaga dodatkowych patchy**, można zainstalować jeden z poniższych.

***
UWAGA!

Instalujesz na własną odpowiedzialność! Koniecznie zapoznaj się z uwagami przed instalacją kernela w Fedorze!
***

## Dostępne Kernele
### kernel-fsync
Zawiera patche:
- esync
- fsync
- futex2
- zen
***
UWAGA! 

Kernel-fsync podmienia zainstalowany w systemie domyślny kernel.
***

```
dnf copr enable sentry/kernel-fsync
dnf update --refresh
```

### xanmod
Zawiera patche:
- esync
- fsync
- futex2
***
UWAGA! 

Występują problemy z działaniem KVM (wirtualna karta sieciowa). Jeśli potrzebujesz wirtualizacje systemów NIE instaluj tego kernela.
***
```
sudo dnf copr enable rmnscnce/kernel-xanmod
sudo dnf install kernel-xanmod-edge
```

### liquorix
Zawiera patche:
- esync
- fsync
- futex2
***
UWAGA! 

Występują problemy z działaniem KVM oraz VirtualBox (brak modułów). Jeśli potrzebujesz wirtualizacje systemów NIE instaluj tego kernela.
***
```
sudo dnf copr enable rmnscnce/kernel-lqx
sudo dnf in kernel-lqx kernel-lqx-devel kernel-lqx-headers
```