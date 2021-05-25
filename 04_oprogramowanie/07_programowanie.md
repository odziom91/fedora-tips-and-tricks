# 4.7 Programowanie

## Microsoft Visual Studio Code
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