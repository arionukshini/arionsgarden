---
{"dg-publish":true,"permalink":"/semester-5/sisteme-operative/notes-gpt/","tags":["universitet","semestri-5","sisteme-operative"],"dg-note-properties":{"tags":["universitet","semestri-5","sisteme-operative"]}}
---

# Sisteme Operative — shënime nga ligjëratat dhe ushtrimet

## Si lidhen temat

Lënda fillon me rolin e sistemit operativ, vazhdon me funksionet, shërbimet dhe strukturën e tij, pastaj trajton proceset dhe komunikimin ndërmjet tyre. Ushtrimet i zbatojnë këto koncepte në Ubuntu përmes terminalit, gjuhës C, thirrjeve sistemore, lejeve të fajllave dhe makinave virtuale.

1. **Bazat:** pjesët e kompjuterit, ndërprerjet, nisja e sistemit, llojet e sistemeve operative dhe multiprogramimi.
2. **Funksionet:** menaxhimi i proceseve, memories, fajllave, pajisjeve, hyrjes/daljes, memories cache dhe sigurisë.
3. **Ndërfaqet:** ndërfaqja e përdoruesit, API-të, thirrjet sistemore, programet sistemore, lidhësi dhe ngarkuesi.
4. **Struktura:** organizimi i bërthamës, ndërtimi dhe nisja e sistemit, gjetja e gabimeve dhe përmirësimi i performancës.
5. **Proceset:** gjendjet, PCB-ja, skedulimi, ndërrimi i kontekstit, krijimi dhe përfundimi.
6. **Komunikimi:** memoria e përbashkët, kalimi i mesazheve, gypat, socket-at dhe RPC-ja.
7. **Zbatimi praktik:** Ubuntu, komandat, lejet, kompajlimi në C, folderët e përbashkët, kopjimi i fajllave, fork/exec/wait dhe shtimi i një thirrjeje sistemore.

## 1. Çfarë bën sistemi operativ?

### Përkufizimi dhe qëllimi

**Sistemi operativ (SO)** është shtresa softuerike ndërmjet përdoruesve ose aplikacioneve dhe harduerit të kompjuterit. Ai menaxhon harduerin dhe krijon një mjedis ku programet mund të ekzekutohen në mënyrë të përshtatshme dhe efikase. Mund ta shohim në dy role:

- si **ndarës të burimeve**, që vendos si do të ndahen koha e CPU-së, memoria, hapësira ruajtëse dhe pajisjet; dhe
- si **program kontrollues**, që mbikëqyr ekzekutimin dhe parandalon që gabimet ose përdorimi i paautorizuar ta çrregullojnë sistemin.

SO-ja ofron mjedisin dhe shërbimet që u mundësojnë aplikacioneve të kryejnë punë të dobishme. Nuk ekziston një përkufizim i vetëm, i pranuar nga të gjithë, për termin “sistem operativ”. **Bërthama (kernel)** është pjesa qendrore që ekzekutohet me privilegje të plota kontrolli. Softuerët e tjerë që shpërndahen me SO-në mund të jenë programe ose vegla sistemore, pa qenë pjesë e bërthamës. Aplikacionet kryejnë detyrat e përdoruesit. SO-të për përdorim të përgjithshëm dhe për pajisje mobile mund të përfshijnë edhe **softuer ndërmjetës (middleware)**: korniza softuerike që u ofrojnë aplikacioneve mbështetje për baza të të dhënave, grafikë dhe multimedia.

### Këndvështrimi i përdoruesit dhe i sistemit

Nga këndvështrimi i përdoruesit, rëndësi kanë lehtësia e përdorimit, reagimi i shpejtë dhe performanca. Përdoruesi zakonisht nuk merret me mënyrën se si ndahen burimet harduerike. Nga këndvështrimi i sistemit, rëndësi kanë ndarja e burimeve dhe kontrolli: një kompjuter me shumë përdorues duhet t'i ndajë burimet ndërmjet punëve, ta mbajë procesorin të zënë dhe t'i menaxhojë programet. Edhe kompjuterët personalë dhe telefonat duhet të balancojnë kërkesat e aplikacioneve, pajisjeve dhe punëve në prapavijë.

Disa pajisje kanë shumë pak ose aspak ndërfaqe të drejtpërdrejtë me përdoruesin. Kompjuterët e integruar në automjete, pajisje shtëpiake, pajisje industriale e mjekësore dhe produkte të Internetit të Gjërave (IoT) punojnë kryesisht pa ndërhyrjen e përdoruesit. Sistemet mobile duhet të marrin parasysh edhe jetëgjatësinë e baterisë dhe kufizimet e CPU-së e të memories.

### Gjeneratat historike

| Gjenerata | Periudha e përafërt | Zhvillimi kryesor |
| --- | --- | --- |
| E para | 1945–1955 | Llambat elektronike |
| E dyta | 1955–1965 | Tranzistorët dhe sistemet me përpunim në grupe |
| E treta | 1965–1980 | Qarqet e integruara dhe multiprogramimi |
| E katërta | 1980–sot | Kompjuterët personalë |
| E pesta | 1990–sot | Kompjuterët dhe pajisjet mobile |

Këto periudha mbivendosen: secila paraqet një drejtim të rëndësishëm të zhvillimit të kompjuterëve, pa nënkuptuar se teknologjitë e mëparshme u zhdukën menjëherë.

### Llojet kryesore të sistemeve operative

- **SO-të për kompjuterë të mëdhenj qendrorë (mainframe):** përpunojnë shumë punë dhe vëllime të mëdha hyrjeje/daljeje. Shërbimet përfshijnë përpunimin në grupe, përpunimin e transaksioneve dhe ndarjen e kohës.
- **SO-të për serverë:** u shërbejnë shumë përdoruesve ose klientëve përmes rrjetit dhe mundësojnë ndarjen e burimeve harduerike e softuerike.
- **SO-të me shumë procesorë:** shfrytëzojnë disa CPU ose bërthama për ta rritur sasinë e punës së përfunduar për njësi kohe dhe, në disa projektime, besueshmërinë.
- **SO-të për kompjuterë personalë:** mbështesin aplikacione ndërvepruese, kryerjen e shumë detyrave dhe procesorë me shumë bërthama.
- **SO-të për telefona të mençur dhe pajisje dore:** mbështesin ndërfaqe me prekje ose zë dhe menaxhojnë energjinë e burimet e kufizuara.
- **SO-të për IoT dhe sisteme të integruara:** zakonisht janë të vogla, të specializuara, efikase në përdorimin e burimeve dhe të besueshme.
- **SO-të në kohë reale (RTOS):** duhet t'i respektojnë kufizimet kohore. Në **kohë reale të rreptë (hard real time)**, mosrespektimi i afatit konsiderohet dështim i sistemit; në **kohë reale të butë (soft real time)**, vonesa e rezultatit ul cilësinë e shërbimit; në **kohë reale me afat të prerë (firm real time)**, rezultati mund të mos ketë më vlerë pas kalimit të afatit.
- **SO-të për karta të mençura:** punojnë me kufizime shumë të mëdha të memories dhe fuqisë përpunuese.

### Softueri i lirë dhe kodi i hapur

**Softueri i lirë** thekson liritë e përdoruesit për ta përdorur, studiuar, ndryshuar dhe rishpërndarë softuerin sipas licencës së tij; fjala “i lirë” nuk nënkupton vetëm mungesën e çmimit. **Kodi i hapur** thekson qasjen në kodin burimor dhe kushtet e licencimit. Konceptet mbivendosen, por nuk janë krejtësisht të njëjta. GNU/Linux është një familje e njohur sistemesh operative me kod të hapur; Windows është pronësor; sistemet e Apple kombinojnë përbërës të hapur dhe pronësorë.

## 2. Organizimi i kompjuterit dhe funksionimi i SO-së

### Hardueri, memoria dhe ruajtja e të dhënave

Një kompjuter përfshin procesorë (CPU dhe shpesh GPU), memorie (RAM, ROM dhe memorie të shpejtë cache), hapësirë ruajtëse të qëndrueshme (HDD, SSD ose memorie tjetër që i ruan të dhënat pa energji), pajisje hyrëse/dalëse dhe kontrolluesit e tyre, si dhe magjistrale si PCIe, USB dhe SATA.

CPU-ja ka qasje të drejtpërdrejtë në memorien kryesore. RAM-i është i shpejtë, por **i paqëndrueshëm (volatile)**: përmbajtja humbet kur ndërpritet energjia. Ruajtja dytësore është më e ngadalshme, por **e qëndrueshme (nonvolatile)** dhe ka kapacitet shumë më të madh. **Hierarkia e ruajtjes** i vendos memoriet e vogla, të shpejta dhe të kushtueshme afër CPU-së, ndërsa pajisjet me kapacitet më të madh e më të ngadalshme në nivele më të largëta. Të dhënat që përdoren shpesh mund të kopjohen në nivelet më të shpejta.

Ideja e arkitekturës **von Neumann** në ligjëratë është se instruksionet dhe të dhënat ruhen në të njëjtën memorie kryesore dhe përpunohen nga e njëjta CPU.

### Ndërprerjet

Një **ndërprerje (interrupt)** është sinjal që i kërkon CPU-së të trajtojë një ngjarje. SO-ja drejtohet nga ndërprerjet: pajisjet dhe ngjarjet softuerike mund ta ndërpresin përkohësisht punën aktuale, t'i mundësojnë SO-së ta ruajë gjendjen, të ekzekutojë rutinën e shërbimit të ndërprerjes (ISR) dhe pastaj të vazhdojë ekzekutimin.

Rrjedha e thjeshtuar:

1. Një program po ekzekutohet.
2. Një pajisje ose softuer gjeneron ndërprerje.
3. CPU-ja ruan gjendjen aktuale të ekzekutimit.
4. SO-ja identifikon ngjarjen dhe ekzekuton rutinën përkatëse.
5. Rutina e trajton ngjarjen.
6. CPU-ja rikthen gjendjen e mëparshme dhe programi vazhdon.

Ndërprerjet i mundësojnë SO-së t'u përgjigjet operacioneve hyrëse/dalëse dhe ngjarjeve të tjera pa e pyetur vazhdimisht secilën pajisje nëse ka përfunduar punë.

### Nisja e sistemit

**Nisja (booting)** është procesi i fillimit të punës së kompjuterit dhe ngarkimit të bërthamës së SO-së në memorie. Kur kompjuteri ndizet, firmueri fillon ekzekutimin nga një pikë e njohur, inicializon sistemin dhe gjen programin ngarkues të nisjes. Ky program ngarkon dhe nis bërthamën. Bërthama inicializon harduerin dhe monton sistemin rrënjë të fajllave.

Ligjëratat paraqesin BIOS-in tradicional dhe UEFI-n modern. UEFI mbështet konfigurime më të reja dhe disqe më të mëdha. Sistemet Linux shpesh përdorin GRUB si ngarkues nisjeje. Hollësitë varen nga kompjuteri dhe instalimi.

### Sistemet me shumë procesorë dhe grupimet e kompjuterëve

Një **sistem me shumë procesorë**, ose sistem paralel, ka më shumë se një procesor. Si përfitime të mundshme, ligjërata rendit rritjen e sasisë së punës së përfunduar për njësi kohe, uljen e kostos përmes ndarjes së burimeve dhe rritjen e besueshmërisë ose tolerancës ndaj dështimeve. Në **multiprocesim asimetrik**, procesorëve u caktohen detyra të veçanta; në **multiprocesim simetrik (SMP)**, procesorët mund t'i kryejnë detyrat e përgjithshme të sistemit.

Duhet dalluar prania e disa procesorëve fizikë në disa çipa nga prania e disa bërthamave përpunuese brenda një çipi të vetëm (**multicore**). Një procesor me dy bërthama mund të ekzekutojë punë në të dyja bërthamat. Te **serverët blade**, disa pllaka procesorësh, hyrjeje/daljeje dhe rrjeti vendosen në të njëjtën shasi.

Një **grupim kompjuterësh (cluster)** është një grup kompjuterësh të lidhur në rrjet, të quajtur nyje, që bashkëpunojnë për të ofruar një shërbim. Nyjet shpesh ndajnë hapësirën ruajtëse përmes një rrjeti SAN. Në grupimin asimetrik për disponueshmëri të lartë, një nyje mund të qëndrojë në gatishmëri për të zëvendësuar tjetrën në rast dështimi. Në grupimin simetrik, disa nyje ekzekutojnë punë dhe monitorojnë njëra-tjetrën. Grupimet për llogaritje me performancë të lartë (HPC) kërkojnë aplikacione të projektuara për ekzekutim paralel.

### Multiprogramimi dhe ndarja e kohës

- **Multiprogramimi** mban disa programe në RAM, në mënyrë që CPU-ja të kalojë te një tjetër kur programi aktual pret, për shembull, një operacion hyrës/dalës. Qëllimi kryesor është shfrytëzimi sa më i lartë i CPU-së.
- **Ndarja e kohës / kryerja e shumë detyrave (time-sharing / multitasking)** u jep proceseve intervale të shkurtra në CPU, që përdoruesit dhe aplikacionet të marrin përgjigje të shpejtë dhe të mund të ndërveprojnë me sistemin.

Të dyja teknikat ndajnë CPU-në ndërmjet programeve. Multiprogramimi përqendrohet te shfrytëzimi i CPU-së, ndërsa ndarja e kohës te koha e reagimit dhe ndërveprimi.

## 3. Mënyrat e punës, funksionet dhe strukturat e të dhënave

### Mënyra e përdoruesit dhe mënyra e bërthamës

Shumica e CPU-ve ofrojnë të paktën dy mënyra ekzekutimi:

- **Mënyra e përdoruesit (user mode):** aplikacionet e zakonshme ekzekutohen me qasje të kufizuar.
- **Mënyra e bërthamës (kernel mode)**, e quajtur edhe mënyra mbikëqyrëse, sistemore ose e privilegjuar: SO-ja mund të ekzekutojë instruksione të privilegjuara dhe të menaxhojë harduerin e burimet e mbrojtura.

Një **bit i mënyrës (mode bit)** tregon mënyrën aktuale në modelin e ligjëratës: 1 për mënyrën e përdoruesit dhe 0 për mënyrën e bërthamës. Aplikacionet kalojnë në bërthamë përmes kalimeve të kontrolluara, si thirrja sistemore, përjashtimi ose kurthi (trap), apo ndërprerja. Nëse një aplikacion tenton të ekzekutojë instruksion të privilegjuar në mënyrën e përdoruesit, gjenerohet kurth dhe SO-ja e trajton shkeljen.

Gjatë nisjes, kompjuteri fillon në mënyrën e bërthamës. Pasi SO-ja bëhet gati, aplikacionet e zakonshme ekzekutohen në mënyrën e përdoruesit. Disa sisteme ofrojnë mënyra shtesë për virtualizim, për shembull një mënyrë për monitorin e makinave virtuale (VMM).

### Funksionet kryesore të SO-së

1. **Menaxhimi i proceseve:** krijimi dhe fshirja e proceseve e fijeve të ekzekutimit; skedulimi i tyre; pezullimi dhe vazhdimi; mbështetja për sinkronizim, komunikim dhe trajtim të bllokimeve të ndërsjella.
2. **Menaxhimi i memories:** ndjekja e pjesëve të përdorura dhe e proceseve që i përdorin; vendosja se çfarë mbetet në RAM ose zhvendoset; alokimi dhe lirimi i memories.
3. **Menaxhimi i sistemit të fajllave:** organizimi i fajllave dhe direktoriumeve, ruajtja dhe leximi i tyre, menaxhimi i lejeve, lidhja e fajllave me hapësirën në ruajtjen dytësore dhe mbështetja për ndarje e kopje rezervë.
4. **Menaxhimi i pajisjeve dhe i ruajtjes masive:** komunikimi përmes drejtuesve të pajisjeve, kryerja e operacioneve hyrëse/dalëse, alokimi i hapësirës, ndjekja e hapësirës së lirë, skedulimi i disqeve dhe kontrolli i qasjes.
5. **Menaxhimi i sistemit hyrës/dalës:** koordinimi i pajisjeve dhe kërkesave; përdorimi i buferëve, memories cache dhe radhitjes së punëve për pajisje (spooling), kur këto përmirësojnë punën.
6. **Menaxhimi i memories cache:** mbajtja e të dhënave të përdorura së fundmi ose shpesh në memorie më të shpejtë. Fillimisht kontrollohet cache; nëse të dhënat mungojnë, ato merren nga niveli më i ngadalshëm dhe shpesh kopjohen në cache.
7. **Mbrojtja dhe siguria:** mbrojtja kontrollon mënyrën se si proceset i përdorin burimet; siguria mbron sistemin dhe të dhënat nga qasja e paautorizuar dhe keqpërdorimi. Autentikimi vërteton identitetin; autorizimi përcakton çfarë lejohet të bëjë përdoruesi ose procesi; kontrolli i qasjes i zbaton këto rregulla.

### Virtualizimi

**Virtualizimi** paraqet burimet fizike si një ose disa burime virtuale. Një kompjuter fizik mund të ekzekutojë disa makina virtuale (VM) të izoluara, secila me SO-në dhe aplikacionet e veta. Hipervizori ose VMM-ja alokon dhe menaxhon CPU-në, memorien, hapësirën ruajtëse dhe pajisjet fizike.

### Sistemet e shpërndara, klient–server, P2P dhe shërbimet në re

Një **sistem i shpërndarë** përbëhet nga kompjuterë të pavarur, të lidhur në rrjet, që bashkëpunojnë dhe i paraqiten përdoruesit si një sistem i bashkuar. Veçoritë kryesore janë ndarja e të dhënave, shërbimeve dhe burimeve përpunuese; puna e njëkohshme e disa pjesëve; komunikimi përmes rrjetit; mundësia për të shtuar burime kur rritet kërkesa (**shkallëzueshmëria**); dhe vazhdimi i punës edhe kur disa pjesë dështojnë (**toleranca ndaj dështimeve**).

Në modelin **klient–server**, klienti nis kërkesën dhe ofron ndërfaqen ose aplikacionin e përdoruesit, ndërsa serveri përpunon kërkesën, menaxhon burimet e përbashkëta dhe dërgon përgjigjen. Disa klientë mund t'i përdorin të njëjtat burime të serverit. Komunikimi zakonisht kryhet përmes rrjetit, me protokolle si TCP/IP, HTTP ose HTTPS.

Në modelin **P2P (peer-to-peer)**, rrjeti është i decentralizuar: çdo pjesëmarrës mund të veprojë edhe si klient, edhe si server. Të dhënat, burimet dhe fuqia përpunuese shpërndahen ndërmjet nyjeve. Ligjërata përmend Skype, BitTorrent dhe blockchain si shembuj.

**Llogaritja në re (cloud computing)** është modeli i ofrimit të burimeve kompjuterike përmes internetit, për shembull serverë, hapësirë ruajtëse, baza të të dhënave, rrjet dhe softuer.

### Strukturat e të dhënave në bërthamë

- **Vargu (array):** përmbledhje elementesh të indeksuara me qasje të drejtpërdrejtë.
- **Lista e lidhur:** varg nyjesh të lidhura; te lista njëdrejtimëshe çdo nyje tregon pasardhësin, te lista dydrejtimëshe tregon paraardhësin dhe pasardhësin, ndërsa te lista rrethore nyja e fundit lidhet me të parën.
- **Steku (stack):** parimi LIFO, “i fundit që hyn, i pari që del”; shtimi bëhet me push dhe largimi me pop.
- **Radha (queue):** parimi FIFO, “i pari që hyn, i pari që del”.
- **Pema (tree):** hierarki me lidhje prind–fëmijë; një pemë binare ka jo më shumë se dy fëmijë për çdo nyje.
- **Funksioni hash / harta hash:** shndërron çelësin në një indeks ose vlerë hash, që çiftet çelës–vlerë të ruhen e të gjenden shpejt.
- **Harta e biteve (bitmap):** paraqitje kompakte me bite e gjendjes së shumë elementeve, për shembull nëse pozicionet e burimeve janë të lira apo të zëna.

## 4. Shërbimet dhe ndërfaqet e sistemit operativ

### Shërbimet për përdoruesin dhe për sistemin

Shërbimet që i ndihmojnë drejtpërdrejt përdoruesit dhe programet përfshijnë:

- **Ndërfaqen e përdoruesit:** CLI, GUI, ekran me prekje dhe, në disa raste, kontroll me zë.
- **Ekzekutimin e programeve:** ngarkimi, ekzekutimi dhe përfundimi i programit.
- **Operacionet hyrëse/dalëse:** qasja në fajlla dhe pajisje.
- **Manipulimin e sistemit të fajllave:** krijimi, fshirja, kërkimi, listimi, leximi, shkrimi dhe caktimi i lejeve për fajlla e direktoriume.
- **Komunikimin:** shkëmbimi i të dhënave brenda kompjuterit ose përmes rrjetit.
- **Zbulimin e gabimeve:** identifikimi dhe trajtimi i gabimeve në CPU, memorie, pajisje, operacione hyrëse/dalëse ose programe të përdoruesit.

Shërbimet për funksionim efikas të vetë sistemit përfshijnë alokimin e burimeve, evidentimin e përdorimit dhe regjistrimin e ngjarjeve, mbrojtjen dhe sigurinë. Evidentimi mund të ndjekë kohën e CPU-së dhe përdorimin e memories e të diskut. Mbrojtja kontrollon qasjen në burime; siguria përfshin edhe mbrojtjen nga veprimtaritë e jashtme ose keqdashëse.

### Ndërfaqet e përdoruesit

**Ndërfaqja e vijës së komandave (CLI)** pranon komanda të shkruara përmes interpretuesit të komandave ose shell-it. Shell-i lexon komandën dhe nis programin ose shërbimin përkatës. Linux, Unix dhe Windows ofrojnë interpretues komandash.

**Ndërfaqja grafike e përdoruesit (GUI)** përdor dritare, ikona, meny, butona dhe komandim përmes mausit ose prekjes. Shumë SO ofrojnë edhe GUI, edhe CLI. Ekrani me prekje mbështet veprime dhe gjeste të drejtpërdrejta; komandat me zë shtojnë një mënyrë tjetër të hyrjes.

### API-ja dhe thirrjet sistemore

**Thirrja sistemore (system call)** është ndërfaqja programuese për kërkimin e një shërbimi të bërthamës. Aplikacionet e përdorin për operacione që kontrollohen nga SO-ja, si krijimi i një procesi, leximi i një fajlli, dërgimi i të dhënave në rrjet ose qasja në pajisje. Bibliotekat e C-së dhe C++ zakonisht i paraqesin këto operacione si funksione.

**API-ja** është ndërfaqja që përdor programuesi i aplikacionit. Ajo mund të përfshijë një ose disa thirrje sistemore dhe t'i fshehë hollësitë e nivelit të ulët. Ligjërata përmend Win32 për Windows, POSIX për sisteme të ngjashme me Unix-in (përfshirë Linux dhe macOS), dhe Java API për programet në makinën virtuale Java. Programi mbështetet në API, ndërsa shtresa e thirrjeve sistemore ia përcjell kërkesën SO-së për zbatim.

Rruga e thjeshtuar e leximit të një fajlli:

**Aplikacioni → API-ja/funksioni i bibliotekës → ndërfaqja e thirrjeve sistemore → shërbimi i bërthamës → pajisja/drejtuesi → rezultati ose gabimi**

Në shumë sisteme, çdo thirrje sistemore identifikohet me një numër. Ndërfaqja e thirrjeve sistemore e drejton kërkesën te funksioni përkatës dhe kthen rezultatin ose gjendjen e përfundimit. Aplikacionet duhet ta respektojnë ndërfaqen e API-së, pa pasur nevojë ta njohin zbatimin brenda bërthamës.

| Grupi i thirrjeve sistemore | Operacionet tipike / shembuj |
| --- | --- |
| Kontrolli i proceseve | krijimi, ekzekutimi, pritja, përfundimi; fork(), exec(), exit() |
| Menaxhimi i fajllave | open(), read(), write(), close() |
| Menaxhimi i pajisjeve | kërkimi, konfigurimi dhe lirimi i pajisjeve; ioctl(), read(), write() |
| Menaxhimi i memories | hartëzimi dhe heqja e hartëzimit të memories; mmap(), munmap() |
| Komunikimi | gypat, soketat, dërgimi dhe pranimi i të dhënave |
| Mbrojtja dhe siguria | lejet dhe identiteti, p.sh. chmod(), setuid(), access() |

### Veglat sistemore, aplikacionet, lidhësi dhe ngarkuesi

**Veglat dhe shërbimet sistemore** mbështesin detyra të zakonshme: manipulimin e fajllave, raportimin e gjendjes, konfigurimin, mbështetjen për gjuhë programuese, ngarkimin e programeve, komunikimin dhe punët në prapavijë. Shërbimet që punojnë në prapavijë quhen edhe demonë (daemons). Ato veprojnë pa ndërveprim të drejtpërdrejtë me përdoruesin dhe shpesh merren me shtypje, regjistrim ngjarjesh, kontroll të diskut ose skedulim. Një vegël sistemore zakonisht është program në hapësirën e përdoruesit dhe nuk është pjesë e bërthamës.

Aplikacionet, si shfletuesit, editorët, programet për fletëllogaritje, veglat e zhvillimit, bazat e të dhënave, luajtësit e mediave dhe lojërat, ekzekutohen mbi SO-në dhe kërkojnë shërbimet e saj.

Kompajleri përkthen kodin burimor në fajlla objekt të zhvendosshëm. **Lidhësi (linker)** bashkon fajllat objekt dhe bibliotekat në një fajll të ekzekutueshëm. **Ngarkuesi (loader)** e vendos fajllin e ekzekutueshëm në memorie që ai të mund të ekzekutohet. Programi i ndërtuar për një SO mund të mos punojë në një tjetër për shkak të dallimeve në formatet binare, bashkësinë e instruksioneve të CPU-së dhe ndërfaqet e thirrjeve sistemore.

## 5. Projektimi dhe struktura e sistemit operativ

### Qëllimet e projektimit dhe ndarja politikë–mekanizëm

Qëllimet nga këndvështrimi i përdoruesit përfshijnë përshtatshmërinë, lehtësinë e mësimit, besueshmërinë, sigurinë dhe shpejtësinë. Qëllimet nga këndvështrimi i sistemit përfshijnë lehtësinë e projektimit, zbatimit e mirëmbajtjes, fleksibilitetin, besueshmërinë dhe efikasitetin. Projektimi varet nga hardueri dhe lloji i sistemit të synuar: kompjuter personal, pajisje mobile, sistem i shpërndarë ose sistem në kohë reale.

Duhet të ndahet **politika** nga **mekanizmi**:

- **Politika:** çfarë vendimi do të merret? Shembull: cili proces do ta marrë CPU-në më pas?
- **Mekanizmi:** si do të zbatohet vendimi? Shembull: si do ta kalojë skeduluesi CPU-në te procesi i zgjedhur?

Kjo ndarje mundëson ndryshimin e politikës pa e riprojektuar mekanizmin.

SO-të moderne janë sisteme softuerike të mëdha që zhvillohen për një kohë të gjatë. Zakonisht pjesa më e madhe shkruhet në gjuhë të nivelit të lartë, si C ose C++, ndërsa gjuha assembly përdoret në ndërfaqet e nivelit të ulët me harduerin.

### Strukturat kryesore

| Struktura | Ideja bazë | Përparësitë | Mangësitë / kufizimet |
| --- | --- | --- | --- |
| E thjeshtë | Strukturë minimale ose jo qartë e përcaktuar për sisteme të vogla; shembulli historik MS-DOS ka ndarje të dobët dhe qasje të gjerë në harduer. | Ndërtohet lehtë; ka pak ngarkesë shtesë; mund të jetë e shpejtë. | Izolim i dobët; një dështim mund ta prekë tërë sistemin; funksionalitet i kufizuar. |
| Monolitike | Shumica e shërbimeve ekzekutohen së bashku në një hapësirë të vetme adresimi të bërthamës. UNIX-i tradicional është shembulli i ligjëratës. | Komunikim i shpejtë ndërmjet pjesëve; rrugë e drejtpërdrejtë ekzekutimi. | Shumë kod punon me privilegje të plota; dështimi i një shërbimi të bërthamës mund ta rrëzojë sistemin; pjesët mund të varen ngushtë nga njëra-tjetra. |
| Me shtresa | SO-ja ndahet në nivele: hardueri në fund dhe shërbimet për përdoruesin në krye; çdo shtresë përdor shtresat më poshtë. | Kuptohet, izolohet, korrigjohet dhe mirëmbahet më lehtë. | Kufijtë ndërmjet shtresave kërkojnë planifikim; kalimi nëpër shtresa mund të shtojë ngarkesë. |
| Me mikrobërthamë | Në bërthamë mbeten vetëm funksionet thelbësore; shërbimet e tjera ekzekutohen në hapësirën e përdoruesit dhe komunikojnë me mesazhe. | Bërthamë më e vogël; izolim më i mirë i dështimeve dhe bartshmëri; më pak kod me privilegje të plota. | Mesazhet dhe kalimet ndërmjet mënyrave të punës shtojnë kosto; menaxhimi i shërbimeve është kompleks. |
| Modulare | Module të pavarura ofrojnë funksione, si drejtues pajisjesh ose sisteme fajllash, dhe mund të ngarkohen ose largohen. | Fleksibilitet dhe zgjerim më i lehtë; përgjegjësi më të qarta për modulet. | Modulet duhet të bashkëveprojnë saktë; komunikimi dhe menaxhimi i tyre shtojnë kompleksitet. |
| Me bërthamë hibride | Kombinon elemente të disa strukturave për të balancuar performancën, izolimin dhe fleksibilitetin. | Mund të ruajë ekzekutimin e shpejtë në bërthamë dhe njëkohësisht t'i organizojë shërbimet në module. | Projektim më kompleks; mbeten disa kosto të komunikimit ndërmjet pjesëve. |

Ligjërata e përshkruan Linux-in si monolitik, me module që ngarkohen në mënyrë dinamike. Windows është kryesisht monolitik, por përfshin edhe nënsisteme në mënyrën e përdoruesit dhe module të ngarkueshme. macOS/iOS dhe Android paraqiten si sisteme me shtresa ose hibride, të ndërtuara nga bërthama dhe korniza softuerike të niveleve më të larta. SO-të moderne shpesh kombinojnë disa qasje.

### Nisja, zbulimi i gabimeve dhe performanca

Hapat e përgjithshëm për ndërtimin dhe instalimin e një SO-je nga kodi burimor janë: sigurimi ose shkrimi i kodit, konfigurimi për sistemin e synuar, kompajlimi, instalimi dhe nisja e sistemit të ri.

Veglat për zbulimin dhe korrigjimin e gabimeve përfshijnë regjistrat e sistemit, kopjet e memories së procesit pas dështimit (core dumps) dhe kopjet e memories së bërthamës pas rrëzimit të SO-së (crash dumps). Kopja e memories së procesit regjistron gjendjen e tij pas dështimit të aplikacionit; kopja e bërthamës regjistron gjendjen e kernelit pas dështimit të SO-së. Përmirësimi i performancës fillon me gjetjen e pengesës kryesore. Për shembull, kur shfrytëzimi i CPU-së qëndron afër 100%, duhet të kontrollohet cilat procese po e shpenzojnë atë. Vegla si top ose Task Manager ndihmojnë në vëzhgimin e përdorimit të burimeve.

## 6. Proceset dhe skedulimi i CPU-së

### Programi dhe procesi

**Programi** është kod pasiv i ruajtur në disk. **Procesi** është një instancë aktive e një programi në ekzekutim. Kur një fajll i ekzekutueshëm ngarkohet dhe përgatitet për t’u ekzekutuar, krijohet procesi. Procesit i nevojiten burime si koha e CPU-së, memoria, hyrja/dalja (I/O), fajllat dhe të dhënat fillestare.

Imazhi i procesit në memorie zakonisht përfshin:

- **Pjesën e kodit (text/code):** instruksionet e ekzekutueshme.
- **Pjesën e të dhënave (data):** ndryshoret globale dhe statike.
- **Heap-in:** memorien e alokuar dinamikisht gjatë ekzekutimit.
- **Stekun (stack):** thirrjet e funksioneve, parametrat, ndryshoret lokale dhe adresat e kthimit.

Procesi me një fije ekzekutimi (thread) ka një numërues programi. Procesi me shumë fije ka numërues programi dhe gjendje ekzekutimi për secilën fije.

### Gjendjet e procesit dhe kalimet ndërmjet tyre

- **I ri (new):** procesi është duke u krijuar.
- **I gatshëm (ready):** ndodhet në memorie dhe pret kohë në CPU.
- **Në ekzekutim (running):** është duke u ekzekutuar në CPU.
- **Në pritje / i bllokuar (waiting/blocked):** pret një ngjarje, shpesh përfundimin e I/O-së ose lirimin e një burimi.
- **I përfunduar (terminated):** e ka përfunduar ekzekutimin ose është ndalur.

Kalimet kryesore janë: **i ri → i gatshëm** kur pranohet; **i gatshëm → në ekzekutim** kur i caktohet CPU-ja; **në ekzekutim → i gatshëm** kur i merret CPU-ja për t’ia dhënë një procesi tjetër; **në ekzekutim → në pritje** kur kërkon I/O ose pret një ngjarje; **në pritje → i gatshëm** kur ngjarja përfundon; **në ekzekutim → i përfunduar** kur del.

Kur memoria është e pamjaftueshme, procesi mund të pezullohet dhe të zhvendoset në memorien sekondare. Mund të pezullohet si një proces i gatshëm, ashtu edhe një proces i bllokuar që është duke pritur. Sipas modelit të ligjëratës, këtë e menaxhon skeduluesi afatmesëm, i quajtur edhe shkëmbyes (swapper).

### Blloku i kontrollit të procesit dhe tabela e proceseve

Sistemi operativ e ruan gjendjen e menaxhimit të secilit proces në një **bllok të kontrollit të procesit (Process Control Block, PCB)**. Ky quhet edhe bllok i kontrollit të detyrës. PCB-ja zakonisht përmban:

- PID-in dhe gjendjen e procesit;
- numëruesin e programit dhe regjistrat e CPU-së;
- prioritetin e skedulimit dhe lidhjet me radhët;
- informacionin për menaxhimin e memories;
- të dhëna për shfrytëzimin e burimeve, si përdorimi dhe kufizimet e CPU-së;
- gjendjen e I/O-së dhe pajisjet e caktuara procesit.

Tabela e proceseve i indekson proceset dhe përmban referenca te PCB-të e tyre.

### Radhët, skeduluesit, dispeçeri dhe ndërrimi i kontekstit

- **Radha e punëve (job queue):** punët e reja që presin në disk ose në grupin e punëve që duhet të pranohen në sistem.
- **Radha e proceseve të gatshme (ready queue):** proceset në memorie që janë të gatshme për CPU.
- **Radha e proceseve të bllokuara / e pajisjes:** proceset që presin I/O ose një burim tjetër.
- **Radha e proceseve të pezulluara:** proceset që janë larguar përkohësisht nga memoria kryesore.

Tri rolet e skeduluesve:

1. **Skeduluesi afatgjatë / i punëve:** zgjedh cilat punë të pranohen nga grupi i punëve në memorien kryesore. Aktivizohet më rrallë dhe ndikon në numrin e proceseve që ndodhen në sistem.
2. **Skeduluesi afatshkurtër / i CPU-së:** zgjedh procesin e gatshëm që do të ekzekutohet në vijim. Aktivizohet shpesh.
3. **Skeduluesi afatmesëm / shkëmbyesi:** pezullon proceset dhe më vonë i rikthen, për të menaxhuar mungesën e memories dhe prioritetet.

Pasi skeduluesi i CPU-së e zgjedh procesin, **dispeçeri (dispatcher)** e realizon kalimin: ndërron kontekstin, kalon në mënyrën e përdoruesit kur duhet dhe vazhdon te vlera e ruajtur e numëruesit të programit të procesit të zgjedhur.

**Ndërrimi i kontekstit (context switch)** ruan gjendjen e procesit aktual dhe rikthen gjendjen e një procesi tjetër. Kjo mundëson ndarjen e kohës së CPU-së ndërmjet proceseve, por krijon kosto shtesë: gjatë ndërrimit, CPU-ja nuk kryen punë të aplikacionit. Sa më shumë gjendje të duhet të ruhet, aq më e madhe mund të jetë kjo kosto.

### Krijimi i proceseve

Proceset mund të krijohen gjatë inicializimit të sistemit, përmes një thirrjeje sistemore për krijimin e procesit, si përgjigje ndaj kërkesës së përdoruesit ose kur fillon një punë në grup (batch job). Gjatë nisjes krijohen si procese që ndërveprojnë me përdoruesin, ashtu edhe procese që punojnë në prapavijë (daemons).

Procesi i ri merr PID dhe PCB. Sistemi operativ i alokon burimet, ngarkon ose mapon programin në memorie, inicializon gjendjen e ekzekutimit dhe e vendos në radhën e proceseve të gatshme.

Prindi dhe fëmija mund t’i ndajnë të gjitha burimet, një pjesë të tyre ose të kenë burime të pavarura. Ata mund të ekzekutohen në mënyrë konkurrente, ose prindi mund të presë derisa fëmija të përfundojë. Marrëdhëniet prind–fëmijë formojnë pemën e proceseve.

Në Unix/Linux:

- **fork()** krijon një proces fëmijë. Prindi dhe fëmija vazhdojnë pas thirrjes, por marrin vlera të ndryshme kthimi.
- **exec()** zëvendëson imazhin e programit të procesit thirrës me një program të ri. Nuk krijon proces tjetër. Në rast suksesi, nuk kthehet te programi i vjetër.
- **wait() / waitpid()** i mundëson prindit të presë fëmijën dhe të marrë statusin e përfundimit të tij.

Windows përdor CreateProcess() për të krijuar proces. Ligjërata thekson se Windows nuk e paraqet hierarkinë e proceseve në të njëjtën mënyrë si Unix.

### Përfundimi i proceseve, proceset zombie dhe proceset jetime

Procesi mund të përfundojë normalisht, të hasë gabim ose përjashtim fatal, të përfundohet nga një proces tjetër, ta tejkalojë kufirin kohor ose të ndalet për shkak të kushteve të burimeve. Sistemi operativ i liron burimet e tij dhe e largon nga menaxhimi aktiv.

Në disa sisteme operative, përfundimi i prindit shkakton edhe përfundimin e fëmijëve; kjo quhet **përfundim kaskadë**. Në Linux, fëmijët që vazhdojnë pas përfundimit të prindit zakonisht adoptohen si procese jetime.

**Procesi zombie** është një fëmijë që ka përfunduar, por prindi ende nuk e ka marrë statusin e tij të daljes. Mbetet një hyrje e vogël në tabelën e proceseve; programi nuk është më duke u ekzekutuar. Thirrja wait()/waitpid() e merr statusin dhe i mundëson sistemit operativ ta largojë këtë hyrje.

**Procesi jetim (orphan)** është procesi, prindi i të cilit përfundon para tij. Në Linux, një proces i tillë adoptohet nga procesi përgjegjës për mbledhjen e statuseve të fëmijëve, shpesh systemd me PID 1. Për t’i shmangur proceset zombie të panevojshme, prindi duhet t’i marrë statuset e fëmijëve. Jetëgjatësia e proceseve prind dhe fëmijë duhet të menaxhohet me qëllim që të mos krijohen procese jetime pa nevojë.

## 7. Komunikimi ndërmjet proceseve (IPC)

### Pse komunikojnë proceset?

Proceset mund të jenë **të pavarura**, kur nuk ndikojnë te njëri-tjetri, ose **bashkëpunuese**, kur ndikojnë te njëri-tjetri ose ndajnë informacion. Bashkëpunimi mundëson ndarjen e të dhënave, koordinimin e veprimeve, menaxhimin e burimeve dhe ndërtimin e programeve në module.

Dy modelet themelore të IPC-së janë **memoria e përbashkët** dhe **kalimi i mesazheve**. Mekanizma të tjerë përfshijnë gypat (pipes), semaforët, sinjalet, socket-at dhe thirrjet e procedurave në distancë.

### Memoria e përbashkët dhe modeli prodhues–konsumues

Në IPC përmes memories së përbashkët, proceset bien dakord për një zonë memorieje që mapohet në hapësirën e adresave të secilit proces. Sistemi operativ e krijon zonën, ndërsa proceset kryejnë lexime dhe shkrime të zakonshme në të. Meqë disa procese mund të qasen në të njëjtën memorie, ato duhet të koordinohen që të shmangin ndryshime të njëkohshme që bien në konflikt. Prandaj sinkronizimi është i domosdoshëm.

Në modelin **prodhues–konsumues**, prodhuesi shton elemente në një bufer, ndërsa konsumuesi i largon. Për shembull, kompajleri mund të prodhojë kod assembly që e përdor asembleri; një server uebi mund të prodhojë përmbajtje që e konsumon shfletuesi.

- **Buferi i pakufizuar:** nuk ka kufi praktik të kapacitetit. Konsumuesi mund të presë kur buferi është bosh, ndërsa prodhuesi nuk pret për hapësirë.
- **Buferi i kufizuar:** ka kapacitet të caktuar. Konsumuesi pret kur buferi është bosh, ndërsa prodhuesi pret kur buferi është plot.

Buferi i thjeshtë rrethor në ligjëratë përdor një varg me indekset **in** dhe **out**:

- **in** tregon pozitën e ardhshme të lirë.
- **out** tregon elementin e ardhshëm që duhet të konsumohet.
- Buferi është bosh kur **in == out**.
- Buferi është plot kur **(in + 1) % BUFFER_SIZE == out**.

Kjo paraqitje e lë qëllimisht një pozitë të papërdorur, që gjendja bosh të dallohet nga gjendja plot. Pra, vargu me madhësi N mund të mbajë më së shumti N−1 elemente. Unazat e pritjes aktive në sllajde e ilustrojnë logjikën, por shpenzojnë kohë të CPU-së. Implementimet praktike përdorin mekanizma sinkronizimi, si semaforë ose ndryshore kushti.

### Kalimi i mesazheve

Kalimi i mesazheve përdor operacione si **send(message)** dhe **receive(message)**. Nuk kërkon hapësirë të përbashkët adresash dhe është i dobishëm për komunikim ndërmjet kompjuterëve në rrjet. Mesazhet mund të kenë madhësi fikse ose të ndryshueshme.

Zgjedhjet kryesore në organizimin e komunikimit:

- **Emërtimi i drejtpërdrejtë:** dërguesi dhe pranuesi e identifikojnë njëri-tjetrin. Në emërtimin simetrik, të dyja palët e emërtojnë palën tjetër; në atë asimetrik, kjo nuk është e domosdoshme nga të dyja anët.
- **Emërtimi i tërthortë:** proceset dërgojnë dhe marrin mesazhe përmes një kutie postare ose porti me identifikues unik.
- **Komunikimi bllokues / sinkron:** dërgimi bllokues pret derisa të pranohet mesazhi; pranimi bllokues pret derisa të ketë mesazh.
- **Komunikimi jobllokues / asinkron:** dërgimi përfundon edhe nëse pranuesi nuk e ka marrë ende mesazhin; pranimi kthen një mesazh nëse është në dispozicion ose tregon se nuk ka mesazh.
- **Buferimi:** radha mund të ketë kapacitet zero (takim i drejtpërdrejtë, ku dërguesi pret), kapacitet të kufizuar (dërguesi pret kur mbushet) ose kapacitet të pakufizuar (sipas modelit, dërguesi nuk pret për hapësirë).

### Krahasimi i memories së përbashkët me kalimin e mesazheve

Pasi të krijohet zona, memoria e përbashkët mund të jetë më e shpejtë për bartje të mëdha ose të shpeshta, sepse shkëmbimi bëhet përmes qasjeve të zakonshme në memorie. Megjithatë, proceset duhet të sinkronizohen me kujdes. Kalimi i mesazheve është shpesh më i lehtë përmes rrjetit dhe shmang konfliktet e drejtpërdrejta në memorien e përbashkët, por thirrjet sistemore, kopjimi dhe ndërhyrja e bërthamës mund të shtojnë kosto. Ai përshtatet mirë për mesazhe më të vogla dhe sisteme të shpërndara.

### Gypat, socket-at dhe RPC-ja

Në komunikimin **half-duplex**, të dhënat mund të kalojnë në të dy drejtimet, por jo njëkohësisht. Në komunikimin **full-duplex**, ato kalojnë në të dy drejtimet në të njëjtën kohë.

- **Gypi anonim / i zakonshëm (anonymous pipe):** zakonisht lidh procese të afërta, si prindi dhe fëmija, dhe zakonisht është njëdrejtimësh. Për komunikim në të dy drejtimet përdoren dy gypa. Në Unix, pipe() kthen përshkruesit e fajllave: fd[0] për lexim dhe fd[1] për shkrim; përdoren read(), write() dhe close(). Windows ofron API për gypa anonimë, si CreatePipe(), ReadFile() dhe WriteFile().
- **Gypi me emër (named pipe) / FIFO:** identifikohet me emër dhe mund të lidhë procese pa lidhje prind–fëmijë. Në Unix, FIFO-ja është lokale dhe zakonisht përdoret për komunikim njëdrejtimësh; krijohet me mkfifo() dhe përdoret përmes open(), read(), write() dhe close(). Gypat me emër në Windows mund të mbështesin komunikim në të dy drejtimet dhe përmes rrjetit, me API si CreateNamedPipe() dhe ConnectNamedPipe(). Këto veçori varen nga sistemi operativ.
- **Socket-i:** pikë fundore e komunikimit. Socket-i i rrjetit zakonisht identifikohet nga adresa IP dhe numri i portit; proceset që komunikojnë përdorin nga një pikë fundore në secilën anë.
- **Thirrja e procedurës në distancë (Remote Procedure Call, RPC):** i mundëson programit të thërrasë një procedurë në një kompjuter tjetër përmes një ndërfaqeje që i ngjan thirrjes së zakonshme të funksionit. RPC-ja fsheh pjesën më të madhe të shkëmbimit në rrjet pas një abstraksioni kërkesë–përgjigje.

## 8. Ushtrimet praktike: Ubuntu, fajllat, C dhe VirtualBox

### Ubuntu në VirtualBox

Rrjedha e punës në material është: instalimi i VirtualBox-it, sigurimi i një ISO-je të Ubuntu-së që i përshtatet kompjuterit, krijimi i makinës virtuale (VM) dhe instalimi i Ubuntu-së nga ISO-ja. Makina virtuale ofron një mjedis të përshtatshëm për mësimin e sistemeve operative dhe punën me bërthamën.

### Kompajlimi i bërthamës Linux (ushtrimi nga materiali më i vjetër)

Ushtrimi hyrës përdor Linux 4.14.299 si shembull. Hapat e përgjithshëm janë: instalimi i paketave të nevojshme për ndërtim, shkarkimi dhe nxjerrja e kodit burimor në **/usr/src**, konfigurimi me **make menuconfig** (në ushtrim përzgjidhet sistemi i fajllave ext4), kompajlimi, instalimi i moduleve dhe i bërthamës, pastaj rinisja. Paketa të përmendura në material janë **gcc**, **make**, **libncurses5-dev**, **gawk**, **zlib1g**, **g++**, **flex** dhe **libssl-dev**. Para instalimit të paketave, materiali përditëson edhe listën e tyre.

Shembulli historik i komandave nga PDF-ja:

~~~sh
wget https://www.kernel.org/pub/linux/kernel/v4.x/linux-4.14.299.tar.xz
sudo tar -xvf linux-4.14.299.tar.xz -C /usr/src/
cd /usr/src/linux-4.14.299
sudo make menuconfig
sudo make
sudo make modules_install
sudo make install
reboot
~~~

Ky version i bërthamës dhe emrat e paketave të tij janë të vjetër dhe mund të mos funksionojnë drejtpërdrejt në një version të ri të Ubuntu-së. PDF-ja përmend **ARCH=i386** për një konfigurim të caktuar 32-bitësh/64-bitësh. Përcaktimi i arkitekturës duhet t’i përshtatet sistemit të synuar dhe mjeteve të kompajlimit, prandaj ky opsion duhet kontrolluar sipas udhëzimeve të bërthamës përkatëse.

### Ndarja e një folderi ndërmjet Windows-it dhe Ubuntu-së

Për ta ndarë një folder të Windows-it me Ubuntu-në brenda makinës virtuale:

1. Instalo ose aktivizo VirtualBox Guest Additions në sistemin mysafir.
2. Në Windows, krijo një folder, për shembull **D:\sharedubuntu**.
3. Në VirtualBox, shtoje te **Devices → Shared Folders**, cakto shtegun e Windows-it dhe emrin e ndarjes. Zgjidh **Make Permanent** nëse konfigurimi duhet të ruhet.
4. Në Ubuntu, krijo një pikë montimi, për shembull **~/Desktop/windowshare**, pastaj montoje folderin e ndarë.

Shembull komandash:

~~~sh
mkdir -p ~/Desktop/windowshare
sudo mount -t vboxsf sharedubuntu ~/Desktop/windowshare
mount | grep vboxsf
~~~

Montimi manual është i përkohshëm dhe humbet pas rinisjes së sistemit mysafir, përveç nëse është konfiguruar montimi automatik. Ushtrimi i përditësuar përmend opsionin **Auto-mount** të VirtualBox-it dhe shtimin e përdoruesit në grupin **vboxsf**. Nëse shfaqet gabimi **unknown filesystem type 'vboxsf'**, mjetet Guest Additions mungojnë ose nuk janë aktive. Materiali sugjeron instalimin e **virtualbox-guest-utils** dhe **virtualbox-guest-x11**, pastaj rinisjen; disponueshmëria e paketave varet nga versioni i Ubuntu-së.

Anëtarësimi në grupin **vboxsf** rregullon lejet e qasjes në folderin e ndarë; ai nuk e bën vetvetiu montimin të përhershëm.

Ushtrimi i transferimit kontrollon të dy drejtimet: lexo një fajll të krijuar në Windows përmes **~/Desktop/windowshare/**, pastaj krijo një fajll në Ubuntu dhe kopjoje në folderin e ndarë që të shfaqet edhe në Windows. Për shembull:

~~~sh
cat ~/Desktop/windowshare/detyra.txt
echo "Pershendetje nga Ubuntu" > pergjigje.txt
cp pergjigje.txt ~/Desktop/windowshare/
~~~

Pas rinisjes së Ubuntu-së, folderi i montuar manualisht nuk është më i lidhur. Nevojitet Auto-mount i VirtualBox-it ose një konfigurim i qëndrueshëm montimi. Për çmontim manual, materiali përdor **sudo umount ~/Desktop/windowshare**. Folderi që shërben si pikë montimi hiqet vetëm kur është bosh. Nëse është aktivizuar **Make Permanent**, ndarja mbetet e konfiguruar në VirtualBox edhe pas çmontimit.

Për fajllat e tu përdor editorin pa privilegje root, për shembull shmang **sudo gedit**: fajllat e krijuar kështu mund të bëhen pronë e root-it. Përdor sudo vetëm për veprimin administrativ që i kërkon këto privilegje.

### Komandat themelore të terminalit dhe lejet

| Komanda | Çfarë bën |
| --- | --- |
| <code>pwd</code> | Shfaq shtegun e folderit aktual. |
| <code>ls -l</code> | Liston fajllat me lejet, pronarin, grupin, madhësinë dhe kohën e ndryshimit. |
| <code>cd folder/</code> | Kalon në folderin e dhënë. |
| <code>cat file</code> | Shfaq përmbajtjen e fajllit. |
| <code>echo "text" &gt; file</code> | Shkruan tekst në fajll, duke zëvendësuar përmbajtjen ekzistuese. |
| <code>cp source destination</code> | Kopjon një fajll. |
| <code>chmod 600 file</code> | Pronari mund të lexojë dhe shkruajë; grupi dhe të tjerët nuk kanë leje. |
| <code>chmod 644 file</code> | Pronari mund të lexojë dhe shkruajë; grupi dhe të tjerët mund të lexojnë. |
| <code>chmod 755 file</code> | Pronari mund të lexojë, shkruajë dhe ekzekutojë; grupi dhe të tjerët mund të lexojnë dhe ekzekutojnë. |
| <code>whoami</code> | Shfaq llogarinë e përdoruesit aktual. |
| <code>sudo command</code> | Ekzekuton një komandë me privilegje të ngritura, nëse përdoruesi është i autorizuar. |
| <code>gcc source.c -o program</code> | Kompajlon kodin C dhe cakton emrin e fajllit të ekzekutueshëm. |
| <code>./program</code> | Ekzekuton programin që ndodhet në folderin aktual. |

Te **ls -l**, një shënim si **-rwxr-xr--** fillon me karakterin që tregon llojin e fajllit, pastaj vijojnë lejet për pronarin, grupin dhe të tjerët. Çdo treshe përdor **r** për lexim, **w** për shkrim dhe **x** për ekzekutim. Forma numerike e chmod-it përdor vlera oktale: lexim=4, shkrim=2 dhe ekzekutim=1; vlerat mblidhen për secilën kategori. Prandaj 6 nënkupton lexim+shkrim, 4 vetëm lexim dhe 5 lexim+ekzekutim. Shkronja **d** në fillim, në vend të **-**, tregon një folder.

**whoami** shfaq përdoruesin e zakonshëm; **sudo whoami** zakonisht shfaq **root**. Krijimi i fajllave me sudo mund t’i bëjë pronë të root-it dhe t’ia pamundësojë përdoruesit të zakonshëm ndryshimin e tyre. Ubuntu zakonisht e mundëson qasjen administrative përmes sudo-s, pa kërkuar hyrje të drejtpërdrejtë në root për punët e zakonshme. Mund të caktohet fjalëkalim për root-in, por zakonisht nuk nevojitet për ushtrimet e zakonshme.

Shell-i zakonisht kërkon programe vetëm në folderët e listuar në **PATH**, pa e përfshirë automatikisht folderin aktual. Parashtesa **./** e përcakton shprehimisht fajllin në folderin aktual.

### Kompajlimi në C dhe unaza me dyfishim

Programi i ushtrimit është:

~~~c
#include <stdio.h>

int main(void)
{
    int i, data = 0;
    for (i = 1; i <= 64; i += i) {
        data = i * 2;
        printf("data=%d\n", data);
    }
    return 0;
}
~~~

**i += i** e dyfishon i-në: ajo merr vlerat 1, 2, 4, 8, 16, 32 dhe 64, prandaj unaza ekzekutohet shtatë herë. Vlerat e data-s që shtypen janë 2, 4, 8, 16, 32, 64 dhe 128. Nëse përditësimi ndryshohet në **i++**, vizitohet çdo numër i plotë nga 1 deri në 64 dhe unaza ekzekutohet 64 herë. Për t’i shtypur vetëm numrat çift, mund të fillosh nga 2 dhe të shtosh 2 në çdo hap, ose të kontrollosh kushtin **i % 2 == 0**.

Komanda **gcc hello.c -o test** aktivizon mjetet e kompajlimit dhe krijon fajllin e ekzekutueshëm me emrin **test**. Kodi burimor mbetet në hello.c. Programi ekzekutohet me **./test**.

### Faktorieli dhe tejkalimi i kapacitetit të numrave të plotë

Programi për faktorielin lexon n dhe llogarit prodhimin 1×2×…×n. Ushtrimi kërkon krahasimin e rasteve n=5, 20 dhe 25. Tipat numerikë me madhësi fikse e tejkalojnë kapacitetin e tyre për vlera më të mëdha të n-së. Në sistemet e zakonshme 64-bitëshe me GCC, edhe **unsigned long long** është i pamjaftueshëm për 21! e tutje, ndërsa 20! mund të përfaqësohet. Pra, 25! nuk mund të ruhet në këtë tip. Për vlera më të mëdha nevojitet bibliotekë për numra të mëdhenj ose shumëzim i implementuar shifër pas shifre. Duhet kontrolluar edhe hyrja negative.

### Kopjimi i fajllit me thirrje sistemore

Ushtrimi i kopjimit tregon se si një vegël si **cp** i përdor shërbimet e sistemit operativ. Programi C hap fajllin burimor vetëm për lexim, krijon fajllin e destinacionit, lexon vazhdimisht blloqe në një bufer, shkruan bajtat e lexuar, kontrollon gabimet dhe në fund mbyll të dy përshkruesit e fajllave.

**open()** dhe **creat()** kthejnë përshkruesin e fajllit (FD), ose −1 në rast gabimi. **read()** kthen numrin e bajtave të lexuar, 0 kur arrihet fundi i fajllit (EOF), ose −1 për gabim. **write()** kthen numrin e bajtave të shkruar, i cili mund të jetë më i vogël se numri i kërkuar; prandaj shkrimi mund të duhet të përsëritet.

Skema kryesore:

~~~c
int src = open(argv[1], O_RDONLY);
int dest = creat(argv[2], 0644);
char buf[1024];
ssize_t n;

while ((n = read(src, buf, sizeof buf)) > 0) {
    /* Në përdorim praktik duhet përsëritur derisa të shkruhen të gjithë n bajtat. */
    if (write(dest, buf, (size_t)n) != n) {
        /* trajto gabimin në shkrim */
    }
}
/* trajto n < 0, pastaj thirr close(src) dhe close(dest) */
~~~

Shembulli i plotë në material kontrollon nëse janë dhënë saktësisht dy argumente të komandës, i raporton gabimet me perror(), përdor bufer prej 1024 bajtash dhe i mbyll përshkruesit edhe kur has gabim. Një program i qëndrueshëm për përdorim praktik duhet t’i trajtojë edhe shkrimet e pjesshme dhe gabimet gjatë mbylljes.

~~~sh
gcc copy.c -o copy
./copy original.txt copy.txt
cat copy.txt
cmp original.txt copy.txt
~~~

**cmp** nuk shfaq asgjë kur fajllat janë të njëjtë. Kur fajlli burimor mungon, pritet një gabim si **No such file or directory**, që do të thotë se fajlli ose folderi i kërkuar nuk ekziston.

### Ushtrimi për krijimin e proceseve: fork(), exec(), wait()

Ushtrimi i përditësuar për Ubuntu thekson përfshirjen e saktë të hederëve dhe aktivizimin e paralajmërimeve të kompajlerit. Në GCC 15, thirrja e një funksioni pa deklarim është gabim, prandaj duhet të përfshihen deklarimet për të gjitha funksionet e përdorura:

~~~c
#include <sys/types.h>
#include <sys/wait.h>
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>
~~~

Sjellja kryesore e **fork()**:

| Vlera e kthyer  | Kuptimi                                              |
| --------------- | ---------------------------------------------------- |
| më e vogël se 0 | Krijimi dështoi.                                     |
| 0               | Jemi në procesin fëmijë.                             |
| më e madhe se 0 | Jemi në procesin prind; vlera është PID-i i fëmijës. |

Të dy proceset vazhdojnë pas fork(). Fëmija mund të thërrasë **execlp("ls", "ls", (char *)NULL)** për ta zëvendësuar imazhin e programit të vet me **ls**, duke e kërkuar përmes PATH-it. Nëse exec ka sukses, kodi i vjetër i fëmijës nuk vazhdon më; kodi pas thirrjes shërben për trajtimin e dështimit. Prindi mund të thërrasë **wait(NULL)** për të pritur përfundimin e fëmijës.

Kompajlimi me paralajmërime të aktivizuara, siç rekomandon materiali i përditësuar:

~~~sh
gcc -Wall -Wextra procesi.c -o procesi
./procesi
~~~

Kur shtyp tekst para exec-it, përfshi një rresht të ri dhe zbraz buferin stdout nëse duhet. Përndryshe, teksti mund të mbetet në bufer dhe të humbet kur exec e zëvendëson imazhin e procesit. **getpid()** kthen PID-in e procesit aktual; **getppid()** kthen PID-in e prindit. **ps -f** shfaq listën e detajuar të proceseve, përfshirë PID dhe PPID; **ps -ef --forest** i shfaq proceset si pemë. Në ushtrim përmenden gjendje si në ekzekutim, në gjumë, i ndalur, zombie dhe joaktiv.

Materiali përdor edhe **ps -el** për një listim më të hollësishëm të proceseve në tërë sistemin. Kolonat e dobishme janë **F** (flamujt e procesit), **S** (gjendja: p.sh. R në ekzekutim, S në gjumë, T i ndalur, Z zombie), **PRI/NI** (prioriteti dhe vlera nice), **SZ** (madhësia në memorie, e shprehur në faqe) dhe **WCHAN** (vendi në bërthamë ku procesi pret). Dalja mund të kufizohet ose filtrohet me **head** dhe **grep**.

Nëse programi thërret fork() dy herë radhazi, pa kushte, në thirrjen e dytë secili proces ekzistues krijon një fëmijë: gjithsej bëhen 2² = 4 procese, një fillestar dhe tre fëmijë të rinj. Në përgjithësi, n thirrje të njëpasnjëshme dhe pa kushte të fork() japin 2ⁿ procese gjithsej, ose 2ⁿ−1 procese të reja, duke supozuar se të gjitha thirrjet kanë sukses. Çdo proces që arrin te printf shtyp një herë, ndërsa renditja e rreshtave varet nga skeduluesi dhe mund të ndryshojë. Prindërit duhet t’i marrin statuset e fëmijëve me **wait()** ose **waitpid()**.

### Shtimi i një thirrjeje sistemore: koncepti dhe varësia nga versioni

Ushtrimet për thirrjet sistemore ilustrojnë rrugën nga aplikacioni te bërthama. Njëri shembull shton një rutinë në bërthamë që mbledh dy numra të plotë, ndërsa tjetri shkruan **Hello world** në regjistrin e bërthamës. Udhëzimi historik për Linux 4.8 ndryshon një folder të kodit burimor dhe Makefile-in, shton një hyrje në tabelën e thirrjeve sistemore sipas arkitekturës, deklaron rutinën në një heder të bërthamës, e rindërton dhe instalon bërthamën, rinis sistemin dhe e thërret numrin nga një program C përmes **syscall()**.

Në material, tabelat historike janë **syscall_32.tbl** për sistemin 32-bitësh dhe **syscall_64.tbl** për atë 64-bitësh. Funksioni **printk()** shkruan mesazhin në regjistrin e bërthamës, i cili mund të shikohet me komandën **dmesg**.

Qëllimet e ushtrimit janë:

1. Implementimi brenda bërthamës duhet të përfshihet në procesin e ndërtimit të saj.
2. Sistemi operativ duhet ta drejtojë numrin e kërkuar të thirrjes sistemore te implementimi përkatës.
3. Programi në hapësirën e përdoruesit e përdor ndërfaqen e thirrjeve sistemore për të kaluar argumente dhe për të marrë rezultatin.
4. Numri i thirrjes sistemore dhe ndërfaqja binare (ABI) varen nga arkitektura dhe versioni i bërthamës.

**Numrat 354 ose 380, shtegu linux-4.8 dhe komandat e ndërtimit në material janë shembuj të lidhur me versione të caktuara.** Ato nuk zbatohen automatikisht në një bërthamë të sotme. Ndërtimi dhe instalimi i bërthamës e ndryshon sistemin operativ me të cilin niset makina; ushtrimi duhet bërë në një VM të dedikuar për eksperimente, sipas udhëzimeve për versionin konkret. Edhe ushtrimi hyrës i kompajlimit përdor shembullin më të vjetër Linux 4.14. Komanda **uname -r** shfaq versionin e bërthamës në ekzekutim, ndërsa **uname -a** shfaq të dhëna më të gjera për sistemin.

## 9. Përsëritje e shpejtë dhe dallime që duhen ditur

- **Programi dhe procesi:** programi është një fajll i ekzekutueshëm në disk; procesi është një instancë aktive e tij, me gjendje dhe burime gjatë ekzekutimit.
- **Bërthama dhe sistemi operativ:** bërthama është pjesa me privilegje që menaxhon burimet; sistemi operativ përfshin edhe programe e shërbime të tjera sistemore.
- **Mënyra e përdoruesit dhe mënyra e bërthamës:** aplikacionet kanë qasje të kufizuar; bërthama mund të ekzekutojë instruksione të privilegjuara.
- **API-ja dhe thirrja sistemore:** API-ja është ndërfaqja që përdor programuesi; thirrja sistemore kërkon një shërbim nga bërthama.
- **Politika dhe mekanizmi:** politika vendos çfarë do të bëhet; mekanizmi përcakton si do të realizohet.
- **Multiprogramimi dhe ndarja kohore:** multiprogramimi synon shfrytëzimin sa më të madh të CPU-së; ndarja kohore synon përgjigje të shpejtë dhe përdorim ndërveprues.
- **Gjendja gati dhe gjendja në pritje:** procesi gati pret vetëm CPU-në; procesi në pritje pret një ngjarje ose burim përpara se të mund të vazhdojë.
- **Tre skeduluesit:** afatgjati pranon punë në memorie, afatshkurtri zgjedh procesin e radhës për CPU, ndërsa afatmesmi pezullon dhe rikthen procese.
- **Ndërrimi i kontekstit:** ruan gjendjen e një procesi dhe rikthen gjendjen e një tjetri; kjo kohë është shpenzim shtesë i sistemit.
- **fork(), exec() dhe wait():** fork() krijon proces fëmijë; exec() zëvendëson programin brenda procesit thirrës; wait() pret dhe mbledh statusin e përfundimit të fëmijës.
- **Procesi zombie dhe procesi jetim:** zombie ka përfunduar, por prindi nuk ia ka mbledhur statusin; procesit jetim i ka përfunduar prindi.
- **Memoria e përbashkët dhe kalimi i mesazheve:** memoria e përbashkët lejon lexim/shkrim të drejtpërdrejtë, por kërkon sinkronizim; kalimi i mesazheve shkëmben të dhëna me dërgim dhe pranim.
- **Buferi rrethor:** me një pozitë të lënë bosh, buferi është bosh kur **in == out**, është plot kur **(in + 1) % N == out** dhe ruan deri në **N−1** elemente.
- **Gypi dhe socket-i:** gypi lidh rrjedhën e të dhënave ndërmjet proceseve; socket-i është pikë fundore komunikimi që mund të përdoret edhe për komunikim në rrjet.
- **Koha reale e rreptë dhe e butë:** te sistemi i rreptë, humbja e afatit përbën dështim; te sistemi i butë, humbja e afatit ul cilësinë e shërbimit.
- **Lejet 600, 644 dhe 755:** 600 i jep pronarit lexim/shkrim; 644 u jep të tjerëve edhe lexim; 755 i jep pronarit lexim/shkrim/ekzekutim dhe të tjerëve lexim/ekzekutim.
- **Pse përdoret ./programi?** Sepse folderi aktual zakonisht nuk përfshihet në PATH; **./** e përcakton shprehimisht vendndodhjen e programit.
- **Pse folderi i përbashkët nuk duket pas rinisjes?** Montimi manual humbet pas rinisjes; duhet montim automatik ose konfigurim i përhershëm.
- **Pse sudo touch fajlli mund të sjellë problem?** Fajlli mund të krijohet me pronar root, prandaj përdoruesi i zakonshëm mund të mos ketë të drejtë ta ndryshojë.
- **Pse dy thirrje të njëpasnjëshme fork() japin katër procese?** Thirrjen e dytë e ekzekutojnë të dy proceset që ekzistojnë pas thirrjes së parë. Formula **2ⁿ** vlen kur të gjitha thirrjet kanë sukses dhe çdo proces i ekzekuton të gjitha thirrjet.
