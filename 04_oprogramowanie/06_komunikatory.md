# 4.6 Komunikatory internetowe

## Discord
Popularny komunikator tekstowo-głosowy dla graczy (i nie tylko).
```
sudo dnf install discord
```
## Microsoft Teams
Komunikator dla szkół i firm od firmy Microsoft.

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

Zainstaluj Teams:
```
sudo dnf install teams
```