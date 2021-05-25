# 3.8 Gamemode
Gamemode jest oprogramowaniem przeznaczonym do optymalizacji działania gier w Linux.

## Instalacja
Zainstalowanie gamemode odbywa się przy pomocy komendy:
```
sudo dnf install gamemode
```

Lutris w Fedorze instaluje to oprogramowanie automatycznie jako jedną z zależności.

## Jak to działa?
Jeśli chcesz uruchomić grę z optymalizacją gamemode dopisz do komendy uruchomieniowej frazę gamemoderun.

Przykłady:
```
gamemoderun ./game
```
```
gamemoderun wine ~/gry/gra/gra.exe
```

## Gamemode i Steam
Aby uruchomić grę ze Steam z obsługą gamemode należy wejść w ustawienia uruchamianej gry i dopisać w opcjach uruchamiania:
```
gamemoderun %command%
```

## Gamemode i Lutris
Gamemode może być używany w Lutrisie. Jeśli chcesz go uruchomić - przejdź do opcji gry lub runnera, który ma obsługiwać gamemode. W zakładce **"System Options"** zaznacz opcję **"Enable Feral GameMode"**. Zapisz zmiany i uruchom grę.