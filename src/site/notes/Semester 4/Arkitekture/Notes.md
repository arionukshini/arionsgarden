---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/notes/"}
---

# Konceptet themelore te kompjuteret si sistem hierarkik

## Dallimi midis 4 koncepteve

**Arkitektura e kompjuterit** ka te beje me veqorite e sistemit qe jane te dukshme per programuesit, dmth vetite qe ndikojne direkt ne menyren e ekzekutimit te programit.

PSh. numri i bitave per paraqitje te numrave, menyra e adresimit te memories etj.

**Organizimi i kompjuterit** ka të bëjë me njësitë operacionale dhe ndërlidhjet në mes tyre me të cilat realizohen specifikat e një arkitekture

PSh. Detajet harduerike të cilat janë transparente për programuesin paraqesin veçoritë që kanë të bëjnë me organizimin e kompjuterit: sinjalet e kontrollit, teknologjia e memories, ndërmjetësit midis kompjuterit dhe periferive.

*Shumica e prodhuesve të kompjuterëve ofrojnë modele me arkitekturë të njëjtë por me organizim të ndryshëm, duke rezultuar në performanca dhe çmime të ndryshme.*

**Struktura e kompjuterit** nënkupton mënyrën me të cilën ndërlidhen komponentët e kompjuterit.
**Funksioni i kompjuterit** nënkupton operacionet e komponentave individuale që janë pjesë e strukturës.

Kompjuterët kryejnë katër funksione kryesore: 
- Përpunojnë të dhënat 
- Ruajnë (memorojnë) të dhënat 
- Bartin të dhënat 
- Kontrollojnë funksionet e sipërpërmendura.

![Pasted image 20260401172013.png](/img/user/Pasted%20image%2020260401172013.png)

Kompjuteri duhet te jete i afte qe te barte te dhena mes vetes dhe rrethies se jashtme.

Rrethina e kompjuterit perbehet nga pajisje qe sherbejne si burime ose cak i te dhenave. Kur te dhenat merren ose dergohen ne pajisje e cila eshte e lidhur drejtperdrejt me kompjuter, procesi quhet input-output dhe pajisja eshte perferike.
Kur te dhenat levizin me distance me te gjate, procesi njihet si komunikim i te dhenave.
*Se fundi duhet te kete kontroll te ketyre tri funksioneve (procesimit, ruajtjes dhe bartjes se te dhenave).* 

Kompjuteri mund të funksionojë si një pajisje për bartjen e të dhënave (Fig. 2a), thjesht transferimin e të dhënave nga një linjë periferike ose e komunikimit në një tjetër.
![Pasted image 20260401173053.png](/img/user/Pasted%20image%2020260401173053.png)

Kompjuteri mund të funksionojë si pajisje për ruajtjen e të dhënave (Fig. 2b), me të dhëna të transferuara nga rrethina e jashtme në kujtesë të kompjuterit (storage) – leximi dhe anasjelltas – shkrimi.
![Pasted image 20260401173126.png](/img/user/Pasted%20image%2020260401173126.png)

Diagrami në Fig. 2c tregon operacionet që përfshijnë procesimin e të dhënave, në të dhëna ose në kujtesë.
![Pasted image 20260401173217.png](/img/user/Pasted%20image%2020260401173217.png)

Diagrami në Fig. 2d tregon operacionet që përfshijnë procesimin e të dhënave dhe rrugëtimin ndërmjet kujtesës dhe rrethinës së jashtme.
![Pasted image 20260401173251.png](/img/user/Pasted%20image%2020260401173251.png)

## Struktura e kompjuterit

Ne figuren me poshte eshte paraqitja me e thjeshte e nje kompjuteri. 
![Pasted image 20260401173703.png](/img/user/Pasted%20image%2020260401173703.png)

Ekzistojne keter komponente kryesore strukturore:
1. **Njesia qendrore e procesimit (CPU):** Kontrollon operacionet e kompjuterit dhe kryen funksionet e procesimit te te dhenave. Referohet shpesh vetem si **procesor**.
2. **Memoria kryesore (main memory):** Ruan te dhenat.
3. **Hyrja/Dalja (I/O):** Barte te dhenat ndermjet kompjuterit (brenda) dhe rrethines se jashtme.
4. **Nderlidhjet e sistemit (System interconnection):** Jane disa mekanizma qe sigurojne komunikimin ndermjet CPU, memories kryesore dhe I/O qe nenkupton magjistralen e sistemit (system bus). Basat bazohet ne nje numer te linjave perquese ne te cilat kyqen komponentet.

## Evolucioni i performancës së kompjuterëve 

### Gjenerata e parë (Gypat me vakum)

Konstruktimi zgjati prej 1943 deri 1946. Perbehet prej 18,000 grypav elektronik, 140 kW, 30 tona. Ishte decimal (jo binar), 5000 operacione per mbledhje ne sekond dhe programohej me dore permes nderpreresve.

### Makina e John von Naumann-it (Turingut)

Njihet si kopmjuteri IAS, 1952. Bazohet ne konceptin e memorimit te programit dhe te dhenave. ALU punonte me te dhena binare. Njesia e kontrollit interpretonte instruksionet duke i marre ato nga memoria per ti ekzekutuar dhe paisjet H/D kontrolloheshin nga njesia e kontrollit.

Kontributi i ketij është pionierizimi i arkitekturës së kompjuterit, e cila është baza e  kompjuterëve modern. Kjo  përfshin një memorie që mund të lexohet dhe shkruhet, procesor që kryen operacione aritmetike dhe logjike, dhe një mekanizëm për transferimin e të dhënave midis memories dhe procesorit.

Në Fig. 7 është paraqitur struktura e përgjithshme e kompjuterit IAS i cili përbëhet nga: 
**Memorie kryesore** (e cila ruan të dhënat dhe instruksionet*) 
**Njësia Aritmetiko-Logjike (ALU)** e aftë për të vepruar me të dhëna binare. 
**Njësia e kontrollit**, e cila interpreton instrusionet në memorie dhe bën që ato të ekzekutohen.
**Pajisjet hyrëse/dalëse (I/O)** që operojnë nga njësia e kontrollit.
![Pasted image 20260401182841.png](/img/user/Pasted%20image%2020260401182841.png)

- Memoria për të dhëna dhe instruksione bazohet në 1000 lokacione memoruese (fjalë) prej 40 bita secila.
- Instruksionet: 2 x 20 bita 
- Bashkësia e regjistrave (memoria e CPU)
	- Memory Buffer Register (MBR) 
	- Memory Address Register (MAR)
	- Instruction Register (IR)
	- Instruction Buffer Register (IBR)
	- Program Counter 
	- Accumulator dhe Multiplier Quotient