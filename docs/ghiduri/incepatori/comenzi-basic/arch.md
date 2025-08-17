# Arch (Pacman)

## Actualizare pachete
```bash
sudo pacman -Syu
```
## Căutare pachete
```bash
pacman -Ss nume-pachet
```
## Instalare aplicație (ex: Firefox)
```bash
sudo pacman -S firefox
```
## Ștergere aplicație
```bash
sudo pacman -R firefox
```

# [Arch User Repository (AUR)](https://aur.archlinux.org/) cu yay

⚠️ **Atenție:** Toate pachetele de pe AUR sunt create și încărcate de utilizatori.  
Nu sunt verificate oficial de echipa Arch, deci există riscul să conțină cod malițios.  
În practică, majoritatea (mai ales aplicațiile populare) sunt sigure, dar trebuie să fii atent.  

---

#### Cum verifici un pachet AUR

1. Intră pe pagina pachetului (ex: [Spotify](https://aur.archlinux.org/packages/spotify)).  
2. În partea dreaptă, apasă pe **[View PKGBUILD](https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=spotify)**.  
3. Se va deschide fișierul PKGBUILD – un script care arată exact ce face pachetul.  

Nu e nevoie să înțelegi tot codul, dar e important să verifici **link-urile** de unde descarcă fișierele.  

Exemplu:  
În cazul Spotify, vezi că descarcă de pe `http://repository.spotify.com` – domeniul oficial Spotify, deci e în regulă.  

---

#### Dacă nu ești sigur

Dacă nu poți decide singur dacă un PKGBUILD e sigur:  
- Poți copia tot codul din PKGBUILD și să îl analizezi cu un AI (ex: ChatGPT, Google Gemini).  
- Sau întrebi direct pe forumurile Arch/Reddit pentru confirmare.  

---

## Actualizare pachete
```bash
yay
```
## Căutare pachete
```bash
yay nume-pachet
```
## Instalare aplicație (ex: Firefox)
```bash
yay -S firefox
```
## Ștergere aplicație
```bash
yay -R firefox
```

### Despre yay

`yay` poate să instaleze nu doar pachete din **AUR**, ci și pachete oficiale din repo-urile Arch.  
Deci îl poți folosi ca manager unic, fără să mai combini comenzi cu `pacman`.  
