# NVIDIA și Linux – situația actuală

Mult timp, plăcile NVIDIA au fost mai greu de folosit pe Linux comparativ cu AMD.  
Problemele erau legate în special de driverele vechi open source (**Nouveau**) și de suportul slab pentru Wayland.  
Situația s-a schimbat în prezent, NVIDIA oferă acum **drivere open kernel modules**, care pe plăcile moderne pot fi mai bune decât cele proprietare.  

---

## Tipuri de drivere NVIDIA

### Nouveau
- Primul driver open source pentru NVIDIA, dezvoltat de comunitate.  
- Nu oferă suport pentru plăcile moderne, are performanță scăzută și lipsesc multe funcții.  
- Se mai folosește doar ca fallback și nu este recomandat în utilizarea de zi cu zi.  

### Drivere proprietare (closed source)
- Lansate și întreținute de NVIDIA.  
- Compatibile complet cu CUDA și aplicații profesionale.  
- Încă necesare pe plăcile mai vechi, unde driverele open nu au suport complet.  

### Drivere NVIDIA open (Open Kernel Modules)
- Publicate în 2022 și menținute de NVIDIA.  
- Se integrează direct cu kernelul Linux și funcționează foarte bine pe generațiile recente (RTX 2000 și mai noi).  
- În multe cazuri sunt mai stabile și mai performante decât cele proprietare.  
- Recomandate pentru plăcile moderne.  

---

## AMD vs NVIDIA pe Linux

- **AMD**  
  - Driverele open source sunt incluse direct în kernel și Mesa.  
  - Nu necesită instalare suplimentară.  
  - Suport foarte bun pentru gaming, desktop și Wayland.  

- **NVIDIA**  
  - Pe plăcile moderne, driverele open NVIDIA sunt alegerea recomandată.  
  - Pe plăcile mai vechi, driverele proprietare rămân necesare.  
  - Instalarea poate diferi între distribuții, dar suportul este mult mai bun decât în trecut.  

---

# Concluzie

- **Nouveau** este vechi și nu ar trebui folosit decât ca soluție de urgență.  
- **Driverele proprietare** sunt utile pentru plăcile vechi sau pentru CUDA.  
- **Driverele open NVIDIA** sunt recomandate pentru plăcile moderne.  
- **AMD** rămâne mai simplu de folosit, dar și NVIDIA are acum suport mult mai bun pe Linux.  
