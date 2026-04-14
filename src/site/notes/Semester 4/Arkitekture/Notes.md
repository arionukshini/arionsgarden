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

Njihet si kompjuteri IAS, 1952. Bazohet ne konceptin e memorimit te programit dhe te dhenave. ALU punonte me te dhena binare. Njesia e kontrollit interpretonte instruksionet duke i marre ato nga memoria per ti ekzekutuar dhe paisjet H/D kontrolloheshin nga njesia e kontrollit.

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

Me kohe, u be e mundur te paketoheshin me shume komponente ne te njejtin chip. Kjo reprezenton ligjin e Moor-it.
Gordon Moor ishte bashkethemelues i Intelit.
Numri i transistoreve brenda cipit do te dyfishohet per qdo dy vite.
![Pasted image 20260402151131.png](/img/user/Pasted%20image%2020260402151131.png)

Për 15 vite, nga 1986 deri në 2001, performanca e procesorit u rrit me një mesatare prej 52%, por deri në vitin 2018, kjo ishte ngadalësuar në vetëm 3.5% në vit - një ndalesë virtuale. Arsyja kryesore eshte se po i afrohemi kurfirit fizik. Kjo do të thotë një fund për s*hkallëzimin e Dennard - një tjetër 'ligj' kompjuterik, i cili thotë se ndërsa transistorët bëhen më të vegjël, kërkesat e tyre për energji gjithashtu zvogëlohen, duke e bërë nevojën për energji për zonë afërsisht konstante, edhe pse transistorët janë të paketuar më dendur.*

Konsekuencat e Ligjit te Moorit jane te thella:
• Fuqia procesuese dyfishohet afërsisht çdo dy vjet për të njëjtin çmim, prandaj kostoja e çipave mbetet pothuajse e pandryshuar. 
• Rritja e dendësisë së paketimit shkurton rrugët elektrike ndërmjet portave logjike dhe memories, duke rritur shpejtësinë e funksionimit.  
• Kompjuterët bëhen më të vegjël dhe mund të përdoren më lehtë në ambiente të ndryshme.  
• Zvogëlohen kërkesat për energji.  
• Ndërlidhjet në qarqet e integruara janë më të besueshme sesa lidhjet me pikje.

## Gjenerata e katert dhe e peste e kompjutereve (mikroprocesoret)

Pasi densiteti i elementeve ne chip vazhdoi te rritet, shume elemente u vendosen ne nje chip, u paraqit nevoja e konstruktimit te kompjuterit me nje procesor te vetem.
**Zbulim i madh u arrit ne vitin 1971, kur Intel zhvilloi 4004.**
4004 ishte qipi i pare qe permbante te gjitha komponentet e nje CPU ne nje paketim te vetem.
Procesori 8080 ishte një mikroprocesor 8 bitësh.
![Pasted image 20260402155013.png](/img/user/Pasted%20image%2020260402155013.png)
![Pasted image 20260402155030.png](/img/user/Pasted%20image%2020260402155030.png)

### Evoluimi i mikroprocesoreve

Ekzistojnë dy lloje kryesore të mikroprocesorëve që njeherit kanë qenw edhe në konkurrencë të përhershme gjatë gjithë zhvillimit të tyre,
1. Pentium dhe 
2. Power PC (PPC) 

Dallimi kryesor në mes Pentium dhe PPC është në arkitekturën që ata adoptuan. 

**Pentium** miratoi arkitekturën CISC (Complex Instruction Set Computer), e cila ka instruksione komplekse që marrin cikle të shumta të CPU-së.
**PPC** miratoi arkitekturën RISC (Reduced Instruction Set Computer), e cila ka instruksione më të thjeshta që kërkojnë vetëm një instruksion të vetëm për t'u ekzekutuar. 

- Prodhues i mikroprocesorëve Pentium është Intel-i 
- Procesorët Power PC (RISC superskalar) janë zhvilluar bashkërisht nga IBM, Motorola, dhe Apple qysh nga viti 1991.

### Zhvillimi i mikroprocesoreve Intel

- 1971, Inteli e zhvilloi mikroprocesorin e parë 4 bitësh, të njohur si 4004 
- 1972, 8008 (8-bita)
- 1974, 8080 ( mikroprocesori i parë për përdorime gjenerale, 8 bita për të dhena, u përdor në PC e parë Altair )
- 1978, 8086 (16-bita, shumë më i fuqishëm, keshi i instruksioneve; 8088 – 8 bitësh dhe u përdor në IBM PC e parë )
- 1982, 80286 (20 bita për adresa, memorien 16MB) 
- 1985, 80386 (32-bita, përkrahte multitaskingun)
- 1989, 80486 (procesori i parë pipeline për instruksione dhe kesh të fuqishëm, koprocesorin matematik)
- 1993, Pentium (superskalar, ekzekutonte më shumë instruksione në paralel)
- 1995, Pentium Pro (organizim të avancuar superskalar, parashikim të degëzimit, analizonte rrjedhën e të dhënave, ekzekutim spekulativ)
- 1997, Pentium II (MMX teknologjii, procesim të grafikës, video dhe audio)
- 1999, Pentium III (instruksione shtesë me pikë levizëse për grafikë 3D)
- 2000, Pentium 4 (superpipelining, avancim në multimedia)
- Itanium (64 bita)
- Itanium 2
- Pentium Dual-Core E2220 
- Pentium G870 
- 2019 - Pentium Silver J5040 
- 2022 - Pentium Gold G7400TE

### Zhvillimi i mikroprocesoreve Power PC

- 1993 – 601
- 1994 – 603 (low-end), 604 (desktop)
- 1995 – 620 (64-bit për servera high-end)
- 1997 – G3 (kesh me dy nivele brenda çipit)
- 1999 – G4 (multiprocesorë brenda çipit) 
- 2003 – G5 
- 2004, Motorola e braktis prodhimin e çipave
- 2004, IBM hyn në tregun e industrisë së lojërave duke e ruajtur tregun për Power PC: Nintendo, Sony Playstation III,Micosoft Xbox 360
- 2005, Apple e ndërpreu prodhimin e procesorëve PowerPC për PC e veta. kur Apple shpalli kalimin e saj në arkitekturën x86, duke përdorur procesorët e Intel.

## Sistemet e mbjella - ARM

Arkitektura ARM (Acorn RISC Machine) i referohet një arkitekture të procesorit që ka evoluar nga parimet e dizajnit të arkitekturës RISC dhe përdoret në sistemet e mbjella.

Sistemet ARM fillimisht janë disejnur për përdorim ne mikrokompjuterët në përgjithësi, por aktualisht përdoren ne sistemet e mbjella (embeded ). Termi sistemi i embeded i referohet përdorimit të elektronikës dhe softuerit brenda një produkti, në krahasim me një kompjuter me qëllim të përgjithshëm.

Përkufizim i përgjithshëm: *Një kombinim i harduerit dhe softuerit kompjuterik, dhe ndoshta edhe pjesë të tjera shtesë mekanike, të dizajnuara për të kryer një funksion të dedikuar. Në shumë raste, sistemet e ngulitura janë pjesë e një sistemi ose produkti më të madh p.sh në vetura , makina larëse etj.*

Fig. 16 tregon organizimin e një sistemi të integruar ku përveç procesorit dhe memories, ka një numër elementesh që ndryshojnë nga kompjuteridesktop ose laptop me qëllim të përgjithshëm.
![Pasted image 20260402182333.png](/img/user/Pasted%20image%2020260402182333.png)
![Pasted image 20260402182423.png](/img/user/Pasted%20image%2020260402182423.png)

## **Permbledhje**

Kompjuterët e mbjellë gjenden në makinat e sodit: mikrovalë, makinat e larjes, shumicën e printerëve, në shumicën e suiqave të rrjetës dhe në të gjitha veturat modele të reja. 
Procesorët në Pajisjet Personale Mobile (PMD) shpesh konsiderohen si embedded kompjuter, por shpesh do i mbajmë ato si kategori të ndara sepse PMD janë platforma që mund të ekzekutojnë softuer të zhvilluar eksternal dhe ata ndajnë shumë karakteristika të kompjuterëve desktop. 
Embedded kompjuterët kanë një përhapje më të gjerë në fuqinë procesuese dhe çmim. 
Përshijnë procesorët 8 bitësh dhe 16 bitësh që mund të kushtojnë më pak se dhjeta centa, mikroprocesorët 32 bitësh që ekzekutojnë 100 milion instruksione/s që kushtojnë më pak se 5 $, dhe së fundi procesorët për sviçat e rrjetës që mund të ekzekutojnë miliard instruksione/s.

### Kuptimi i "i" tek Apple

Prej vititi 1998 iPad është prefiksi i. Çfarë kuptimi ka???
Në një event të Apple më 1998, Steve Jobs prezantoi iMac-un, duke shpjeguar edhe lidhjen mes "i" dhe "Mac". 
Ai tha: 
*“iMac vjen nga lidhja e internetit me thjeshtësinë e Macintosh," 
"Ne po e synojmë që konumatorëve t’iu ofrojmë një kompjuter I cili përdoret thjeshte për të hyrë në internet dhe shpejt”* 
Ky prefix është zgjeruar pastaj edhe te iPhone e kështu me radhë.

## Arkitektura e Harvardit

![Pasted image 20260402183256.png](/img/user/Pasted%20image%2020260402183256.png)

Kjo i referohet nje strukture memorie ne te cilen procesori eshte i lidhur me dy lokacione memorie te pavarura nepermjet dy grupeve te pavarura te basave.
Ne origjinalen, nje lokacion memoie mban istruksionet e programit dhe tjetri mban te dhenat.

Ajo ka sinjale fizikisht të ndara dhe ruajtje për memorien e kodit dhe te te dhenave. *Është e mundur të qaseni njëkohësisht në memorien e programit dhe memorien e të dhënave në të njëjtën kohë.*

#### Cili është dallimi në mes arkitekturës së Von Neumann dhe Arkitekturës së Harvardit?

Dallimi kryesor midis dy arkitekturave është se në arkitekturën e Von Neumann e gjithë memoria është e aftë të ruajë të gjithë elementët e programit, të dhënat dhe instruksionet;
Në arkitekturën e Harvardit memoria ndahet në dy memorie: një për të dhënat dhe një për instruksione.

## Cloud computing

**Cloud networking** - Shumë zgjidhje të kompjuterëve në cloud mbështeten në Internet, që është vetëm një pjesë e infrastrukturës së rrjetit. Një shembull i cloud networking është ofrimi i rrjeteve me performancë të lartë dhe/ose besueshmëri të lartë midis provajderit dhe abonentit.
Cloud networking i referohet përdorimit të teknologjisë së cloud-it për të krijuar, menaxhuar dhe optimizuar rrjete kompjuterike.
Qëllimi kryesor i kompjuterëve në cloud është të ofrojë mundësinë e përdorimit me qira të resurseve kompjuterike.
Praktikisht, të gjithë shërbimet në cloud ofrohen duke përdorur një nga tri modelet kryesore: SaaS, PaaS dhe IaaS.
**Software si Shërbim (Software as a Service - SaaS)** Siç sugjeron emri ky model ofron shërbime për klientët në formën e softuerit - softuer aplikacionesh; sh. Gmail.
**Platformë si Shërbim (Platform as a Service -PaaS)** - Ofron shërbim për klientët në formën e një platforme mbi të cilën mund të ekzekutohen aplikacionet e klientit. Sh. Google App Engine.
**Infrastrukturë si Shërbim (IaaS)** – Klienti ka qasje në infrastrukturën bazë të cloud-it. IaaS ofron makina virtuale dhe harduer të tjerë, si dhe sisteme operative, të cilat mund të kontrollohen përmes një ndërfaqeje programimi aplikacionesh (API). Sh. Azure, Amazon EC2.

# Problemet e performaces

Zhvillimi i teknologjise ka mundesuar ne dizajnimin e mikroprocesoreve qe perfshijne: procesimin e imazheve, zerit, simulim dhe modelim, videokonferenca.

**Numri i operacioneve brenda një intervali kohor e shpreh shpejtësinë e mikroprocesorit.**

Përderisa shpëjtësia e procesorit është rritur dukshëm ndër vite, shpejtësia me të cilën të dhënat mund të transferohen ndërmjet memories dhe procesorit ka mbetur “keq”. Interfejsi (ndërfaqja) ndërmjet procesorit dhe memories kryesore është rruga më kruciale në tërë kompjuterin, sepse është përgjegjëse për të mbajtur një rrjedhë konstantë të instruksioneve programore dhe dhe të dhënave ndërmjet çipave memorues dhe procesorit.
Nëse memoria DRAM nuk e përcjell shpejtësinë e mikroprocesorit, mikroprocesori kalon në gjendje të pritjes duke humbur një pjesë të kohës së procesimit.

Si zgjidhet ky problem?
-  Duke e rritur numrin e bitëve të DRAM-it dhe duke e rritur gjerësinë e basit
- Me ndryshimin e interfejsit të DRAM-it duke shtuar keshin ose ndonjë skemë baferuese tjetër.
- Duke e reduktuar frekuencën e qasjes së memories. Shtimi i keshit* në çip. Kjo përfshin përfshirjen e një ose më shumë niveleve të keshit në çipin e procesorit
- Duke e rritur gjerësinë e brezit midis procesorit dhe memories: përmes basit me shpejtësi më të madhe dhe hierarkisë së basave.

*Keshi është një memorie relativisht e vogël e ndërthurur ndërmjet një memorie më të madhe, më të ngadalshme dhe logjikën e qasjes në memorie më të madhe.*

### Teknikat përshpejtuese të mikroprocesorit

- Pipelining (Me pipelining, procesori mundët njëkohësisht të punojë në instruksione të shumëfishta. P.sh, përderisa një instruksion është duke u ekzekutuar, kompjuteri është duke dekoduar një tjetër instruksion. 
- Keshi brenda pllakës 
- Parashikimi i degëzimit (procesori shikon përpara në kodin e instruksionit që përcillet prej memories dhe parashikon cilat degëzime, ose grupe instruksionesh, ka të ngjarë që të ekzekutohen më pas). 
- Analiza e rrjedhës së të dhënave 
- Ekzekutimi spekulativ

Performanca e procesorit ka ecur shume perpara ne krahasim me komponentet e tjere te kompjuterit.

![Pasted image 20260407151951.png](/img/user/Pasted%20image%2020260407151951.png)

Çfarë është më e rëndësishme? Madhësia e RAM-it apo shpejtësia e procesorit?
Me një CPU të ngadaltë dhe shumë RAM, ju keni një pajisje të ngadaltë. Me një CPU të shpejtë dhe me pak RAM, ju keni një pajisje të vonuar performance. 
*Të dyja janë po aq të rëndësishme pasi punojnë së bashku për të rritur performancën e kompjuterit.*

![Pasted image 20260407152222.png](/img/user/Pasted%20image%2020260407152222.png)

Faktoret per rritjen e performances jane: rritja e frekuences se taktit dhe dendesia e komponenteve.
Me rritjen e keto dyjave dolen disa veshtiresi:
- Disipacion i fuqisë. 
- Vonesa RC. 
- Latenta e memories (vonesa).

Sot fuqia është sfida më e madhe e dizajnerëve për çdo klasë të kompjuterëve. 
**Së pari:** fuqia duhet të sjellët në çip dhe të shpërndahet përreth çipit ku mikroprocesorët modern shfrytëzojnë me qindra pina dhe shtresa të shumëfishta interkonektuese për fuqi dhe tokëzim. 
**Së dyti:** Fuqia harxhohet (shpërndahet) si nxehtësi dhe duhet të largohet.
Për cipat CMOS, tradicionalisht konsumi i fuqisë ka qenë dhe është gjatë komutimit të transistorëve, e quajtur fuqi dinamike.
Transistori komuton nga 0 -> 1 dhe 1 -> 0 (ngarkimit dhe zbrazjes së kondensatorëve)
![Pasted image 20260407153003.png](/img/user/Pasted%20image%2020260407153003.png)
*Vlera më e ultë e frekuencës së klokut në mënyrë direkte redukton fuqinë.*

Fuqia: Me rritjen e densitetit dhe shpejtësisë së taktit rritet edhe dendësia e fuqisë (W/cm2 ) në çip (problemet me ftohje).
Vonesa RC: shpejtësia midis transistorëve kufizohet me R dhe C të përçuesve që i lidhin këta transistorë.
- R rritet sepse lidhjet janë shumë të holla
- C rritet sepse komponentët janë më afër 
- Nga kjo rrjedh se vonesa kohore τ = RC rritet.

### Latenca e memories

Latenca është koha ndërmjet fillimit dhe përfundimit të një ngjarje.

Një tjetër fushë e fokusit në projektim është menaxhimi i pajisjeve të hyrje/dalje. Ndërsa kompjuterët bëhen më të shpejtë dhe më të fuqishem, zhvillohen aplikacione më të sofistikuara që mbështesin përdorimin e periferikëve me kërkesa intensive për hyrje/dalje.
![Pasted image 20260407154507.png](/img/user/Pasted%20image%2020260407154507.png)

Mikroprocesorët modern ofrojnë  teknika me qëllim të përmirësimit të efiqiencës së energjisë. Teknikat për reduktimin e fuqisë janë: 
1. **Do nothing well:** Shumica e mikroprocesorëve sot shkyçin klokun e moduleve joaktive për të ruajtur energjinë dhe fuqinë dinamike.
2. **Skalimi Dinamik Tension – Frekuencë (DVFS):** (direkt nga formula e mëparshme. PMD-të, laptopët madje edhe serverët kanë perioda të aktivitetit të ultë ku nuk kanë nevojë të operojnë me frekuencë dhe tension të lartë. Mikroprocesorët modern kryesisht ofrojnë disa frekuenca kloku dhe tensione në të cilat operojnë që të shfrytëzojnë me pak fuqi dhe energji).

Në Fig. 4 paraqitet kursimi potencial i fuqisë për një server për tre kloke të ndryshme: 2,4 GHz, 1,8 GHz dhe 1 GHz.
![Pasted image 20260407154920.png](/img/user/Pasted%20image%2020260407154920.png)

3. Dizajnimi për raste tipike. Duke marrë parasysh që PMD-të dhe laptopët shpesh janë “të papunë”, atëherë iu ofrojnë memories dhe kujtesës një mod pune me gjendje të ultë të fuqisë për të kursyer energjinë. Në këtë mod s’mund t’iu qaseni DRAM-it ose DISK-ut derisa të ktheheni në aktivitet të plotë për shkrim/lexim. 
4. Overclocking-u Nga viti 2008 Inteli ofrojë “ turbo modin” i dedikuar që çipi të punojë me takt më të lartë për periudha të shkurta kohore. Në këtë mod rritet fuqia konsumuese e procesorit duke gjeneruar kështu më shumë nxehtësi. P.sh. 3.3 GHz Core i7 mund të ekzekutojë shkurt për 3.6 GHz. (“duke shkyçur të gjitha bërthamat tjera dhe duke mbetur vetëm ajo me klok më të lartë”)

### Procesorët me shumë bërthama

Disa procesorë brenda nje çipi. Shumica e CPU-ve moderne kanë shumë bërthama (nga 2 në 64 e mw lart). Performanca me të gjitha bërthamat ose me disa bërthama është një metrikë shumë e rëndësishme. Jo të gjitha bërthamat janë të barabarta: dallojnë në performance dhe efikasitetit, ose dallojnë në klokat e tyre.
Intel dhe AMD tani rrisin numrin e bërthamave përgjatë gjeneratave, pra një CPU me dy bërthama është pothuajse si dy CPU me një bërthamë të ngjitur së bashku. CPU-të me katër bërthama është si 4 CPU me një bërthamë të ngjitur së bashku.

![Pasted image 20260407155658.png](/img/user/Pasted%20image%2020260407155658.png)
![Pasted image 20260407155710.png](/img/user/Pasted%20image%2020260407155710.png)
![Pasted image 20260407155728.png](/img/user/Pasted%20image%2020260407155728.png)
![Pasted image 20260407155741.png](/img/user/Pasted%20image%2020260407155741.png)
![Pasted image 20260407155811.png](/img/user/Pasted%20image%2020260407155811.png)

### Shkallëzimi i transistorëve

Madhësia karakteristike- Madhësinë minimale të transistor-it ose telit përçues në dimension x ose y është zvogëluar nga 10 mikrona në vitin 1971 në 0.032 mikrona në vitin 2011 (rreth 300 X). 
Prodhimi në vitin 2015 është referuar si proces “11 nanometra”. performanca e transistorit shkallëzohet linearisht me një zvogëlim linear në tiparin e madhësisë.
Vonesa në përçues nuk do të thotë që nuk përmirësohet me tiparin e madhësisë
![Pasted image 20260407160114.png](/img/user/Pasted%20image%2020260407160114.png)

## Vlerësimi dhe krahasimi performancave të sistemeve kompjuterike

Fraza kompjuteri “X” është më i shpejtë se kompjuteri “Y” përdorët këtu për të kuptuar qe execution time (koha e ekzekutimit) është me e voglë në “X” se në “Y” për taskun e dhënë.
Në veçanti nëse “X” është n-herë (ku n > 1) më i shpejtë se “Y” do të thotë se:
$$ n = \frac{koha \space e  \space ekezekutimit  \space te  \space Y}{koha \space e   \space ekezekutimit \space te \space X}$$
Vlera reçiproke e kohës së ekzekutimit është reçiprokja e performancës së kompjuterit.
$$ n = \frac{koha \space e  \space ekezekutimit  \space te  \space Y}{koha \space e   \space ekezekutimit \space te \space X}=\frac{\frac{1}{performanca \space Y}}{\frac{1}{performanca \space X}}=\frac{performanca X}{performanca \space Y}$$
**Koha e ekzekutimit mund të llogaritet si koha që merr procesori për të kryer këtë operacion**.

Në praktikë, programet janë shumë më komplekse dhe ndikohen nga shumë faktorë: sasia e të dhënave që duhet të përpunohen, shpejtësia e memories, shpejtësia e disqeve dhe shumë faktorë tjerë.
Në esencë të gjithë procesorët janë të konstruktuar të përdorin klokun ekzekutues në një normë konstante. Kjo kohë diskrete quhet: ticks, clock ticks, clock periods, cloks, cycles, ose clock cycles.

**Pipeline** është një teknikë për rritjen e performancës së procesorëve në kompjuter. Kjo teknikë ndan procesin e ekzekutimit të një instruksioni në faza të ndryshme dhe e lë procesorin të përpunojë disa instruksione në të njëjtën kohë, në një proces të përkryer të punës. Procesorët modernë përdorin pipeline për të përmirësuar performancën dhe për të lejuar që një instruksion të jetë në proces të ekzekutimit ndërkohë që procesori ekzekuton një tjetër instruksion.
P.sh. në një procesor (me një bërthamë- uniprocessor) që përdor pipeline, ekzekutimi i një instruksioni ndahet në disa faza të ndryshme, siç janë nxjerrja e instruksionit nga memoria, dekodimi i instruksionit, ekzekutimi i instruksionit dhe shkrimi i rezultatit. Procesori i ndan këto faza dhe procesorët me pipeline mund të përpunojnë disa instruksione në të njëjtën kohë. Kjo teknikë rrit performancën e procesorëve duke lejuar ekzekutimin e një instruksioni të ndjekur menjëherë pas ekzekutimit të një instruksioni tjetër në proces të përkryer të punës.

Ne kete menyre, pipeline lejon qe procesori te bej shume instruksione ne te njejten kohe qe rrit performancen e procesoreve.

Një shembull i ekzekutimit pipeline me një uniprocessor mund të jetë mbledhja e dy numrave: 
1. Marrja e dy numrave nga memoria dhe vendosja e tyre në regjistrat e procesorit 
2. Ekzekutimi i operacionit të mbledhjes midis dy regjistrave. 
3. Vendosja e rezultatit të mbledhjes në regjistrin e procesorit që përdoret për ruajtjen e rezultateve matematikore.

**Pipeline në një uniprocessor nuk mund të quhet paralelizëm i vërtetë, sepse vetëm një instruksion ekzekutohet në një kohë të caktuar.**

### Formula n shi

![Pasted image 20260408131515.png](/img/user/Pasted%20image%2020260408131515.png)
$$Frekuenca \space e \space klokut_{B} = \frac{nr.cikleve \space te \space kolkut \space CPU_{B}}{koha \space e \space CPU_{B}} = \frac{1.2 * cikle \space klokut_{A}}{6s}$$

$$nr. cikleve \space te \space klokut_{A} = frekuenca \space e \space klokut_{A} * koha \space e \space CPU_{A}=2GHz*10s=20*10^{9}$$

$$Frekuenca \space e \space klokut_{B} = \frac{1.2*20*10^{9}}{6s}=4GHz$$

## Koha e CPU-së (Koha e ekzekutimit të CPU-së)

CPU time është koha është koha ndërmjet fillimit dhe përfundimit të ekzekutimit të një programi të caktuar.

$$koha \space e \space CPU = numri \space i \space cikleve \space te \space klokut \space te \space CPU \space per \space nje \space program * koha \space e \space ciklit \space te \space kolkut$$

$$koha \space e \space CPU = \frac{numri \space i \space cikleve \space te \space klokut \space te \space CPU \space per \space nje \space program}{frekuenca \space e \space kolkut}$$

**Definojmë numrin e instruksioneve (instruction count) –Ic për një program si numër të instruksioneve të ekzekutuara të makinës për atë program deri sa të ekzekutohet komplet ose për një interval kohor të përcaktuar.**

Nëse njohim numrin e cikleve të klokut dhe numrin e instruksioneve për një ekzekutim të caktuar të një programi të caktuar, atëherë mund të llogarisim numrin mesatar të cikleve të klokut për instruksion **CPI (Clock Cicle per Instruction)**
$$CPI = \frac{numri \space i \space cikleve \space te \space klokut \space te \space CPU \space per \space nje \space program}{numri \space i \space instruksioneve (IC)}$$

![Pasted image 20260408132448.png](/img/user/Pasted%20image%2020260408132448.png)

$$koha \space e \space CPU = CPI *Ic*T_{clk} = \frac{CPI*Ic}{f_{clk}}$$

ku $f_{clk}$ paraqet frekuencen e klokut te procesorit.
Një tjetër metrikë e zakonshme e performancës për një procesor është norma (shkalla) me të cilën ekzekutohen instruksionet, të shprehura si **miliona instruksione për sekondë (MIPS)**. E referuar MIPS rate.
$$t_{CPU}= CPI *Ic*T_{clk}$$

$$MIPS = \frac{Ic}{t_{CPU}*10^6}=\frac{Ic}{CPI*Ic*T_{clk}*10^6}=\frac{f_{clk}}{CPI*10^6}$$

Fatkeqësisht është vështirë të ndërrohet njëri parametër i izoluar komplet prej tjerëve sepse teknologjia bazë është e involvuar në ndërrimin e tjetrës karakteristikë:
1. **Numri i Instruksioneve për një program** —Përcaktohet nga programi, ISA (seti i instruksioneve) dhe teknologjia e compiler-it 
2. **Mesatarja e cikleve për Instruksion** —Përcaktohet nga harduare-i i CPU-së 
3. **Koha e ciklit të klokut** – Përcaktohet nga teknologjia e harduerit dhe organizimi

### Detyra 1

![Pasted image 20260408133107.png](/img/user/Pasted%20image%2020260408133107.png)
![Pasted image 20260408133129.png](/img/user/Pasted%20image%2020260408133129.png)
![Pasted image 20260408133140.png](/img/user/Pasted%20image%2020260408133140.png)
### Detyra 2

![Pasted image 20260408133200.png](/img/user/Pasted%20image%2020260408133200.png)

## Ligji i Amdal-it

**Përdoret për të gjetur përmirësimin maksimal të mundshëm të sistemit kompjuterik kur vetëm një pjesë e sistemit është përmirësuar.**

Ligji i Amdahl-it definon “përmirësimin e shpejtësisë”-speedup-in që mund të fitohet duke shfrytëzuar një përmirësim të një tipari të veçantë.

Çka është speedup-i?
**Supozojmë që kemi bërë një përmirësim në kompjuter i cili do të përmirësojë performancën e tij kur aj përmirësim shfrytëzohet.**

Pra, Speedup tregon se sa me shpejt ekzekutohet një “task” kur shfrytëzohet kompjuteri me përmirësim në krahasim me kompjuterin origjinal (pa përmirësim).
Konsideroni qe një program ekzekutohet me vetëm një procesor. Lë të jetë T(1) koha e përgjithshme e ekzekutimit të këtij programi me shfrytëzimin e single processor-it (koha e ekzekutimit të programit në një bërthamë), ndërsa T(N) lë të jetë koha e ekzekutimit të programit në Nbërthama (procesorë). Atëherë,
![Pasted image 20260408134827.png](/img/user/Pasted%20image%2020260408134827.png)

Nëse vendosni N procesorë, a do të duhet të fitoni speedup-in n herë?
Gjithmonë ekziston një pjesë e operacionit total që është në mënyrë serike (sekuenciale) dhe nuk mund të paralelizohet pavarësisht se çfarë bëni.
Në rastin e paralelizmit, nëse shënojmë me P pjesën e programit që mund të paralelizohet (ashtu që të fitohet nga paralelizmi), dhe (1 − P) është pjesa që nuk mund të paralelizohet - mbetet serike (sekuenciale), atëherë përmirësimi maksimal i shpejtësisë që mund të arrihet me N procesorë është:
![Pasted image 20260408135253.png](/img/user/Pasted%20image%2020260408135253.png)
![Pasted image 20260408135309.png](/img/user/Pasted%20image%2020260408135309.png)

Ky ekuacion është paraqitur në Fig. 24. Mund të nxirren dy rezultate të rëndësishme:
1. Nëse P është e vogël, përdorimi i procesorëve paralel ka efekt të vogël. 
2. Nëse N i afrohet infinitit, atëherë përmirësimi maksimal i shpejtësisë (speedup-i) kufizohet me 1/(1 – P), dhe nuk ka ndikim rritja e numrit të procesorëve.

P.sh nëse P = 90%, atëherë 1- P= 10%, atëherë problemi mund të përshpejtohet maksimumi me faktorin 10, pa marrë parasysh sa është vlera e N. Për këtë arsye procesimi paralel është i dobishëm vetëm për një numër të vogël të procesorëve.
![Pasted image 20260408135413.png](/img/user/Pasted%20image%2020260408135413.png)

*Pse nuk mund të arrihet paralelizmi 100% në procesorët me shumë bërthama?*
Keni paralelizëm 100% kur të gjitha bërthamat janë duke kryer punë gjatë gjithë kohës. D.m.th kur edhe bërthamat idle (të pa puna) llogarisin diçka. Varet nga programi që ekzekutoni në sistem. Është vështirë të gjesh një program që mund të jetë plotësisht paralel. Në inxhinieri kompjuterike mund të ekzistoj ndonjë shembulli programit si llogaritja e mbledhjes së një bashkësi numrash. Numrat mund të ndahet në mënyrë të barabartë në procesorë të shumtë. Kështu, secili procesorë do të prodhojë një shumë të parciale. Mirëpo, krejt në fund, një numër i vetëm nga një grup i reduktuar i procesorëve do të kërkohet për të grumbulluar rezultatet e pjesshme. Pra, paska punë që mund të ekzekutohen vetëm sekuencialisht. Mund të theksohet se edhe nëse keni një algoritëm paralel, mund të mos funksionojë përtej një niveli të caktuar paralelizmi.

![Pasted image 20260408140805.png](/img/user/Pasted%20image%2020260408140805.png)

Ligji i Amdalit na jep një mënyrë të shpejtë për të gjetur përmirësimin e shpejtësisë (speedup-in e përgjithshëm) nga disa përmirësime, gjë që varet nga dy faktorë: 
1. Pjesa e kohës (fraction time) së llogaritjes në kompjuterin original (Fractionenhanced ) që mund të konvertohet për të marrë avantazhin e përmirësimit.
P.sh. nëse 20 sekondat e kohës së ekzekutimit të një programi që merr 60 sekonda në total mund të përdoren si një përmirësim, atëherë fraksioni është 20/60. Ky raport quhet Raporti i përmirësimit = Fraction enhanced dhe është çdoherë më i vogël se 1.
2. Përmirësimi i fituar nga mënyra e ekzekutimit të përmirësuar (Speedup enhanced) 
d.m.th. sa më shpejt do të funksiononte detyra (tasku) nëse mënyra e përmirësuar do të përdorej për të gjithë programin P.sh. Nëse një pjesë e programit merr 2 sekonda në mod përmirësimi, ndërsa 5 sekonda në mod origjinal, atëherë përmirësimi është 5/2. Vërehet se Speedupenhanced është çdoherë më i madh se 1.

Speedup i përgjithshëm është raporti i kohëve të ekzekutimit (pa përmirësim/me përmirësim)
![Pasted image 20260408141603.png](/img/user/Pasted%20image%2020260408141603.png)

![Pasted image 20260408141622.png](/img/user/Pasted%20image%2020260408141622.png)
![Pasted image 20260408141640.png](/img/user/Pasted%20image%2020260408141640.png)

## Permbledhje

Vlerësimi i përformancës së CPU-së: 
Kur kompjuteri përdor CPU-në që funksionon me një shpejtësi konstante të clokut ose frekuencë e klokut f.
![Pasted image 20260408141745.png](/img/user/Pasted%20image%2020260408141745.png)
Shpejtësia e klokut të CPU-së varet nga organizimi (dizajni) specifik i CPU-së dhe teknologjia e implementimit të harduerit (VLSI) e përdorur. 
Prej këtu: *Një instruksion i vetëm i makinës mund të marrë një ose më shumë cikle të CPU-së për t'u përfunduar të quajtur si Ciklet për Instruksion (CPI)*.

Disa nga instruksionet e procesorit që kërkojnë vetëm një cikël kloku për të ekzekutuar janë: 
**MOV:** Ky instruksion i lejon procesorit të lëviz një vlerë të dhënë nga një lokacion në tjetrin brenda memories se kompjuterit ose ndërmjet regjistrave të ndryshëm. Shpesh njihet si instruksion “Copy” sepse bën kopjimin e te dhënës dhe e vendos në një lokacion të ri, pa ndryshuar të dhënat origjinale. 
**ADD:** Ky instruksion i lejon procesorit të shtojë dy vlera dhe të ruajë rezultatin në një regjistër të caktuar. 
**SUB:** instruksioni SUB është një lloj instruksioni që përdoret në procesorët kompjuterikë për të zbritur një vlerë nga një tjetër. Zakonisht përdoret në operacionet aritmetike, ku dy vlera duhet të zbriten nga njëra-tjetra për të marrë një rezultat.

Instruksionet e procesorit janë pjesë e kodit të programit dhe zakonisht ruhen në memorien kryesore (RAM) të sistemit kompjuterik, në disa segmente të caktuara të kësaj memorie të njohura si segmente të kodit. Këto segmente ruajnë kodin e programit, përfshirë instruksionet dhe të dhënat.
Pasi MM është më e ngadaltë se regjistrat e procesorit, instruksionet por edhe të dhënat e tjera të programit kopjohen në nivele të ndryshme të memories (për shembull, Cache) në mënyrë që të përmirësohet shpejtësia e ekzekutimit të programit.
Kur një program është gati për të ekzekutuar një instruksion, CPU kopjon instruksionin nga memoria kryesore dhe e vendos atë në regjistrin e instruksioneve (IR-instruction register). Pastaj CPU e interpreton instruksionin dhe e ekzekuton atë, duke përdorur regjistrat e tjera të procesorit si dhe nëse është e nevojshme, duke kryer akses në memorien e kryesore për të përpunuar të dhëna të tjera.

Një program specifik “A” për t’u ekzekutuar në një makinë specifike (CPU), ka parametrat e mëposhtëm: 
1. Numrin total të instruksioneve të ekzekutuara për program (Ic) 
2. Numri mesatar i cikleve për instruksion (CPI mesatare)
![Pasted image 20260408142714.png](/img/user/Pasted%20image%2020260408142714.png)
3. Koha e ciklit të makinës (CPU-së) 

Koha e CPU-së varet nga programi i cili ekzekutohet, dukë përfshirë: 
- Numrin e instruksioneve që ekzekutohen 
- Llojet e instruksioneve të ekzekutuara dhe frekuenca
![Pasted image 20260408142852.png](/img/user/Pasted%20image%2020260408142852.png)

![Pasted image 20260408143013.png](/img/user/Pasted%20image%2020260408143013.png)

![Pasted image 20260408144444.png](/img/user/Pasted%20image%2020260408144444.png)
![Pasted image 20260408144507.png](/img/user/Pasted%20image%2020260408144507.png)
![Pasted image 20260408144517.png](/img/user/Pasted%20image%2020260408144517.png)
![Pasted image 20260408144541.png](/img/user/Pasted%20image%2020260408144541.png)

![Pasted image 20260408144427.png](/img/user/Pasted%20image%2020260408144427.png)

THE END!