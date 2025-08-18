# X11 vs Wayland

Pe Linux, interfața grafică are nevoie de un protocol care să facă legătura între aplicații și serverul grafic.  
Standardul clasic a fost **X11** (sau X.Org Server), dar de câțiva ani direcția clară este trecerea la **Wayland**.  

---

## X11 (X.Org)

- Apărut în anii ’80, a rămas standardul implicit pe Linux timp de decenii.  
- Arhitectură foarte complexă și încărcată cu extensii adăugate de-a lungul anilor.  
- Oferă compatibilitate excelentă cu orice aplicație, dar are probleme fundamentale:  
  - lipsă de izolare între aplicații (oricare poate spiona altă fereastră),  
  - consum suplimentar de resurse,  
  - performanță limitată pe hardware modern.  

---

## Wayland

- Creat ca alternativă modernă la X11, cu design simplificat.  
- Ferestrele și aplicațiile comunică direct cu compositorul grafic, ceea ce oferă latență mai mică și securitate mai bună.  
- Integrare mult mai bună cu hardware și tehnologii noi (refresh variabil, HiDPI, touch, GPU modern).  

---

## Suport în funcție de Desktop Environment (DE) / Compositor

- **Foarte bun suport pentru Wayland:**  
  - **GNOME** – folosește Wayland ca implicit pe multe distribuții (Fedora, Ubuntu).  
  - **KDE Plasma (5.27+ și 6)** – aproape complet pe Wayland, recomandat.  
  - **Hyprland și alte tiling compositors moderne** – construite direct pe Wayland.  

- **Suport limitat sau lipsă:**  
  - **XFCE** – încă orientat spre X11, suport Wayland abia la început.  
  - **Cinnamon** – suport foarte slab pentru Wayland.  
  - **MATE, LXQt** – în principal pe X11.  

---

## Verifică ce rulezi

```bash
echo $XDG_SESSION_TYPE
```
Rezultatul va fi **x11** sau **wayland**.

---

## Ce ar trebui folosit?

**Wayland** este direcția clară și ar trebui folosit ori de câte ori există suport în DE-ul sau compositorul tău.
Deși X11 rămâne disponibil pentru compatibilitate, viitorul dezvoltării pe Linux se concentrează pe Wayland, iar suportul aplicațiilor devine din ce în ce mai bun.

---

## Concluzie

  - **X11**: încă util pentru aplicații vechi și DE-uri fără suport Wayland, dar depășit.
  - **Wayland**: standardul actual și viitor, mai sigur și mai performant.
