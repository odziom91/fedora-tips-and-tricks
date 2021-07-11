# 10.2 Wyłączenie SELinux
W związku z problemami z QEMU/KVM oraz VirtualBox na kernelach xanmod oraz liquorix należy wyłączyć Security-Enhanced Linux (SELinux).
Aby tego dokonać należy uruchomić w edytorze tekstowym z uprawnieniami administratora plik jak poniżej:
```
sudo nano /etc/sysconfig/selinux
```
W pliku odnajdujemy linię:
```
SELINUX=enforcing
```
i zmienamy jej wartość na:
```
SELINUX=disabled
```
Po zmianach należy uruchomić ponownie system.

Po restarcie można sprawdzić status SELinux komendą:
```
sestatus
```
