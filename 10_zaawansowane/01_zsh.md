# 10.1 zsh
zsh jest jedną z wielu powłók systemowych nadającą się do interaktywnej pracy z systemem, jak również do wykonywania skryptów.

## Instalacja zsh
Aby zainstalować powłokę zsh należy użyć komendy:
```
sudo dnf install zsh
```
Po zainstalowaniu zsh należy ustawić go jako główną powłokę systemową:
```
chsh -s $(which zsh)
```
Po zmianie powłoki należy się wylogować i zalogować ponownie do swojego konta lub uruchomić ponownie system.

## oh-my-zsh
W celu ułatwienia konfiguracji powłoki zsh i rozszerzenia funkcjonalności warto zainstalować oh-my-zsh.

Zalety oh-my-zsh:
- około 300 dostępnych pluginów
- ponad 140 motywów
- automatyczna, niezależna od systemu aktualizacja oh-my-zsh

Przed rozpoczęciem instalacji upewnij się, że masz zainstalowany pakiet ```git``` - jeśli go nie masz zainstaluj komendą:

```
sudo dnf install git
```

Instalacja oh-my-zsh przy pomocy skyptu:
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Modyfikacja konfiguracji odbywa się przy pomocy pliku .zshrc, który znajduje się w katalogu domowym użytkownika.
***
UWAGA!

Plik .zshrc jest plikiem ukrytym.
***
Aby rozpocząć konfigurację pliku wydaj polecenie:
```
nano ~/.zshrc
```
Najważniejsze zmienne:
- wybór motywu:
```
ZSH_THEME="robbyrussell"
```
Lista motywów dostępna jest [tutaj](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes).
- wybór pluginów:
```
plugins=(git)
```
Pluginy wypisuje się w nawiasie, każdy oddzielony spacją.

Lista pluginów dostępna jest [tutaj](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins).
- automatyczna aktualizacja (bez zapytania)
```
DISABLE_UPDATE_PROMPT=true
```
- wyłączenie automatycznych aktualizacji
```
DISABLE_AUTO_UPDATE=true
```
W przypadku wyłączenia automatycznych aktualizacji można je wykonać samodzielnie wykonując polecenie
```
omz update
```

Więcej informacji o dodatku oh-my-zsh - [https://github.com/ohmyzsh/ohmyzsh](https://github.com/ohmyzsh/ohmyzsh)