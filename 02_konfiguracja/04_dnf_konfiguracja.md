# 2.4 dnf - konfiguracja menedżera pakietów

Umiejscowienie pliku konfiguracyjnego:
```/etc/dnf/dnf.conf```

Opcje, które warto dodać do pliku konfiguracyjnego:
```installonly_limit=2``` przydatne przy instalacji kerneli, stare kernele zostaną automatycznie usuwane
```clean_requirements_on_remove=True``` usuwa zależności, które są przypisane do zainstalowanego pakietu
Przyspieszenie działania - dodaj poniższe linie:
```
deltarpm=False
metadata_timer_sync=3600
max_parallel_downloads=10
ip_resolve=4
```
```defaultyes=True``` - domyślny wybór "T" lub "Y" - umożliwia zatwierdzanie instalacji pakietów przyciskiem Enter
