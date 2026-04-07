---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/chat-gpt/"}
---

**UDHËZUES I PLOTË PËR MËSIM**

_Arkitektura e Kompjuterëve - bazuar në PDF-in e ngarkuar_

|   |   |
|---|---|
|Çfarë përfshin|Shpjegim i organizuar i të gjitha temave kryesore të slajdeve, formulat e performancës, konceptet kryesore, dallimet që bien në provim dhe një plan të qartë se çfarë duhet mësuar përmendësh.|

# Si ta përdorësh këtë dokument

**•** Fillimisht lexo vetëm titujt dhe nënkapitujt që ta krijosh hartën e lëndës në mendje.

**•** Pastaj mëso definicionet bazë: arkitekturë, organizim, strukturë, funksion, CPU, ALU, njësi e kontrollit, bus, cache, pipeline, CPI, MIPS, speedup.

**•** Në fund mëso formulat dhe shembujt numerikë, sepse aty zakonisht dalin pyetje provimi.

# 1. Pamja e përgjithshme e PDF-it

## Çfarë mbulon ky material

PDF-i i ngarkuar i mbulon kryesisht këto blloqe: konceptet themelore të kompjuterit si sistem hierarkik; dallimin mes arkitekturës, organizimit, strukturës dhe funksionit; modelin funksional të kompjuterit; strukturën e kompjuterit dhe CPU-së; evoluimin historik të kompjuterëve; makinën e von Neumann-it dhe kompjuterin IAS; gjeneratat e kompjuterëve; ligjin e Moore-it; mikroprocesorët Intel, PowerPC dhe ARM; arkitekturën Harvard; cloud computing; problemet e performancës; pipeline; multi-core; metrikat si koha e CPU-së, CPI dhe MIPS; si dhe ligjin e Amdahl-it.

## Si është e organizuar logjikisht

Edhe pse numrat e disa slajdeve duken pak të çrregulluar, përmbajtja ndahet natyrshëm në tri pjesë të mëdha. Pjesa e parë shpjegon bazat teorike dhe strukturën e kompjuterit. Pjesa e dytë jep historinë dhe evolucionin teknologjik. Pjesa e tretë merret me performancën: si matet, prej çfarë varet dhe pse nuk mund të rritet pafund.

# 2. Konceptet themelore

## Arkitektura

Arkitektura e kompjuterit përfshin ato veçori që i sheh programuesi dhe që ndikojnë drejtpërdrejt në ekzekutimin e programit. Këtu hyjnë: seti i instruksioneve, mënyra si paraqiten numrat dhe karakteret me bita, mënyrat e adresimit, si dhe mekanizmat e komunikimit me hyrje/dalje. Pra, arkitektura tregon çfarë ofron sistemi.

## Organizimi

Organizimi i kompjuterit tregon si realizohen në harduer ato që arkitektura i premton. Këtu hyjnë sinjalet e kontrollit, teknologjia e memories, rruga e të dhënave, ndërmjetësit me periferitë dhe mënyra konkrete e implementimit. Pra, organizimi tregon si realizohet sistemi.

## Struktura

Struktura e kompjuterit është mënyra si lidhen komponentët me njëri-tjetrin. Me fjalë të thjeshta: kush lidhet me kë dhe përmes çfarë ndërlidhjeje.

## Funksioni

Funksioni i kompjuterit ka të bëjë me operacionet që kryen secili komponent. Sipas slajdeve, kompjuteri ka katër funksione bazë: përpunon të dhëna, ruan të dhëna, bart të dhëna dhe kontrollon këto procese.

## Dallimi më i rëndësishëm që duhet mbajtur mend

Pyetja klasike është kjo: a është ekzistenca e instruksionit të shumëzimit pjesë e arkitekturës apo organizimit? Përgjigjja: nëse procesori ofron instruksion shumëzimi, kjo është arkitekturë. Nëse shumëzimi realizohet me njësi të dedikuar harduerike apo me shumë mbledhje të njëpasnjëshme, kjo është organizim.

# 3. Modeli funksional i kompjuterit

## Bartja e të dhënave

Kompjuteri duhet të mund të lëvizë të dhëna ndërmjet vetes dhe rrethinës së jashtme. Kur kjo ndodh me pajisje të lidhura drejtpërdrejt, quhet input/output. Kur ndodh në distanca më të mëdha, quhet komunikim i të dhënave.

## Ruajtja e të dhënave

Kompjuteri ruan të dhënat në memorie. Proceset kryesore këtu janë leximi dhe shkrimi. Ruajtja nuk është vetëm arkivim; ajo është themeli që lejon ekzekutimin e programeve dhe mbajtjen e rezultateve të përkohshme.

## Përpunimi i të dhënave

Përpunimi nënkupton ndryshimin ose transformimin e të dhënave përmes operacioneve aritmetike dhe logjike. Kjo kryhet kryesisht nga ALU-ja.

## Kontrolli

Pa kontroll, tre funksionet e tjera nuk mund të koordinohen. Njësia e kontrollit menaxhon rrjedhën e instruksioneve dhe përdorimin e burimeve të sistemit.

# 4. Struktura e kompjuterit

## Katër komponentët kryesorë

Sipas slajdeve, struktura bazë e kompjuterit përbëhet nga: CPU, memoria kryesore, hyrja/dalja dhe ndërlidhjet e sistemit. Ndërlidhjet e sistemit zakonisht realizohen përmes system bus.

## CPU

CPU kontrollon operacionet e kompjuterit dhe kryen përpunimin e të dhënave. Ai është zemra logjike e sistemit.

## Memoria kryesore

Memoria kryesore ruan të dhënat dhe instruksionet që duhen për ekzekutim. Ajo është shumë më afër CPU-së se ruajtja afatgjatë.

## Hyrja/Dalja

I/O bart të dhënat ndërmjet pjesës së brendshme të kompjuterit dhe rrethinës së jashtme.

## System bus

Busi i sistemit është rruga kryesore për komunikim mes CPU-së, memories dhe I/O-së. Kur ta shohësh fjalën 'bas' në slajde, zakonisht nënkupton bus.

# 5. Përbërja e CPU-së

## ALU

Njësia Aritmetike dhe Logjike kryen llogaritje si mbledhja, zbritja, krahasimi dhe operacionet logjike. Kur një pyetje kërkon 'kush e përpunon të dhënën?', përgjigjja zakonisht është ALU-ja, e komanduar nga njësia e kontrollit.

## Njësia e kontrollit

Njësia e kontrollit interpreton instruksionet, gjeneron sinjale kontrolli dhe koordinon komponentët e brendshëm të CPU-së. Ajo nuk bën llogaritjen vetë; ajo e drejton sistemin.

## Regjistrat

Regjistrat janë memoriet më të vogla dhe më të shpejta në CPU. Ato mbajnë përkohësisht adresa, operandë, rezultate dhe pjesë të instruksioneve.

## Ndërlidhjet e brendshme

Këto janë rrugët me të cilat ALU, regjistrat dhe njësia e kontrollit shkëmbejnë të dhëna brenda CPU-së.

# 6. Evolucioni historik i kompjuterëve

## Gjenerata e parë - gypat me vakum

Shembulli kryesor është ENIAC. Duhet mbajtur mend se ishte shumë i madh, harxhonte shumë energji, ishte decimal dhe programohej me dorë përmes ndërprerësve. Kjo gjeneratë ishte e fuqishme për kohën, por shumë joefikase.

## Makina e von Neumann-it

Kontributi kryesor i John von Neumann-it është ideja që programi dhe të dhënat të ruhen në të njëjtën memorie. Kjo quhet stored-program concept dhe është baza e shumicës së kompjuterëve modernë.

## Gjenerata e dytë - transistorët

Zëvendësimi i gypave me transistorë e bëri kompjuterin më të vogël, më të besueshëm dhe më efikas.

## Gjenerata e tretë - qarqet e integruara

Komponentë të shumtë filluan të vendosen në të njëjtin çip. Kjo rriti performancën dhe uli madhësinë e sistemeve.

## Gjenerata e katërt dhe e pestë - mikroprocesorët

Këtu fillon epoka e kompjuterëve personalë dhe mikroprocesorëve modernë. Rritja e densitetit të transistorëve e bëri të mundur futjen e shumë funksioneve në një çip të vetëm.

# 7. IAS dhe regjistrat kryesorë

## Memoria e IAS

Kompjuteri IAS kishte 1000 lokacione memoruese me nga 40 bita secila. Një fjalë 40-bitëshe mund të mbante të dhëna ose dy instruksione nga 20 bita.

## IR - Instruction Register

IR e mban kodin operues të instruksionit që po ekzekutohet. Pra, ai tregon çfarë veprimi duhet bërë tani.

## MAR - Memory Address Register

MAR e mban adresën e lokacionit të memories që duhet lexuar ose shkruar.

## MBR - Memory Buffer Register

MBR e mban fjalën që po dërgohet në memorie ose po merret prej memories/I-O-së.

## IBR - Instruction Buffer Register

IBR e ruan përkohësisht pjesën e djathtë të instruksionit, kur një fjalë e memories përmban dy instruksione.

## PC - Program Counter

PC e mban adresën e instruksionit të ardhshëm. Mbaje mend si treguesi i vendit ku do të vazhdojë programi.

## AC dhe MQ

Accumulator dhe Multiplier-Quotient përdoren për operandë dhe rezultate. Në shumëzim, rezultati 80-bitësh ndahet: pjesa e sipërme në AC dhe pjesa e poshtme në MQ.

# 8. Ligji i Moore-it dhe miniaturizimi

## Ligji i Moore-it

Idetë kryesore në slajde janë se numri i transistorëve në çip është rritur me ritëm të shpejtë dhe fuqia procesuese është dyfishuar afërsisht çdo dy vjet për çmim të ngjashëm. Kjo ka sjellë rritje të performancës, ulje të madhësisë dhe ulje relative të kostos për fuqi llogaritëse.

## Pse ka rëndësi

Nga ky zhvillim vijnë disa pasoja: rrugët elektrike bëhen më të shkurtra, konsumet mund të optimizohen, kompjuterët bëhen më të vegjël dhe më të shpejtë. Por në një moment rritja me një bërthamë fillon të ngadalësohet për shkak të kufijve termikë dhe energjetikë.

# 9. Mikroprocesorët modernë

## Intel

Slajdet japin evolucionin nga 4004 e deri te Pentium, Pentium Pro dhe familjet më moderne. Ideja kryesore nuk është të mësosh çdo vit, por të kuptosh drejtimin: më shumë bita, më shumë tranzistorë, superscalar execution, branch prediction dhe ekzekutim spekulativ.

## PowerPC

PowerPC përmendet si alternativë ndaj Intel-it. Edhe sot përdoret në disa fusha të veçanta si embedded dhe disa sisteme serverike.

## ARM

ARM është shumë e rëndësishme për embedded systems dhe pajisje mobile. Duhet ta lidhësh me efikasitet energjetik, dizajn RISC dhe përdorim të gjerë në telefona, tableta dhe sisteme të integruara.

## Sistemet e mbjella

Kompjuterët e mbjellë gjenden kudo: mikrovalë, makina larëse, printerë, pajisje rrjeti, vetura. Ideja kryesore: kompjuteri nuk është vetëm laptopi apo desktopi, por edhe kontrolluesi special për një funksion specifik.

# 10. Arkitektura Harvard dhe cloud

## Harvard architecture

Në arkitekturën Harvard, memoria e instruksioneve dhe memoria e të dhënave janë fizikisht të ndara. Kjo lejon qasje paralele dhe shmang disa kufizime të modelit von Neumann.

## Dallimi nga von Neumann

Te von Neumann, instruksionet dhe të dhënat ndajnë të njëjtën memorie dhe shpesh të njëjtin kanal. Te Harvard, ato ndahen. Në provim, pyetja tipike është: 'a përdoret e njëjta adresë fizike për instruksione dhe të dhëna?' Kjo është e vërtetë për von Neumann, jo për Harvard.

## Cloud computing

Slajdet japin një hyrje te cloud networking dhe cloud services. Ideja qendrore është dhënia me qira e resurseve kompjuterike. PaaS përmendet si platformë mbi të cilën klienti mund të zhvillojë ose ekzekutojë aplikacione.

# 11. Problemet e performancës

## Pse performanca nuk varet vetëm nga CPU

Rritja e shpejtësisë së procesorit nuk mjafton nëse memoria, bus-i ose I/O-ja janë të ngadalta. Kjo quhet problem i balansimit të performancës.

## Shpejtësia e mikroprocesorit

Shpejtësia shprehet me numrin e operacioneve në një interval kohor, por në praktikë duhet parë edhe sa cikle kërkon një instruksion dhe sa shpejt është kloku.

## RAM apo CPU?

Slajdet theksojnë se një sistem me CPU shumë të shpejtë por me pak RAM mund të ngadalësohet, dhe po ashtu një sistem me shumë RAM por me CPU të dobët mbetet i ngadaltë. Pra, performanca është çështje ekuilibri.

## Konsumi i fuqisë

Rritja e frekuencës dhe densitetit sjell probleme termike dhe të energjisë. Fuqia dinamike lidhet me komutimin e transistorëve. Kjo është një nga arsyet pse u kalua drejt multi-core në vend të rritjes pafund të frekuencës.

# 12. Multi-core dhe paralelizmi

## Pse kaluam te shumë bërthama

Kur performanca e një procesori me një bërthamë u ngadalësua, industria filloi të rrisë performancën duke vendosur disa bërthama brenda një çipi.

## Çfarë fiton sistemi

Nëse programi mund të ndahet në pjesë që punojnë paralelisht, shumë bërthama japin rritje të dukshme të performancës.

## Çfarë kufizon fitimin

Jo çdo pjesë e programit paralelizohet. Gjithmonë ka pjesë serike, sinkronizim, komunikim dhe vonesa të memories. Këto kufizime lidhen direkt me ligjin e Amdahl-it.

# 13. Matja e performancës

## Koha e ekzekutimit

Metrika më e rëndësishme është execution time. Një kompjuter quhet më i shpejtë nëse e kryen të njëjtin punim në kohë më të vogël.

## Frekuenca dhe koha e ciklit

Frekuenca e klokut dhe koha e ciklit janë reciproke. Sa më e lartë frekuenca, aq më e vogël koha e një cikli.

## CPI

CPI është numri mesatar i cikleve të klokut për instruksion. Sa më i vogël CPI, aq më mirë, nëse faktorët e tjerë mbesin të njëjtë.

## IC

Instruction Count është numri i instruksioneve të ekzekutuara nga programi. Dy procesorë mund të kenë frekuencë të ndryshme, por performanca varet edhe nga sa instruksione duhen për të kryer detyrën.

## MIPS

MIPS është numri i milionave instruksioneve për sekondë. Është metrikë e përdorur shpesh, por jo gjithmonë e mjaftueshme vetë, sepse instruksione të ndryshme nuk kanë të njëjtën kosto.

# 14. Formulat kryesore që duhet t’i dish

## Formula bazë e kohës së CPU-së

Koha e CPU-së = Numri i instruksioneve × CPI × koha e ciklit të klokut.

## Formula alternative

Meqë koha e ciklit = 1 / frekuenca, atëherë Koha e CPU-së = (Numri i instruksioneve × CPI) / frekuenca.

## Performanca

Performanca është në raport të zhdrejtë me kohën. Pra, nëse koha zvogëlohet, performanca rritet.

## Speedup

Speedup = Koha e vjetër / Koha e re.

## Ligji i Amdahl-it

Speedup-i i përgjithshëm varet nga pjesa e detyrës që përfitohet nga përmirësimi dhe nga madhësia e vetë përmirësimit. Sa më e madhe pjesa serike, aq më i kufizuar është speedup-i maksimal.

# 15. Pipeline

## Ideja bazë

Pipeline e ndan ekzekutimin e një instruksioni në faza. Në vend që një instruksion ta përfundojë krejt punën para se të fillojë tjetri, instruksione të ndryshme mund të jenë njëkohësisht në faza të ndryshme.

## Përfitimi

Pipeline rrit throughput-in, sepse procesori punon më vazhdimisht. Nuk do të thotë domosdo që një instruksion i vetëm përfundon shumë më shpejt, por se përfundojnë më shumë instruksione për njësi kohe.

## Kufizimet

Hazard-et, degëzimet dhe varësitë e të dhënave mund ta ulin efikasitetin e pipeline-it.

# 16. Ligji i Amdahl-it

## Çfarë thotë ligji

Nëse vetëm një pjesë e programit mund të përmirësohet ose paralelizohet, atëherë shpejtësia totale e sistemit nuk mund të kalojë një kufi të caktuar. Pjesa serike mbetet pengesa kryesore.

## Interpretimi praktik

Edhe nëse 95% e programit paralelizohet, 5% serik e kufizon rritjen maksimale të shpejtësisë. Kjo është arsyeja pse 'N procesorë = N herë më shpejt' nuk është e vërtetë në praktikë.

## Si bie në provim

Zakonisht jepet përqindja e pjesës që mund të përmirësohet, pastaj jepet speedup-i i asaj pjese ose numri i procesorëve, dhe kërkohet speedup-i total.

# 17. Gjërat që duhen mësuar përmendësh

## Lista e shkurtër e definicioneve

Arkitekturë, organizim, strukturë, funksion, ALU, njësia e kontrollit, regjistër, I/O, bus, von Neumann, Harvard, pipeline, CPI, MIPS, speedup, Amdahl.

## Lista e figurave / ideve

Modeli funksional i kompjuterit, katër komponentët kryesorë të kompjuterit, përbërja e CPU-së, struktura IAS, gjeneratat e kompjuterëve, Moore, multi-core, pipeline.

## Lista e formulave

Koha e CPU-së, lidhja mes frekuencës dhe kohës së ciklit, speedup-i dhe logjika e Amdahl-it.

# 18. Pyetje tipike që mund të dalin

## Teori

Shpjego dallimin mes arkitekturës dhe organizimit. Shpjego dallimin mes von Neumann dhe Harvard. Trego komponentët kryesorë të kompjuterit dhe funksionin e secilit. Çfarë roli ka njësia e kontrollit? Çfarë janë regjistrat?

## Llogaritje

Llogarit kohën e CPU-së kur jepen IC, CPI dhe frekuenca. Krahaso dy kompjuterë kur jepen koha e ciklit dhe CPI. Gjej MIPS rate. Zgjidh detyrë me ligjin e Amdahl-it.

# 19. Plan 3-ditor për mësim

## Dita 1

Mëso pjesën teorike: konceptet themelore, funksionet e kompjuterit, strukturën e kompjuterit, CPU-në, IAS-in, gjeneratat dhe dallimin von Neumann / Harvard.

## Dita 2

Mëso pjesën e evolucionit dhe teknologjisë: Moore, mikroprocesorët, ARM, embedded systems, cloud, dhe arsyen pse multi-core u bë i domosdoshëm.

## Dita 3

Mëso formulat dhe bëj ushtrimet: koha e CPU-së, CPI, MIPS, pipeline si ide, speedup dhe ligji i Amdahl-it. Në fund bëj vetë-pyetje pa i parë shënimet.

# 20. Përmbledhja finale

## Në një fjali për çdo bllok

Kompjuteri është sistem që përpunon, ruan, bart dhe kontrollon të dhëna. Arkitektura tregon çfarë sheh programuesi; organizimi tregon si realizohet në harduer. CPU përbëhet nga ALU, njësia e kontrollit dhe regjistrat. Von Neumann ruan programin dhe të dhënat në të njëjtën memorie; Harvard i ndan. Evolucioni teknologjik kaloi nga gypat, te transistorët, te qarqet e integruara, te mikroprocesorët. Performanca matet me kohën e ekzekutimit dhe varet nga IC, CPI dhe frekuenca. Pipeline dhe multi-core rrisin performancën, por ligji i Amdahl-it e kufizon speedup-in maksimal.

# Tabela e formulave kryesore

|   |   |
|---|---|
|**Koncepti**|**Formula / ideja**|
|Koha e CPU-së|CPU time = IC × CPI × clock cycle time|
|Koha e ciklit|clock cycle time = 1 / frequency|
|Speedup|Speedup = old time / new time|
|Performanca|Performance ∝ 1 / execution time|
|MIPS|MIPS = instruction count / (execution time × 10^6)|

# Checklist i fundit para provimit

**□** A mund ta shpjegosh dallimin arkitekturë vs organizim pa e ngatërruar?

**□** A i di 4 funksionet bazë të kompjuterit?

**□** A i di 4 komponentët kryesorë të strukturës së kompjuterit?

**□** A i di pjesët kryesore të CPU-së?

**□** A e kupton stored-program concept te von Neumann?

**□** A mund ta dallosh Harvard nga von Neumann?

**□** A e di formulën e kohës së CPU-së?

**□** A mund të llogarisësh speedup dhe detyra të Amdahl-it?