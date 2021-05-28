# 3.2 Vulkan

## Czym jest Vulkan?
Vulkan jest niskopoziomowym, wieloplatformowym interfejsem programowania aplikacji, który ma na celu wspomagać tworzenie grafiki 3D.
Podobnie jak w przypadku OpenGL, Vulkan wspiera aplikacje 3D takie jak, np.: gry komputerowe.
Środowisko to oferuje większą kontrolę nad kartą graficzną i niższe obciążenie procesora graficznego przy tych samych zadaniach co OpenGL.

## Lista obsługiwanych kart graficznych
NVidia: [https://developer.nvidia.com/vulkan-driver](https://developer.nvidia.com/vulkan-driver)

AMD: [https://www.amd.com/en/technologies/vulkan](https://www.amd.com/en/technologies/vulkan)

Intel: [https://www.intel.pl/content/www/pl/pl/support/articles/000005524/graphics.html](https://www.intel.pl/content/www/pl/pl/support/articles/000005524/graphics.html)

## Instalacja Vulkan
Obsługa Vulkan powinna być instalowana automatycznie wraz z instalacją sterownika wideo.
Jeśli jednak brakuje odpowiednich pakietów w systemie wykonaj poniższą komendę i uruchom ponownie system:
```
sudo dnf install vulkan
```