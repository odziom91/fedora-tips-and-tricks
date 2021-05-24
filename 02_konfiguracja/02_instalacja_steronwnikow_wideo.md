# 2.2 Sterowniki karty graficznej

## 2.2.1 NVidia
Fedora jako domyślny sterownik wykorzystuje otwartoźródłowy Nouveau. Zalecane jest, aby zainstalować sterownik zamknięty od NVidia w celu znacznego wzrostu wydajności w systemie oraz w grach.
W tym celu należy dodać repozytorium RPM Fusion (opisane w rozdziale 2.1), a następnie wykorzystać jeden z poniższych zestawów komend.

UWAGA!
Secure Boot w BIOS/UEFI musi być wyłączony!

UWAGA!
Karty z serii 6/7/5 (FX series)/4/3/2 nie są obsługiwane!

### NVidia (karty wydane po 2012 roku)
sudo dnf update -y

sudo dnf install akmod-nvidia

sudo dnf install xorg-x11-drv-nvidia-cuda

### NVidia - seria 400/500 (karty wydane w latach 2010 - 2012)
dnf update -y

sudo dnf install xorg-x11-drv-nvidia-390xx akmod-nvidia-390xx

sudo dnf install xorg-x11-drv-nvidia-390xx-cuda #optional for cuda up to 9.2 support

### NVidia - seria 8/9/200/300 (uwaga! karty nie są wspierane przez NVidię od 2019 roku!)
sudo dnf update -y

sudo dnf install xorg-x11-drv-nvidia-340xx akmod-nvidia-340xx

sudo dnf install xorg-x11-drv-nvidia-340xx-cuda #optional for cuda up to 6.5 support


Po zainstalowaniu sterowników należy odczekać do dwóch minut, a następnie uruchomić ponownie system.
