# Cum să pui un ISO Linux pe un stick USB

Există două metode populare: cu **Rufus** pe Windows sau cu comanda **dd** pe Linux.  

---

## Pe Windows

1. Descarcă Rufus: [rufus.ie](https://rufus.ie/en/)  
2. Deschide aplicația și verifică să fie selectat stick-ul USB.  
3. La **Boot selection**, apasă pe **SELECT** și alege fișierul `.iso` descărcat.  
4. Dacă apare un mesaj cu *ISOHybrid image*, lasă opțiunea recomandată.  
5. La **Partition scheme**:  
   - **GPT** pentru sisteme moderne (UEFI).  
   - **MBR** pentru sisteme mai vechi (BIOS).  
6. Restul setărilor le poți lăsa cum sunt.  
7. Apasă **START** și așteaptă să termine.  

---

## Pe Linux

Poți folosi comanda `dd`. Ai grijă: șterge complet discul pe care scrii.  

1. Află ce nume are stick-ul USB:  

   ```bash
   lsblk
   ```

   Uită-te la dimensiune și identifică stick-ul. **Atenție**: nu confunda cu SSD-ul sau alte discuri.  

   Exemplu de rezultat:  

   ```
   sdc
   ├─sdc1
   └─sdc2
   ```

   În cazul ăsta, stick-ul e `/dev/sdc`. (Folosește doar `sdc`, fără numerele de la partiții.)  

2. Rulează comanda:  

   ```bash
   sudo dd if=/home/USER/Downloads/nume.iso of=/dev/sdX bs=4M status=progress oflag=sync
   ```

   Înlocuiește:  
   - `USER` cu numele tău de utilizator.  
   - `nume.iso` cu numele fișierului descărcat.  
   - `sdX` cu stick-ul tău (ex. `sdc`).  
