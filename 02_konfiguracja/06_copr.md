# 2.6 - Copr - oprogramowanie od społeczności

***
**UWAGA!**

Jeśli jesteś początkującym użytkownikiem Fedory **ODRADZAMY** instalację oprogramowania z Copr. W przypadku braków oprogramowania w dnf skorzystaj z bezpieczniejszego **Flatpaka**. Używanie Copr powinno być **ostatecznością** i tylko w przypadku, gdy **WIESZ, CO ROBISZ**!
***

## O Copr słów kilka
Zdarza się, iż po zainstalowaniu dostępnych repozytoriów mimo wszystko pewne oprogramowanie jest niedostępne. Są to między innymi - niestandardowe kernele, czy oprogramowanie kompilowane ze źródeł, które nie posiadają paczek RPM.
W tym celu można użyć Copr - prostego w obsłudze systemu budowy pakietów, prowadzonego przez społeczność Fedory. Z punktu widzenia użytkownika systemu, to zbiór mini-repozytoriów, które można dodać do systemu, uzyskując dostęp do dodatkowego oprogramowania.

Wbrew prostoty należy zwrócić uwagę na zagrożenia, które mogą wynikać z używania Copr.

## Dlaczego **nie zaleca się** używania Copr?
- Copr **nie jest** oficjalnie wspierany przez Fedorę.
- Copr zawiera oprogramowanie udostępnianie przez społeczność - przez co **mogą pojawiać się błędy**.
- Copr posiada pakiety, które mogą **mocno ingerować w system operacyjny**, co w **katastrofalnym** skutku może go **unieruchomić**.

## Jak korzystać z Copr z poziomu konsoli?
Obsługa Copr dostępna jest z poziomu menedżera pakietów dnf, a składnia jest bardzo podobna. Zasadniczą róznicą między standardową instalacją pakietów jest to, że należy najpierw wyszukać repozytorium, a następnie je aktywować.

Oto lista komend, które są najczęściej używane:
- wyszukiwanie frazy:
```
dnf copr search <fraza>
```
- dodanie repozytorium od wskazanego użytkownika
```
dnf copr enable <user\repozytorium>
```
- usunięcie repozytorium od wskazanego użytkownika
```
dnf copr disable <user\repozytorium>
```

Pozostałe komendy są identyczne jak w dnf - patrz rozdział 2.1.