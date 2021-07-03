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

Kernel-fsync podmienia zainstalowany w systemie domyślny kernel. Jeśli chcesz tego uniknąć zapoznaj się z podpunktem b).
***

#### a) Instalacja
```
dnf copr enable sentry/kernel-fsync
dnf update --refresh
```
#### b) Wymuszenie aktualizacji kernel-fsync
Kernel fsync o dziwo posiada taką samą nazwę pakietu, co domyślny kernel w Fedorze. Po dodaniu repozytorium kernel-fsync i aktualizacjach systemu pakiety zaczną się podmieniać wzajemnie, przez co fsync może być niedostępny.

Aby naprawić tą sytuację wystarczy odnaleźć plik **/etc/yum.repos.d/fedora-updates.repo** i wyedytować jego zawartość.

Po jego otworzeniu, na przykład komendą:
```
sudo nano /etc/yum.repos.d/fedora-updates.repo
```
należy dopisać w każdej z sekcji (updates, updates-debuginfo oraz updates-source) opcję:e
```
exclude=kernel*
```

Po dopisaniu linii - zapisujemy i zamykamy plik.

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