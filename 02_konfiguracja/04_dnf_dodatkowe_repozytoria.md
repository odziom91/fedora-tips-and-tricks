# 2.4 dnf - dodatkowe repozytoria

W tym rozdziale znajdziesz opcjonalne repozytoria dla oprogramowania niedostępnego w oficjalnym repozytorium i RPM Fusion.

## Opera
```
sudo tee /etc/yum.repos.d/opera.repo <<RPMREPO
[opera]
name=Opera packages
type=rpm-md
baseurl=https://rpm.opera.com/rpm
gpgcheck=1
gpgkey=https://rpm.opera.com/rpmrepo.key
enabled=1
RPMREPO
```
Instalacja wersji stabilnej:
```
sudo dnf install opera-stable
```
Instalacja wersji deweloperskiej:
```
sudo dnf install opera-developer
```

## Microsoft Edge

Zaimportuj klucz:
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
```

Dodaj repozytorium:
```
sudo dnf config-manager --add-repo https://packages.microsoft.com/yumrepos/edge
```

Zaktualizuj repozytoria:
```
sudo dnf update
```

Zainstaluj przeglądarkę - dostępna jest w trzech wersjach:

a) wersja stabilna
```
sudo dnf install microsoft-edge-stable
```

b) wersja beta
```
sudo dnf install microsoft-edge-beta
```

c) wersja deweloperska
```
sudo dnf install microsoft-edge-dev
```

## Microsoft Teams

Zaimportuj klucz:
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
```

Dodaj repozytorium:
```
sudo tee /etc/yum.repos.d/ms-teams.repo << 'EOL'
[teams]
name=teams
baseurl=https://packages.microsoft.com/yumrepos/ms-teams
enabled=1
gpgcheck=1
gpgkey=https://packages.microsoft.com/keys/microsoft.asc
EOL
```

Zaktualizuj repozytoria:
```
sudo dnf update
```

Zainstaluj Teams:
```
sudo dnf install teams
```

## Microsoft Visual Studio Code

Zaimportuj klucz:
```
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
```

Dodaj repozytorium:
```
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
```

Zaktualizuj repozytoria:
```
sudo dnf update
```

Zainstaluj Visual Studio Code:
```
sudo dnf install code
```

## Microsoft Skype
Dodaj repozytorium:
```
sudo curl -o /etc/yum.repos.d/skype-stable.repo https://repo.skype.com/rpm/stable/skype-stable.repo
```
Zainstaluj Skype for Linux:
```
sudo dnf install skypeforlinux
```