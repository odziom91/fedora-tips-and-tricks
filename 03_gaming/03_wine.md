# 3.3 Wine

## Czym jest Wine?

![Wine](./gfx/wine_1.png)

Wine to oprogramowanie umożliwiające uruchamianie aplikacji tworzonych z myślą o systemie Windows w systemie Linux. Wine **NIE JEST** emulatorem a powłoką systemową (stąd nazwa od pierwszych liter sentencji - **W**ine **I**s **N**ot an **E**mulator). Jest to zaleta, gdyż w przypadku programów emulowanych zdarzają się spadki wydajności lub błędy oraz nadmierne wykorzystanie pamięci, a powłoka systemowa umożlwia zachowanie aplikacji identycznie jak w środowisku natywnym systemu Windows.

Rozwój oprogramowania Wine w ostatnich latach znacznie przyspieszył, dzięki czemu znacznie powiększyła się baza uruchamianych aplikacji systemu Windows.

## Zanim zaczniemy...
Należy mieć na uwadze fakt, iż obsługa oprogramowania dla systemu Windows wygląda trochę inaczej pod systemem Linux. Czasami wymaga ona interwencji ze strony użytkownika. Nie mniej jednak warto posiąść wiedzę z obsługi tej powłoki.

W przypadku gier komputerowych obsługa jest znacznie prostsza od tego, co znajduje się w poniższym opisie. Istnieje mnóstwo aplikacji, które ułatwiają instalację i uruchamianie oprogramowania spod Windows, a do nich można zaliczyć:
```
- Lutris
- GameHub
- PlayOnLinux
- Bottles
- Q4wine
```

Warto też wspomieć, że Valve wraz z platformą Steam umożlwiają uruchomienie gier wprost z biblioteki z wykorzystaniem Proton.

A jeśli to jeszcze mało, powstają środowiska uruchomieniowe dla innych launcherów jak na przykład Epic Games Store - Heroic Games Launcher.

## Jak zainstalować Wine?
Aby zainstalować Wine wraz z wymaganymi zależnościami wykonaj polecenie:
```
sudo dnf install wine
```

Dodatkowo zalecana jest instalacja dodatkowego oprogramowania Winetricks - do zarządzania prefixami (nazywanymi również "butelkami" - nawiązanie do butelek wina ;) ):
```
sudo dnf install winetricks
```

## Jak posługiwać się Wine?

### Sposób najprostszy
Najprostszym sposobem na uruchomienie aplikacji stworzonej dla systemu Windows jest użycie komendy, która uruchomi program w domyślnym prefixie w katalogu domowym:
```
wine nazwa_pliku.exe
```
Większość środowisk graficznych umożliwia również uruchamianie plików wykonywalnych przez podwójne kliknięcie na plik .exe - jak w Windowsie!

### Prefix (aka "butelka")

Wykonanie domyślnej akcji utworzy prefix, który znajdziemy w katalogu domowym użytkownika:
```
~/.wine
```
Gdy wejdziemy do katalogu (domyślnie jest on ukryty) zobaczymy reprezentację plików i katalogów, które odzwierciedlają system operacyjny Windows, czyli:
```
katalog: drive_c - będący odzwierciedleniem dysku C: systemu Windows

katalog: dosdevices - zawierający linki symboliczne do dysków systemowych oraz urządzeń systemowych (na przykład portów szeregowych)

pliki: system.reg, user.reg, userdef.reg - będące odzwierciedleniem rejestru systemowego Windows.
```
Powyższa informacja przyda się w przypadku, gdy będziemy potrzebowali wyedytować jakiś plik lub ustawienie.

### Uruchamianie aplikacji w innym prefixie
Aby uruchomić aplikację z wykorzystaniem innego prefixu należy poprzedzić komendę ```wine``` zmienną ```WINEPREFIX```.

Przykład uruchomienia instalatora aplikacji z użyciem prefixu w katalogu ```/home/odziom/moj_prefix```:
```
WINEPREFIX="/home/odziom/moj_prefix" wine setup.exe
```
W przypadku gdy instalowane jest oprogramowanie dla systemu Windows, program instalacyjny doda odpowienie wpisy w "Menu Start". Wine doda je również do menu systemu Windows (w sekcji Wine). Dzięki temu późniejsze uruchomienie aplikacji jest znacznie prostsze i ogranicza się do kilku kliknięć menu systemowego.

