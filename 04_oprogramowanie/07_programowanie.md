# 4.7 Programowanie

## Microsoft Visual Studio Code
Oprogramowanie dla programistów od firmy Microsoft.
### Instalacja przez dnf
Zaimportuj klucz:
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
```

Dodaj repozytorium:
```
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
```

Zainstaluj Visual Studio Code:
```
sudo dnf install code
```

### Instalacja przez Flatpak
```
flatpak install flathub com.visualstudio.code
```