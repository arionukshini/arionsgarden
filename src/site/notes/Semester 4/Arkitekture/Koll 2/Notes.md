---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/koll-2/notes/"}
---

# 3 - FUNKSIONI I KOMPJUTERIT DHE INTERKONEKSIONI

Në nivel të lartë, kompjuteri përbëhet nga: 
- CPU (Central Processing Unit) 
- Memoria kryesore 
- Modulet Hyrëse/Dalëse (I/O Modules)
- *Komunikimi mes tyre behet permes basit te sistemit*

Keto komponente nevojiten per realizimin e funksionit baze, **ekzekutimin e programeve**.

Sistemi kompjuterik karakterizohet nga: 
- Shkëmbimi i të dhënave dhe sinjaleve kontrolluese; 
- Struktura e interkoneksionit ndërmjet komponentëve. 
Pamja në nivel të lartë ndihmon në: 
- Analizën e performancës; 
- Identifikimin e ngushticave (bottlenecks); 
- Përmirësimin e besueshmërisë së sistemit.

## Komponentet kryesore te sistemit kompjuterik

Shumica e kompjutereve bazohen ne arkitekturen e **von Neumann**.

Konceptet kryesore të arkitekturës von Neumann: 
- Të dhënat dhe instruksionet ruhen në një memorie të vetme shkrimlexim. 
- Përmbajtja e memories adresohet sipas lokacionit, pa marrë parasysh llojin e të dhënave. 
- Ekzekutimi i instruksioneve realizohet në mënyrë sekuenciale (një instruksion pas tjetrit), përveç nëse rrjedha e programit modifikohet.

Memoria nuk e di cfare permban ajo ruan vetem bita (0 dhe 1) , ndersa kuptimi i tyre percaktohet nga programi dhe CPU.

Ekzistojne dy qasje per realizimin e funksioneve kompjuterike:
1. Programimi ne hardware
2. ne software.

### Programimi ne hardware

Hardueri projektohet per nje funksion te caktuar dhe programi realizohet fizikish ne harduer.

![Pasted image 20260622160304.png](/img/user/Pasted%20image%2020260622160304.png)

### Programimi ne softuer

Kompjuteret perdorin programimin ne softuer, ne vend te ndryshimit te harduerit.

Çdo instruksion: 
- interpretohet nga interpretuesi i instruksioneve; 
- gjeneron sinjale kontrolluese për harduerin.

**Epersia kryesore** - funksioni i sistemit ndryshohet përmes softuerit, pa ndryshuar harduerin.
![Pasted image 20260622160543.png](/img/user/Pasted%20image%2020260622160543.png)

## CPU

![Pasted image 20260622160729.png](/img/user/Pasted%20image%2020260622160729.png)

Figura paraqet pamjen ne nivel te larte te komponenteve kryesore te sistemit kompjuterik dhe komunikimin ndermjet tyre. 

**CPU-ja:** Shihet se CPU-ja shkëmben të dhëna me memorien. Për këtë qëllim, zakonisht përdoren dy regjistra të CPU-së: 
- **MAR (Memory Address Register)** – ruan adresën në memorie për operacionin e ardhshëm të leximit/shkrimit. 
- **MBR (Memory Buffer Register)** – ruan të dhënat që do të shkruhen në memorie ose pranon të dhënat e lexuara nga memoria.
- **PC (Program Counter)** – regjistri që ruan adresën e instruksionit vijues që duhet të sillet nga memoria në CPU.
- **IR (Instruction Register)** – regjistri që ruan instruksionin aktual që është duke u ekzekutuar nga CPU-ja.
- **I/O AR (Input/Output Address Register)** – regjistri që ruan adresën e pajisjes hyrëse/dalëse me të cilën CPU-ja dëshiron të komunikojë. Identifikon pajisjen H/D gjatë komunikimit.
- **I/O BR (Input/Output Buffer Register)** – regjistri ndërmjetësues H/D që përdoret për ruajtjen e përkohshme të të dhënave gjatë shkëmbimit ndërmjet 
- **Njësia e ekzekutimit (Execution Unit)** – pjesa e CPU-së që kryen operacionet aritmetike dhe logjike mbi të dhënat, si: mbledhja, zbritja, krahasimi, operacionet logjike AND, OR dhe NOT. 
- **Njësia e Kontrollit (Control Unit – CU)** interpreton instruksionet dhe gjeneron sinjalet kontrolluese për koordinimin e punës së regjistrave, memories dhe moduleve H/D.

Kapaciteti i regjistrave MAR, MBR, PC, IR, I/O AR dhe I/O BR varet nga lloji dhe arkitektura e procesorit. Ne procesor modern, keta regjistra zakonisht kane madhesi 32-bit ose 64-bit.

Perveq ketyre regjistrave, mund te permbajne edhe tjere:
- **Regjistra të përgjithshëm (GPR – General Purpose Registers)** përdoren për ruajtjen e përkohshme të operandëve, adresave dhe rezultateve. Shumë procesorë modernë përmbajnë 16, 32 ose më shumë regjistra të përgjithshëm. 
- **Regjistra statusi / flamujsh (Flag Registers)** ruajnë informata mbi gjendjen e operacioneve të fundit: Zero Flag, Carry Flag, Overflow Flag, Interrupt Flag. 
- **Regjistra kontrolli (Control Registers)** përdoren për kontrollin e memories dhe funksioneve të procesorit. 
- **Regjistra SIMD / Vektorialë** përdoren për përpunim paralel të të dhënave në multimedia, grafikë dhe inteligjencë artificiale (IA).

**Njësia për Numra me Presje Lëvizëse (FPU – Floating Point Unit)** përdoret për operacione matematike me saktësi të lartë mbi numrat realë. 
**Njësitë SIMD / Vektoriale** përdoren për përpunim paralel të të dhënave në multimedia, grafikë dhe inteligjencë artificiale. 

Në procesorët modernë përdoren edhe: 
- njësi cache, 
- njësi për parashikim të degëzimeve dhe 
- njësi për ekzekutim paralel të instruksioneve.

## Memoria kryesore

Moduli memorues bazohet në një bashkësi të lokacioneve memoruese të definuar me adresa të numëruara në mënyrë sekuenciale (0,1,2…n-3, n-1), memoria kryesore mund të organizohet si matricë e bitve. Secili rresht reprezenton një lokacion memorues.

Për një memorie 96-bite (Fig. 4) ne mund të organizojmë si: 12 × 8 bit, ose 8 × 12 bit, ose 6 × 16 bit, ose madje si 96 × 1 bit apo edhe si 1 × 96 bit
![Pasted image 20260622162420.png](/img/user/Pasted%20image%2020260622162420.png)

## Moduli I/O

Të gjitha pajisjet I/O janë më të ngadalshme se memoria kryesore (dhe CPUja), prandaj duhen modulet I/O.
![Pasted image 20260622162611.png](/img/user/Pasted%20image%2020260622162611.png)

Pajisjet e jashtme zakonisht nuk lidhen direkt në basin e sistemit kompjuterik. Moduli I/O është një interfejs (ndërfaqe) për pajisjet e jashtme (periferikët) me CPU dhe Memorien.

Funksionet kryesore të një moduli H/D (I/O Module) përfshijnë: 
- Kontroll dhe timing 
- Komunikimin e procesorit 
- Komunikimin e pajisjes H/D 
- Baferimin e të dhënave 
- Zbulimin e gabimit

#### Kontroll dhe timing