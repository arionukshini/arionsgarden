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

Fig. 8 tregon që Njësia e kontrollit dhe Njësia Aritmetiko-Logjike (ALU) përmbajnë lokacione memoruese, të quajtura regjistra të definuar si në vijim:
![Pasted image 20260402104725.png](/img/user/Pasted%20image%2020260402104725.png)

### Bashkesia e regjistrave (memoria e CPU)

- **Instruction Buffer Register** E ruan përkohësisht pjesën e djathtë të instruksionit
- **Program Counter** E përmban adresën e instruksionit vijues (dy instruksioneve) që sjellen prej memories
- **Accumulator and Multiplier Quotient** Ruajnë përkohësisht operandet dhe rezultatet e operacioneve të ALU; p.sh. nëse shumëzohen dy numra 40 bitësh, rezultati është numër 80 bitësh, 40 bitët me peshë të madhe ruhen në Akumulator kurse 40 bitat me peshë të vogël vendosën në regjistrin MQ.
- **Memory Buffer Register** E përmban fjalën që duhet ruajtur në memorie ose të dërgohet në njësinë H/D, ose të pranojë fjalën nga memoria ose nga njësia H/D.
- **Memory Address Register** E specifikon adresën e memories për fjalën që duhet lexuar ose shkruar.
- **Instruction Register** E përmban kodin operues të instruksionit që është duke u ekzekutuar. Ky kod operues përbëhet prej 8 bitëve.

### Formati i memories IAS

Kjo memorie bazohet ne 1000 lokacione memoruese prej 40 shifrave binare secila. Te dhenat dhe instruksionet ruhen ne memorie.
- Formati i fjales per numra
Numrat paraqiten ne forme binare, instruksioni poashtu eshte kod binar. *Secili numer eshte reprezentuar nga biti i parashenjes dhe nje vlere 39 bite.*
- Formati i fjlaes per instruksione
Nje fjale permben dy instruksione nga 20 bita, ku secili instruksion bazohet ne nje kod operues 8 bite i cili specifikon operacionin dhe adrese 12 bite qe percakton nje nga fjalet ne memorie (0-999).
![Pasted image 20260402105844.png](/img/user/Pasted%20image%2020260402105844.png)

Secili cikel i instruksionit perfshine dy nencikle:
- Sjellja e instruksionit
- Ekzekutimi i instruksionit

**Cikli i sjelljes së instruksionit**
- Sjellët (bartet, ngarkohet) kodi i operacionit në regjistrin IR. 
- Pjesa e adresës ngarkohet në regjistrin MAR. 
-  Ky instruksion mund të merret nga regjistri IBR ose nga memoria e kompjuterit duke e ngarkuar fjalën në MBR, pastaj në IBR, IR dhe MAR.

Kur kodi i operacionit vendoset në IR, atëherë fillon ekzekutimi i instruksionit, gjegjësisht nëncikli i dytë.

**Cikli i ekzekutimit**
- Qarqet e kontrollit e dekodojnë kodin e operacionit;
- Qarqet e kontrollit e ekzekutojnë instruksionin duke dërguar sinjalet e duhura kontrolluese që bëjnë bartjen e të dhënave ose kryerjen (ekzekutimin) e operacionit nga ana ALU.

### Instruksionet e kompjuterit IAS

IAS kishte gjithsej 21 instruksione qe gruphen ne 5 lloje:
1. Per transfer te dhenave
2. Per degezim te pakushtezuar
3. Per degezim te kushtezuar
4. Aritmetike
5. Per modifikimin e adreses

## Kompjuterët e gjeneratës së dytë (Transistorët)

Ndryshimi i pare kryesor vjen me zevendesimin e gypave te vakumit me transistor, qe jane me te vegjel, me te lire, shperndajne me pak nxehtesi dhe harxhojne me pak energji elektrike.
Transistori u shpik ne laboratorin e Bell-it me 1947 dge bga viti 1950 kishte nje revolucion ne kompjuteret.
IBM nuk ishte kompania e pare qe ofroi kete teknologji te re, por ishte NCR & RCA e pastaj IBM me IBM 7000  ne dhjetor 1957.

### Klasifikimi i kompjutereve sipas gjeneratave

![Pasted image 20260402141151.png](/img/user/Pasted%20image%2020260402141151.png)

Figura paraqet konfigurimin e IBM 7094, i gjenerates se dyte. E rendesishme per ket lloj kompjuteri ishte perdorimi i kanaleve te te dhenave.
Ky kanal eshte nje modul i pavarur I/O me procesorin e vet dhe grupin e vet te instruksioneve.
![Pasted image 20260402141436.png](/img/user/Pasted%20image%2020260402141436.png)

## Gjenerata e tretë (Qarqet e integruara)

Gjate 1950-1960, pajisjet elektronike ishin te ndertuara nga komponentet dikrete: transistoret, rezistoret, kondensatoret etj. Pas 1960 filloje zhvillimi i elektronikes digjitale dhe industrise kompjuterike dhe kishte nje prirje ne zvoglimin e madhesise se qarqeve elektronike.
Dy lloje të komponentëve janë të nevojshme: gates (portat) dhe memory cells (qelizat memoruese).

**Porta** është një komponentë që implementon një funksion të thjeshtë logjik ose Boolean (Fig. 11 ). Quhen porta sepse ato kontrollojnë rrjedhën e të dhënave në të njëjtën mënyrë si në kanal.
**Qeliza memoruese** (Fig. 12) është një komponentë që mund të ruaj një bit të të dhënash; kështu që kjo komponentë mund të jetë në njërën nga dy gjendjet stabile në çdo kohë.
![Pasted image 20260402142028.png](/img/user/Pasted%20image%2020260402142028.png)

Duke lidhur numer te madh te keto dyjave konstruktohet kompjuteri.

Këtë mund t'a lidhim me katër funksionet themelore:
**Ruajtja e të dhënave:** realizohet me qeliza memoruese.
**Procesimi i të dhënave:** Realizohet përmes portave. 
**Bartja e të dhënave:** Rrugët midis komponentëve përdoren për të bartur të dhëna nga memoria në memorie dhe nga memoria përmes portave në memorie. 
**Kontrolli:** Rrugët ndërmjet komponentëve mund të bartin sinjale kontrolluese.

**Qarku i integruar (IC)** – komponentët si transistorët, rezistorët dhe përçuesit mund të fabrikohen në një pllakë gjysmëpërçuese të silicit (Vafer). Këto komponentë përmes një procesi të metalizimit duke formuar qarqe. Fig. 13 paraqet konceptet bazë të ndërtimit të qarkut të integruar. Një vafer i hollë i Silicit është ndarë në një matricë të zonave të vogla, secila me disa milimetra katrorë. Mostër e qarkut identik është ndërtuar në secilën sipërfaqe dhe vaferi është ndarë në chipa. Secili Chip ka shumë porta dhe/ose qeliza memoruese plus një një numër të hyrjeve dhe daljeve për lidhje.
![Pasted image 20260402145038.png](/img/user/Pasted%20image%2020260402145038.png)

Sistemi IBM/360, Nga viti 1964, IBM kishte një kontroll të fortë në tregun e kompjuterave me Serinë e makinave 7000. Kjo ishte familja e parë e planifikuar e kompjuterëve. Familja mbulonte një gamë të gjerë të performancës dhe të kostos. Tabela 2 tregon disa nga karakteristikat kryesore të modeleve të ndryshme në vitin 1965 (secili anëtar i familjes dallon nga një model numër).
![Pasted image 20260402145123.png](/img/user/Pasted%20image%2020260402145123.png)

DEC PDP-8 Në të njëjtin vit që IBM lëshoi sistemin e parë të IBM/360, një tjetër kompjuter u shfaq: PDP-8 nga Digital Equipment Corporation Çmimi prej 16,000 dollarësh llogaritej mjaft e lirë për secilin teknik laboratori që të ketë një të tillë. Vetëm disa muaj më parë sistemi IBM/360 seri e kompjuterë mainframe kushtonte qindra mijëra dollar.

Modelet e vonshme te PDP-8 perdoren nje strukture e cila quhej OMNIBUS (magjistrale BUS). Kjo perbehej nga 96 rruge te ndara, qe perdoreshin per bartje, kontrolla, adresa dhe sinjale te te dhenave, perdorimi i tyre duhet kontrolluar nga CPU-ja.

## Ligji i Moorit