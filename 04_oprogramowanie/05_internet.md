## 4.5 Oprogramowanie internetowe

## Firefox
Przeglądarka internetowa oparta o otwartym kodzie źródłowym na silniku Gecko.
```
sudo dnf install firefox
```
## Opera
Darmowa przeglądarka internetowa na licencji freeware, tworzona i rozwijana przez norweską firmę Opera Software ASA. 

Aby zainstalować przeglądarkę należy dodać repozytorium:
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
## Thunderbird
Klient poczty elektronicznej oparty o otwartym kodzie źródłowym.
```
sudo dnf install thunderbird
```