---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/koll-2/notes/"}
---

# 3 - FUNKSIONI I KOMPJUTERIT DHE INTERKONEKSIONI

Në nivel të lartë, kompjuteri përbëhet nga: 
- CPU (Central Processing Unit) 
- Memoria Modulet 
- Modulet Hyrëse/Dalëse (I/O Modules)

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

##

![Pasted image 20260622160729.png](/img/user/Pasted%20image%2020260622160729.png)