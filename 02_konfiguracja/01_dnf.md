# 2.1 dnf - obsługa menedżera pakietów w konsoli

## O dnf słów kilka
Każda dystrybucja systemu Linux posiada **menedżer pakietów**, który umożliwia instalację oprogramowania z tak zwanych **"repozytoriów"**.
Repozytoria to nic innego jak **"zbiór oprogramowania"**, który znajduje się na serwerach.

W Fedorze domyślnym menedżerem pakietów, dostępnym na tym systemie jest **dnf** - nazywany również jako "**d**a**n**di**f**ied yum", gdyż jest następną generacją menedżera pakietów **yum** istniejącego w Fedorze **do wersji 22**.

## Podstawowa obsługa dnf
Działanie menedżera pakietów dnf opiera się na wydawaniu komend w konsoli. Nie jest to trudne, a poniższa ściąga umożliwi szybkie wdrożenie.

Lista najczęściej używanych komend (jeśli nie jesteś zalogowany na koncie root, a jesteś administratorem - każdą należy poprzedzić komendą **sudo**):
- wyszukanie oprogramowania
```
dnf search <fraza/pakiet>
```
- instalacja oprogramowania
```
dnf install <nazwa pakietu>
```
- reinstalacja oprogramowania
```
dnf reinstall <nazwa pakietu>
```
- aktualizacja systemu
```
dnf upgrade
``` 
lub
```
dnf update
```
- usuwanie oprogramowania (z zależnościami lub bez, w zależności od konfiguracji dnf)
```
dnf remove <nazwa pakietu>
```
- usuwanie niepotrzebnych zależności
```
dnf autoremove
```
- czyszczenie pamięci podręcznej
```
dnf clean
```
- informacje o pakiecie
```
dnf info <pakiet>
```
