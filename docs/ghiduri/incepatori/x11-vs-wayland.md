# X11 vs Wayland

Pe Linux, interfața grafică are nevoie de un protocol care să facă legătura între aplicații și serverul grafic.  
Mult timp standardul a fost **X11** (X.Org Server), dar în prezent direcția este trecerea la **Wayland**.  

---

## X11 (X.Org)

- Lansat în anii ’80 și folosit ca standard principal timp de decenii.  
- Arhitectură complicată, cu multe extensii adăugate în timp.  
- Puncte forte: compatibilitate excelentă cu aproape toate aplicațiile.  
- Probleme majore:  
  - lipsă de izolare între aplicații (oricare poate accesa informații din altă fereastră),   
  - performanță limitată pe hardware și funcții moderne.  

---

## Wayland

- Creat ca înlocuitor simplificat și modern pentru X11.  
- Aplicațiile comunică direct cu compositorul grafic → latență mai mică, securitate mai bună.  
- Suport mai bun pentru tehnologii noi: refresh variabil, ecrane HiDPI, touchscreen, GPU moderne.  

---

## Suport în funcție de Desktop Environment (DE) / Compositor

- **Wayland matur și recomandat:**  
  - **GNOME** – implicit pe multe distribuții (Fedora, Ubuntu).  
  - **KDE Plasma (5.27+ și Plasma 6)** – suport stabil, complet recomandat.  
  - **Hyprland și alți compositori moderni** – construite direct pentru Wayland.  

- **Wayland limitat sau lipsă:**  
  - **XFCE** – funcționează în principal pe X11, suport Wayland abia la început.  
  - **Cinnamon** – suport foarte slab pentru Wayland.  
  - **MATE, LXQt** – rămân în principal pe X11.  

---

## Cum verifici ce rulezi

```bash
echo $XDG_SESSION_TYPE
```
Rezultatul va fi **x11** sau **wayland**.

---

## Ce ar trebui folosit?

- Dacă DE-ul tău are suport bun pentru Wayland, folosește-l.
- X11 rămâne util pentru aplicații vechi și pentru medii fără suport Wayland, dar este depășit.
- Wayland este standardul actual și viitor, mai sigur și mai performant.
