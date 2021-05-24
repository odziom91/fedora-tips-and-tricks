# 2.2 dnf - konfiguracja menedżera pakietów
Menedżer pakietów dnf może zostać skonfigurowany do własnych preferencji.
Dodatkowa konfiguracja pomoże w zoptymalizowaniu pobierania plików i znacznie ułatwi pracę.

Plik konfiguracyjny znajduje się w lokalizacji:
```
/etc/dnf/dnf.conf
```

Aby przejść do jego edycji możesz wykorzystać dowolny edytor - uruchomiony z prawami administratora:
```
sudo nano /etc/dnf/dnf.conf
```

Poniżej znajdziesz opcje, które warto dodać do pliku konfiguracyjnego:
- Limit instalacji pakietów
```
installonly_limit=2
```
- automatyczne usuwanie zależności
```
clean_requirements_on_remove=True
```
- domyślne wybór "T" - zatwierdzanie instalacji przyciskiem Enter
```
defaultyes=True
```
- optymalizacja pobierania pakietów:
```
deltarpm=False
metadata_timer_sync=3600
max_parallel_downloads=10
ip_resolve=4
```

Po wprowadzeniu zmian pamiętaj o zapisaniu pliku!