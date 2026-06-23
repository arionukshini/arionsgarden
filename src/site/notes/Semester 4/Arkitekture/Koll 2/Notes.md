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

Kontrolli i transferit të të dhënave nga një pajisje e jashtme për procesorin mund të përfshijë sekuencën e hapave vijues:
1. Procesori ‘merr në pyetje’ modulin I/O për të kontrolluar statusin e pajisjes së bashkangjitur. 
2. Moduli I/O i kthen statusin e pajisjes 
3. Nëse pajisja është operacionale dhe e gatshme për të transmetuar, procesori kërkon transferimin e të dhënave, përmes një komande në modulin I/O. 
4. Moduli I / O merr një njësi të të dhënave (p.sh., 8 ose 16 bit) nga pajisje e jashtme. 
5. Të dhënat transferohen nga moduli I / O te procesori.

#### Komunikimi i procesorit

Dekodimi i komandës: Moduli I / O pranon komandat nga procesori, të cilat dërgohen zakonisht si sinjale në busin e kontrollit, p.sh disku magnetik.

#### Komunikimi i pajisjes I/O

![Pasted image 20260622180625.png](/img/user/Pasted%20image%2020260622180625.png)
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
![Pasted image 20260622183327.png](/img/user/Pasted%20image%2020260622183327.png)

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

![Pasted image 20260622184516.png](/img/user/Pasted%20image%2020260622184516.png)

**Regjistrat e brendshëm të CPU**
- Numëruesi i programit (PC) = adresa e instruksionit 
- Regjistri i instruksionit (IR) = instruksioni që është duke u ekzekutuar 
- Akumulatori (AC) = regjistër i përkohshëm

**Lista e pjesëshme e kodeve të operacionit**
- 0001 (1H) = ngarko akumulatorin me përmbajtje nga memoria 
- 0010 (2H) = ruaje AC në memorie 
- 0101 (5H) = mbledh AC me përmbajtjen e memories

![Pasted image 20260622184708.png](/img/user/Pasted%20image%2020260622184708.png)

![Pasted image 20260622215048.png](/img/user/Pasted%20image%2020260622215048.png)
![Pasted image 20260622215105.png](/img/user/Pasted%20image%2020260622215105.png)
![Pasted image 20260622215119.png](/img/user/Pasted%20image%2020260622215119.png)
![Pasted image 20260622215148.png](/img/user/Pasted%20image%2020260622215148.png)
![Pasted image 20260622215203.png](/img/user/Pasted%20image%2020260622215203.png)
![Pasted image 20260622215216.png](/img/user/Pasted%20image%2020260622215216.png)
![Pasted image 20260622215240.png](/img/user/Pasted%20image%2020260622215240.png)

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

![Pasted image 20260622221003.png](/img/user/Pasted%20image%2020260622221003.png)

Pajisjet periferike (Device) gjenerojnë kërkesa për ndërprerje kur kanë nevojë për shërbim nga CPU-ja. Këto kërkesa dërgohen te **Interrupt Controller**, i cili menaxhon, prioritizon dhe përcjell ndërprerjet drejt procesorit.
![Pasted image 20260622221253.png](/img/user/Pasted%20image%2020260622221253.png)

CPU-ja mund të pranojë dy lloje kryesore të ndërprerjeve:
- **Maskable Interrupts** – ndërprerje që mund të çaktivizohen ose injorohen përkohësisht nga procesori. 
- **Non-Maskable Interrupts (NMI)** – ndërprerje kritike që nuk mund të injorohen dhe duhet të trajtohen menjëherë.
Ky mekanizem mundeson qe procesori te reagoje ne menyre efikase.

![Pasted image 20260622222628.png](/img/user/Pasted%20image%2020260622222628.png)

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

![Pasted image 20260622223512.png](/img/user/Pasted%20image%2020260622223512.png)
Fig. 13.a Rrjedha e programit të kontrolluar pa interrapte

![Pasted image 20260623103155.png](/img/user/Pasted%20image%2020260623103155.png)
Fig. 13.b Rrjedha e programit të kontrolluar me interrapte: pritja e shkurtë

![Pasted image 20260623103223.png](/img/user/Pasted%20image%2020260623103223.png)
Fig. 13.c Rrjedha e programit të kontrolluar me interrapte: pritja e gjatë

### Interruptet dhe Cikli i Instruksionit

Me përdorimin e interrupteve, procesori mund të vazhdojë ekzekutimin e instruksioneve të tjera gjatë kohës që një operacion I/O është në progres.

Kur pajisja eksterne është e gatshme të pranojë më shumë të dhëna ose kërkon shërbim, moduli I/O dërgon një sinjal kërkese për ndërprerje procesorit.

Procesori: 
- pezullon përkohësisht ekzekutimin e programit aktual, 
- kalon te rutina e trajtimit të ndërprerjes (Interrupt Handler),
- realizon shërbimin për pajisjen I/O, 
- dhe më pas vazhdon ekzekutimin normal të programit.

![Pasted image 20260623123505.png](/img/user/Pasted%20image%2020260623123505.png)

SO* janë përgjegjës për pezullimin e programit të userit dhe më pas rifillimin e tij në të njëjtën pikë.

#### Serviset (shërbimet) e Sistemit Operativ 
Zhvillimi i programit
Ekzekutues i programeve 
Detektimi i gabimeve dhe përgjigja 
Kalkulimi (mbajtja e evidencave)
Sistemi Operativ është menaxher i resurseve

Në fazën e interraptit, procesori kontrollon për të parë nëse ka ndodhur ndonjë ndërprerje, e treguar nga prania e sinjalit të ndonjë interrapti. Nëse nuk ka ndërprerje në pritje, procesori vazhdon te faza e marrjes (fetches) dhe merr instruksionet e ardhshme të programit aktual.
![Pasted image 20260623124045.png](/img/user/Pasted%20image%2020260623124045.png)

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
![Pasted image 20260623125539.png](/img/user/Pasted%20image%2020260623125539.png)

#### Trajtimi i interrapteve të mbivendosura (Nested i Interrupts)

Programi i përdoruesit ekzekutohet normalisht derisa ndodh interrupt-i X. Procesori kalon te Interrupt Handler X, ruhet ne stack kur kalon tek Y. Gjatë ekzekutimit të tij mund të ndodhë një interrupt tjetër (Y) me prioritet më të lartë (Fig. 17)
![Pasted image 20260623125655.png](/img/user/Pasted%20image%2020260623125655.png)

