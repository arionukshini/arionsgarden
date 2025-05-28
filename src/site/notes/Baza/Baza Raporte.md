---
{"dg-publish":true,"permalink":"/baza/baza-raporte/"}
---

# Raportet (BIE 2)

Per kete pjese te raporteve perdorim programin LTspice.

Pasi ta hapim programin shkojme te "File" pastaj "New Schematic".

![LTspice_zO6P3pFHCr.jpg](/img/user/LTspice_zO6P3pFHCr.jpg)

Pas kesaj mund te fillojme me rastet me poshte.

1. $V = 20; \space R_{1} = 5; \space R_{2}=5;$

Per kete rast kemi nje gjenerator dhe 2 rezistor. Marrim rezistorin e pare dhe me "Ctrl+R" e kthejme ne forme horizontale dhe e marrim rezitroin e pare ne forme vertikale. Po ashtu marrim nje gjenerator te tensionit.

![LTspice_xOA4yjMVsY.png](/img/user/LTspice_xOA4yjMVsY.png)

Pastaj marrim "wire" dhe i lidhim keta mes vete. Marrim nje tokezim "Ground" dhe e lidhim me qark.

Per te vendosur vlera tek elementet e qarkut, me tasten e djathte te mausit klikojme mbi elementet dhe vendosim vlerat e caktuara.

E ekzakutojme qarkun, tek "Run" dhe per kohe e zgjedhim 100m. Varesisht se qka klikojme marrim pamje te ndryshme ne ekran.

![LTspice_U3018Poru4.png](/img/user/LTspice_U3018Poru4.png)
![LTspice_RG0zgjpY8H.png](/img/user/LTspice_RG0zgjpY8H.png)

2. $V=20; \space R_{1}=20 ; \space L_{1}=3m;$

Proceduar jane pothuajse te ngjashme, perveqese ne kete rast e kemi nje bobine ne vend te dy rezistoreve. Pora zgjedhim bobinen dhe e vendosim dhe lidhim me qark.

![NVIDIA_Overlay_ED4aAHjLTQ.png](/img/user/NVIDIA_Overlay_ED4aAHjLTQ.png)
![NVIDIA_Overlay_tFomCGYwJv.png](/img/user/NVIDIA_Overlay_tFomCGYwJv.png)

3. $V= (Amplitude=20,Frekuenca=50); \space R_{1}=50; \space L_{1}=3m;$

Ne kete rast kur vendosim vleren per V, e klikojme advanced, pastaj zgjedhim opsionin "SINE" edhe aty vendosim vleren e amplitudes dhe frekuences, kurse vlerat tjera jane 0.

![NVIDIA_Overlay_5Uz6E4CUAF.png](/img/user/NVIDIA_Overlay_5Uz6E4CUAF.png)![NVIDIA_Overlay_2Aav7fQyqE.png](/img/user/NVIDIA_Overlay_2Aav7fQyqE.png)

4. $V= (Amplitude=20,Frekuenca=50); \space R_{1}=50; \space C_{1}=10\micro;$

E ngjashme me rastin 3, i vetmi dallim eshte se e marrim nje kondensator ne vedn te bobines.

![NVIDIA_Overlay_6657SXU1mC.png](/img/user/NVIDIA_Overlay_6657SXU1mC.png)
![NVIDIA_Overlay_5URSF3aA9R.png](/img/user/NVIDIA_Overlay_5URSF3aA9R.png)

5. $V=20; \space R_{1}=20; \space L_{1}=3m;$

Vendosim vleart si gjithe. Por kur e ekzakutojme, pra tek run, tek kutia qe thot "Start external DC supply voltages at 0V" e klikojme ate, dhe pastaj tek koha vendosim 1.5m.

![LTspice_riOSR20JJv.png](/img/user/LTspice_riOSR20JJv.png)
![LTspice_98uPu1Bf2A.png](/img/user/LTspice_98uPu1Bf2A.png)

6. $V=15; \space R_{1}=25; \space C_{1}=20\micro;$

Vendosim vleart si gjithe. Por kur e ekzakutojme, pra tek run, tek kutia qe thot "Start external DC supply voltages at 0V" e klikojme ate, dhe pastaj tek koha vendosim 1.5m.

![LTspice_IM4rvsEJjz.png](/img/user/LTspice_IM4rvsEJjz.png)
![LTspice_udQmZEjM1p.png](/img/user/LTspice_udQmZEjM1p.png)