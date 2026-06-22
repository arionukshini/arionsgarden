---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/koll-2/chat-gpt/"}
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

# Kapitulli 4 - Memoria kesh

## Cka duhet te dish pas ketij kapitulli

Pas ketij kapitulli duhet te jesh ne gjendje te:

- Shpjegosh karakteristikat kryesore te sistemeve memoruese.
- Kuptosh pse perdoret hierarkia e memories.
- Shpjegosh qellimin e memories kesh.
- Dallosh hit, miss, hit rate, miss rate dhe miss penalty.
- Perdoresh formulen e kohes efektive te qasjes ne memorie.
- Dallosh pasqyrimin direkt, asociativ dhe set-asociativ.
- Kuptosh politikat e zevendesimit dhe politikat e shkrimit.
- Shpjegosh pse perdoren nivele te shumta te keshit.

## 1. Sistemi memorues kompjuterik

Memoria eshte nje nga komponentet me te rendesishem te arkitektures se kompjuterit. Sistemet memoruese dallohen sipas:

- lokacionit,
- kapacitetit,
- njesise se transferit,
- metodes se qasjes,
- performances,
- llojit fizik,
- karakteristikave fizike,
- kostos.

Ne sisteme moderne nuk perdoret vetem nje lloj memorie. Per shkak te kerkesave te ndryshme per shpejtesi, kapacitet dhe kosto, perdoret **hierarki e memories**.

## 2. Lokacioni i memories

Sipas lokacionit, memoria ndahet ne:

| Lloji | Shembuj | Tipare |
|---|---|---|
| **Memorie interne** | Regjistra, cache, RAM | Brenda sistemit kryesor, shume e shpejte. |
| **Memorie eksterne** | HDD, SSD, USB flash, disqe optike, cloud storage | Kapacitet me i madh, me e ngadalshme. |

Regjistrat jane me afer CPU-se dhe me te shpejtet. RAM-i eshte memoria kryesore e punes. Memoria eksterne ruan te dhenat ne menyre me te perhershme.

## 3. Kapaciteti dhe njesia e adresueshme

**Kapaciteti** tregon sa te dhena mund te ruaje memoria.

Per memorien interne, kapaciteti zakonisht shprehet ne:

- byte,
- KB,
- MB,
- GB.

**Njesia e adresueshme** eshte njesia me e vogel qe mund te adresohet nga procesori. Ne shume sisteme moderne kjo eshte bajti.

Raporti kryesor:

```text
2^A = N
```

Ku:

- `A` = numri i biteve te adreses,
- `N` = numri i njesive te adresueshme.

Shembull i rendesishem: nje sistem 32-bit mund te adresoje maksimalisht `2^32` njesi. Nese njesia eshte bajti, atehere maksimumi eshte rreth 4 GB.

## 4. Njesia e transferit

**Njesia e transferit** eshte sasia e te dhenave qe transferohet ne nje operacion.

Per memorien interne, njesia e transferit lidhet me numrin e linjave elektrike brenda/jashte modulit memorues.

Transferi mund te behet:

- me fjale,
- me blloqe,
- me faqe, varur nga niveli i hierarkise.

Te cache zakonisht transferohet nje **bllok** ose **cache line**, jo vetem fjala e kerkuar.

## 5. Metodat e qasjes

Metodat kryesore te qasjes ne memorie:

| Metoda | Shpjegimi | Shembull |
|---|---|---|
| **Qasje sekuenciale** | Te dhenat lexohen ne rend. Koha e qasjes varet nga pozita. | Shiriti magnetik. |
| **Qasje direkte** | Blloqet kane adresa fizike; arrihet afersisht lokacioni, pastaj kerkohet sakte. | Disku magnetik. |
| **Qasje e rastit** | Cdo lokacion adresohet direkt dhe koha e qasjes eshte afersisht konstante. | RAM. |
| **Qasje asociative** | Kerkimi behet sipas permbajtjes, jo sipas adreses. | Cache asociative. |

## 6. Performanca e memories

Termat kryesore:

- **Koha e qasjes** - koha nga kerkesa deri te marrja e te dhenes.
- **Koha e ciklit memorues** - koha e qasjes plus koha e nevojshme para se te filloje qasja tjeter.
- **Shpejtesia e transmetimit** - sa shpejt transferohen te dhenat brenda ose jashte memories.

Per memorie me qasje te rastit:

```text
Shpejtesia e transmetimit = 1 / koha e ciklit
```

## 7. Lloji fizik dhe karakteristikat fizike

Sipas llojit fizik, memoriet mund te jene:

- gjysmepercjellese,
- magnetike,
- optike,
- flash.

Sipas karakteristikave fizike:

- **Volatile** - humb permbajtjen kur largohet energjia. Shembull: RAM.
- **Nonvolatile** - ruan permbajtjen edhe pa energji. Shembull: ROM, flash, SSD.

## 8. Hierarkia e memories

Hierarkia e memories organizohet nga memoriet me te shpejta dhe me te shtrenjta drejt memorieve me te ngadalta dhe me te lira.

Renditja tipike:

```text
Regjistra -> L1 Cache -> L2 Cache -> L3 Cache -> RAM -> SSD/HDD -> Cloud/arkiv
```

Duke levizur poshte hierarkise:

- kostoja per bit bie,
- kapaciteti rritet,
- koha e qasjes rritet,
- frekuenca e qasjes nga procesori zvogelohet.

Ideja kryesore: **memoriet e vogla dhe te shpejta mbajne te dhenat qe perdoren shpesh, ndersa memoriet e medha dhe me te ngadalta mbajne pjesen tjeter.**

## 9. Pse nevojitet hierarkia e memories

CPU-ja punon shume me shpejt se memoria kryesore. Nese CPU-ja do te priste gjithmone RAM-in ose diskun, performanca do te binte shume.

Hierarkia e memories zgjidh problemin duke vendosur memorie te shpejte afer CPU-se.

Shembull:

- CPU-ja kerkon instruksione dhe te dhena.
- Se pari kontrollohen regjistrat/cache.
- Nese mungojne, kerkohet RAM-i.
- Nese mungojne ne RAM, perdoret memoria sekondare.

## 10. Principet e memories kesh

**Memoria kesh** eshte memorie e vogel, shume e shpejte dhe me kosto te larte. Ajo ruan kopje te blloqeve te memories kryesore qe perdoren shpesh.

Qellimi:

- te zvogeloje kohen mesatare te qasjes ne memorie,
- te zvogeloje pritjen e CPU-se,
- te shfrytezoje lokalitetin e referencave.

Kur CPU-ja kerkon nje fjale:

1. Kerkohet ne cache.
2. Nese gjendet, i dergohet CPU-se menjehere.
3. Nese nuk gjendet, merret blloku nga memoria kryesore dhe vendoset ne cache.
4. Pastaj fjala dergohet te CPU-ja.

## 11. Cache hit dhe cache miss

| Termi | Kuptimi |
|---|---|
| **Hit** | E dhena e kerkuar gjendet ne cache. |
| **Hit rate (h)** | Probabiliteti qe kerkesa te jete hit. |
| **Miss** | E dhena nuk gjendet ne cache. |
| **Miss rate (m)** | Probabiliteti i mungeses ne cache. `m = 1 - h`. |
| **Miss penalty** | Koha shtese per ta sjelle bllokun nga niveli me i ulet i memories. |

Formula e rendesishme:

```text
EMAT = Tc + m * Tm
```

Ku:

- `EMAT` = Effective Memory Access Time,
- `Tc` = koha e qasjes ne cache,
- `m` = miss rate,
- `Tm` = miss penalty.

## 12. Lokaliteti i referencave

Cache funksionon mire per shkak te **lokalitetit te referencave**.

Dy forma kryesore:

- **Lokaliteti hapesinor** - nese perdoret nje lokacion, ka gjase te perdoren edhe lokacionet afer tij.
- **Lokaliteti kohor** - nese perdoret nje e dhene tani, ka gjase te perdoret perseri se shpejti.

Shembull: instruksionet e programit shpesh ekzekutohen me radhe, prandaj kur merret nje instruksion, ia vlen te merret edhe blloku qe e permban.

## 13. Nivelet e keshit

Procesoret moderne zakonisht kane disa nivele cache.

| Niveli | Tipare |
|---|---|
| **L1** | Me i shpejti, me i vogli, zakonisht brenda cdo berthame. |
| **L2** | Me i madh se L1, pak me i ngadalte. |
| **L3** | Me i madh, me i ngadalte se L1/L2, shpesh i perbashket per disa berthama. |
| **L4 / L0** | Mund te ekzistojne ne disa CPU moderne, varur nga dizajni. |

Rrjedha tipike:

```text
CPU -> L1 -> L2 -> L3 -> RAM
```

Nese e dhena nuk gjendet ne L1, kerkohet ne L2. Nese nuk gjendet ne L2, kerkohet ne L3. Nese mungon edhe aty, merret nga RAM.

## 14. Cache dhe DMA

Te dhenat nga pajisjet H/D zakonisht nuk kalojne fizikisht permes CPU-se. Per kete perdoret **DMA (Direct Memory Access)**.

Me DMA:

- pajisja H/D transferon te dhena direkt ne RAM,
- CPU-ja nuk merret me cdo bajt te transferimit,
- sistemi behet me efikas.

Ne arkitektura moderne duhet pasur kujdes per koherencen ndermjet cache dhe RAM, sepse pajisja mund te ndryshoje RAM-in ndersa CPU-ja ka kopje ne cache.

## 15. Struktura cache / memorie kryesore

Memoria kryesore ndahet ne **blloqe**. Cache ndahet ne **linja**.

- Numri i linjave ne cache eshte me i vogel se numri i blloqeve ne memorien kryesore.
- Ne cdo moment, vetem disa blloqe te memories kryesore jane rezidente ne cache.
- Kur lexohet nje fjale nga nje bllok, zakonisht transferohet i gjithe blloku.
- Cdo linje cache ka nje **tag** qe tregon cili bllok i memories kryesore gjendet aty.

## 16. Elementet e projektimit te cache-it

Elementet kryesore:

- adresat e cache-it,
- madhesia e cache-it,
- madhesia e linjes,
- funksioni i pasqyrimit,
- algoritmi i zevendesimit,
- politika e shkrimit,
- numri i niveleve,
- cache i ndare ose i unifikuar.

## 17. Cache logjik dhe cache fizik

Kur perdoret memorie virtuale, CPU-ja gjeneron adresa virtuale. MMU i perkthen ne adresa fizike.

| Lloji | Shpjegimi |
|---|---|
| **Cache logjik / virtual** | Cache perdor adresa virtuale. Mund te jete me i shpejte sepse qasja ndodh para perkthimit nga MMU. |
| **Cache fizik** | Cache perdor adresa fizike. Me i sigurt per dallimin ndermjet proceseve, por qasja mund te perfshije perkthimin e adreses. |

Problemi i cache logjik: procese te ndryshme mund te kene adresa virtuale te njejta qe i referohen adresave fizike te ndryshme.

## 18. Cache i ndare dhe cache i unifikuar

| Lloji | Shpjegimi |
|---|---|
| **Cache i ndare** | Cache i vecante per instruksione dhe cache i vecante per te dhena. |
| **Cache i unifikuar** | Instruksionet dhe te dhenat ruhen ne te njejtin cache. |

Cache i ndare mund te rrise bandwidth-in sepse instruksionet dhe te dhenat mund te qasen paralelisht.

## 19. Funksioni i pasqyrimit

Sepse ka me pak linja cache se blloqe ne memorien kryesore, duhet nje rregull qe tregon ku vendoset nje bllok i memories ne cache. Ky rregull quhet **funksion i pasqyrimit**.

Teknikat kryesore:

- pasqyrimi direkt,
- pasqyrimi asociativ,
- pasqyrimi set-asociativ.

## 20. Pasqyrimi direkt

Te **pasqyrimi direkt**, cdo bllok i memories kryesore mund te vendoset vetem ne nje linje te caktuar te cache-it.

Formula:

```text
i = j mod m
```

Ku:

- `i` = numri i linjes ne cache,
- `j` = numri i bllokut ne memorien kryesore,
- `m` = numri total i linjave ne cache.

Struktura e adreses:

```text
Tag | Line number | Block offset
```

Perparesi:

- implementim i thjeshte,
- kosto me e ulet,
- qasje e shpejte.

Mangesi:

- konfliktet jane te shpeshta,
- dy blloqe qe pasqyrohen ne te njejten linje nuk mund te qendrojne bashke,
- mund te kete cache miss edhe kur cache ka hapesire diku tjeter.

## 21. Pasqyrimi asociativ

Te **pasqyrimi plotesisht asociativ**, nje bllok i memories kryesore mund te vendoset ne cilen do linje te cache-it.

Struktura e adreses:

```text
Tag | Block offset
```

Perparesi:

- fleksibilitet i larte,
- me pak konflikte se pasqyrimi direkt,
- mund te shfrytezoje me mire hapesiren ne cache.

Mangesi:

- duhet krahasuar tag-u me te gjitha linjat ne cache,
- kerkon qark kompleks,
- me i shtrenjte per implementim.

Kur cache eshte plot, duhet algoritmi i zevendesimit.

## 22. Pasqyrimi set-asociativ

**Pasqyrimi set-asociativ** eshte kompromis ndermjet pasqyrimit direkt dhe atij asociativ.

Cache ndahet ne sete. Cdo set permban disa linja.

Nje bllok i memories kryesore:

- mund te vendoset vetem ne nje set te caktuar,
- por brenda atij seti mund te vendoset ne cilendo linje.

Formula:

```text
set = block_number mod number_of_sets
```

Nese cdo set ka `k` linja, quhet **k-menyresh set-asociativ**.

Struktura e adreses:

```text
Tag | Set number | Block offset
```

Perparesi:

- me pak konflikte se pasqyrimi direkt,
- me pak kompleks se pasqyrimi plotesisht asociativ,
- perdoret shume ne sisteme moderne.

## 23. Krahasimi i teknikave te pasqyrimit

| Teknikë | Ku vendoset blloku? | Perparesi | Mangesi |
|---|---|---|---|
| **Direkt** | Vetem ne nje linje te caktuar. | I thjeshte dhe i lire. | Shume konflikte. |
| **Asociativ** | Ne cilen do linje. | Fleksibilitet maksimal. | Qark kompleks dhe i shtrenjte. |
| **Set-asociativ** | Ne nje set te caktuar, ne cilendo linje te atij seti. | Kompromis shume i mire. | Me kompleks se direkt. |

## 24. Algoritmet e zevendesimit

Kur cache eshte plot dhe ndodh miss, duhet zgjedhur cili bllok te largohet.

Politika te zakonshme:

- **LRU (Least Recently Used)** - largohet blloku qe nuk eshte perdorur per kohen me te gjate.
- **FIFO (First In First Out)** - largohet blloku qe ka hyre i pari ne cache.
- **Random** - largohet nje bllok ne menyre te rastit.

LRU zakonisht jep rezultate te mira, por mund te jete me i veshtire per implementim ne cache me asociativitet te larte.

## 25. Politikat e shkrimit

Kur CPU-ja shkruan ne cache, duhet vendosur si sinkronizohet ndryshimi me memorien kryesore.

| Politika | Shpjegimi | Perparesi | Mangesi |
|---|---|---|---|
| **Write-through** | Te dhenat shkruhen edhe ne cache edhe ne memorie kryesore. | Memoria kryesore eshte gjithmone e perditesuar. | Me shume trafik ne bus, me ngadale. |
| **Write-back** | Te dhenat shkruhen vetem ne cache; memoria perditesohet kur blloku largohet. | Me pak trafik, me shpejt. | Me kompleks, duhet bit i modifikimit/dirty bit. |

Te write-through shpesh perdoret **write buffer** per te mos e ndalur CPU-ne gjate shkrimit.

## 26. Permbledhje per mesim te shpejte

Mbaji mend keto:

- **Cache = memorie e vogel dhe e shpejte afer CPU-se**
- **Qellimi = zvogelim i kohes mesatare te qasjes ne memorie**
- **Hit = e dhena gjendet ne cache**
- **Miss = e dhena mungon ne cache**
- **Miss rate = 1 - hit rate**
- **EMAT = Tc + m * Tm**
- **Lokaliteti kohor = e dhena mund te perdoret perseri se shpejti**
- **Lokaliteti hapesinor = lokacionet afer mund te perdoren se shpejti**
- **Pasqyrim direkt = nje bllok shkon vetem ne nje linje**
- **Pasqyrim asociativ = nje bllok mund te shkoje kudo**
- **Set-asociativ = nje bllok shkon ne nje set, por ne cilendo linje brenda setit**
- **LRU/FIFO = politika zevendesimi**
- **Write-through/write-back = politika shkrimi**

## 27. Pyetje te mundshme per provim

## 27.1 Pse perdoret hierarkia e memories?

Sepse CPU-ja eshte shume me e shpejte se memoria kryesore dhe memoria eksterne. Hierarkia vendos memorie te vogla dhe te shpejta afer CPU-se, ndersa memoriet me te medha dhe me te lira vendosen me poshte.

## 27.2 Cfare eshte memoria kesh?

Memoria kesh eshte memorie e vogel dhe shume e shpejte qe ruan kopje te blloqeve te memories kryesore qe perdoren shpesh. Ajo zvogelon kohen mesatare te qasjes ne memorie.

## 27.3 Cfare eshte cache hit dhe cache miss?

Cache hit ndodh kur e dhena e kerkuar gjendet ne cache. Cache miss ndodh kur e dhena nuk gjendet ne cache dhe duhet te merret nga nje nivel me i ulet i hierarkise.

## 27.4 Cfare eshte lokaliteti i referencave?

Eshte prirja e programeve qe te perdorin perseri te dhenat/instruksionet e fundit ose lokacionet afer tyre. Kjo e ben cache-in efektiv.

## 27.5 Cili eshte dallimi mes pasqyrimit direkt dhe asociativ?

Te pasqyrimi direkt, cdo bllok mund te vendoset vetem ne nje linje te caktuar. Te pasqyrimi asociativ, cdo bllok mund te vendoset ne cilendo linje cache.

## 27.6 Cfare eshte pasqyrimi set-asociativ?

Eshte kompromis ku cache ndahet ne sete. Nje bllok shkon ne nje set te caktuar, por mund te vendoset ne cilendo linje brenda atij seti.

## 27.7 Cili eshte dallimi mes write-through dhe write-back?

Write-through shkruan ndryshimin ne cache dhe memorie kryesore menjehere. Write-back shkruan fillimisht vetem ne cache dhe e perditeson memorien kryesore kur blloku largohet nga cache.

---

# Kapitulli 5 - Memoria gjysmepercjellese

## Cka duhet te dish pas ketij kapitulli

Pas ketij kapitulli duhet te jesh ne gjendje te:

- Dallosh DRAM dhe SRAM.
- Shpjegosh pse DRAM ka nevoje per refresh.
- Kuptosh pse SRAM perdoret per cache.
- Shpjegosh llojet kryesore te ROM-it.
- Shpjegosh rolin e memories flash.
- Kuptosh organizimin e brendshem te cipeve te memories.
- Shpjegosh detektimin dhe korrigjimin e gabimeve.
- Kuptosh idene e kodit te Hamming-ut.

## 1. Llojet kryesore te memories gjysmepercjellese

Memoria gjysmepercjellese perdoret si memorie kryesore, cache dhe memorie e perhershme ne sisteme kompjuterike.

Llojet kryesore:

- **DRAM**
- **SRAM**
- **ROM**
- **PROM**
- **EPROM**
- **EEPROM**
- **Flash memory**

Ne praktike:

- **DRAM** perdoret kryesisht per memorien kryesore.
- **SRAM** perdoret kryesisht per cache.
- **ROM/Flash** perdoren per ruajtje te perhershme te firmware-it dhe te dhenave.

## 2. DRAM - Dynamic RAM

**DRAM** ruan bitet si ngarkese elektrike ne kondensatore.

Qeliza tipike DRAM permban:

- nje transistor,
- nje kondensator.

Ideja:

- kondensatori i ngarkuar paraqet `1`,
- kondensatori i pa ngarkuar paraqet `0`.

DRAM quhet dinamike sepse ngarkesa ne kondensator humbet gradualisht.

## 3. Shkrimi dhe leximi ne DRAM

Gjate shkrimit:

- vendoset tension ne linjen e bitit,
- tensioni i larte paraqet `1`,
- tensioni i ulet paraqet `0`,
- aktivizohet linja e adreses,
- kondensatori ngarkohet ose shkarkohet.

Gjate leximit:

- aktivizohet linja e adreses,
- transistori lejon leximin e ngarkeses,
- sense amplifier detekton vleren,
- leximi mund ta dobesoje ngarkesen, prandaj e dhena duhet restauruar.

## 4. Refresh ne DRAM

Kondensatori ne DRAM shkarkohet gradualisht. Prandaj DRAM duhet te rifreskohet periodikisht.

**Refresh** do te thote:

- lexohet permbajtja,
- rivendoset vlera e bitit,
- ngarkesa ne kondensator rikthehet.

Mangesi:

- refresh merr kohe,
- rrit konsumin e energjise,
- ndikon negativisht ne performance.

Per provim: **DRAM eshte me e dendur dhe me e lire, por ka nevoje per refresh.**

## 5. SRAM - Static RAM

**SRAM** perdor qeliza statike, zakonisht me flip-flop/latch, jo kondensatore.

Qeliza SRAM zakonisht perbehet nga:

- latch me transistore te kryqezuar,
- transistore kontrolli per qasje ne qelize.

SRAM nuk ka nevoje per refresh sepse gjendja ruhet sa kohe ka energji.

Per provim: **SRAM eshte me e shpejte se DRAM, por me e shtrenjte dhe me densitet me te vogel.**

## 6. Operacionet ne SRAM

Gjate leximit:

- zgjidhet rreshti/fjala,
- qeliza lidhet me linjat e bitit,
- vlera lexohet pa e ndryshuar gjendjen e qelizes.

Leximi duhet te jete **jo-destruktiv**, pra qeliza nuk duhet ta humbe vleren.

Gjate shkrimit:

- linjat e bitit vendosen ne vleren e re,
- aktivizohet linja e fjales,
- gjendja e latch-it detyrohet te ndryshoje sipas vleres se re.

## 7. Krahasimi DRAM dhe SRAM

| Tipari | DRAM | SRAM |
|---|---|---|
| Ruajtja e bitit | Kondensator + transistor | Flip-flop/latch |
| Refresh | Po | Jo |
| Shpejtesia | Me e ngadalshme | Me e shpejte |
| Densiteti | Me i larte | Me i ulet |
| Kostoja per bit | Me e ulet | Me e larte |
| Perdorimi tipik | Memorie kryesore | Cache |

## 8. ROM - Read Only Memory

**ROM** eshte memorie vetem per lexim.

Karakteristikat:

- jo e avullueshme,
- ruan permbajtjen pa energji,
- permbajtja zakonisht nuk ndryshohet gjate perdorimit normal,
- perdoret per firmware dhe programe qe duhet te jene gjithmone te pranishem.

Perparesi:

- programi/te dhenat jane pergjithmone ne memorie,
- nuk duhet te ngarkohen nga ruajtja sekondare.

Mangesi:

- ndryshimi i permbajtjes eshte i veshtire ose i pamundshem,
- gabimet ne permbajtje jane problem serioz.

## 9. Llojet e ROM-it

| Lloji | Shpjegimi |
|---|---|
| **ROM** | Shkruhet gjate fabrikimit. Nuk ndryshohet me pas. |
| **PROM** | Prodhohet e zbrazet dhe programohet nje here elektrikisht. |
| **EPROM** | Mund te fshihet dhe riprogramohet; fshirja zakonisht behet me drite ultraviolet. |
| **EEPROM** | Mund te fshihet dhe shkruhet elektrikisht, zakonisht ne nivel bajtesh. |
| **Flash** | Forme e EEPROM, fshin blloqe me shpejtesi me te madhe dhe me densitet me te larte. |

## 10. PROM

**PROM (Programmable ROM)** eshte memorie jo e avullueshme qe shkruhet vetem nje here.

Karakteristikat:

- prodhohet si memorie e zbrazet,
- programohet me pajisje speciale,
- pas programimit, te dhenat ruhen pergjithmone,
- me fleksibile se ROM klasik sepse mund te programohet pas prodhimit.

## 11. EPROM

**EPROM (Erasable PROM)** mund te fshihet dhe riprogramohet.

Karakteristikat:

- lexohet dhe shkruhet elektrikisht,
- para shkrimit duhet fshire permbajtja,
- fshirja zakonisht behet duke ekspozuar cipin ne drite ultraviolet,
- me e shtrenjte se PROM, por me fleksibile.

## 12. EEPROM

**EEPROM (Electrically Erasable PROM)** mund te fshihet dhe shkruhet elektrikisht.

Karakteristikat:

- nuk ka nevoje per drite ultraviolet,
- mund te perditesohen bajte te vecante,
- me fleksibile se EPROM,
- me e shtrenjte dhe me densitet me te ulet se EPROM.

## 13. Flash memory

**Flash memory** eshte forme e memories gjysmepercjellese jo te avullueshme.

Karakteristikat:

- perdor fshirje elektrike,
- fshin blloqe te qelizave ne nje veprim,
- eshte me e shpejte se EEPROM per fshirje/shkrim ne blloqe,
- ka densitet te larte,
- perdoret ne SSD, USB, karta memorie dhe pajisje mobile.

Flash eshte ndermjet EPROM dhe EEPROM ne kosto dhe funksionalitet.

## 14. Logjika e cipit te memories

Te memoriet gjysmepercjellese, ceshtje kryesore eshte sa bite mund te lexohen ose shkruhen ne te njejten kohe.

Cipi permban matrice te qelizave memoruese.

Matrica mund te organizohet si:

```text
W fjale x B bite per fjale
```

Shembull nga kapitulli:

- DRAM 16 Mbit,
- organizim `4M x 4`,
- 4 bite lexohen ose shkruhen njekohesisht.

Adresimi mund te ndahet ne:

- adrese rreshti,
- adrese kolone.

Sinjale te rendesishme:

- **RAS (Row Address Select)** - zgjedh rreshtin.
- **CAS (Column Address Select)** - zgjedh kolonen.
- **WE (Write Enable)** - aktivizon shkrimin.
- **OE (Output Enable)** - aktivizon daljen/leximin.

## 15. Paketimi i cipeve

Nje qark i integruar vendoset ne paketim fizik. Pinat perdoren per lidhje me sistemin e jashtem.

Pinat mund te perfshijne:

- linja adresash,
- linja te dhenash,
- sinjale kontrolli,
- furnizim me energji,
- tokezim.

Shembull: EPROM 8-Mbit i organizuar si `1M x 8` ka adresa per 1M fjale dhe 8 linja te dhenash.

## 16. Gabimet ne memorie

Memoria gjysmepercjellese mund te kete gabime.

Kategorite:

- **gabime harduerike** - defekte fizike, probleme mjedisi, prodhim, demtime;
- **gabime softuerike** - ndryshime te perkohshme te biteve, shpesh nga rrezatim ose efekte elektrike.

Gabimet mund te jene:

- te perhershme,
- te perkohshme.

## 17. Detektimi dhe korrigjimi i gabimeve

Kur te dhenat shkruhen ne memorie:

1. mbi te dhenat aplikohet nje funksion,
2. gjenerohet nje kod kontrolli,
3. ruhen te dhenat bashke me kodin.

Nese fjala e te dhenave ka `M` bite dhe kodi ka `K` bite, atehere fjala e ruajtur ka:

```text
M + K bite
```

Kur lexohet fjala:

1. nga te dhenat gjenerohet perseri kodi,
2. kodi i ri krahasohet me kodin e ruajtur,
3. nga krahasimi kuptohet nese ka gabim.

Rezultatet e mundshme:

- nuk ka gabim,
- ka gabim qe mund te korrigjohet,
- ka gabim qe vetem detektohet ose nuk mund te korrigjohet.

## 18. Kodi i Hamming-ut

Kodi i Hamming-ut perdoret per te zbuluar dhe korrigjuar gabimin e nje biti.

Ideja:

- shtohen bite kontrolli/pariteti,
- gjate leximit krijohet **sindroma**,
- sindroma tregon nese ka gabim dhe ku ndodhet.

Rregullat nga kapitulli:

- Nese sindroma eshte `0000`, nuk eshte detektuar gabim.
- Nese sindroma ka vetem nje bit `1`, gabimi eshte ne nje bit kontrolli.
- Nese sindroma ka me shume se nje bit `1`, vlera numerike e sindromes tregon pozicionin e bitit te te dhenave qe ka gabim.

Per provim: **Hamming mund te korrigjoje gabime me nje bit dhe te ndihmoje ne detektimin e gabimeve ne memorie.**

## 19. Permbledhje per mesim te shpejte

Mbaji mend keto:

- **DRAM = kondensator, ka refresh, perdoret per RAM**
- **SRAM = latch/flip-flop, nuk ka refresh, perdoret per cache**
- **ROM = jo e avullueshme, vetem lexim**
- **PROM = programohet nje here**
- **EPROM = fshihet dhe riprogramohet**
- **EEPROM = fshihet/shkruhet elektrikisht**
- **Flash = fshirje ne blloqe, perdoret ne SSD/USB**
- **RAS/CAS = zgjedhje rreshti dhe kolone ne DRAM**
- **ECC = detektim/korrigjim gabimesh**
- **Kodi i Hamming-ut = korrigjon gabim nje-bit**

## 20. Pyetje te mundshme per provim

## 20.1 Cili eshte dallimi mes DRAM dhe SRAM?

DRAM ruan bitet si ngarkese ne kondensator dhe ka nevoje per refresh. SRAM ruan bitet me latch/flip-flop, nuk ka nevoje per refresh dhe eshte me e shpejte, por me e shtrenjte.

## 20.2 Pse DRAM duhet te rifreskohet?

Sepse kondensatoret shkarkohen gradualisht. Pa refresh, ngarkesa humbet dhe bashke me te humbet edhe e dhena.

## 20.3 Pse SRAM perdoret per cache?

Sepse eshte shume e shpejte dhe nuk ka nevoje per refresh. Kjo e ben te pershtatshme per nivelet e cache-it afer CPU-se.

## 20.4 Cfare eshte ROM?

ROM eshte memorie jo e avullueshme, kryesisht vetem per lexim, qe ruan permbajtjen edhe pa energji. Perdoret per firmware dhe programe te perhershme.

## 20.5 Cili eshte dallimi mes EPROM dhe EEPROM?

EPROM fshihet zakonisht me drite ultraviolet dhe pastaj riprogramohet. EEPROM fshihet dhe shkruhet elektrikisht, madje mund te perditesoje bajte te vecante.

## 20.6 Cfare eshte memoria flash?

Flash eshte memorie jo e avullueshme qe fshihet elektrikisht ne blloqe. Perdoret ne SSD, USB dhe pajisje mobile.

## 20.7 Cfare ben kodi i Hamming-ut?

Kodi i Hamming-ut shton bite kontrolli dhe perdor sindromen per te zbuluar dhe korrigjuar gabime me nje bit ne fjalen e memories.

---

# Kapitulli 6 - Memoria eksterne dhe memoria virtuale

## Cka duhet te dish pas ketij kapitulli

Pas ketij kapitulli duhet te jesh ne gjendje te:

- Shpjegosh organizimin e diskut magnetik.
- Kuptosh mekanizmin e leximit dhe shkrimit ne disk.
- Shpjegosh trasete, sektoret, cilindrat dhe kokat.
- Kuptosh faktoret qe ndikojne ne performancen e diskut.
- Shpjegosh idene e RAID dhe SSD sipas kapitullit/librit baze.
- Kuptosh idene e memories virtuale.
- Shpjegosh faqet, page frames, page table dhe page fault.
- Dallosh adresen virtuale nga adresa fizike.

## 1. Disku magnetik

Disku magnetik eshte pajisje ruajtese qe perdor siperfaqe magnetike per te ruajtur te dhena.

Nje disk perbehet nga:

- pjata rrethore,
- material jo magnetik si substrate,
- shtrese magnetike ne siperfaqe,
- koke per lexim/shkrim,
- mekanizem rrotullimi,
- kontrollues disku.

Materialet dhe dizajni synojne:

- siperfaqe me uniforme,
- me pak defekte,
- ngurtesi me te mire,
- ruajtje me te besueshme.

## 2. Mekanizmi i shkrimit dhe leximit

Leximi dhe shkrimi kryhen me koken per lexim/shkrim.

Gjate shkrimit:

- rryma kalon neper peshtjelle,
- krijohet fushe magnetike,
- fusha magnetizon siperfaqen poshte kokes,
- krijohen paterna magnetike qe perfaqesojne bitet.

Gjate leximit:

- siperfaqja magnetike leviz nen koke,
- ndryshimet magnetike induktojne sinjal elektrik,
- sinjali interpretohet si te dhena binare.

Gjate leximit/shkrimit, koka zakonisht eshte e palevizshme mbi nje trase, ndersa disku rrotullohet.

## 3. Organizimi i te dhenave ne disk

Termat kryesore:

| Termi | Shpjegimi |
|---|---|
| **Koka** | Pajisja qe lexon/shkruan mbi siperfaqen e diskut. |
| **Trase / piste** | Rreth koncentrik ne siperfaqen e diskut ku ruhen te dhenat. |
| **Sektor** | Ndarje e trasese; njesi baze e adresimit/transferit ne disk. |
| **Cilinder** | Bashkesi trasash me te njejtin pozicion ne pjata/siperfaqe te ndryshme. |
| **Cluster** | Grup sektorësh qe sistemi i skedareve i trajton si njesi alokimi. |

## 4. Shpejtesia dhe organizimi i regjistrimit

Problemi: pjeset afer qendres se diskut levizin me ngadale se pjeset afer skajit te jashtem.

Dy qasje:

- **CAV (Constant Angular Velocity)** - disku rrotullohet me shpejtesi kendore konstante.
- **Regjistrim ne zona te shumefishta** - trasete ndahen ne zona; zonat e jashtme mund te kene me shume sektore.

## 5. CAV - Constant Angular Velocity

Te CAV:

- disku rrotullohet me shpejtesi kendore konstante,
- blloqet adresohen direkt me trase dhe sektor,
- koka leviz ne trasen e duhur dhe pret sektorin e duhur.

Perparesi:

- adresim i thjeshte direkt,
- qasje relativisht e shpejte ne sektorin e kerkuar.

Mangesi:

- trasete e jashtme mund te ruajne me shume te dhena fizikisht, por shpesh nuk shfrytezohen plotesisht nese numri i sektoreve eshte i njejte.

## 6. Karakteristikat fizike te diskut

Disku magnetik mund te klasifikohet sipas:

- koka fikse ose koka te levizshme,
- disk i largueshem ose i palargueshem,
- nje pjate ose pjata te shumefishta,
- nje koke per siperfaqe,
- organizim me cilindra.

Ne disqe me pjata te shumefishta, kokat per siperfaqe te ndryshme levizin te koordinuara. Trasete me te njejtin pozicion ne siperfaqe te ndryshme formojne cilindrin.

## 7. Formatimi i diskut

Disku duhet te kete menyre per te identifikuar:

- fillimin e trasese,
- fillimin dhe fundin e sektorit,
- adresen e sektorit,
- kontrollin e gabimeve.

Prandaj, disku formatohet me te dhena kontrolli qe nuk jane pjese e te dhenave te perdoruesit.

Fushat tipike:

- ID e sektorit,
- fusha e te dhenave,
- kode per detektim gabimesh,
- hapesira sinkronizuese.

## 8. Performanca e diskut magnetik

Koha totale e qasjes ne disk varet nga disa komponente.

Termat kryesore:

- **Seek time** - koha per te levizur koken ne trasen e duhur.
- **Rotational latency** - koha e pritjes derisa sektori i duhur te vije nen koke.
- **Access time** - `seek time + rotational latency`.
- **Transfer time** - koha per te transferuar te dhenat pasi sektori eshte nen koke.

Formula baze:

```text
Access time = Seek time + Rotational latency
```

Koha totale I/O perfshin edhe kohen e transferit dhe vonesa nga kontrolluesi/sistemi.

## 9. RAID dhe SSD

Kapitulli tregon se pjeset per **RAID** dhe **Solid State Drives** duhet te perpunohen edhe nga libri baze.

Ideja e RAID:

- **RAID (Redundant Array of Independent Disks)** perdor disa disqe si nje sistem te vetem logjik.
- Qellimi eshte rritja e performances, besueshmerise, ose te dyjave.
- Nivele te ndryshme RAID perdorin striping, mirroring dhe paritet.

Ideja e SSD:

- **SSD (Solid State Drive)** perdor flash memory.
- Nuk ka pjese mekanike levizese.
- Ka latency me te ulet se HDD.
- Eshte me rezistent ndaj goditjeve mekanike.
- Ka kufizime te shkrimit/fshirjes per qelizat flash.

## 10. Memoria virtuale - ideja kryesore

Memoria virtuale eshte mekanizem qe lejon programet te perdorin nje hapesire adresash me te madhe ose me te rregullt se memoria fizike reale.

Ideja:

- programi punon me adresa virtuale,
- sistemi i perkthen ne adresa fizike,
- disa faqe mund te jene ne RAM,
- disa faqe mund te jene ne disk.

Memoria virtuale quhet virtuale sepse nuk eshte e gjitha RAM fizik.

## 11. Analogjia me cache

Cache ruan nje nenbashkesi te RAM-it.

Memoria virtuale ruan ne RAM nje nenbashkesi te hapesires virtuale te procesit.

Analogjia:

| Cache | Memoria virtuale |
|---|---|
| Cache line / bllok | Faqe |
| Cache miss | Page fault |
| Cache ruan pjese te RAM-it | RAM ruan pjese te hapesires virtuale |
| Niveli me i ulet: RAM | Niveli me i ulet: disk |

## 12. Pse perdoret memoria virtuale

Fillimisht, memoria virtuale u perdor per te zgjeruar RAM-in.

Me vone u be e rendesishme edhe per:

- mbrojtjen e memories,
- izolimin e proceseve,
- thjeshtimin e programimit,
- menaxhimin automatik te RAM-it dhe diskut.

Pa memorie virtuale, programeri do te duhej ta ndante manualisht programin ne pjese qe futen ne RAM.

## 13. Proceset dhe hapesira e adresave

Kur nje program ekzekutohet, ai quhet **proces**.

Cdo proces ka hapesiren e vet te adresave.

Programi gjeneron adresa gjate:

- instruksioneve `load`,
- instruksioneve `store`,
- marrjes se instruksioneve nga memoria.

Adresat qe gjeneron programi konsiderohen **adresa virtuale**. Ato duhet te perkthen ne **adresa fizike** para qasjes reale ne RAM.

## 14. Faqet dhe page frames

Ne memorien virtuale, hapesira ndahet ne **faqe**.

- **Faqe (page)** - bllok i memories virtuale.
- **Page frame** - vend ne memorien fizike ku mund te vendoset nje faqe.

Madhesia e faqes zakonisht eshte fuqi e 2-shit, p.sh. 4 KB ose 8 KB.

Nese faqja nuk gjendet ne RAM, ajo duhet te sillet nga disku.

## 15. Page table dhe page fault

Cdo proces ka **page table** qe mbahet nga sistemi operativ.

Page table tregon:

- cila faqe virtuale eshte ne cilin page frame fizik,
- nese faqja eshte valide,
- nese faqja eshte ne disk,
- informata kontrolli dhe mbrojtje.

**Page fault** ndodh kur procesi kerkon nje faqe qe nuk gjendet ne memorien fizike.

Kur ndodh page fault:

1. thirret sistemi operativ,
2. gjendet faqja ne disk,
3. nese RAM-i eshte plot, largohet nje faqe tjeter,
4. faqja e kerkuar sillet ne RAM,
5. perditesohet page table,
6. procesi vazhdon.

Algoritme zevendesimi mund te perdoren, p.sh. **LRU (Least Recently Used)**.

## 16. Adresimi virtual dhe fizik

Nje adrese virtuale ndahet ne:

```text
Numri i faqes | Offset
```

Nje adrese fizike ndahet ne:

```text
Numri i page frame | Offset
```

Offset-i mbetet i njejte, ndersa numri i faqes perkthhet ne numrin e page frame-it.

Shembull nga kapitulli:

Nese hapesira virtuale eshte 8 KB dhe madhesia e faqes eshte 1 KB:

```text
8 KB / 1 KB = 8 faqe virtuale = 2^3
```

Pra duhen 3 bite per numrin e faqes. Meqenese 1 KB = `2^10`, duhen 10 bite per offset.

Adresa virtuale:

```text
3 bite page number | 10 bite offset
```

Nese memoria fizike eshte 4 KB dhe faqja eshte 1 KB:

```text
4 KB / 1 KB = 4 page frames = 2^2
```

Adresa fizike:

```text
2 bite frame number | 10 bite offset
```

## 17. Permbledhje per mesim te shpejte

Mbaji mend keto:

- **Disku magnetik ruan te dhena me fusha magnetike**
- **Koka lexon/shkruan, disku rrotullohet**
- **Trase = rreth ne disk**
- **Sektor = njesi brenda trasese**
- **Cilinder = trase me pozicion te njejte ne disa siperfaqe**
- **Seek time = levizja e kokes**
- **Rotational latency = pritja per sektorin**
- **Access time = seek time + rotational latency**
- **RAID = disa disqe si nje sistem logjik**
- **SSD = ruajtje me flash, pa pjese mekanike**
- **Memoria virtuale = adresa virtuale + perkthim ne adresa fizike**
- **Faqe = bllok virtual**
- **Page frame = bllok fizik ne RAM**
- **Page fault = faqja nuk eshte ne RAM**
- **Page table = tabela qe lidh faqet virtuale me frame-at fizik**

## 18. Pyetje te mundshme per provim

## 18.1 Cfare eshte disku magnetik?

Disku magnetik eshte pajisje ruajtese qe ruan te dhena ne siperfaqe magnetike. Ai perdor pjata rrotulluese dhe koka per lexim/shkrim.

## 18.2 Si shkruhen te dhenat ne disk magnetik?

Rryma ne koken e shkrimit krijon fushe magnetike, e cila magnetizon zona ne siperfaqen e diskut. Keta paterna magnetike perfaqesojne bitet.

## 18.3 Cfare jane traseja, sektori dhe cilindri?

Traseja eshte rreth koncentrik ne siperfaqen e diskut. Sektori eshte pjese e trasese. Cilindri eshte bashkesi trasash me te njejtin pozicion ne siperfaqe te ndryshme.

## 18.4 Nga cka varet performanca e diskut?

Varet nga seek time, rotational latency, transfer time, kontrolluesi i diskut dhe organizimi i sistemit.

## 18.5 Cfare eshte RAID?

RAID eshte perdorimi i disa disqeve si nje sistem logjik per te rritur performancen, besueshmerine ose te dyjat.

## 18.6 Cfare eshte memoria virtuale?

Memoria virtuale eshte mekanizem qe lejon proceset te perdorin adresa virtuale. Sistemi i perkthen ato ne adresa fizike dhe perdor RAM-in e diskun per te menaxhuar faqet.

## 18.7 Cfare eshte page fault?

Page fault ndodh kur procesi kerkon nje faqe qe nuk gjendet ne RAM. Sistemi operativ duhet ta sjelle faqen nga disku dhe te perditesoje page table.

## 18.8 Cili eshte dallimi mes faqes dhe page frame?

Faqja eshte bllok i memories virtuale. Page frame eshte bllok ne memorien fizike ku mund te vendoset nje faqe.
