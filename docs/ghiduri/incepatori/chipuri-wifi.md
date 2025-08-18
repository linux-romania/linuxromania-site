# Chipurile Wi-Fi și suportul lor în Linux

## 1. De ce contează chipset-ul, nu doar marca adaptorului

La alegerea unui adaptor Wi-Fi (USB sau intern), brandul (TP-Link, Asus, D-Link etc.) nu este cel mai important, ci chipset-ul din interior (Intel, MediaTek, Realtek, Qualcomm Atheros).  

Pe Linux, driverul trebuie să fie deja inclus în kernel sau disponibil ca modul separat. Dacă chipsetul nu are driver bun, apar probleme cu stabilitatea, viteza și compatibilitatea.

---

## 2. Chipseturi bine suportate în Linux

### 🔹 Intel
- Cel mai bun suport general, mai ales pe laptopuri.  
- Driverul **iwlwifi** e inclus direct în kernel.  
- **Pro:** stabilitate, performanță bună, actualizări regulate.  
- **Contra:** mai greu de găsit ca adaptor USB, mai des integrat ca placă internă M.2/PCIe.  

### 🔹 MediaTek / Ralink (driver mt76)
- Suport bun direct în kernel.  
- Recomandate pentru adaptoare USB plug-and-play.  
- **Pro:** compatibilitate bună, performanță decentă.  

### 🔹 Qualcomm Atheros
- Suport foarte bun prin driverele **ath9k, ath10k, ath11k**.  
- **Pro:** stabilitate și suport pe termen lung.  
- **Contra:** mai rar pe adaptoare USB moderne.  

---

## 3. Realtek și Linux – de ce sunt probleme

- Chipseturi foarte răspândite și ieftine (ex: RTL8188, RTL8812, RTL8821, RTL8852).  
- **Problema:** driverele oficiale Realtek nu sunt incluse în kernel → trebuie instalate manual de pe GitHub sau repo-uri terțe.  
- Multe drivere neoficiale sunt slab întreținute → nu mai merg după update-uri de kernel.  
- Consecințe: instabilitate, deconectări, viteză slabă, lipsă suport pentru funcții moderne (5GHz, Wi-Fi 6, monitor mode).  

**Exemple frecvente:**  
- `rtl8188eu`, `rtl8812au`, `rtl8821cu` – cer drivere manuale.  
- `rtl8852be` (Wi-Fi 6) – suport foarte recent și încă experimental.  
---

## 4. Cum verifici ce chipset ai

- Pentru adaptor USB:  
```bash
lsusb
```
- Pentru plăci PCIe:
```bash
lspci
```
