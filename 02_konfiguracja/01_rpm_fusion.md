# 2.1 Repozytorium RPM Fusion
Domyślnie Fedora korzysta z oprogramowania otwartoźródłowego (Open Source).
Aby móc instalować oprogramowanie / sterowniki niewolne należy dodać repozytorium RPM Fusion.

Komenda:
```
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

Po zatwierdzeniu zainstalowania pakietu można używać nowego repozytorium.
