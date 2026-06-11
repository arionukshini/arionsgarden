---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/koll-2/flashcards/","tags":["flashcards","arkitekture-kompjuterike","koll2"]}
---


# Flashcards - Arkitekturë Kompjuterike Koll 2

Përdori për active recall: mbulo përgjigjen, thuaje me zë, pastaj kontrollo.

## Kapitulli 3 - Funksioni i kompjuterit dhe interkoneksioni

### Karta 3.1
**Pyetje:** Cilat janë katër komponentet kryesore të sistemit kompjuterik?

**Përgjigje:** CPU-ja, memoria kryesore, modulet H/D dhe basi i sistemit.

### Karta 3.2
**Pyetje:** Cili është funksioni bazë i kompjuterit?

**Përgjigje:** Ekzekutimi i programeve të ruajtura në memorie.

### Karta 3.3
**Pyetje:** Çfarë shkëmbehet ndërmjet komponenteve kryesore të kompjuterit?

**Përgjigje:** Të dhëna, adresa dhe sinjale kontrolluese.

### Karta 3.4
**Pyetje:** Cila është ideja kryesore e arkitekturës von Neumann?

**Përgjigje:** Instruksionet dhe të dhënat ruhen në të njëjtën memorie shkrim-lexim dhe qasen përmes adresave.

### Karta 3.5
**Pyetje:** Pse memoria nuk e di vetë çfarë përmban?

**Përgjigje:** Sepse memoria ruan vetëm bitë; CPU-ja dhe programi e përcaktojnë kuptimin e tyre.

### Karta 3.6
**Pyetje:** Si ekzekutohen zakonisht instruksionet në modelin von Neumann?

**Përgjigje:** Në mënyrë sekuenciale, një pas një, përveç kur rrjedha ndryshohet nga jump, branch ose interrupt.

### Karta 3.7
**Pyetje:** Cili është dallimi mes programimit në harduer dhe programimit në softuer?

**Përgjigje:** Në harduer funksioni realizohet fizikisht; në softuer funksioni ndryshohet me instruksione pa ndryshuar harduerin.

### Karta 3.8
**Pyetje:** Pse programimi në softuer është më fleksibil?

**Përgjigje:** Sepse i njëjti harduer mund të kryejë detyra të ndryshme duke ekzekutuar programe të ndryshme.

### Karta 3.9
**Pyetje:** Çfarë është regjistri në CPU?

**Përgjigje:** Lokacion shumë i shpejtë brenda CPU-së për ruajtje të përkohshme të adresave, instruksioneve ose të dhënave.

### Karta 3.10
**Pyetje:** Çfarë ruan PC?

**Përgjigje:** Adresën e instruksionit vijues që duhet të sillet nga memoria.

### Karta 3.11
**Pyetje:** Çfarë ruan IR?

**Përgjigje:** Instruksionin aktual që është duke u ekzekutuar.

### Karta 3.12
**Pyetje:** Çfarë ruan MAR?

**Përgjigje:** Adresën e memories për operacionin e ardhshëm lexim/shkrim.

### Karta 3.13
**Pyetje:** Çfarë ruan MBR?

**Përgjigje:** Të dhënat që lexohen nga memoria ose shkruhen në memorie.

### Karta 3.14
**Pyetje:** Çfarë ruan I/O AR?

**Përgjigje:** Adresën e pajisjes ose modulit hyrës/dalës me të cilin komunikon CPU-ja.

### Karta 3.15
**Pyetje:** Çfarë ruan I/O BR?

**Përgjigje:** Të dhëna të përkohshme që shkëmbehen mes CPU-së dhe modulit H/D.

### Karta 3.16
**Pyetje:** Cili është dallimi mes MAR dhe MBR?

**Përgjigje:** MAR ruan adresën e memories; MBR ruan të dhënat që transferohen me memorien.

### Karta 3.17
**Pyetje:** Cili është dallimi mes PC dhe IR?

**Përgjigje:** PC tregon adresën e instruksionit të ardhshëm; IR mban instruksionin aktual.

### Karta 3.18
**Pyetje:** Çfarë bën njësia e kontrollit?

**Përgjigje:** Koordinon punën e regjistrave, memories, moduleve H/D dhe njësive ekzekutuese.

### Karta 3.19
**Pyetje:** Çfarë bën ALU?

**Përgjigje:** Kryen operacione aritmetike dhe logjike.

### Karta 3.20
**Pyetje:** Çfarë bën FPU?

**Përgjigje:** Kryen operacione me numra realë ose me presje lëvizëse.

### Karta 3.21
**Pyetje:** Si organizohet memoria kryesore?

**Përgjigje:** Si bashkësi lokacionesh memoruese, ku çdo lokacion ka adresë.

### Karta 3.22
**Pyetje:** Pse pajisjet H/D zakonisht nuk lidhen direkt me CPU-në dhe memorien?

**Përgjigje:** Sepse janë më të ngadalshme, kanë formate/shpejtësi të ndryshme dhe kërkojnë kontroll, baferim dhe zbulim gabimesh.

### Karta 3.23
**Pyetje:** Çfarë është moduli H/D?

**Përgjigje:** Ndërfaqe ndërmjet pajisjeve të jashtme dhe CPU-së/memories.

### Karta 3.24
**Pyetje:** Cilat janë funksionet kryesore të modulit H/D?

**Përgjigje:** Kontroll/timing, komunikim me procesorin, komunikim me pajisjen, baferim dhe zbulim gabimesh.

### Karta 3.25
**Pyetje:** Çfarë është baferimi?

**Përgjigje:** Ruajtje e përkohshme e të dhënave gjatë transferimit ndërmjet komponenteve me shpejtësi të ndryshme.

### Karta 3.26
**Pyetje:** Pse është i rëndësishëm baferimi?

**Përgjigje:** Sepse parandalon që CPU-ja ose memoria e shpejtë të presin direkt pajisjet e ngadalshme.

### Karta 3.27
**Pyetje:** Çfarë është spooling?

**Përgjigje:** Formë e baferimit, p.sh. dokumenti vendoset në bafer printeri që CPU-ja të vazhdojë punë tjera.

### Karta 3.28
**Pyetje:** Çfarë është basi i sistemit?

**Përgjigje:** Rruga e interkoneksionit që lidh CPU-në, memorien dhe modulet H/D.

### Karta 3.29
**Pyetje:** Cilat janë tri pjesët kryesore të basit?

**Përgjigje:** Data Bus, Address Bus dhe Control Bus.

### Karta 3.30
**Pyetje:** Çfarë bart Data Bus?

**Përgjigje:** Të dhëna ndërmjet CPU-së, memories dhe moduleve H/D.

### Karta 3.31
**Pyetje:** Çfarë bart Address Bus?

**Përgjigje:** Adresa të lokacioneve të memories ose pajisjeve H/D.

### Karta 3.32
**Pyetje:** Çfarë bart Control Bus?

**Përgjigje:** Sinjale kontrolluese dhe sinkronizuese si Read, Write, Interrupt, Clock dhe Reset.

### Karta 3.33
**Pyetje:** Cilat janë dy fazat bazë të ciklit të instruksionit?

**Përgjigje:** Fetch cycle dhe Execute cycle.

### Karta 3.34
**Pyetje:** Çfarë ndodh gjatë fetch cycle?

**Përgjigje:** CPU-ja përdor PC për ta marrë instruksionin nga memoria, e vendos në IR dhe zakonisht e rrit PC.

### Karta 3.35
**Pyetje:** Çfarë ndodh gjatë execute cycle?

**Përgjigje:** CPU-ja dekodon instruksionin dhe kryen operacionin e kërkuar.

### Karta 3.36
**Pyetje:** Në kompjuterin hipotetik, çfarë bën opcode `1H`?

**Përgjigje:** Ngarkon AC me përmbajtjen nga memoria.

### Karta 3.37
**Pyetje:** Në kompjuterin hipotetik, çfarë bën opcode `2H`?

**Përgjigje:** Ruan përmbajtjen e AC në memorie.

### Karta 3.38
**Pyetje:** Në kompjuterin hipotetik, çfarë bën opcode `5H`?

**Përgjigje:** Mbledh AC me përmbajtjen nga memoria.

### Karta 3.39
**Pyetje:** Çfarë bën instruksioni `1940` në shembull?

**Përgjigje:** Ngarkon AC me përmbajtjen e adresës 940.

### Karta 3.40
**Pyetje:** Çfarë bën instruksioni `5941` në shembull?

**Përgjigje:** Mbledh AC me përmbajtjen e adresës 941.

### Karta 3.41
**Pyetje:** Çfarë bën instruksioni `2941` në shembull?

**Përgjigje:** Ruan AC në adresën 941.

### Karta 3.42
**Pyetje:** Çfarë është interrupt?

**Përgjigje:** Ngjarje që kërkon nga CPU-ja ta ndalojë përkohësisht programin aktual dhe të trajtojë një ngjarje tjetër.

### Karta 3.43
**Pyetje:** Çfarë është ISR?

**Përgjigje:** Interrupt Service Routine, rutina që trajton ndërprerjen.

### Karta 3.44
**Pyetje:** Pse interruptet e përmirësojnë performancën?

**Përgjigje:** Sepse CPU-ja mund të vazhdojë punë tjera derisa pajisjet e ngadalshme H/D punojnë në sfond.

### Karta 3.45
**Pyetje:** Çfarë ndodh kur ndodh një interrupt?

**Përgjigje:** CPU-ja ruan kontekstin, kalon te handler-i, e shërben ngjarjen, rikthen kontekstin dhe vazhdon programin.

### Karta 3.46
**Pyetje:** Cili është dallimi mes maskable interrupt dhe NMI?

**Përgjigje:** Maskable interrupt mund të çaktivizohet ose injorohet përkohësisht; NMI është kritik dhe duhet trajtuar.

### Karta 3.47
**Pyetje:** Çfarë është polling?

**Përgjigje:** Kur CPU-ja kontrollon vazhdimisht statusin e pajisjes për të parë nëse është gati.

### Karta 3.48
**Pyetje:** Pse polling është joefikas?

**Përgjigje:** Sepse CPU-ja harxhon kohë duke kontrolluar ose pritur pajisje të ngadalshme.

### Karta 3.49
**Pyetje:** Çfarë janë nested interrupts?

**Përgjigje:** Kur një interrupt me prioritet më të lartë e ndërpret handler-in e një interrupt-i me prioritet më të ulët.

### Karta 3.50
**Pyetje:** Cila është përparësia e interrupteve me prioritet?

**Përgjigje:** Pajisjet ose ngjarjet kritike trajtohen më shpejt.

## Kapitulli 4 - Memoria kesh

### Karta 4.1
**Pyetje:** Pse përdoret hierarkia e memories?

**Përgjigje:** Sepse CPU-ja është shumë më e shpejtë se memoria kryesore/eksterne, ndërsa memoriet e shpejta janë të vogla dhe të shtrenjta.

### Karta 4.2
**Pyetje:** Çfarë ndodh duke lëvizur poshtë hierarkisë së memories?

**Përgjigje:** Kostoja për bit bie, kapaciteti rritet, koha e qasjes rritet dhe qasja nga CPU-ja bëhet më e rrallë.

### Karta 4.3
**Pyetje:** Rendite hierarkinë e memories nga më e shpejta te më e ngadalta.

**Përgjigje:** Regjistra -> L1 cache -> L2 cache -> L3 cache -> RAM -> SSD/HDD -> arkiv/cloud.

### Karta 4.4
**Pyetje:** Çfarë është memoria interne?

**Përgjigje:** Memorie brenda sistemit kryesor, si regjistrat, cache dhe RAM.

### Karta 4.5
**Pyetje:** Çfarë është memoria eksterne?

**Përgjigje:** Ruajtje me kapacitet më të madh dhe zakonisht më e ngadalshme, si HDD, SSD, USB flash ose cloud.

### Karta 4.6
**Pyetje:** Çfarë është njësia e adresueshme?

**Përgjigje:** Njësia më e vogël që mund të adresohet nga procesori, shpesh një bajt.

### Karta 4.7
**Pyetje:** Cila është formula që lidh bitët e adresës me njësitë e adresueshme?

**Përgjigje:** `2^A = N`, ku A është numri i bitëve të adresës dhe N numri i njësive të adresueshme.

### Karta 4.8
**Pyetje:** Sa memorie mund të adresojë një sistem 32-bit me adresim në bajt?

**Përgjigje:** `2^32` bajtë, rreth 4 GB.

### Karta 4.9
**Pyetje:** Cilat janë metodat kryesore të qasjes në memorie?

**Përgjigje:** Qasje sekuenciale, direkte, e rastit dhe asociative.

### Karta 4.10
**Pyetje:** Çfarë është qasja e rastit?

**Përgjigje:** Çdo lokacion mund të adresohet direkt me kohë qasjeje përafërsisht konstante.

### Karta 4.11
**Pyetje:** Çfarë është qasja asociative?

**Përgjigje:** Kërkimi bëhet sipas përmbajtjes, jo sipas adresës.

### Karta 4.12
**Pyetje:** Çfarë është koha e qasjes?

**Përgjigje:** Koha nga kërkesa për memorie deri te momenti kur të dhënat janë të gatshme.

### Karta 4.13
**Pyetje:** Çfarë është koha e ciklit memorues?

**Përgjigje:** Koha e qasjes plus koha shtesë para se të fillojë qasja tjetër.

### Karta 4.14
**Pyetje:** Çfarë është memoria volatile?

**Përgjigje:** Memorie që humb përmbajtjen kur largohet energjia.

### Karta 4.15
**Pyetje:** Çfarë është memoria nonvolatile?

**Përgjigje:** Memorie që ruan përmbajtjen edhe pa energji.

### Karta 4.16
**Pyetje:** Çfarë është memoria kesh?

**Përgjigje:** Memorie e vogël dhe shumë e shpejtë afër CPU-së që ruan kopje të blloqeve të memories kryesore.

### Karta 4.17
**Pyetje:** Cili është qëllimi kryesor i cache-it?

**Përgjigje:** Zvogëlimi i kohës mesatare të qasjes në memorie dhe i pritjes së CPU-së.

### Karta 4.18
**Pyetje:** Çfarë është cache hit?

**Përgjigje:** Kur e dhëna e kërkuar gjendet në cache.

### Karta 4.19
**Pyetje:** Çfarë është cache miss?

**Përgjigje:** Kur e dhëna e kërkuar nuk gjendet në cache dhe duhet marrë nga një nivel më i ulët.

### Karta 4.20
**Pyetje:** Çfarë është miss rate?

**Përgjigje:** Probabiliteti i cache miss; `m = 1 - h`.

### Karta 4.21
**Pyetje:** Çfarë është miss penalty?

**Përgjigje:** Koha shtesë që nevojitet për ta shërbyer një miss nga një nivel më i ulët i memories.

### Karta 4.22
**Pyetje:** Cila është formula e EMAT?

**Përgjigje:** `EMAT = Tc + m * Tm`.

### Karta 4.23
**Pyetje:** Në `EMAT = Tc + m * Tm`, çfarë është `Tc`?

**Përgjigje:** Koha e qasjes në cache.

### Karta 4.24
**Pyetje:** Në `EMAT = Tc + m * Tm`, çfarë është `m`?

**Përgjigje:** Miss rate.

### Karta 4.25
**Pyetje:** Në `EMAT = Tc + m * Tm`, çfarë është `Tm`?

**Përgjigje:** Miss penalty.

### Karta 4.26
**Pyetje:** Çfarë është lokaliteti kohor?

**Përgjigje:** Nëse një e dhënë përdoret tani, ka gjasa të përdoret përsëri së shpejti.

### Karta 4.27
**Pyetje:** Çfarë është lokaliteti hapësinor?

**Përgjigje:** Nëse përdoret një lokacion, ka gjasa të përdoren edhe lokacionet afër tij.

### Karta 4.28
**Pyetje:** Pse cache transferon blloqe dhe jo vetëm një fjalë?

**Përgjigje:** Për të shfrytëzuar lokalitetin hapësinor.

### Karta 4.29
**Pyetje:** Cila është radha tipike e kërkimit të të dhënës në cache?

**Përgjigje:** L1 -> L2 -> L3 -> RAM.

### Karta 4.30
**Pyetje:** Çfarë është DMA?

**Përgjigje:** Direct Memory Access, mekanizëm ku pajisja H/D transferon të dhëna direkt në/nga RAM pa e ngarkuar CPU-në me çdo bajt.

### Karta 4.31
**Pyetje:** Çfarë është cache line?

**Përgjigje:** Një linjë/bllok në cache ku ruhet një bllok i kopjuar nga memoria kryesore.

### Karta 4.32
**Pyetje:** Pse çdo cache line ruan tag?

**Përgjigje:** Për të identifikuar cili bllok i memories kryesore gjendet në atë linjë.

### Karta 4.33
**Pyetje:** Cilat janë tri teknikat kryesore të pasqyrimit në cache?

**Përgjigje:** Pasqyrimi direkt, asociativ dhe set-asociativ.

### Karta 4.34
**Pyetje:** Çfarë është pasqyrimi direkt?

**Përgjigje:** Çdo bllok i memories kryesore mund të vendoset vetëm në një linjë të caktuar të cache-it.

### Karta 4.35
**Pyetje:** Cila është formula e pasqyrimit direkt?

**Përgjigje:** `i = j mod m`, ku i është linja në cache, j blloku në memorie dhe m numri i linjave të cache-it.

### Karta 4.36
**Pyetje:** Cila është struktura e adresës te pasqyrimi direkt?

**Përgjigje:** `Tag | Line number | Block offset`.

### Karta 4.37
**Pyetje:** Cila është përparësia kryesore e pasqyrimit direkt?

**Përgjigje:** Është i thjeshtë, i lirë dhe i shpejtë për implementim.

### Karta 4.38
**Pyetje:** Cila është mangësia kryesore e pasqyrimit direkt?

**Përgjigje:** Shkakton shumë konflikte sepse disa blloqe konkurrojnë për të njëjtën linjë.

### Karta 4.39
**Pyetje:** Çfarë është pasqyrimi plotësisht asociativ?

**Përgjigje:** Çdo bllok i memories kryesore mund të vendoset në cilëndo linjë të cache-it.

### Karta 4.40
**Pyetje:** Cila është struktura e adresës te pasqyrimi asociativ?

**Përgjigje:** `Tag | Block offset`.

### Karta 4.41
**Pyetje:** Cila është mangësia kryesore e pasqyrimit asociativ?

**Përgjigje:** Kërkon harduer më kompleks për krahasim paralel të tag-eve.

### Karta 4.42
**Pyetje:** Çfarë është pasqyrimi set-asociativ?

**Përgjigje:** Blloku shkon në një set të caktuar, por mund të vendoset në cilëndo linjë brenda atij seti.

### Karta 4.43
**Pyetje:** Cila është formula e set-it te pasqyrimi set-asociativ?

**Përgjigje:** `set = block number mod number of sets`.

### Karta 4.44
**Pyetje:** Cila është struktura e adresës te pasqyrimi set-asociativ?

**Përgjigje:** `Tag | Set number | Block offset`.

### Karta 4.45
**Pyetje:** Çfarë do të thotë k-way set-associative?

**Përgjigje:** Çdo set ka k linja cache.

### Karta 4.46
**Pyetje:** Pse pasqyrimi set-asociativ përdoret shumë?

**Përgjigje:** Sepse zvogëlon konfliktet e pasqyrimit direkt pa kompleksitetin maksimal të pasqyrimit plotësisht asociativ.

### Karta 4.47
**Pyetje:** Çfarë është algoritmi i zëvendësimit në cache?

**Përgjigje:** Rregulli që zgjedh cili bllok largohet kur cache është plot dhe ndodh miss.

### Karta 4.48
**Pyetje:** Çfarë zëvendëson LRU?

**Përgjigje:** Bllokun që nuk është përdorur për kohën më të gjatë.

### Karta 4.49
**Pyetje:** Çfarë zëvendëson FIFO?

**Përgjigje:** Bllokun që ka hyrë i pari në cache.

### Karta 4.50
**Pyetje:** Çfarë është write-through?

**Përgjigje:** Shkrimi bëhet menjëherë edhe në cache edhe në memorien kryesore.

### Karta 4.51
**Pyetje:** Çfarë është write-back?

**Përgjigje:** Shkrimi bëhet fillimisht vetëm në cache; memoria kryesore përditësohet kur blloku largohet.

### Karta 4.52
**Pyetje:** Cila është përparësia kryesore e write-through?

**Përgjigje:** Memoria kryesore është gjithmonë e përditësuar.

### Karta 4.53
**Pyetje:** Cila është përparësia kryesore e write-back?

**Përgjigje:** Ka më pak trafik në bus dhe zakonisht performancë më të mirë.

## Kapitulli 5 - Memoria gjysmëpërçuese

### Karta 5.1
**Pyetje:** Cilat janë dy format tradicionale të RAM-it?

**Përgjigje:** DRAM dhe SRAM.

### Karta 5.2
**Pyetje:** Për çka përdoret zakonisht DRAM?

**Përgjigje:** Për memorien kryesore.

### Karta 5.3
**Pyetje:** Për çka përdoret zakonisht SRAM?

**Përgjigje:** Për cache memory.

### Karta 5.4
**Pyetje:** Si e ruan DRAM një bit?

**Përgjigje:** Si ngarkesë elektrike në kondensator.

### Karta 5.5
**Pyetje:** Nga cilat elemente përbëhet qeliza tipike DRAM?

**Përgjigje:** Nga një transistor dhe një kondensator.

### Karta 5.6
**Pyetje:** Pse DRAM quhet dinamike?

**Përgjigje:** Sepse ngarkesa në kondensator humbet gradualisht dhe duhet rifreskuar.

### Karta 5.7
**Pyetje:** Çfarë bën refresh në DRAM?

**Përgjigje:** Lexon dhe rishkruan vlerën e ruajtur për ta rikthyer ngarkesën në kondensator.

### Karta 5.8
**Pyetje:** Pse refresh ndikon negativisht në performancë?

**Përgjigje:** Sepse merr kohë, konsumon energji dhe ndërhyn në qasjet normale në memorie.

### Karta 5.9
**Pyetje:** Si e ruan SRAM një bit?

**Përgjigje:** Me latch ose flip-flop.

### Karta 5.10
**Pyetje:** Pse SRAM nuk ka nevojë për refresh?

**Përgjigje:** Sepse latch-i e ruan gjendjen sa kohë ka energji.

### Karta 5.11
**Pyetje:** Cila është përparësia kryesore e SRAM ndaj DRAM?

**Përgjigje:** SRAM është më e shpejtë dhe nuk kërkon refresh.

### Karta 5.12
**Pyetje:** Cila është mangësia kryesore e SRAM ndaj DRAM?

**Përgjigje:** SRAM është më e shtrenjtë dhe ka densitet më të vogël.

### Karta 5.13
**Pyetje:** Cila ka densitet më të lartë, DRAM apo SRAM?

**Përgjigje:** DRAM.

### Karta 5.14
**Pyetje:** Cila është më e përshtatshme për cache, DRAM apo SRAM?

**Përgjigje:** SRAM.

### Karta 5.15
**Pyetje:** Çfarë do të thotë lexim jo-destruktiv në SRAM?

**Përgjigje:** Leximi nuk duhet ta ndryshojë ose humbë vlerën e ruajtur në qelizë.

### Karta 5.16
**Pyetje:** Çfarë është ROM?

**Përgjigje:** Memorie jo e avullueshme, kryesisht vetëm për lexim gjatë përdorimit normal.

### Karta 5.17
**Pyetje:** Për çka përdoret zakonisht ROM?

**Përgjigje:** Për firmware ose programe/të dhëna të përhershme.

### Karta 5.18
**Pyetje:** Çfarë është PROM?

**Përgjigje:** ROM i programueshëm që mund të shkruhet një herë pas prodhimit.

### Karta 5.19
**Pyetje:** Çfarë është EPROM?

**Përgjigje:** PROM që mund të fshihet, zakonisht me dritë ultraviolet, dhe të riprogramohet.

### Karta 5.20
**Pyetje:** Çfarë është EEPROM?

**Përgjigje:** PROM që mund të fshihet dhe shkruhet elektrikisht.

### Karta 5.21
**Pyetje:** Cili është dallimi kryesor mes EPROM dhe EEPROM?

**Përgjigje:** EPROM zakonisht fshihet me dritë UV; EEPROM fshihet dhe shkruhet elektrikisht.

### Karta 5.22
**Pyetje:** Çfarë është flash memory?

**Përgjigje:** Memorie gjysmëpërçuese jo e avullueshme që fshihet elektrikisht në blloqe.

### Karta 5.23
**Pyetje:** Ku përdoret flash memory?

**Përgjigje:** Në SSD, USB, karta memorie, pajisje mobile dhe ruajtje firmware-i.

### Karta 5.24
**Pyetje:** Çfarë bëjnë RAS dhe CAS në DRAM?

**Përgjigje:** RAS zgjedh rreshtin, CAS zgjedh kolonën.

### Karta 5.25
**Pyetje:** Pse adresat në DRAM multipleksohen në rresht dhe kolonë?

**Përgjigje:** Për ta zvogëluar numrin e pinave të adresës në çip.

### Karta 5.26
**Pyetje:** Cilat janë dy kategoritë kryesore të gabimeve në memorie?

**Përgjigje:** Gabime harduerike dhe gabime softuerike.

### Karta 5.27
**Pyetje:** Çfarë janë gabimet softuerike në memorie?

**Përgjigje:** Ndryshime të përkohshme të bitëve, shpesh nga rrezatimi ose efektet elektrike.

### Karta 5.28
**Pyetje:** Nëse fjala ka M bitë të dhënash dhe kodi K bitë, sa bitë ruhen gjithsej?

**Përgjigje:** `M + K` bitë.

### Karta 5.29
**Pyetje:** Çfarë është sindroma në korrigjimin e gabimeve?

**Përgjigje:** Vlerë kontrolluese që tregon nëse ka gabim dhe ku mund të jetë.

### Karta 5.30
**Pyetje:** Çfarë bën kodi i Hamming-ut?

**Përgjigje:** Detekton dhe korrigjon gabime me një bit.

### Karta 5.31
**Pyetje:** Çfarë do të thotë sindroma zero te Hamming?

**Përgjigje:** Nuk është detektuar gabim.

### Karta 5.32
**Pyetje:** Çfarë identifikon një sindromë jo-zero te Hamming?

**Përgjigje:** Pozicionin e bitit në gabim, varësisht nga vlera e sindromës.

## Kapitulli 6 - Memoria eksterne dhe memoria virtuale

### Karta 6.1
**Pyetje:** Çfarë është disku magnetik?

**Përgjigje:** Pajisje ruajtëse që ruan të dhëna në sipërfaqe magnetike.

### Karta 6.2
**Pyetje:** Cilat janë pjesët kryesore të një sistemi me disk magnetik?

**Përgjigje:** Pjata, sipërfaqe magnetike, kokë lexim/shkrim, mekanizëm rrotullimi dhe kontrollues disku.

### Karta 6.3
**Pyetje:** Si shkruhen të dhënat në disk magnetik?

**Përgjigje:** Rryma në kokën e shkrimit krijon fushë magnetike që magnetizon zona të sipërfaqes së diskut.

### Karta 6.4
**Pyetje:** Si lexohen të dhënat nga disku magnetik?

**Përgjigje:** Ndryshimet magnetike nën kokë induktojnë sinjal elektrik që interpretohet si bitë.

### Karta 6.5
**Pyetje:** Çfarë është traseja/pista?

**Përgjigje:** Rreth koncentrik në sipërfaqen e diskut ku ruhen të dhënat.

### Karta 6.6
**Pyetje:** Çfarë është sektori?

**Përgjigje:** Ndarje e trasesë dhe njësi bazë e adresimit/transferit në disk.

### Karta 6.7
**Pyetje:** Çfarë është cilindri?

**Përgjigje:** Bashkësi trasash me të njëjtin pozicion në disa sipërfaqe të diskut.

### Karta 6.8
**Pyetje:** Çfarë është cluster?

**Përgjigje:** Grup sektorësh që sistemi i skedarëve e trajton si njësi alokimi.

### Karta 6.9
**Pyetje:** Çfarë është CAV?

**Përgjigje:** Constant Angular Velocity, kur disku rrotullohet me shpejtësi këndore konstante.

### Karta 6.10
**Pyetje:** Cila është mangësia e CAV të thjeshtë?

**Përgjigje:** Trasetë e jashtme mund të mos shfrytëzohen plotësisht nëse numri i sektorëve është fiks.

### Karta 6.11
**Pyetje:** Çfarë është regjistrimi në zona?

**Përgjigje:** Ndarja e trasave në zona, ku zonat e jashtme mund të ruajnë më shumë sektorë.

### Karta 6.12
**Pyetje:** Pse formatohet disku?

**Përgjigje:** Për të shënuar sektorët, adresat, informacionin sinkronizues dhe fushat për kontroll gabimesh.

### Karta 6.13
**Pyetje:** Çfarë është seek time?

**Përgjigje:** Koha që nevojitet për ta lëvizur kokën në trasenë e duhur.

### Karta 6.14
**Pyetje:** Çfarë është rotational latency?

**Përgjigje:** Koha e pritjes derisa sektori i duhur të rrotullohet nën kokë.

### Karta 6.15
**Pyetje:** Çfarë është access time te disku?

**Përgjigje:** `Seek time + rotational latency`.

### Karta 6.16
**Pyetje:** Çfarë është transfer time?

**Përgjigje:** Koha për transferimin e të dhënave pasi sektori është nën kokë.

### Karta 6.17
**Pyetje:** Çfarë është RAID?

**Përgjigje:** Redundant Array of Independent Disks, disa disqe që punojnë si një sistem logjik.

### Karta 6.18
**Pyetje:** Cili është qëllimi i RAID?

**Përgjigje:** Rritja e performancës, besueshmërisë ose të dyjave.

### Karta 6.19
**Pyetje:** Çfarë është striping në RAID?

**Përgjigje:** Ndarja e të dhënave në disa disqe për performancë më të lartë.

### Karta 6.20
**Pyetje:** Çfarë është mirroring në RAID?

**Përgjigje:** Kopjimi i të dhënave në më shumë se një disk për besueshmëri.

### Karta 6.21
**Pyetje:** Çfarë është pariteti në RAID?

**Përgjigje:** Informacion shtesë që ndihmon në rikonstruktimin e të dhënave pas dështimit të një disku.

### Karta 6.22
**Pyetje:** Çfarë është SSD?

**Përgjigje:** Solid State Drive, pajisje ruajtëse me flash memory dhe pa pjesë mekanike lëvizëse.

### Karta 6.23
**Pyetje:** Cila është përparësia kryesore e SSD ndaj HDD?

**Përgjigje:** Latencë më e ulët sepse nuk ka lëvizje mekanike të kokës ose rrotullim pllakash.

### Karta 6.24
**Pyetje:** Çfarë është memoria virtuale?

**Përgjigje:** Mekanizëm që lejon programet të përdorin adresa virtuale që përkthehen në adresa fizike.

### Karta 6.25
**Pyetje:** Pse quhet memorie virtuale?

**Përgjigje:** Sepse hapësira e adresave që sheh programi nuk është e gjitha RAM fizik.

### Karta 6.26
**Pyetje:** Cilat janë dy qëllime kryesore të memories virtuale?

**Përgjigje:** Zgjerim logjik i memories dhe mbrojtje/izolim i proceseve.

### Karta 6.27
**Pyetje:** Çfarë është procesi?

**Përgjigje:** Program në ekzekutim bashkë me strukturat e nevojshme për menaxhimin e tij.

### Karta 6.28
**Pyetje:** Çfarë është hapësira e adresave e një procesi?

**Përgjigje:** Bashkësia e adresave virtuale që procesi mund të përdorë.

### Karta 6.29
**Pyetje:** Kur gjeneron adresa një program?

**Përgjigje:** Gjatë instruksioneve load, store dhe fetch të instruksioneve.

### Karta 6.30
**Pyetje:** Çfarë është adresa virtuale?

**Përgjigje:** Adresa që gjeneron programi/procesi.

### Karta 6.31
**Pyetje:** Çfarë është adresa fizike?

**Përgjigje:** Adresa reale në RAM pas përkthimit.

### Karta 6.32
**Pyetje:** Çfarë është faqja/page?

**Përgjigje:** Bllok i memories virtuale.

### Karta 6.33
**Pyetje:** Çfarë është page frame?

**Përgjigje:** Bllok fizik në RAM ku mund të vendoset një faqe.

### Karta 6.34
**Pyetje:** Çfarë është page table?

**Përgjigje:** Tabelë që lidh faqet virtuale me page frames fizike.

### Karta 6.35
**Pyetje:** Çfarë është page fault?

**Përgjigje:** Kur procesi kërkon një faqe që nuk është aktualisht në RAM.

### Karta 6.36
**Pyetje:** Çfarë ndodh gjatë page fault?

**Përgjigje:** OS e sjell faqen nga disku, mund të largojë një faqe tjetër, përditëson page table dhe vazhdon procesin.

### Karta 6.37
**Pyetje:** Cili është ekuivalenti i cache miss te memoria virtuale?

**Përgjigje:** Page fault.

### Karta 6.38
**Pyetje:** Si ndahet adresa virtuale?

**Përgjigje:** `Page number | Offset`.

### Karta 6.39
**Pyetje:** Si ndahet adresa fizike?

**Përgjigje:** `Page frame number | Offset`.

### Karta 6.40
**Pyetje:** Çfarë ndodh me offset-in gjatë përkthimit virtual-fizik?

**Përgjigje:** Offset-i mbetet i njëjtë.

## Detyra të shkurtra

### Detyra 1
**Pyetje:** Një sistem byte-addressable ka adresa 32-bit. Sa memorie mund të adresohet maksimalisht?

**Përgjigje:** `2^32` bajtë, rreth 4 GB.

### Detyra 2
**Pyetje:** Një cache ka 64 linja. Sa bitë duhen për line number?

**Përgjigje:** 6 bitë, sepse `64 = 2^6`.

### Detyra 3
**Pyetje:** Një bllok ka madhësi 256 B. Sa bitë duhen për block offset?

**Përgjigje:** 8 bitë, sepse `256 = 2^8`.

### Detyra 4
**Pyetje:** Një bllok/faqe ka madhësi 1 KB. Sa bitë duhen për offset?

**Përgjigje:** 10 bitë, sepse `1 KB = 2^10` bajtë.

### Detyra 5
**Pyetje:** Në pasqyrim direkt, cache ka 6 linja. Në cilën linjë shkon blloku 17?

**Përgjigje:** `17 mod 6 = 5`, pra në linjën 5 nëse numërimi fillon nga 0.

### Detyra 6
**Pyetje:** Nëse hit rate është 99%, sa është miss rate?

**Përgjigje:** 1%.

### Detyra 7
**Pyetje:** Nëse `Tc = 10 ns`, `m = 0.01`, dhe `Tm = 100 ns`, sa është EMAT?

**Përgjigje:** `10 + 0.01 * 100 = 11 ns`.

### Detyra 8
**Pyetje:** Hapësira virtuale është 8 KB dhe madhësia e faqes 1 KB. Sa faqe virtuale ka?

**Përgjigje:** 8 faqe.

### Detyra 9
**Pyetje:** Hapësira virtuale është 8 KB dhe faqja 1 KB. Sa bitë duhen për numrin e faqes?

**Përgjigje:** 3 bitë.

### Detyra 10
**Pyetje:** Memoria fizike është 4 KB dhe faqja 1 KB. Sa page frames ka?

**Përgjigje:** 4 page frames.

### Detyra 11
**Pyetje:** Memoria fizike është 4 KB dhe faqja 1 KB. Sa bitë duhen për frame number?

**Përgjigje:** 2 bitë.

### Detyra 12
**Pyetje:** Një format instruksioni ka 4 bitë opcode dhe 12 bitë adresë. Sa kode operacionesh janë të mundshme?

**Përgjigje:** `2^4 = 16` kode operacionesh.

### Detyra 13
**Pyetje:** Një format instruksioni ka 12 bitë adresë. Sa fjalë memorike mund të adresohen?

**Përgjigje:** `2^12 = 4096` fjalë.

## Karta kurth

### Kurth 1
**Pyetje:** PC apo MAR: cili ruan adresën e instruksionit vijues?

**Përgjigje:** PC ruan adresën e instruksionit vijues; MAR ruan adresën për qasjen aktuale në memorie.

### Kurth 2
**Pyetje:** IR apo MBR: cili ruan instruksionin aktual?

**Përgjigje:** IR ruan instruksionin aktual; MBR ruan të dhënat që transferohen me memorien.

### Kurth 3
**Pyetje:** Cili shkakton kërkim në RAM: cache hit apo cache miss?

**Përgjigje:** Cache miss.

### Kurth 4
**Pyetje:** Miss rate është `h` apo `1 - h`?

**Përgjigje:** `1 - h`.

### Kurth 5
**Pyetje:** Në pasqyrim direkt, a mund të shkojë blloku në cilëndo linjë cache?

**Përgjigje:** Jo. Mund të shkojë vetëm në linjën e zgjedhur nga `j mod m`.

### Kurth 6
**Pyetje:** Në pasqyrim plotësisht asociativ, a ka fushë line number?

**Përgjigje:** Jo. Adresa ka tag dhe block offset.

### Kurth 7
**Pyetje:** Cila politikë e mban memorien kryesore gjithmonë të përditësuar: write-through apo write-back?

**Përgjigje:** Write-through.

### Kurth 8
**Pyetje:** Cila përdor kondensatorë: DRAM apo SRAM?

**Përgjigje:** DRAM.

### Kurth 9
**Pyetje:** Cila ka nevojë për refresh: DRAM apo SRAM?

**Përgjigje:** DRAM.

### Kurth 10
**Pyetje:** Cili është blloku fizik në RAM: page apo page frame?

**Përgjigje:** Page frame.

### Kurth 11
**Pyetje:** Cili është blloku virtual: page apo page frame?

**Përgjigje:** Page.

### Kurth 12
**Pyetje:** Cili shkon në disk: cache miss apo page fault?

**Përgjigje:** Page fault.

### Kurth 13
**Pyetje:** Seek time apo rotational latency: cila është lëvizja e kokës?

**Përgjigje:** Seek time.

### Kurth 14
**Pyetje:** Seek time apo rotational latency: cila është pritja për sektorin?

**Përgjigje:** Rotational latency.

### Kurth 15
**Pyetje:** Cila e lejon CPU-në të vazhdojë punë derisa pajisja punon: interrupt apo polling?

**Përgjigje:** Interrupt.

