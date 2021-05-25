# 3.9 Obsługa padów

## XBox Series Wireless Controller
Otwartoźródłowe sterowniki dla kontrolerów XBox Series Wireless Controller.
### xpadneo
1. Zainstaluj pakiety dkms oraz git:
```
sudo dnf install dkms git
```
2. Pobierz pliki z repozytorium xpadneo:
```
git clone https://github.com/atar-axis/xpadneo.git
```
3. Przejdź do katalogu xpadneo:
```
cd xpadneo
```
4. Uruchom plik install.sh z uprawnieniami administratora:
```
sudo ./install.sh
```
5. Po instalacji zrestartuj system.