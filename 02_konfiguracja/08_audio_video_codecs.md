# Kodeki audio/wideo

W przypadku problemów z wyświetlaniem obrazu, zdjęć lub dźwięku w aplikacjach, czy grach istnieje prawdopodobieństwo, iż brakuje w systemie bibliotek (kodeków). Aby poprawić błąd możesz skorzystać z komend poniżej.

## Instalacja wtyczek GStreamer
Ta paczka naprawia większość błędów z dźwiękiem i obrazem.
```
sudo dnf install gstreamer1-plugins-{bad-\*,good-\*,base} gstreamer1-plugin-openh264 gstreamer1-libav --exclude=gstreamer1-plugins-bad-free-devel
```

## Instalacja Lame
Ta paczka doinstaluje Lame. Niektóre programy enkodujące/dekodujące wymagają jej do zapisu/odczytu plików MP3.
```
sudo dnf install lame\* --exclude=lame-devel
```

## Aktualizacja grupy Multimedia
```
sudo dnf group upgrade --with-optional Multimedia
```