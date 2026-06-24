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

![Pasted image 20260622160304.png](/img/user/Semester%204/Images/Pasted%20image%2020260622160304.png)

### Programimi ne softuer

Kompjuteret perdorin programimin ne softuer, ne vend te ndryshimit te harduerit.

Çdo instruksion: 
- interpretohet nga interpretuesi i instruksioneve; 
- gjeneron sinjale kontrolluese për harduerin.

**Epersia kryesore** - funksioni i sistemit ndryshohet përmes softuerit, pa ndryshuar harduerin.
![Pasted image 20260622160543.png](/img/user/Semester%204/Images/Pasted%20image%2020260622160543.png)

## CPU

![Pasted image 20260622160729.png](/img/user/Semester%204/Images/Pasted%20image%2020260622160729.png)

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
![Pasted image 20260622162420.png](/img/user/Semester%204/Images/Pasted%20image%2020260622162420.png)

## Moduli I/O

Të gjitha pajisjet I/O janë më të ngadalshme se memoria kryesore (dhe CPUja), prandaj duhen modulet I/O.
![Pasted image 20260622162611.png](/img/user/Semester%204/Images/Pasted%20image%2020260622162611.png)

Pajisjet e jashtme zakonisht nuk lidhen direkt në basin e sistemit kompjuterik. Moduli I/O është një interfejs (ndërfaqe) për pajisjet e jashtme (periferikët) me CPU dhe Memorien.

Funksionet kryesore të një moduli H/D (I/O Module) përfshijnë: 
- Kontroll dhe timing 
- Komunikimin e procesorit 
- Komunikimin e pajisjes H/D 
- Baferimin e të dhënave 
- Zbulimin e gabimit

#### Kontroll dhe timing

Kontrolli i transferit të të dhënave nga një pajisje e jashtme për procesorin mund të përfshijë sekuencën e hapave vijues:
1. Procesori ‘merr në pyetje’ modulin I/O për të kontrolluar statusin e pajisjes së bashkangjitur. 
2. Moduli I/O i kthen statusin e pajisjes 
3. Nëse pajisja është operacionale dhe e gatshme për të transmetuar, procesori kërkon transferimin e të dhënave, përmes një komande në modulin I/O. 
4. Moduli I / O merr një njësi të të dhënave (p.sh., 8 ose 16 bit) nga pajisje e jashtme. 
5. Të dhënat transferohen nga moduli I / O te procesori.

#### Komunikimi i procesorit

Dekodimi i komandës: Moduli I / O pranon komandat nga procesori, të cilat dërgohen zakonisht si sinjale në busin e kontrollit, p.sh disku magnetik.

#### Komunikimi i pajisjes I/O

![Pasted image 20260622180625.png](/img/user/Semester%204/Images/Pasted%20image%2020260622180625.png)
Fig. 6 paraqet organizimin e brendshëm të një moduli hyrës/dalës dhe komunikimin e tij me CPU-në dhe pajisjen periferike.

#### Baferimi i të dhënave

Baferimi është i nevojshëm për shkak të mospërputhjes së shpejtësisë ndërmjet procesorit, memories dhe pajisjeve periferike gjatë transferimit të të dhënave.

*Një bafer është një hapësirë e memories që përdoret për ruajtjen e përkohshme të të dhënave gjatë transferimit të tyre nga një komponent në tjetrin.*

Print buffering quhet spooling.

YouTube player mbanë ca hapësirë në memorie, që quhet bafer, ku para-ngarkon një numër frames kornizash paraprakisht, dhe vazhdon ta shtojë atë në të njëjtën kohë video shfaqet.

## Basi i sistemit (System Bus)

Basi i sistemit mundëson shkëmbimin e të dhënave, adresave dhe sinjaleve kontrolluese ndërmjet komponentëve të sistemit kompjuterik.

**Komponentët kryesorë të Basit të Sistemit:**

**Data Bus:** përdoret për transferimin dykahësh të të dhënave ndërmjet CPUsë, memories dhe moduleve H/D. Gjerësia e tij (p.sh. 32-bit ose 64-bit) ndikon në sasinë e të dhënave që transferohen në një operacion. 
**Address Bus:** përdoret për transferimin e adresave të memories dhe pajisjeve H/D, komunikim njekahesh.
**Control Bus:** përdoret për transmetimin e sinjaleve kontrolluese dhe sinkronizuese, si: Read, Write, Interrupt, Clock, Reset. 

Performanca e sistemit kompjuterik ndikohet drejtpërdrejt nga karakteristikat e Basit të Sistemit. **Performanca e bus-it varet kryesisht nga:**

**Gjerësia e bus-it (Bus Width):** përcakton sa bita mund të transferohen njëkohësisht. P.sh.: një Data Bus 32-bit transferon 32 bit në një cikël, ndërsa një Data Bus 64-bit transferon 64 bit në një cikël. 
**Frekuenca e punës:** përcakton sa herë në sekondë realizohen transferimet e të dhënave. 
**Shpejtësia e transferimit:** varet nga kombinimi i gjerësisë së bus-it dhe frekuencës së tij.

## Funksionimi i Kompjuteritit

Në formën më të thjeshtë, përpunimi i instruksioneve përbëhet nga dy hapa kryesorë:
1. Fetch Cycle (Cikli i sjelljes së instruksionit): Procesori lexon (fetch) instruksionin nga memoria kryesore. 
2. Execute Cycle (Cikli i ekzekutimit): Procesori ekzekuton instruksionin e sjellur.

Në fillim të çdo cikli të instruksionit, procesori sjell instruksionin nga memoria duke përdorur adresën e ruajtur në regjistrin: **PC (Program Counter)**. 
Pas çdo sjelljeje të instruksionit: 
- procesori zakonisht e rrit automatikisht vlerën e PC-së; 
- në mënyrë që të sjellë instruksionin vijues nga adresa pasuese e memories.

### Sjellja dhe ekzekutimi i instruksionit (Instruction Fetch and Execute)

Procesori fillimisht sjell instruksionin nga memoria (Fetch Cycle), pastaj e interpreton dhe e ekzekuton atë (Execute Cycle). Ky proces përsëritet vazhdimisht derisa sistemi të ndalet (HALT).
![Pasted image 20260622183327.png](/img/user/Semester%204/Images/Pasted%20image%2020260622183327.png)

Në përgjithësi, veprimet e procesorit ndahen në katër kategori kryesore:
1. Processor–Memory: Transferimi i të dhënave ndërmjet procesorit dhe memories.
2. Processor–I/O: Transferimi i të dhënave ndërmjet procesorit dhe pajisjeve hyrëse/dalëse përmes moduleve I/O.
3. Data Processing: Kryerja e operacioneve aritmetike dhe logjike mbi të dhënat.
4. Control: Ndryshimi i rrjedhës së ekzekutimit të programit. P.sh.një instruksion mund të kërkojë që instruksioni i ardhshëm të merret nga një adresë tjetër e memories. Në këtë rast përditësohet regjistri PC me adresën e re të ekzekutimit.
### Kompjuteri hipotetik

Për të lehtësuar kuptueshmërinë e ekzekutimit të instruksioneve do të supozojmë se kemi një kompjuter hipotetik të thjeshtuar i cili përmban:
- Procesori përmban një regjistër të thjeshtë të të dhënave që quhet Akumulator (AC).
- Instruksionet dhe të dhënat janë me madhësi 16 bit të gjata (gjatësia e fjalës në bit).

Formati i instruksionit siguron 4 bit për opcode (kodin e operacionit) kështu që nuk mund të ketë sa më shumë se $2^4$ = 16 kode të ndryshme të operacionit dhe 12 bit për adresë pra, deri në $2^{12}$ = 4096 (4 K) fjalë të ndryshme mund të adresohen direkt.

#### Të përmbledhim: 
**Formati i instruksionit është:** 
0-3 bit e kodit të operacionit
4-15 bitt e adresave
16 kode të operacioneve
4096 fjalë

**Formati i numrave:**
0 biti i parashenjës
1-15 vlera e numrit

![Pasted image 20260622184516.png](/img/user/Semester%204/Images/Pasted%20image%2020260622184516.png)

**Regjistrat e brendshëm të CPU**
- Numëruesi i programit (PC) = adresa e instruksionit 
- Regjistri i instruksionit (IR) = instruksioni që është duke u ekzekutuar 
- Akumulatori (AC) = regjistër i përkohshëm

**Lista e pjesëshme e kodeve të operacionit**
- 0001 (1H) = ngarko akumulatorin me përmbajtje nga memoria 
- 0010 (2H) = ruaje AC në memorie 
- 0101 (5H) = mbledh AC me përmbajtjen e memories

![Pasted image 20260622184708.png](/img/user/Semester%204/Images/Pasted%20image%2020260622184708.png)

![Pasted image 20260622215048.png](/img/user/Semester%204/Images/Pasted%20image%2020260622215048.png)
![Pasted image 20260622215105.png](/img/user/Semester%204/Images/Pasted%20image%2020260622215105.png)
![Pasted image 20260622215119.png](/img/user/Semester%204/Images/Pasted%20image%2020260622215119.png)
![Pasted image 20260622215148.png](/img/user/Semester%204/Images/Pasted%20image%2020260622215148.png)
![Pasted image 20260622215203.png](/img/user/Semester%204/Images/Pasted%20image%2020260622215203.png)
![Pasted image 20260622215216.png](/img/user/Semester%204/Images/Pasted%20image%2020260622215216.png)
![Pasted image 20260622215240.png](/img/user/Semester%204/Images/Pasted%20image%2020260622215240.png)

Për çdo cikël instruksioni të caktuar, disa gjendje mund të jenë zero dhe tjerat mund të vizitohen më shumë se një herë. 
Përshkrimi i gjendjeve bëhet sa vijon:
- **Llogaritja e adresës së instruksionit (iac)** Përcakton adresën e instruksionit vijues që do të ekzekutohet. Zakonisht, kjo përfshin shtimin e një numri fiks në adresën e instruksionit të mëparshëm. P.sh. nëse çdo instruksion është 16 bit i gjatë dhe memoria organizohet në fjalë me 16 bit, atëherë shtoni 1 në adresën e mëparshme.
- **Sjellja e instruksionit (if)** Instruksioni lexohet nga lokacioni i tije memorues në procesor.
- **Dekodimi i operacionit të instruksionit (iod)** Analizohet instruksioni për të përcaktuar llojin e operacionit që do të kryhet dhe operandit (et) që do të përdoren. 
- **Llogaritja e adresës së operandit (oac)** Nëse operacioni përfshin referencimin e një operandi i cili është në memorie ose në dispozicion nëpërmjet I / O, atëherë përcaktohet adresa e operandit. 
- **Sjellja e operandit (of)** Operandi sjellët nga memoria ose lexohet nga I/O. 
- **Veprimi me të dhënat (do)** Kryen operacionin që lidhet me instruksion. 
- **Llogaritja e adresës së operandit (oac)** 
- **Memorimi i operandit (os)** Shkruan rezultatin në memorie ose jashtë në I/O.

### Interraptet

- Virtualisht të gjithë kompjuterët sigurojnë mekanizëm me anën e të cilëve modulet tjera (p.sh. I/O, memoria) mund ta ndërprejnë procesimin normal të procesorit (sepse janë më të ngadalshme se CPU-ja).
- Interruptet (ndërprerjet) sigurojnë kryesisht një mënyrë për të përmirësuar efikasitetin e procesimit. P.sh. shumë pajisje eksterne janë shumë më të ngadalshme se procesori. 
- "*Një ngjarje që i kërkon CPU-së të ndalojë ekzekutimin e programit aktual dhe të sigurojë ca shërbime në lidhje me ngjarjen*" = **Interrapt**

![Pasted image 20260622221003.png](/img/user/Semester%204/Images/Pasted%20image%2020260622221003.png)

Pajisjet periferike (Device) gjenerojnë kërkesa për ndërprerje kur kanë nevojë për shërbim nga CPU-ja. Këto kërkesa dërgohen te **Interrupt Controller**, i cili menaxhon, prioritizon dhe përcjell ndërprerjet drejt procesorit.
![Pasted image 20260622221253.png](/img/user/Semester%204/Images/Pasted%20image%2020260622221253.png)

CPU-ja mund të pranojë dy lloje kryesore të ndërprerjeve:
- **Maskable Interrupts** – ndërprerje që mund të çaktivizohen ose injorohen përkohësisht nga procesori. 
- **Non-Maskable Interrupts (NMI)** – ndërprerje kritike që nuk mund të injorohen dhe duhet të trajtohen menjëherë.
Ky mekanizem mundeson qe procesori te reagoje ne menyre efikase.

![Pasted image 20260622222628.png](/img/user/Semester%204/Images/Pasted%20image%2020260622222628.png)

#### Polling
CPU-ja periodikisht verifikon çdo pajisje “të shoh” nëse ka nevojë për shërbime. 
- Merr kohën e CPU-së edhe kur nuk ka kërkesa në pritje
- Koha e reagimit rritet.

### Problemi i Pritjes gjatë Operacionev I/O - Transferimi i të Dhënave pa Ndërprerje

Pas çdo operacioni WRITE, procesori duhet të presë derisa printeri ta përfundojë operacionin. 
Gjatë kësaj kohe CPU-ja mbetet joaktive (idle). 
Kjo pritje mund të zgjasë, qindra apo mijëra cikle instruksionesh. 
Si rezultat: 
- procesori nuk shfrytëzohet në mënyrë efikase
- performanca e sistemit zvogëlohet

Ideja Kryesore: Pa mekanizmin e ndërprerjeve, CPU-ja humb shumë kohë duke pritur pajisjet I/O.

Programi I/O përbëhet nga tri pjesë kryesore:
1. Përgatitja e Operacionit I/O 
	- Përgatitja e parametrave të pajisjes. 
	- Kopjimi i të dhënave në buffer. 
2. Ekzekutimi i Operacionit I/O 
	- Dërgohet komanda te pajisja.
	- Procesori pret për përfundimin e operacionit.
	- Mund të përdoret polling për kontroll periodik. 
3. Përfundimi i Operacionit 
	- Kontrollohet rezultati i operacionit. 
	- Vendoset një flag për sukses ose dështim.

![Pasted image 20260622223512.png](/img/user/Semester%204/Images/Pasted%20image%2020260622223512.png)
Fig. 13.a Rrjedha e programit të kontrolluar pa interrapte

![Pasted image 20260623103155.png](/img/user/Semester%204/Images/Pasted%20image%2020260623103155.png)
Fig. 13.b Rrjedha e programit të kontrolluar me interrapte: pritja e shkurtë

![Pasted image 20260623103223.png](/img/user/Semester%204/Images/Pasted%20image%2020260623103223.png)
Fig. 13.c Rrjedha e programit të kontrolluar me interrapte: pritja e gjatë

### Interruptet dhe Cikli i Instruksionit

Me përdorimin e interrupteve, procesori mund të vazhdojë ekzekutimin e instruksioneve të tjera gjatë kohës që një operacion I/O është në progres.

Kur pajisja eksterne është e gatshme të pranojë më shumë të dhëna ose kërkon shërbim, moduli I/O dërgon një sinjal kërkese për ndërprerje procesorit.

Procesori: 
- pezullon përkohësisht ekzekutimin e programit aktual, 
- kalon te rutina e trajtimit të ndërprerjes (Interrupt Handler),
- realizon shërbimin për pajisjen I/O, 
- dhe më pas vazhdon ekzekutimin normal të programit.

![Pasted image 20260623123505.png](/img/user/Semester%204/Images/Pasted%20image%2020260623123505.png)

SO* janë përgjegjës për pezullimin e programit të userit dhe më pas rifillimin e tij në të njëjtën pikë.

#### Serviset (shërbimet) e Sistemit Operativ 
Zhvillimi i programit
Ekzekutues i programeve 
Detektimi i gabimeve dhe përgjigja 
Kalkulimi (mbajtja e evidencave)
Sistemi Operativ është menaxher i resurseve

Në fazën e interraptit, procesori kontrollon për të parë nëse ka ndodhur ndonjë ndërprerje, e treguar nga prania e sinjalit të ndonjë interrapti. Nëse nuk ka ndërprerje në pritje, procesori vazhdon te faza e marrjes (fetches) dhe merr instruksionet e ardhshme të programit aktual.
![Pasted image 20260623124045.png](/img/user/Semester%204/Images/Pasted%20image%2020260623124045.png)

Nëse një interrupt është në pritje atëherë:
1. Procesori e suspendon (ndërpret) ekzekutimin e programit aktual 
2. E ruan adresën e instruksionit vijues (vlerën e PC) dhe të dhënat tjera të nevojshme (thënë shkurt, e memoron kontekstin)
3. E vendos në PC adresën e nënprogramit për trajtimin e ndërprerjes (interrupt handler). Ky nënprogram merret me sherbimin e ndërprerjes dhe është pjesë sistemit operativ. 
4. E proceson ndërprerjen: procesori kalon në ciklin e sjelljes duke e sjellur instruksionin e parë të nënprogramit për trajtimin e ndërprerjes. Ky nenprogram e përcakton llojin e ndërprerjes dhe veprimet e duhura për atë, në rastin tonë e përcakton se cili modul I/O e ka gjeneruar ndërprerjen dhe kalon në ekzekutimin e nënprogramit për modulin përkatës. Kur përfundon nënprogrami i ndërprerjes, procesori kthehet në vendin e ndërprerjes (veprimi i ardhshëm) 
5. E rikthen kontekstin dhe e vazhdon programin e shfrytëzuesit.

### Ndërprerjet e Shumfishta

Ne sisteme reale mund te ket disa interrupte ne te njejten kohe.

#### **Qasja 1: Qaktivizimi i interrupteve**
- Gjate trajtimit te nje interrupti, interruptet e tjera qaktivizohen perkohesisht.
- Interrupt-et e reja mbeten në pritje (pending).
- Pas përfundimit të interrupt-it aktual, procesori kontrollon interrupte e tjera.

Përparësitë e kësaj qasje:
- Implementim i thjeshtë. 
- Interrupt-et trajtohen në rend sekuencial. 

Mangësitë e kësaj qasje: 
- Nuk merr parasysh prioritetin ose urgjencën e pajisjeve. 
- Mund të shkaktojë humbje të të dhënave në pajisje të shpejta komunikimi.

#### **Qasja 2 — Interruptet me Prioritet**

Çdo interrupt ka nivel prioriteti. Një interrupt me prioritet më të lartë mund ta ndërpresë trajtimin e një interrupt-i me prioritet më të ulët. Kjo qasje përdoret në sistemet moderne për trajtim më efikas të pajisjeve kritike.

Përparësitë e kësaj qasje: 
- Reagim më i shpejtë ndaj pajisjeve kritike. 
- Zvogëlon mundësinë e humbjes së të dhënave. 
- Përdoret gjerësisht në sistemet moderne kompjuterike. 

Mangësitë e kësaj qasje: 
- Implementim më kompleks. 
- Kërkon mekanizma për menaxhimin e prioriteteve. 
- Interrupt-et me prioritet të ulët mund të vonohen për një kohë të gjatë

#### Trajtimi i ndërprerjve të shumëfishta - sekuencore

Kur ndodh një interrupt, procesori pezullon përkohësisht programin e përdoruesit. Kontrolli transferohet te rutina përkatëse e interrupt-it (Interrupt Handler X). Gjatë trajtimit të këtij interrupt-i, interruptet të tjera çaktivizohen përkohësisht. - Nëse ndodh një interrupt tjetër (Interrupt Handler Y), ai nuk trajtohet menjëherë, por mbetet në pritje (Fig. 16)
![Pasted image 20260623125539.png](/img/user/Semester%204/Images/Pasted%20image%2020260623125539.png)

#### Trajtimi i interrapteve të mbivendosura (Nested i Interrupts)

Programi i përdoruesit ekzekutohet normalisht derisa ndodh interrupt-i X. Procesori kalon te Interrupt Handler X, ruhet ne stack kur kalon tek Y. Gjatë ekzekutimit të tij mund të ndodhë një interrupt tjetër (Y) me prioritet më të lartë (Fig. 17)
![Pasted image 20260623125655.png](/img/user/Semester%204/Images/Pasted%20image%2020260623125655.png)

# 4 - MEMORIA KESH

Kompjuterë personalë: desktopë, laptopë 
Sisteme me performancë të lartë: serverë, superkompjuterë 
Pajisje mobile: telefona inteligjentë, tabletë 
Sisteme embedded dhe IoT 
Platforma edukative dhe zhvillimore: Raspberry Pi dhe të ngjashme 
Sisteme industriale të automatizimit: PLC dhe kontrollorë industrialë.

Perdorin:
- procesorë multi-core,
- memorie cache me shumë nivele 
- integrim të lartë të funksioneve në një çip (SoC).
- komunikim të shpejtë ndërmjet komponentëve

Hierarkia e memories organizohet nga memoriet:
- më të shpejta dhe më të shtrenjta, 
- drejt më të ngadalta dhe më ekonomike. 
Hierarkia tipike e memories përfshin: 
- Regjistrat (Registers), 
- Cache Memory, 
- RAM,SSD/HDD ose Flash Memory.

**Memoria cache** është një element esencial në sistemet moderne kompjuterike. 
Memoria Cache dhe përdoret për: 
- rritjen e shpejtësisë së qasjes në të dhëna, 
- uljen e vonesës ndërmjet CPU-së dhe memories kryesore,
- përmirësimin e performancës së përgjithshme të sistemit.

## NË PËRGJITHËSI PËR SISTEMIN MEMORUES KOMPJUTERIK

![Pasted image 20260623135247.png](/img/user/Semester%204/Images/Pasted%20image%2020260623135247.png)

**Lokacioni (vendndodhja):** i referohet faktit nëse memoria kompjuterike është interne apo eksterne.

**Kapaciteti:** Kapaciteti i memories tregon sasinë e të dhënave që memoria mund të ruajë.

Për memorien interne: bytes (1 Byte = 8 bits) ose words (8, 16, 32, 64 bit).

Për memorien eksterne: GB, TB, PB.

Procesorët aktual-modern zakonisht kan madhesi fjale, 32 ose 64 bit.

**Njësia e adresueshme** paraqet sasinë minimale të memories që CPU-ja mund ta adresojë drejtpërdrejt.
Çdo lokacion në memorie ka një adresë unike.
Procesori përdor adresat për leximin dhe shkrimin e të dhënave në memorie.

Llojet kryesore: 
1. Byte-addressable memory, ku cdo adresë i referohet: 1 byte (8 bits).
2. Word-addressable memory, ku cdo adresë i referohet: 1 word-i të plotë.

Madhësia e word-it varet nga arkitektura e procesorit. 
Procesor 8-bit → 1 word = 8 bits 
Procesor 16-bit → 1 word = 16 bits
...

Marredhenia ndermjet adresave dhe memories $2^{A}=N$ ku:
A = numri i biteve te adreses
N = numri i njesive te adresueshme

$2^{32} = 4 GB$
RAM-i mbi kufirin 4 GB nuk ka adresa që sistemi 32-bit mund t’ia caktojë dhe, si rezultat, nuk mund të përdoret drejtpërdrejt.

**Njësia e transferit:** Për memorie interne, njësia e transferit është e barabartë me numrin e linjave elektrike brenda dhe jashtë modulit memorues.

**Metoda e qasjes:** Nje tjeter karakteristik e sistemeve memoruese. Kjo perfshim:
- Qasjsen sekuenciale: Memoria eshte e organizuar ne njesi te te dhenave qe quhen rreshta.
- Qasjen direkte: sikurse të qasja sekuenciale, qasja direkte përfshin mekanizmin e përbashkët (share) lexo-shkruaj. Megjithatë blloqet individuale ose rreshtat kanë një adresë unike e bazuar në lokacion fizik.
- Qasjen e rastit (Random access): Çdo lokacion i adresueshem në memorie ka një mekanizëm unik fizikisht të adresueshem.
- Qasjen associative (shoqëruese): Ky është një lloj i qasjes së rastit në memorie që mundëson një krahasim të lokacioneve të dëshiruara të bitit brenda një fjale për një përshtatje specifike dhe për ta bërë këtë për të gjitha fjalët njëkohësisht.

**Parametrat e performances:**
- Koha e qasjes (latency- vonesa): Për memorien me qasje të rastit, kjo është koha e nevojshme që të kryhet operacioni i shkrimit ose leximit.
- Koha e ciklit memorues: Ky koncept aplikohet te memoriet me qasje të rastit dhe përbëhet prej kohës së qasjes plus koha shtesë e kërkuar para se një qasje e dytë mund të fillojë.
- Shpejtësia e transmetimit: Kjo paraqet shpejtësinë me të cilën të dhënat mund të transferohen Brenda apo jashtë njësisë memoruese. Për memorien me qasje të rastit, kjo është e barabartë me 1/(koha e ciklit).

Për memorie që nuk janë me qasje të rastit, vlejnë relacionet e mëposhtme:
![Pasted image 20260623151705.png](/img/user/Semester%204/Images/Pasted%20image%2020260623151705.png)

**Karakteristikat fizike:** Ne memoriet volatile (të avullueshme)-informatat humben kur shkyçet furnizimi me energji elektrike, në kontrast me memoriet nonvoltile që informacioni njëherë ruhet dhe mbetet aty pa u dëmtuar edhe kur nuk ka energji elektrike.
**Organizimi:** për memoriet me qasje të rastit, organizimi është thelbësor. Kjo nënkupton rregullimin fizik të bitëve për të formuar fjalët.

## Hierarkia e memories

- memoria kryesore (qendrore, memoria e punës, primare) - RAM 
- memoria e jashtme (eksterne, sekondare) - hard disqet, memoriet gjysmëperçuese, cloud storage, shiritat magnetik, CD dhe DVD disku etj.

Në përbërje të kompjuterit gjendet edhe memoria fikse ROM (për ruajtje të përhershme të të dhënave – të dhënat shënohen vetëm një herë dhe mund të lexohen sa herë që duam.

*Për shkak të harmonizimit të shpejtësisë në mes të: Procesorit - RAM-it - memories eksterne, përdoret një memorie ndërmjetësuese - **kesh memorie** (memorie e përkohshme)*

Memoria virtuale - trajtohet si memorie me kapacitet më të madh por me shpejtësi të përafërt me memorien qendrore.

Në Fig. 1 është treguar hierarkia e memories e ndarë në nivele. Niveli 1 paraqet memorien më të shpejtë por më të vogël, ndërsa Niveli n paraqet memorien më të ngadaltë por më të madhe.
![Pasted image 20260623162534.png](/img/user/Semester%204/Images/Pasted%20image%2020260623162534.png)

![Pasted image 20260623162836.png](/img/user/Semester%204/Images/Pasted%20image%2020260623162836.png)

Duke shkuar nga lartë-poshtë hierarkisë së memorieve kemi sa vijon:
1. Rënie e kostos për bit 
2. Rritja e kapacitetit
3. Rritja e kohës së qasjes 
4. Zvogëlimi i frekuencës së qasjes në memorie nga procesori

### **Kerneli**

Një program që ekzekutohet gjatë gjithë kohës në kompjuter, është kernel-i.
Kerneli është një program që menaxhon kërkesat input / output nga softueri dhe i përkthen ato në instruksione për CPU-në dhe komponentë të tjera elektronike të një kompjuteri.
![Pasted image 20260623163650.png](/img/user/Semester%204/Images/Pasted%20image%2020260623163650.png)

Kerneli ka kontrollë komplete mbi çdo gjë që ndodh në sistem.
Eshte pjesa e pare e S.O qe ngarkohet gjate startimit.
Kur një kompjuter dështon në “ngritje” kjo nënkupton që kerneli është prishur.

Kerneli siguron shërbimet themelore për pjesët tjera të S.O, zakonisht duke përfshirë këtu menaxhimin e memories, menaxhimin e proceseve, menaxhimin e fajllave dhe menaxhimin I/O.

![Pasted image 20260623175250.png](/img/user/Semester%204/Images/Pasted%20image%2020260623175250.png)

## PRINCIPET E KESH MEMORIES

Në Fig. 5.a paraqitet memoria kryesore (me kapacitet të madh dhe shpejtësi më të ulët) së bashku me memorien kesh, e cila ka kapacitet më të vogël por shpejtësi shumë më të lartë. 
Shfrytëzimi i memories kesh zvogëlon kohën e pritjes së procesorit gjatë marrjes së të dhënave nga memoria kryesore, duke reduktuar numrin e gjendjeve të pritjes (wait states).

![Pasted image 20260623182158.png](/img/user/Semester%204/Images/Pasted%20image%2020260623182158.png)

**Cache memoria** ruan kopje të blloqeve të memories kryesore që përdoren më shpesh, prandaj kur procesori kërkon të lexojë/shkruaj një fjalë nga/në memorie, fillimisht kontrollohet nëse ajo gjendet në cache.
Për shkak të fenomenit të lokalitetit të referencave (locality of reference), kur një bllok i të dhënave sillet në cache, ekziston probabilitet i lartë që procesori ta përdorë përsëri atë adresë memorieje ose adresat fqinje brenda të njëjtit bllok.

**Ekzistojnë dy forma të lokalitetit:**
1. **Lokaliteti hapësinor (Spatial locality):** I referohet fenomenit që, kur një adresë e memories referencohet, ka shumë mundësi që adresat fqinje të referencohen brenda një kohe të shkurtër.
2. **Lokaliteti kohor (Temporal locality):** I referohet fenomenit që, nëse një lokacion i memories është referencuar së fundmi, ka shumë mundësi që të referencohet përsëri në të ardhmen e afërt.

![Pasted image 20260623184009.png](/img/user/Semester%204/Images/Pasted%20image%2020260623184009.png)

CPU-të moderne po ashtu kanë edhe kesh shumë të vogël “L0” cache, i cili shpesh është pak KB.

**Niveli 1 – Level 1 (L1):** niveli më i shpejtë dhe ndodhet brenda çdo bërthame të procesorit. Koha e qasjes zakonisht është më pak se 1 ns. Në procesorët modernë të vitit 2026, madhësia e memories L1 zakonisht varion: 64 KB – 256 KB për L1 Data Cache dhe 64 KB – 256 KB për L1 Instruction Cache.
**Niveli 2 (Level 2):** niveli L2 është më i ngadaltë se L1, por ka madhësi më të madhe. Koha e qasjes zakonisht varion nga 2–10 ns. Në procesorët modern, niveli L2 zakonisht varion nga 512 KB deri në 2 MB për bërthamë te procesorët standardë desktop dhe laptop, ndersa deri në 8 MB ose më shumë për bërthamë te disa procesorë high-end dhe serverë modern.
**Niveli 3(Level 3):** është niveli më i madh i memories kesh dhe njëkohësisht më i ngadalshëm se L1 dhe L2. Koha e qasjes zakonisht është rreth 10–40 ns. Në procesorët modernë të vitit 2026, madhësia e memories L3 zakonisht varion nga 8 MB deri në 64 MB te procesorët desktop dhe laptop, por deri në qindra MB te procesorët e serverave dhe high-end modern. Në shumicën e arkitekturave moderne multicore, niveli L3 është “shared cache”, pra ndahet ndërmjet të gjitha bërthamave të procesorit.

#### Cka nëse nuk gjendet në memorien kryesore (RAM)?
Nëse të dhënat nuk gjenden në RAM, ndodh një page fault dhe SO e kërkon në memorien virtuale. Faqja përkatëse ngarkohet nga disku në RAM, blloku transferohet në cache dhe më në fund fjala te procesori.

#### Si realizohet rrjedha e të dhënave ndërmjet pajisjeve hyrëse/dalëse (I/O), memories kryesore dhe cache memories në arkitekturën klasike dhe moderne të kompjuterëve?

Në sistemet klasike por edhe moderne, të dhënat nga pajisjet I/O nuk kalojnë fizikisht përmes procesorit. Për këtë përdoret permes mekanizimit DMA (Direct Memory Access).
- Pajisja I/O transferon të dhënat direkt në RAM dhe anasjelltans nga RAM në I/O
- Procesori vetëm e kontrollon ose inicializon transferimin.
- Pas përfundimit të transferimit, procesori njoftohet me një ndërprerje (interrupt).

Vetëm kur procesori i lexon këto të dhëna nga RAM-i, ato mund të ngarkohen në cache. Pra, rrjedha tipike është: I/O → RAM → Cache → Procesor dhe jo: I/O → Procesor → RAM.

Per qellime te keshimit memoria kryesore konsiderohet te jete e ndare ne blloqe me madhesi fikse, ku secili bllok perbehet nga K fjale. Prandaj memoria kryesore permban: $M = \frac{2^n}{K}$ blloqe.
Cache memoria perbehet nga m blloqe te quajtura linja (chache lines). Qdo linje permban: K fjale te te dhenave, dhe nje etikete (tag) prej disa bitesh, e cila perdoret per identifikimin e bollokut te memories kryesore te ruajtur ne ate linje cache.

![Pasted image 20260623191834.png](/img/user/Semester%204/Images/Pasted%20image%2020260623191834.png)

Numri i linjave ne kesh memorie është më i vogël se numri i blloqeve ne memorie kryesore (m < M).
Pasi ka më shumë blloqe të MM se sa linja keshi, një linjë individuale nuk mund të jetë në mënyrë unike përherë e dedikuar për një bllok të veçante të memories. Prej këtu, çdo linjë e keshit ka një tag (etiketë) që identifikon se cili bllok i memories aktualisht po ruhet.

![Pasted image 20260623194903.png](/img/user/Semester%204/Images/Pasted%20image%2020260623194903.png)
![Pasted image 20260623195918.png](/img/user/Semester%204/Images/Pasted%20image%2020260623195918.png)

**Kur fjala gjendet në kesh (cache hit),** baferi i adresës dhe baferi i të dhënave janë disabled për komunikim sepse komunikimi bëhet vetëm ndërmjet procesorit dhe cache-it, pa trafik përmes basave te sistemit.
**Kur fjala nuk gjendet në kesh (cache miss),** adresa e dëshiruar ngarkohet në sistem bas dhe të dhënat vijnë përmes baferit të të dhënave edhe në kesh ashtu edhe në procesor.

#### Terminologjia themelore

- Hit: CPU gjen përmbajtjen e adresës së memories në chache. 
- Hit rate (h) është probabiliteti i gjetjes së suksesshmem në cache nga CPU-ja 
- Miss: CPU dështon të gjejë në cache.(shkakton udhëtim në nivele me te thella të hierarkisë së memories) 
- Miss rate (m) është probabiliteti i mungesës në cache dhe është i barabartë me 1-h. 
- Miss penalty: “koha e penaltisë” shoqërohet me shërbimin e mungesës në një nivel partikular të hierarkisë së memories (rezulton në vonesë ekstra –p.sh. është koha për ta “pasqyruar “ bllokun prej memorje- në cache). Pra, koha për të zëvendësuar një bllok prej nivelit më të ulët, duke përfshirë kohën e qasjes në nivel më të ulët + kohën e transferit të bllokut.

### Effective Memory Access Time (EMAT)

Koha e kerkimit ne cache për të “pa” nëse lokacioni i memories është veq aty. Pas cache miss (mungesës në cache), koha për të shkuar në nivele më të thella në hierarkinë e memories.
$$EMAT = T_{C} + m * T_{m}$$
ku m eshte cache miss rate, Tc koha e qasjes dhe Tm eshte miss penalty

Adresa – çdo fjalë (e dhënë) ka një adresë në memorie. Procesori bën një kërkesë për një të dhënë (fjalë) duke gjeneruar adresën e të dhënës së caktuar.
Fjala mund të gjendet në ndonjë nivel më të ultë të hierarkisë dhe vendoset në cache para se me vazhduar. Fjala – njësia “natyrale” e organizimit të memories.

Bllok- Një bashkësi e fjalëve (p.sh block 0).
Set - grup i blloqeve në cache.

## ELEMENTET E PROJEKTIMIT TË KESH-it

Kohë pas kohe iu referohemi përdorimit të keshit në kompjuterët e përformancës së lartë (high-performance computing – HPC).

- Adresat e Kesh-it: Logjike dhe Fizike.
- Politikat e shkrimit: Write through and Write back.
- Madhesia e Kesh-it
- Madhesia e linjes
- Funksioni pasqyrimit: Direkt, Asociative, Set associative
- Numri i niveleve te keshit: Me nje, dy ose tre nivele. I unifikuar ose i ndare.

Algoritmi i zevendesimit:
- I perdorur me se paku se fundmi (Least recently used - LRU)
- I pari brenda i pari jashte (First in first out- FIFO)
- Me se paku i perdorur (Least frequently used - LFU)
- E rastit (Random)

### Adresat e KESH-it

Memoria virtuale është një “mundësi e zgjerimit të memories” që lejon programet të adresojnë memorien nga një pikëpamje logjike, pa marrë parasysh sasinë e memories kryesore të disponueshme fizikisht.
Për të lexuar dhe shkruar nga memoria kryesore, një njësi harduerike e quajtur **Njësia e menaxhimit të memories (MMU) përkthen çdo adresë virtuale në një adresë fizike në memorien kryesore.**

Të gjitha kërkesat hyrëse të të dhënave dërgohen në MMU, e cila përcakton nëse të dhënat duhet të nxirren nga ruajtja në cache apo në RAM.
Kur përdoren adresat virtuale, dizajnuesi i sistemit mund të zgjedh të vendosë cache-in midis procesorit dhe MMU (Fig. 9.a) ose midis MMU dhe memories kryesore.

![Pasted image 20260623212502.png](/img/user/Semester%204/Images/Pasted%20image%2020260623212502.png)

**Epersitë e keshit logjik -** shpejtësia e qasjes në cache është më e shpejtë se sa për një cache fizike, sepse cache mund të përgjigjet përpara se MMU të kryejë një përkthim të adresave. 
**Të metat e keshit logjik –** shumica e sistemeve memoruese virtuale furnizojnë çdo aplikacion me të njëjtën hapësirë të adresave virtuale. Pra, çdo aplikacion shef një një memorie virtuale që starton me adresën 0.

![Pasted image 20260623212613.png](/img/user/Semester%204/Images/Pasted%20image%2020260623212613.png)

![Pasted image 20260623222103.png](/img/user/Semester%204/Images/Pasted%20image%2020260623222103.png)

## Funksioni i pasqyrimit

Zgjedhja e funksionit të pasqyrimit përcakton se si është organizuar keshi Mund të përdoren tre teknik
- Pasqyrimi direkt, 
- Pasqyrimi asociativ, dhe 
- Pasqyrimi set asociativ.

*Gjatë pasqyrimit në kesh, blloku i memories kryesore thjesht kopjohet në kesh dhe faktikisht nuk largohet prej memories kryesore.*

![chrome_VnWPe5vs8L.png](/img/user/Semester%204/Images/chrome_VnWPe5vs8L.png)
![Pasted image 20260623223835.png](/img/user/Pasted%20image%2020260623223835.png)

- Meqenëse ka më shumë blloqe në memorie se sa (blloqe) linja keshi, një linjë individuale nuk mund të jetë në mënyrë unike përherë e dedikuar për një bllok të veçantë. 
- Prej këtu, çdo linjë e keshit ka një tag (etiketë) që identifikon bllokun aktual nga memoria kryesore që po ruhet në linjën (bllokun) e memories kesh. 
- Tagu është zakonisht një pjesë e adresës së memories kryesore!!!

### Pasqyrimi direkt

Një bllok i veçantë i memories kryesore mund të pasqyrohet vetëm në një linjë të veçantë të kesh-it.
Numri i linjës (rreshtit) të kesh-it në të cilin mund të pasqyrohet një bllok i veçantë nga memoria kryesore jepet me shprehjen: 
$$i = j \space modulo \space m$$
i - numri i linjës në memorien kesh 
j - numri i bllokut në memorien kryesore (adresa e bllokut të MM) 
m - numri i tërësishëm i linjave në kesh

![Pasted image 20260623224726.png](/img/user/Pasted%20image%2020260623224726.png)

$m$ blloqet tjera të mëmories kryesore pasqyrohen ne kesh sipas të njëjtës mënyrë, bloku $B_{m}$ i memories pasqyrohet prapë në linjën $L_{0}$ , Blloku $B_{m +1}$ pasqyrohet në linjën $L_{1}$, e kështu më radhë.

Pasi CPU gjeneron një kërkesë në memorie
- Numri i rreshtit të fushës së adresës në memorie kryesore përdoret për t’iu qas linjës së veçante të keshit. 
- Fusha e tagut në adresën e CPU është krahasuar më pas me tagun e linjës në kesh. 
- Nëse dy tagat përputhen, ndodh një hit cache dhe fjala e dëshiruar gjendet në cache. 
- Nëse dy tagat nuk përputhen, një cache miss ka ndodhur. 
- Në rastin e cache miss, fjala e kërkuar duhet të sillet nga memoria kryesore 
- Ajo pastaj ruhet në kesh së bashku me tagun e ri duke zëvendësuar atë të mëparshmen.

![Pasted image 20260624151028.png](/img/user/Pasted%20image%2020260624151028.png)

Funksioni i pasqyrimit implementohet lehtë duke përdorur adresat e memories kryesore. **Me qëllim të qasjes në cache, çdo adresë fizike e memories kryesore mund të shihet si e përbërë nga tre fusha.**

![Pasted image 20260624151356.png](/img/user/Pasted%20image%2020260624151356.png)

**Bitët më pak domëthënës (ẘ)** identifikojnë një fjalë unike ose bajt brenda një blloku të memories kryesore.

**Bitët e mbetur (s)** specifikojnë një prej $2^s$ blloqeve të memories kryesore.

![Pasted image 20260624151728.png](/img/user/Pasted%20image%2020260624151728.png)

### Pasqyrimi asociativ 

**Pasqyrimi plotësisht asociativ (Fully Associative Mapping)**

Blloku nga memoria kryesore mund te vendoset në cilën do linjë të keshit.

Në pasqyrimin plotësisht asociativ: 
- Një bllok i memories kryesore mund të pasqyrohet në çdo linjë të lirë (në dispozicion) të keshit 
- Kjo e bën pasqyrimin plotësisht asociativ më fleksibilitet se pasqyrimin direkt.
- Nëse kesh është i plotësuar, një algoritëm zëvendësues është i nevojshëm për të zëvendësuar një bllok. Algoritmi i zëvendësimit sugjeron që blloku të zëvendësohet nëse të gjitha linjat e cache janë zënë.

![Pasted image 20260624163029.png](/img/user/Pasted%20image%2020260624163029.png)

Në pasqyrimin plotësisht asiociativ, adresa fizike përbehet nga dy fusha: Tagu (etiketa = Block number) dhe Block offset-i (fjala).![Pasted image 20260624163205.png](/img/user/Pasted%20image%2020260624163205.png)

Për të përcaktuar nëse një bllok është në cache, logjika e kontrollit të kesh-it duhet njëkohësisht të shqyrtojë etiketën (tagun) e çdo rreshti për një përshtatje.
Në këtë rast, logjika e kontrollit të cache interpreton një adresë të memories thjesht si një etiketë dhe një fushë fjale.
![Pasted image 20260624163706.png](/img/user/Pasted%20image%2020260624163706.png)

Duhet theksuar se asnjëra nga dy fushat e adresës nuk ka kurrfarë lidhje me numrin e linjave të keshit, pra asnjëra fushë në adresë nuk korrespondon me numrin e linjës, kështu që numri e linjave në kesh nuk përcaktohet nga formati i adresës.
![Pasted image 20260624164442.png](/img/user/Pasted%20image%2020260624164442.png)

![Pasted image 20260624175242.png](/img/user/Pasted%20image%2020260624175242.png)

Me ketë teknikë të pasqyrimit ka një fleksibilitet se cili blok do të zëvendësohet kur një bllok i ri lexohet në kesh. Algoritmet zëvendësuese, dizajnohen për të maksimizuar hit ratio. E metë e pasqyrimit asociativ është kërkesa për qark kompleks për të ekzaminuar etiketat e të gjitha linjave të keshit në paralel.

### Pasqyrimi set asociativ

Pasqyrimi set-asociativ është një kompromis që paraqet pikat e forta të qasjeve direkte dhe asociative duke zvogëluar të metat e tyre. Në këtë rast, keshi përbëhet nga një numër i setave, secili prej të cilave përbëhet nga një numër linjash. Marrëdhëniet janë: 
$m = v \space x \space k$ 
$i = j \space modulo \space v$

i = numri setit në kesh 
j = numri i bllokut në memorie kryesore 
m = numri i linjave në kesh
v = numri i setave 
k = numri i linjave në secilin set

**Një bllok i veçantë i memories kryesore mund të pasqyrohet vetëm në një set keshi të veçantë!!! Kjo referohet si pasqyrim k-menyrësh set-asociativ.**

Kur një blok vendoset në një set të restriktuar në kesh, cache është set asociativ. Në shembullin e mëposhtëm Set-i ka 2 blloqe. 
Bloku 3 nga memoria kryesore (i cili bllok ka 4 fjalë) mund të shkojë vetëm në Cashe SET i = (3 MOD 2) = 1 në cache.
![Pasted image 20260624181319.png](/img/user/Pasted%20image%2020260624181319.png)
**(Adresa e Block-ut) MOD (numri i set-eve në cashe)**

Pra këtu k = 2 atëherë kemi një pasqyrim 2-mënyrësh set asociativ.

![Pasted image 20260624181412.png](/img/user/Pasted%20image%2020260624181412.png)

Me pasqyrim set-asociativ, blloku $B_{j}$ mund të pasqyrohet në ndonjë linjë të set-it j.

![Pasted image 20260624181814.png](/img/user/Pasted%20image%2020260624181814.png)

Me pasqyrim asociativ, çdo fjalë pasqyrohet në shumë linja te keshit. Për pasqyrim set-asociativ, çdo fjalë pasqyrohet në të gjitha linjat e keshit në setin specifik, kështu që blloku Bo pasqyrohet në setin 0 dhe kështu me radhë, prandaj keshi set asociativ mundet fizikisht të implementohet si një k- set asociative kesh.
![Pasted image 20260624182808.png](/img/user/Pasted%20image%2020260624182808.png)

![Pasted image 20260624182914.png](/img/user/Pasted%20image%2020260624182914.png)
![Pasted image 20260624182938.png](/img/user/Pasted%20image%2020260624182938.png)

![Pasted image 20260624184422.png](/img/user/Pasted%20image%2020260624184422.png)

## Algoritmet e zëvendësimit

Kur ngjan një “dështim” kontrolleri i Cache-it duhet të zgjedh një bllok që ta zëvendësojë me të dhënën e dëshiruar.

**Te keshi me pasqyrim direkt:** Vetëm një opcion: vetëm një bllok kërkohet për ta gjetur dhe vetëm një bllok duhet zëvendësuar (zëvendësohet blloku në lokacionin ku blloku ardhës ka për të shkuar). 
Për teknikat e **pasqyrimit asociativ** dhe **set-asociativ** është i nevojshëm një algoritëm zëvendësues për të nxjerrë një bllok nga keshi. 
Për të arritur shpejtësi të lartë, një algoritëm i tillë duhet të implementohet në harduer. 

Përdoren kryesisht katër algoritme zëvendësimi:
1. Least Recently used (LRU)- blloku në setin që është përdorur më së pakti gjatë qëndrimit në kesh- nuk është referencuar për një kohë të gjatë- me gjasë është algoritmi më efektiv. Është lehtë i implementueshëm te pasqyrimi dy-mënyrësh set asociative. 
2. First in First Out (FIFO) -Blloku që ka ndenjur për më shumë kohë në cache. 
3. Least frequently used (LFU) – zëvendëson bllokun nga seti që është referencuar më së paku –me gjasë algoritmi më i thjeshtë. 
4. Random - Përfshinë një bllok të zgjedhur rastësisht

E meta e LRU është kompleksiteti i tij: LRU duhet të mbajë një histori qasjeje për secilin bllok, i cili në fund të fundit ngadalëson keshin.

Performanca e memories në hierarki vlerësohet nga **koha efektive e qasjes** (effective access time)-(EAT).
EAT merr në konsideratë raportin e gjetjes (hit ratio) dhe kohët relative të qasjes në nivelet sukcesive të memories.

EAT për dy nivele të memories jepet me:
$$EAT = H*Access_{C} + (1-H)*Access_{MM}$$
ku **H** eshte **cache hit rate**.
$Access_{C}$ dhe $Access_{MM}$ jane kohet e qasjes per kesh dhe memorie kryesore.

## Teknikat e shkrimit në Cache

Koherenca ndërmjet një fjale në Cache dhe kopjes së saj në memorie duhet të mbahet në çdo kohë. 
Një grup teknikash përdoren për operacionet e shkrimit për blloqet në memorien kryesore për sa kohë janë edhe në Cache.

Jane dy teknika (strategji) bazike kur shkruhet ne cache:
1. Write-through
2. Write-back

**Write –through.** Informata shkruhet në të dyja blloqet, në cache dhe në bllok të nivelit tjetër më poshtë në hierarki. Kjo teknikë mban koherencën ndërmjet informacionit në cache dhe kopjes së tij në memorie dhe e tërë kjo reflekton me koston e kohës shtesë për të shkruar informacion në memorie.
![Pasted image 20260624224030.png](/img/user/Pasted%20image%2020260624224030.png)
![Pasted image 20260624224043.png](/img/user/Pasted%20image%2020260624224043.png)

Nevojitet një Write Buffer ndërmjet Cache-it dhe memories.
Procesori: shkruan te dhënat edhe në Cache edhe në Write buffer
Kontrolleri i memories: shkruan përmbajtjen e buffer-it në memorie. 
Write bufferi është vetëm një FIFO.

**Write-back.** Informacioni shkruhet vetëm në bllok të cache-it. Shkrimi në memorie shtyhet deri kur të vjen nevoja për zëvendësim.
Çdo blloku në cache i jepet një bit i quajtur “dirty bit”, që tregon se të paktën një operacion shkrimi ka ndodhur në bllok.
Në momentin e zëvendësimit shikohet biti i “papastërtisë”, nëse është i vendosur atëherë shkruhet në memorien kryesore, përndryshe blloku mbishkruhet nga blloku i ri.
Koherenca sigurohet vetëm në momentin e zëvendësimit.

![Pasted image 20260624224239.png](/img/user/Pasted%20image%2020260624224239.png)
![Pasted image 20260624224255.png](/img/user/Pasted%20image%2020260624224255.png)


