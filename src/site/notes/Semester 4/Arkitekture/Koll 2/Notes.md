---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/koll-2/notes/"}
---

# Kapitulli 3 - Funksioni i kompjuterit dhe interkoneksioni

## Cka duhet te dish pas ketij kapitulli

Pas ketij kapitulli duhet te jesh ne gjendje te:

- Identifikosh komponentet kryesore te sistemit kompjuterik.
- Shpjegosh arkitekturen baze sipas modelit te von Neumann.
- Kuptosh rolin e regjistrave kryesore te CPU-se.
- Shpjegosh organizimin dhe adresimin e memories.
- Shpjegosh rolin e moduleve hyrese/dalese.
- Pershkruash ciklin e sjelljes dhe ekzekutimit te instruksionit.
- Kuptosh rolin e nderprerjeve ne sistemet kompjuterike.
- Dallosh sistemin me nderprerje nga sistemi pa nderprerje.
- Kuptosh rendesine e interkoneksionit ndermjet komponenteve.

## 1. Pamja e nivelit te larte te kompjuterit

Ne nivel te larte, kompjuteri perbehet nga:

- **CPU (Central Processing Unit)** - njesia qendrore e procesimit.
- **Memoria kryesore** - ruan te dhenat dhe instruksionet.
- **Modulet H/D (I/O Modules)** - mundesojne komunikimin me pajisjet hyrese/dalese.
- **Basi i sistemit** - lidh CPU-ne, memorien dhe modulet H/D.

Funksioni baze i kompjuterit eshte **ekzekutimi i programeve**.

Komponentet shkembajne:

- te dhena,
- adresa,
- sinjale kontrolluese.

Pamja ne nivel te larte eshte e rendesishme sepse ndihmon ne:

- analizen e performances,
- identifikimin e ngushticave,
- permiresimin e besueshmerise se sistemit.

## 2. Arkitektura von Neumann

Shumica e kompjutereve moderne bazohen ne konceptet e arkitektures **von Neumann**.

Idete kryesore:

- Te dhenat dhe instruksionet ruhen ne nje memorie te vetme shkrim-lexim.
- Permbajtja e memories adresohet sipas lokacionit.
- Memoria nuk e di vete se cfare permban.
- I njejti varg bitesh mund te interpretohet si numer, tekst, instruksion, figure, audio, etj.
- CPU-ja dhe programi e percaktojne kuptimin e biteve.
- Instruksionet zakonisht ekzekutohen ne menyre sekuenciale, nje pas nje.
- Rrjedha sekuenciale ndryshon vetem kur ka jump, branch, interrupt, ose ndonje mekanizem tjeter kontrolli.

Per provim: **te von Neumann, instruksionet dhe te dhenat ruhen ne te njejten memorie dhe qasen permes adresave.**

## 3. Programimi ne harduer dhe ne softuer

## 3.1 Programimi ne harduer

Programimi ne harduer nenkupton qe funksioni realizohet fizikisht me nje konfigurim te vecante harduerik.

Karakteristikat:

- Komponentet logjike kombinohen per ruajtje te te dhenave binare dhe per operacione aritmetike/logjike.
- Hardueri projektohet per nje funksion te caktuar.
- Programi eshte i realizuar fizikisht ne harduer.
- Nese duhet funksion tjeter, zakonisht duhet ndryshuar konfigurimi harduerik.

Ideja kryesore: hardueri eshte i specializuar per detyren.

## 3.2 Programimi ne softuer

Te kompjuteret e pergjithshem, funksioni ndryshohet permes **instruksioneve softuerike**, jo duke ndryshuar harduerin.

Cdo instruksion:

- interpretohet nga interpretuesi i instruksioneve,
- gjeneron sinjale kontrolluese per harduerin,
- ben qe hardueri te kryeje veprimin e kerkuar.

CPU-ja perbehet nga:

- interpretuesi i instruksioneve,
- njesia aritmetike-logjike,
- njesite kontrolluese dhe regjistrat.

Perparesia kryesore: **funksioni i sistemit ndryshohet me softuer, pa ndryshuar harduerin.**

## 4. Komponentet kryesore te sistemit kompjuterik

Sistemi kompjuterik ka tre komponente kryesore:

- **CPU**
- **Memoria kryesore**
- **Moduli H/D**

Keta komponente komunikojne permes **basit te sistemit**.

CPU-ja shkemben te dhena me memorien dhe modulet H/D. Per kete perdor regjistra te brendshem.

## 5. Regjistrat kryesore te CPU-se

Regjistrat jane lokacione shume te shpejta brenda CPU-se. Ato ruajne perkohesisht adresa, instruksione dhe te dhena gjate ekzekutimit.

| Regjistri | Emri | Roli |
|---|---|---|
| **PC** | Program Counter | Ruan adresen e instruksionit vijues qe duhet te sillet nga memoria. |
| **IR** | Instruction Register | Ruan instruksionin aktual qe po ekzekutohet. |
| **MAR** | Memory Address Register | Ruan adresen e memories per operacionin e ardhshem lexim/shkrim. |
| **MBR** | Memory Buffer Register | Ruan te dhenat qe lexohen nga memoria ose shkruhen ne memorie. |
| **I/O AR** | Input/Output Address Register | Ruan adresen e pajisjes ose modulit H/D me te cilin komunikon CPU-ja. |
| **I/O BR** | Input/Output Buffer Register | Ruan perkohesisht te dhenat qe shkemben CPU-ja me modulin H/D. |
| **AC** | Akumulatori | Regjister i perkohshem per te dhena dhe rezultate, sidomos ne shembullin e kompjuterit hipotetik. |

## 6. Regjistra te tjere ne procesore moderne

Pervec PC, IR, MAR, MBR, I/O AR dhe I/O BR, procesoret moderne kane edhe shume regjistra te tjere.

- **Regjistra te pergjithshem (GPR)** - perdoren per ruajtje te perkohshme te operandeve, adresave dhe rezultateve.
- **Regjistra statusi / flamujsh** - ruajne gjendjen e rezultateve te operacioneve, si Zero Flag, Carry Flag, Overflow Flag dhe Interrupt Flag.
- **Regjistra kontrolli** - perdoren per kontroll te memories, mbrojtjes dhe menyres se punes se procesorit.
- **Regjistra SIMD / vektoriale** - perdoren per perpunim paralel te te dhenave.

Kapaciteti i regjistrave varet nga arkitektura e procesorit. Ne procesore moderne zakonisht hasen regjistra 32-bit ose 64-bit.

## 7. Njesite funksionale te CPU-se

CPU-ja permban regjistra, por edhe njesi funksionale qe mundesojne ekzekutimin e instruksioneve.

Njesite kryesore:

- **Njesia e kontrollit** - koordinon punen e regjistrave, memories, moduleve H/D dhe njesive ekzekutuese.
- **Njesia e ekzekutimit / ALU** - kryen operacione aritmetike dhe logjike.
- **FPU (Floating Point Unit)** - kryen operacione me numra real, pra me presje levizese.
- **Njesite SIMD / vektoriale** - perpunojne disa te dhena paralelisht.

## 8. Memoria kryesore

Memoria kryesore organizohet si bashkesi lokacionesh memoruese.

Karakteristikat:

- Cdo lokacion ka adrese.
- Adresat jane te numeruara ne menyre sekuenciale: `0, 1, 2, ..., n-1`.
- Cdo lokacion ruan nje vlere binare.
- Vlera mund te jete instruksion ose e dhene.
- Gjatesia e fjales varet nga numri i biteve qe trajtohen si nje njesi.

Shembull nga kapitulli:

Nje memorie prej 96 bitesh mund te organizohet si:

- `12 x 8 bit`
- `8 x 12 bit`
- `6 x 16 bit`
- `96 x 1 bit`
- `1 x 96 bit`

Ideja kryesore: **kapaciteti total mund te jete i njejte, por organizimi i memories mund te ndryshoje.**

## 9. Modulet hyrese/dalese

Moduli H/D eshte elementi i trete kritik i sistemit kompjuterik, bashke me CPU-ne dhe memorien.

Pajisjet e jashtme zakonisht nuk lidhen direkt me basin e sistemit. Ato lidhen permes modulit H/D.

Arsyet:

- Pajisjet periferike jane me te ngadalshme se CPU-ja dhe memoria.
- Pajisjet kane formate te ndryshme te te dhenave.
- Pajisjet kane shpejtesi te ndryshme pune.
- Duhet kontroll, sinkronizim, baferim dhe zbulim gabimesh.

Moduli H/D eshte **nderfaqe** ndermjet pajisjeve te jashtme dhe CPU-se/memories.

## 10. Funksionet kryesore te modulit H/D

Funksionet kryesore:

- **Kontroll dhe timing** - koordinon kur dhe si kryhen transferimet.
- **Komunikim me procesorin** - pranon komanda dhe dergon status/te dhena.
- **Komunikim me pajisjen H/D** - dergon/pranon te dhena nga pajisja periferike.
- **Baferim i te dhenave** - ruan perkohesisht te dhenat per shkak te dallimit te shpejtesive.
- **Zbulim i gabimeve** - detekton probleme gjate transferimit.

Rrjedha tipike e komunikimit:

1. Procesori e pyet modulin H/D per statusin e pajisjes.
2. Moduli H/D kthen statusin.
3. Nese pajisja eshte gati, procesori kerkon transferimin.
4. Moduli H/D merr ose dergon nje njesi te te dhenave.
5. Te dhenat transferohen ndermjet modulit H/D dhe procesorit.

## 11. Baferimi i te dhenave

**Baferimi** eshte ruajtje e perkohshme e te dhenave gjate transferimit.

Pse nevojitet:

- CPU-ja dhe memoria punojne shume shpejt.
- Pajisjet periferike zakonisht punojne me ngadale.
- Baferi e zvogelon problemin e mospershtatjes se shpejtesive.

Shembull:

Kur shtypet nje dokument, sistemi operativ e kopjon dokumentin ne nje bafer printeri. Printeri e merr dokumentin nga baferi me ritmin e vet, ndersa CPU-ja mund te vazhdoje pune te tjera.

Ky proces quhet **spooling**.

Per provim: **baferimi mundeson komunikim me efikas ndermjet komponenteve qe kane shpejtesi te ndryshme.**

## 12. Basi i sistemit

Komunikimi ndermjet CPU-se, memories kryesore dhe moduleve H/D realizohet permes **basit te sistemit**.

Basi i sistemit transferon:

- te dhena,
- adresa,
- sinjale kontrolluese.

Komponentet kryesore te basit:

| Pjesa e basit | Roli |
|---|---|
| **Data Bus** | Transferon te dhena ndermjet CPU-se, memories dhe moduleve H/D. Zakonisht eshte dykahesh. |
| **Address Bus** | Bart adresen e lokacionit memorues ose pajisjes H/D. |
| **Control Bus** | Bart sinjale kontrolluese dhe sinkronizuese si Read, Write, Interrupt, Clock dhe Reset. |

Performanca e basit varet nga:

- **gjeresia e basit** - sa bita transferohen ne nje cikel,
- **frekuenca e punes** - sa transferime mund te ndodhin ne sekonde,
- **organizimi/protokolli** - sa mire koordinohen transferimet.

Shembull: basi 64-bit mund te transferoje me shume te dhena ne nje cikel se basi 32-bit.

## 13. Funksionimi i kompjuterit

Funksioni baze i kompjuterit eshte ekzekutimi i programeve te ruajtura ne memorie.

Procesori e ben kete duke:

1. sjelle instruksionin nga memoria,
2. interpretuar instruksionin,
3. ekzekutuar instruksionin,
4. kaluar te instruksioni tjeter.

Forma me e thjeshte e ciklit:

```text
Fetch Cycle -> Execute Cycle -> Fetch Cycle -> Execute Cycle -> ...
```

Ky proces perseritet derisa programi perfundon ose sistemi ndalet.

## 14. Cikli i sjelljes dhe ekzekutimit te instruksionit

## 14.1 Fetch Cycle

Ne ciklin e sjelljes:

- `PC` permban adresen e instruksionit vijues.
- CPU-ja e lexon instruksionin nga memoria.
- Instruksioni vendoset ne `IR`.
- `PC` zakonisht rritet automatikisht per te treguar instruksionin e ardhshem.

## 14.2 Execute Cycle

Ne ciklin e ekzekutimit:

- CPU-ja e dekodon instruksionin.
- Percakton llojin e operacionit.
- Kryen operacionin e kerkuar.

Veprimet e procesorit mund te ndahen ne keto kategori:

- **Processor-Memory** - transferim i te dhenave ndermjet procesorit dhe memories.
- **Processor-I/O** - transferim i te dhenave ndermjet procesorit dhe pajisjeve H/D.
- **Data Processing** - operacione aritmetike dhe logjike.
- **Control** - ndryshim i rrjedhes se ekzekutimit, si jump ose branch.

## 15. Kompjuteri hipotetik

Kapitulli perdor nje kompjuter hipotetik te thjeshtuar per te shpjeguar ekzekutimin e instruksioneve.

Ky kompjuter ka:

- **PC** - adresa e instruksionit qe duhet sjelle.
- **IR** - instruksioni qe po ekzekutohet.
- **AC** - akumulator, regjister i perkohshem per te dhena dhe rezultate.

Formati i instruksionit:

- 4 bitet e pare jane kodi i operacionit.
- 12 bitet tjera jane adresa.

Kjo jep:

- 16 kode operacionesh,
- 4096 fjale memorike.

## 16. Kodet e operacioneve ne shembull

| Kodi | Kuptimi |
|---|---|
| `1H` | Ngarko akumulatorin me permbajtjen nga memoria. |
| `2H` | Ruaje permbajtjen e AC ne memorie. |
| `5H` | Mblidh permbajtjen e AC me permbajtjen nga memoria. |

Shembulli i programit:

```text
1940 -> Ngarko AC me permbajtjen e adreses 940
5941 -> Mblidh AC me permbajtjen e adreses 941
2941 -> Ruaje AC ne adresen 941
```

Nese:

```text
Memoria[940] = 0003
Memoria[941] = 0002
```

Atehere:

```text
AC = 0003
AC = 0003 + 0002 = 0005
Memoria[941] = 0005
```

Ky shembull tregon si CPU-ja:

- sjell instruksione nga memoria,
- i vendos ne `IR`,
- rrit `PC`,
- perdor `AC`,
- ruan rezultatin perseri ne memorie.

## 17. Cikli me i detajuar i instruksionit

Ne sisteme reale, nje instruksion mund te kerkoje me shume se nje qasje ne memorie ose H/D.

Gjendjet kryesore:

- **iac - Instruction Address Calculation** - llogarit adresen e instruksionit vijues.
- **if - Instruction Fetch** - sjell instruksionin nga memoria.
- **iod - Instruction Operation Decode** - dekodon instruksionin dhe percakton operacionin.
- **oac - Operand Address Calculation** - llogarit adresen e operandit.
- **of - Operand Fetch** - sjell operandin nga memoria ose H/D.
- **do - Data Operation** - kryen operacionin e te dhenave.
- **os - Operand Store** - ruan rezultatin ne memorie ose e dergon ne H/D.

Jo te gjitha gjendjet ndodhin per cdo instruksion. Disa mund te mos ndodhin fare, ndersa disa mund te perseriten.

## 18. Nderprerjet

**Nderprerja (interrupt)** eshte nje ngjarje qe i kerkon CPU-se ta ndaloje perkohesisht ekzekutimin e programit aktual dhe te sherbeje ngjarjen.

Me fjale te thjeshta: **interrupt = kerkese per vemendjen e CPU-se.**

Nderprerjet mund te vijne nga:

- pajisjet H/D,
- timeri,
- gabime programore,
- gabime harduerike,
- pajisje komunikimi.

## 19. Pse nevojiten nderprerjet

Pa nderprerje, CPU-ja shpesh duhet te prese pajisjet e ngadalshme H/D.

Shembull:

- CPU-ja dergon komanden `WRITE` te printeri.
- Printeri punon ngadale.
- CPU-ja pret derisa printeri te jete gati.
- Gjate pritjes, CPU-ja mbetet joaktive.

Me nderprerje:

- CPU-ja e nis operacionin H/D.
- CPU-ja vazhdon ekzekutimin e instruksioneve tjera.
- Pajisja H/D punon ne menyre te pavarur.
- Kur pajisja ka nevoje per sherbim, dergon interrupt.
- CPU-ja e trajton interrupt-in dhe pastaj kthehet te programi.

Perfundim: **nderprerjet e rrisin efikasitetin sepse CPU-ja nuk humb kohe duke pritur pajisjet e ngadalshme.**

## 20. ISR - rutina e sherbimit te nderprerjes

**ISR (Interrupt Service Routine)** ose **interrupt handler** eshte rutina qe trajton nderprerjen.

Kur ndodh nje interrupt:

1. CPU-ja pezullon programin aktual.
2. Ruan kontekstin e programit, sidomos vleren e `PC`.
3. Vendos ne `PC` adresen e interrupt handler-it.
4. Ekzekuton rutinen e sherbimit.
5. Rikthen kontekstin e programit.
6. Vazhdon programin nga pika ku u nderpre.

Shembull:

- Shtypet nje tast ne tastiere.
- Tastiera gjeneron interrupt.
- CPU-ja kalon te rutina qe lexon tastin.
- Pas sherbimit, CPU-ja kthehet te programi kryesor.

## 21. Llojet e nderprerjeve

CPU-ja mund te pranoje dy lloje kryesore:

| Lloji | Shpjegimi |
|---|---|
| **Maskable Interrupts** | Nderprerje qe mund te caktivizohen ose injorohen perkohesisht nga procesori. |
| **Non-Maskable Interrupts (NMI)** | Nderprerje kritike qe nuk mund te injorohen dhe duhet te trajtohen menjehere. |

## 22. Klasat e nderprerjeve

Klasat me te shpeshta:

- **Program** - krijohen gjate ekzekutimit te instruksioneve, p.sh. pjesetim me zero, instruksion ilegal, ose qasje jovalide ne memorie.
- **Timer** - krijohen nga timeri i sistemit, shpesh per nevoja te sistemit operativ.
- **I/O** - krijohen nga pajisjet H/D kur jane gati ose kur kerkojne sherbim.
- **Hardware failure** - krijohen nga defekte harduerike, p.sh. gabime te memories ose probleme te energjise.

## 23. Polling dhe sistemi pa nderprerje

**Polling** eshte qasje ku CPU-ja kontrollon vazhdimisht statusin e pajisjes.

Problemi:

- CPU-ja harxhon kohe duke pyetur pajisjen nese eshte gati.
- Nese pajisja eshte e ngadalshme, CPU-ja pret kot.
- Ulet efikasiteti i sistemit.

Sistemi pa nderprerje eshte me i thjeshte, por me pak efikas per operacione H/D.

## 24. Sistemi me nderprerje

Ne sistemin me nderprerje:

- Programi i perdoruesit mund te vazhdoje ekzekutimin.
- Operacioni H/D zhvillohet ne sfond.
- Pajisja lajmeron CPU-ne vetem kur kerkon sherbim.
- CPU-ja nuk qendron idle per nje kohe te gjate.

Cikli i instruksionit behet:

```text
Fetch -> Execute -> Kontrollo interrupt -> Fetch instruksionin tjeter
```

Nese nuk ka interrupt, CPU-ja vazhdon normalisht.

Nese ka interrupt:

1. CPU-ja e pezullon programin aktual.
2. E ruan kontekstin.
3. E vendos adresen e interrupt handler-it ne `PC`.
4. Ekzekuton handler-in.
5. Kthehet te programi i nderprere.

## 25. Sistemi operativ dhe nderprerjet

Sistemi operativ eshte program qe kontrollon ekzekutimin e programeve aplikative dhe sherben si ndermjetesues ndermjet aplikacioneve dhe harduerit.

Ne kontekst te nderprerjeve, sistemi operativ:

- menaxhon pajisjet,
- kontrollon operacionet H/D,
- ofron rutina sherbimi,
- menaxhon kalimin nga programi i perdoruesit te interrupt handler-i,
- ruan dhe rikthen kontekstin e programeve.

## 26. Nderprerjet e shumefishta

Ne sisteme reale mund te ndodhin disa nderprerje ne te njejten kohe.

Shembull:

- printeri perfundon nje operacion,
- linja e komunikimit pranon te dhena te reja,
- te dyja pajisjet kerkojne sherbim nga CPU-ja.

Problemi: CPU-ja duhet te vendose cilen nderprerje ta trajtoje e para.

## 27. Menyrat e trajtimit te nderprerjeve te shumefishta

## 27.1 Caktivizimi i nderprerjeve

Gjate trajtimit te nje interrupt-i, nderprerjet tjera caktivizohen perkohesisht.

Karakteristikat:

- Nderprerjet e reja mbesin ne pritje.
- Pas perfundimit te interrupt-it aktual, CPU-ja kontrollon nderprerjet e tjera.
- Trajtimi behet ne menyre sekuenciale.

Perparesi:

- Qasje e thjeshte.
- Nuk lejon qe nje handler te nderpritet nga tjetri.

Mangesi:

- Pajisjet me rendesi te larte mund te presin me shume se sa duhet.

## 27.2 Nderprerjet me prioritet

Cdo interrupt ka nivel prioriteti.

Rregulli:

- Interrupt me prioritet me te larte mund ta nderprese trajtimin e nje interrupt-i me prioritet me te ulet.

Kjo qasje perdoret ne sisteme moderne sepse pajisjet kritike duhet te trajtohen me shpejt.

Perparesi:

- Pergjigje me e shpejte ndaj ngjarjeve kritike.
- Menaxhim me efikas i pajisjeve te rendesishme.

Mangesi:

- Me komplekse, sepse duhet ruajtur konteksti i disa niveleve.

## 28. Nderprerjet e mbivendosura

Nderprerjet e mbivendosura ndodhin kur nje interrupt handler nderpritet nga nje interrupt tjeter me prioritet me te larte.

Rrjedha tipike:

1. Programi i perdoruesit ekzekutohet normalisht.
2. Ndodh interrupt X.
3. CPU-ja kalon te handler-i X.
4. Gjate handler-it X ndodh interrupt Y me prioritet me te larte.
5. Gjendja e handler-it X ruhet.
6. CPU-ja kalon te handler-i Y.
7. Handler-i Y perfundon.
8. CPU-ja kthehet te handler-i X.
9. Handler-i X perfundon.
10. CPU-ja kthehet te programi i perdoruesit.

Ideja kryesore: **nderprerjet me prioritet lejojne qe ngjarjet me te rendesishme te trajtohen menjehere.**

## 29. Permbledhje per mesim te shpejte

Mbaji mend keto:

- **Kompjuteri = CPU + Memorie + Module H/D + Bas i sistemit**
- **Funksioni baze = ekzekutimi i programeve**
- **von Neumann = instruksionet dhe te dhenat ne te njejten memorie**
- **PC = adresa e instruksionit vijues**
- **IR = instruksioni aktual**
- **MAR = adresa ne memorie**
- **MBR = te dhenat qe hyjne/dalin nga memoria**
- **I/O AR = adresa e pajisjes H/D**
- **I/O BR = bafer per te dhena H/D**
- **Moduli H/D = nderfaqe ndermjet pajisjeve dhe CPU/memories**
- **Baferimi = ruajtje e perkohshme per shkak te dallimit te shpejtesive**
- **Basi = data bus + address bus + control bus**
- **Fetch = sjell instruksionin**
- **Execute = ekzekuton instruksionin**
- **Interrupt = kerkese qe CPU-ja te ndaloje perkohesisht dhe te sherbeje nje ngjarje**
- **ISR = rutina qe trajton interrupt-in**
- **Me interrupt, CPU-ja nuk pret kot pajisjet H/D**
- **Interruptet me prioritet trajtojne me pare ngjarjet kritike**

## 30. Pyetje te mundshme per provim

## 30.1 Cilet jane komponentet kryesore te sistemit kompjuterik?

Komponentet kryesore jane CPU-ja, memoria kryesore, modulet H/D dhe basi i sistemit. CPU-ja ekzekuton instruksionet, memoria ruan te dhenat dhe programet, modulet H/D lidhin pajisjet e jashtme, ndersa basi mundeson shkembimin e te dhenave, adresave dhe sinjaleve kontrolluese.

## 30.2 Cilat jane idete kryesore te arkitektures von Neumann?

Te dhenat dhe instruksionet ruhen ne te njejten memorie shkrim-lexim. Permbajtja e memories qaset sipas adreses. Instruksionet zakonisht ekzekutohen ne menyre sekuenciale, pervec kur rrjedha ndryshohet nga instruksione kontrolli ose nderprerje.

## 30.3 Cfare roli ka PC?

`PC` ruan adresen e instruksionit vijues qe duhet te sillet nga memoria. Pas sjelljes se nje instruksioni, `PC` zakonisht rritet per te treguar instruksionin tjeter.

## 30.4 Cili eshte dallimi mes MAR dhe MBR?

`MAR` ruan adresen e memories ku do te kryhet lexim ose shkrim. `MBR` ruan te dhenat qe lexohen nga memoria ose qe do te shkruhen ne memorie.

## 30.5 Pse nevojiten modulet H/D?

Modulet H/D nevojiten sepse pajisjet e jashtme jane zakonisht me te ngadalshme se CPU-ja dhe memoria. Ato sherbejne si nderfaqe, mundesojne kontroll, timing, baferim, komunikim dhe zbulim gabimesh.

## 30.6 Cfare eshte baferimi?

Baferimi eshte ruajtje e perkohshme e te dhenave gjate transferimit ndermjet komponenteve me shpejtesi te ndryshme. Ai ndihmon qe CPU-ja dhe memoria te mos presin pajisjet e ngadalshme.

## 30.7 Cilat jane pjeset kryesore te basit te sistemit?

Pjeset kryesore jane Data Bus, Address Bus dhe Control Bus. Data Bus bart te dhena, Address Bus bart adresa, ndersa Control Bus bart sinjale kontrolluese dhe sinkronizuese.

## 30.8 Cfare ndodh ne ciklin fetch?

CPU-ja perdor adresen ne `PC` per te sjelle instruksionin nga memoria. Instruksioni vendoset ne `IR`, ndersa `PC` zakonisht rritet per te treguar instruksionin e ardhshem.

## 30.9 Cfare eshte interrupt?

Interrupt eshte nje ngjarje qe kerkon vemendjen e CPU-se. CPU-ja e pezullon perkohesisht programin aktual, ruan kontekstin, ekzekuton interrupt handler-in dhe pastaj kthehet te programi i nderprere.

## 30.10 Pse interruptet e permiresojne performancen?

Sepse CPU-ja nuk duhet te prese pajisjet e ngadalshme H/D. Ajo mund te vazhdoje ekzekutimin e instruksioneve tjera, ndersa pajisja dergon interrupt vetem kur kerkon sherbim.

## 30.11 Si trajtohen interruptet e shumefishta?

Mund te trajtohen duke i caktivizuar perkohesisht interruptet tjera derisa te perfundoje interrupt-i aktual, ose me sistem prioritetesh ku interruptet me prioritet me te larte trajtohen te parat dhe mund te nderpresin handler-et me prioritet me te ulet.

---

# Kapitulli 4 - Vend per shenime

Ketu do te shtohet permbledhja e kapitullit 4 pasi te lexohet PDF-i perkates.

## Konceptet kryesore

-

## Pyetje per provim

-

---

# Kapitulli 5 - Vend per shenime

Ketu do te shtohet permbledhja e kapitullit 5 pasi te lexohet PDF-i perkates.

## Konceptet kryesore

-

## Pyetje per provim

-

---

# Kapitulli 6 - Vend per shenime

Ketu do te shtohet permbledhja e kapitullit 6 pasi te lexohet PDF-i perkates.

## Konceptet kryesore

-

## Pyetje per provim

-
