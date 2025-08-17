# [Flatpak](https://flatpak.org/setup/)

Flatpak nu vine de obicei preinstalat și trebuie instalat manual, în funcție de distribuția pe care o folosești (găsești pașii [aici](https://flatpak.org/setup/)).  
După ce este configurat, majoritatea aplicațiilor pot fi instalate direct din [Flathub](https://flathub.org/), care este cel mai popular depozit Flatpak.  

## Actualizare pachete
```bash
flatpak update
```
## Căutare pachete
```bash
flatpak search nume-aplicatie
```
## Instalare aplicație (ex: Firefox)
```bash
flatpak install flathub org.mozilla.firefox
```
## Ștergere aplicație
```bash
flatpak uninstall org.mozilla.firefox
```

# [Snap](https://snapcraft.io/)

Snap este dezvoltat de Canonical (Ubuntu) și vine preinstalat în Ubuntu.
Pe alte distribuții trebuie instalat manual (instrucțiuni [aici](https://snapcraft.io/docs/installing-snapd).
Aplicațiile Snap se găsesc în [Snap Store](https://snapcraft.io/store).

## Actualizare pachete
```bash
sudo snap refresh
```
## Căutare pachete
```bash
snap find nume-aplicatie
```
## Instalare aplicație (ex: Firefox)
```bash
sudo snap install firefox
```
## Ștergere aplicație
```bash
sudo snap remove firefox
```

# [AppImage](https://appimage.org/)

AppImage este un format portabil: fiecare aplicație vine într-un singur fișier executabil.  
Nu necesită instalare, nu are manager centralizat și nici sistem de update automat.  
Fișierul îl descarci de pe site-ul oficial al aplicației și îl rulezi direct.  

## Pregătire fișier AppImage
După descărcare, trebuie să îi dai permisiuni de execuție:  

```bash
chmod +x aplicatie.AppImage
```
În majoritatea distribuțiilor poți face asta și din interfața grafică:
click dreapta → Properties → Permissions → Run file as executable.

## Rulare aplicație
```bash
./aplicatie.AppImage
```
Sau pur și simplu dublu click pe fișier pentru a-l rula.
