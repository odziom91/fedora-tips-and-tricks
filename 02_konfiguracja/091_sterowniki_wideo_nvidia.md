# 2.9 Sterowniki karty graficznej - NVidia

Fedora jako domyślny sterownik wykorzystuje otwartoźródłowy Nouveau. Zalecane jest, aby zainstalować sterownik zamknięty od NVidia w celu znacznego wzrostu wydajności w systemie oraz w grach.
W tym celu należy dodać repozytorium RPM Fusion (opisane w rozdziale 2.3), a następnie wykorzystać jeden z poniższych zestawów komend.

***
<b style="color:red">WAŻNE!</b>

Secure Boot w BIOS/UEFI musi być <b style="color:red">wyłączony</b>!

Po zainstalowaniu sterowników należy <b style="color:red">odczekać do dwóch minut</b>, a następnie <b>uruchomić ponownie system</b>.

Przed instalacją sterownika <b style="color:red">SPRAWDŹ</b> listę obsługiwanych kart graficznych dla wybranej wersji sterownika!
W przypadku pomyłki pojawi się komunikat:
```
NVIDIA kernel module missing. Falling back to nouveau.
```
Gdy tylko system się uruchomi (graficznie lub w terminalu) podmień sterowniki na właściwe.
***

## NVidia - karty od serii 800 wzwyż + RTX
---
<details>
<summary><b>Lista kart graficznych w rozwinięciu</b></summary>
<b>NVIDIA TITAN Series:</b><br/>
NVIDIA TITAN RTX, NVIDIA TITAN V, NVIDIA TITAN Xp, NVIDIA TITAN X (Pascal), GeForce GTX TITAN X
<br/><br/>
<b>GeForce RTX 30 Series (Notebooks):</b><br/>
GeForce RTX 3080 Ti Laptop GPU, GeForce RTX 3080 Laptop GPU, GeForce RTX 3070 Ti Laptop GPU, GeForce RTX 3070 Laptop GPU, GeForce RTX 3060 Laptop GPU, GeForce RTX 3050 Ti Laptop GPU, GeForce RTX 3050 Laptop GPU
<br/><br/>
<b>GeForce RTX 30 Series:</b><br/>
GeForce RTX 3090, GeForce RTX 3080 Ti, GeForce RTX 3080, GeForce RTX 3070 Ti, GeForce RTX 3070, GeForce RTX 3060 Ti, GeForce RTX 3060, GeForce RTX 3050
<br/><br/>
<b>GeForce RTX 20 Series (Notebooks):</b><br/>
GeForce RTX 2080 SUPER, GeForce RTX 2080, GeForce RTX 2070 SUPER, GeForce RTX 2070, GeForce RTX 2060, GeForce RTX 2050
<br/><br/>
<b>GeForce RTX 20 Series:</b><br/>
GeForce RTX 2080 Ti, GeForce RTX 2080 SUPER, GeForce RTX 2080, GeForce RTX 2070 SUPER, GeForce RTX 2070, GeForce RTX 2060 SUPER, GeForce RTX 2060
<br/><br/>
<b>GeForce MX500 Series (Notebooks):</b><br/>
GeForce MX570, GeForce MX550
<br/><br/>
<b>GeForce MX400 Series (Notebooks):</b><br/>
GeForce MX450
<br/><br/>
<b>GeForce MX300 Series (Notebooks):</b><br/>
GeForce MX350, GeForce MX330
<br/><br/>
<b>GeForce MX200 Series (Notebooks):</b><br/>
GeForce MX250, GeForce MX230
<br/><br/>
<b>GeForce MX100 Series (Notebook):</b><br/>
GeForce MX150, GeForce MX130, GeForce MX110
<br/><br/>
<b>GeForce GTX 16 Series (Notebooks):</b><br/>
GeForce GTX 1660 Ti, GeForce GTX 1650 Ti, GeForce GTX 1650
<br/><br/>
<b>GeForce 16 Series:</b><br/>
GeForce GTX 1660 SUPER, GeForce GTX 1650 SUPER, GeForce GTX 1660 Ti, GeForce GTX 1660, GeForce GTX 1650
<br/><br/>
<b>GeForce 10 Series:</b><br/>
GeForce GTX 1080 Ti, GeForce GTX 1080, GeForce GTX 1070 Ti, GeForce GTX 1070, GeForce GTX 1060, GeForce GTX 1050 Ti, GeForce GTX 1050, GeForce GT 1030, GeForce GT 1010
<br/><br/>
<b>GeForce 10 Series (Notebooks):</b><br/>
GeForce GTX 1080, GeForce GTX 1070, GeForce GTX 1060, GeForce GTX 1050 Ti, GeForce GTX 1050
<br/><br/>
<b>GeForce 900 Series:</b><br/>
GeForce GTX 980 Ti, GeForce GTX 980, GeForce GTX 970, GeForce GTX 960, GeForce GTX 950
<br/><br/>
<b>GeForce 900M Series (Notebooks):</b><br/>
GeForce GTX 980, GeForce GTX 980M, GeForce GTX 970M, GeForce GTX 965M, GeForce GTX 960M, GeForce GTX 950M, GeForce 945M, GeForce 940MX, GeForce 930MX, GeForce 920MX, GeForce 940M, GeForce 930M
<br/><br/>
<b>GeForce 800M Series (Notebooks):</b><br/>
GeForce GTX 860M, GeForce GTX 850M, GeForce 845M, GeForce 840M, GeForce 830M
<br/><br/>
<b>NVIDIA RTX Series:</b><br/>
NVIDIA RTX A6000, NVIDIA RTX A5000, NVIDIA RTX A4500, NVIDIA RTX A4000, NVIDIA RTX A2000 12GB, NVIDIA RTX A2000, NVIDIA T1000 8GB, NVIDIA T1000, NVIDIA T600, NVIDIA T400 4GB, NVIDIA T400
<br/><br/>
<b>NVIDIA RTX Series (Notebooks):</b><br/>
NVIDIA RTX A5000 Laptop GPU, NVIDIA RTX A4000 Laptop GPU, NVIDIA RTX A3000 Laptop GPU, NVIDIA RTX A2000 Laptop GPU, NVIDIA T1200 Laptop GPU , NVIDIA T600 Laptop GPU, NVIDIA T500
<br/><br/>
<b>Quadro RTX Series:</b><br/>
Quadro RTX 8000, Quadro RTX 6000, Quadro RTX 5000, Quadro RTX 4000, Quadro RTX 3000
<br/><br/>
<b>Quadro RTX Series (Notebooks):</b><br/>
Quadro RTX 6000
<br/><br/>
<b>Quadro Series:</b><br/>
Quadro GV100, Quadro GP100, Quadro P6000, Quadro P5200, Quadro P5000, Quadro P4000, Quadro P2200, Quadro P2000, Quadro P1000, Quadro P620, Quadro P600, Quadro P400, Quadro M6000 24GB, Quadro M6000, Quadro M5000, Quadro M4000, Quadro M2000, Quadro K2200, Quadro K1200, Quadro K620
<br/><br/>
<b>Quadro Series (Notebooks):</b><br/>
Quadro T2000, Quadro T1000, Quadro P5200, Quadro P5000, Quadro P4200, Quadro P3200, Quadro P4000, Quadro P3000, Quadro P2000, Quadro P1000, Quadro P600, Quadro P520, Quadro P500, Quadro M2200, Quadro M1200, Quadro M620, Quadro M520, Quadro M5500, Quadro M5000M, Quadro M4000M, Quadro M3000M, Quadro M2000M, Quadro M1000M, Quadro M600M, Quadro M500M, Quadro K2200M, Quadro K620M
<br/><br/>
<b>Quadro Blade/Embedded Series:</b><br/>
Quadro P5000, Quadro P3000, Quadro M5000 SE, Quadro M3000 SE
<br/><br/>
<b>Quadro NVS Series:</b><br/>
NVS 810
<br/><br/>
</details>

---

```
sudo dnf update -y
sudo dnf install akmod-nvidia
sudo dnf install xorg-x11-drv-nvidia-cuda
```

## NVidia - seria 600/700
---
<details>
<summary><b>Lista kart graficznych w rozwinięciu</b></summary>
<b>GeForce 700 Series:</b><br/>
GeForce GTX 780 Ti, GeForce GTX 780, GeForce GTX 770, GeForce GTX 760, GeForce GTX 760 Ti (OEM), GeForce GTX 750 Ti, GeForce GTX 750, GeForce GTX 745, GeForce GT 740, GeForce GT 730, GeForce GT 720, GeForce GT 710
<br/><br/>
<b>GeForce 600 Series:</b><br/>
GeForce GTX 690, GeForce GTX 680, GeForce GTX 670, GeForce GTX 660 Ti, GeForce GTX 660, GeForce GTX 650 Ti BOOST, GeForce GTX 650 Ti, GeForce GTX 650, GeForce GTX 645, GeForce GT 640, GeForce GT 635, GeForce GT 630
<br/><br/>
<b>GeForce 600M Series (Notebooks):</b><br/>
GeForce GT 640M LE<br/><br/>
</details>

---

```
sudo dnf update -y
sudo dnf install xorg-x11-drv-nvidia-470xx akmod-nvidia-470xx
sudo dnf install xorg-x11-drv-nvidia-470xx-cuda
```

## NVidia - seria 400/500 oraz mobilne wersje serii 600
---
<details>
<summary><b>Lista kart graficznych w rozwinięciu</b></summary>
<b>GeForce 600M Series (Notebooks):</b><br/>
GeForce GTX 680MX, GeForce GTX 680M, GeForce GTX 675MX, GeForce GTX 675M, GeForce GTX 670MX, GeForce GTX 670M, GeForce GTX 660M, GeForce GT 650M, GeForce GT 645M, GeForce GT 640M, GeForce GT 640M LE, GeForce GT 635M, GeForce GT 630M, GeForce GT 625M, GeForce GT 620M, GeForce 610M
<br/><br/>
<b>GeForce 500 Series:</b><br/>
GeForce GTX 590, GeForce GTX 580, GeForce GTX 570, GeForce GTX 560 Ti, GeForce GTX 560 SE, GeForce GTX 560, GeForce GTX 555, GeForce GTX 550 Ti, GeForce GT 545, GeForce GT 530, GeForce GT 520, GeForce 510
<br/><br/>
<b>GeForce 500M Series (Notebooks):</b><br/>
GeForce GTX 580M, GeForce GTX 570M, GeForce GTX 560M, GeForce GT 555M, GeForce GT 550M, GeForce GT 540M, GeForce GT 525M, GeForce GT 520M, GeForce GT 520MX
<br/><br/>
<b>GeForce 400 Series:</b><br/>
GeForce GTX 480, GeForce GTX 470, GeForce GTX 465, GeForce GTX 460 SE v2, GeForce GTX 460 SE, GeForce GTX 460, GeForce GTS 450, GeForce GT 440, GeForce GT 430, GeForce GT 420
<br/><br/>
<b>GeForce 400M Series (Notebooks):</b><br/>
GeForce GTX 485M, GeForce GTX 480M, GeForce GTX 470M, GeForce GTX 460M, GeForce GT 445M, GeForce GT 435M, GeForce GT 425M, GeForce GT 420M, GeForce GT 415M, GeForce 410M
<br/><br/>
</details>

---

```
dnf update -y
sudo dnf install xorg-x11-drv-nvidia-390xx akmod-nvidia-390xx
sudo dnf install xorg-x11-drv-nvidia-390xx-cuda
```

## NVidia - stara seria 8000/9000 oraz nowsza 100/200/300
***
<b style="color:red">WAŻNE!<br/>
Karty nie są wspierane przez NVidię od 2019 roku. Poniższy sterownik może przestać działać z nowszymi wersjami kernela.
</b>
<details>
<summary><b>Lista kart graficznych w rozwinięciu</b></summary>
<b>GeForce 300 Series:</b><br/>
GeForce GT 340, GeForce GT 330, GeForce GT 320, GeForce 315, GeForce 310
<br/><br/>
<b>GeForce 300M Series (Notebooks):</b><br/>
GeForce GTS 360M, GeForce GTS 350M, GeForce GT 335M, GeForce GT 330M, GeForce GT 325M, GeForce GT 320M, GeForce 320M, GeForce 315M, GeForce 310M, GeForce 305M
<br/><br/>
<b>GeForce 200 Series:</b><br/>
GeForce GTX 295, GeForce GTX 285, GeForce GTX 280, GeForce GTX 275, GeForce GTX 260, GeForce GTS 250, GeForce GTS 240, GeForce GT 230, GeForce GT 240, GeForce GT 220, GeForce G210, GeForce 210, GeForce 205
<br/><br/>
<b>GeForce 200M Series (Notebooks):</b><br/>
GeForce GTX 285M, GeForce GTX 280M, GeForce GTX 260M, GeForce GTS 260M, GeForce GTS 250M, GeForce GT 240M, GeForce GT 230M, GeForce GT 220M, GeForce G210M, GeForce G205M
<br/><br/>
<b>GeForce 100 Series:</b><br/>
GeForce GT 140, GeForce GT 130, GeForce GT 120, GeForce G100
<br/><br/>
<b>GeForce 100M Series (Notebooks):</b><br/>
GeForce GTS 160M, GeForce GTS 150M, GeForce GT 130M, GeForce GT 120M, GeForce G 110M, GeForce G 105M, GeForce G 103M, GeForce G 102M
<br/><br/>
<b>GeForce 9000 Series:</b><br/>
GeForce 9800 GX2, GeForce 9800 GTX/GTX+, GeForce 9800 GT, GeForce 9600 GT, GeForce 9600 GSO, GeForce 9600 GSO 512, GeForce 9600 GS, GeForce 9500 GT, GeForce 9500 GS, GeForce 9400 GT, GeForce 9400, GeForce 9300 GS, GeForce 9300 GE, GeForce 9300 SE, GeForce 9300, GeForce 9200, GeForce 9100
<br/><br/>
<b>GeForce 9000M Series (Notebooks):</b><br/>
GeForce 9800M GTX, GeForce 9800M GTS, GeForce 9800M GT, GeForce 9800M GS, GeForce 9700M GTS, GeForce 9700M GT, GeForce 9650M GT, GeForce 9650M GS, GeForce 9600M GT, GeForce 9600M GS, GeForce 9500M GS, GeForce 9500M G, GeForce 9400M G, GeForce 9400M, GeForce 9300M GS, GeForce 9300M G, GeForce 9200M GS, GeForce 9100M G
<br/><br/>
<b>GeForce 8000 Series:</b><br/>
GeForce 8800 Ultra, GeForce 8800 GTX, GeForce 8800 GTS 512, GeForce 8800 GTS, GeForce 8800 GT, GeForce 8800 GS, GeForce 8600 GTS, GeForce 8600 GT, GeForce 8600 GS, GeForce 8500 GT, GeForce 8400 GS, GeForce 8400 SE, GeForce 8400, GeForce 8300 GS, GeForce 8300, GeForce 8200, GeForce 8100 /nForce 720a
<br/><br/>
<b>GeForce 8000M Series (Notebooks):</b><br/>
GeForce 8800M GTX, GeForce 8800M GTS, GeForce 8700M GT, GeForce 8600M GT, GeForce 8600M GS, GeForce 8400M GT, GeForce 8400M GS, GeForce 8400M G, GeForce 8200M G, GeForce 8200M
<br/><br/>
</details>

***
```
sudo dnf update -y
sudo dnf install xorg-x11-drv-nvidia-340xx akmod-nvidia-340xx
sudo dnf install xorg-x11-drv-nvidia-340xx-cuda
```

## Lista niewspieranych kart graficznych
Do poniższych kart graficznych nie jest możliwe zainstalowanie sterownika NVidia - należy skorzystać z domyślnego, otwartoźródłowego Nouveau.
***
<b>GeForce 7000 Series:</b><br/>
GeForce 7025 / NVIDIA nForce 630a, GeForce 7050 PV / NVIDIA nForce 630a, GeForce 7050 / NVIDIA nForce 610i, GeForce 7050 / NVIDIA nForce 630i, GeForce 7100 / NVIDIA nForce 630i, GeForce 7100 / NVIDIA nForce 620i, GeForce 7100 GS, GeForce 7150 / NVIDIA nForce 630i, GeForce 7300 SE / 7200 GS, GeForce 7300 LE, GeForce 7300 GS, GeForce 7300 GT, GeForce 7350 LE, GeForce 7500 LE, GeForce 7550 LE, GeForce 7600 LE, GeForce 7600 GS, GeForce 7600 GT, GeForce 7650 GS, GeForce 7800 GS, GeForce 7800 GTX, GeForce 7800 SLI, GeForce 7900 GS, GeForce 7900 GT/GTO, GeForce 7900 GTX, GeForce 7950 GT, GeForce 7950 GX2

<b>GeForce 6000 Series:</b><br/>
GeForce 6100, GeForce 6100 nForce 400, GeForce 6100 nForce 405, GeForce 6100 nForce 420, GeForce 6150, GeForce 6150 LE, GeForce 6150LE / Quadro NVS 210S , GeForce 6150SE nForce 430, GeForce 6200, GeForce 6200 A-LE, GeForce 6200 LE, GeForce 6200 TurboCache(TM), GeForce 6200SE TurboCache(TM), GeForce 6250, GeForce 6500, GeForce 6600, GeForce 6600 GT, GeForce 6600 LE, GeForce 6600 VE, GeForce 6610 XL, GeForce 6700 XL, GeForce 6800, GeForce 6800 GS, GeForce 6800 GS/XT, GeForce 6800 GT, GeForce 6800 LE, GeForce 6800 Ultra, GeForce 6800 XE, GeForce 6800 XT

<b>GeForce 5000 FX Series:</b><br/>
GeForce FX 5100, GeForce FX 5200, GeForce FX 5200 Ultra, GeForce FX 5200LE, GeForce FX 5500, GeForce FX 5600, GeForce FX 5600 Ultra, GeForce FX 5600XT, GeForce FX 5700, GeForce FX 5700 Ultra, GeForce FX 5700LE, GeForce FX 5700VE, GeForce FX 5800, GeForce FX 5800 Ultra, GeForce FX 5900, GeForce FX 5900 Ultra, GeForce FX 5900XT, GeForce FX 5900ZT, GeForce FX 5950 Ultra, GeForce PCX 5300, GeForce PCX 5750, GeForce PCX 5900
***
