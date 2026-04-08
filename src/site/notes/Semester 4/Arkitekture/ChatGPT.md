---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/chat-gpt/"}
---

**ARKITEKTURA E KOMPJUTERËVE**
# 1. Konceptet themelore të kompjuterit si sistem hierarkik

Arkitektura, organizimi, struktura dhe funksioni janë katër nocionet bazë me të cilat përshkruhet një kompjuter. Ideja themelore është që kompjuteri të mos shihet si një kuti e vetme, por si një sistem i ndërtuar në nivele: në nivelin më të lartë shohim kompjuterin si tërësi, më poshtë shohim CPU-në, memorien dhe hyrje/daljen, ndërsa edhe më poshtë shohim regjistrat, ALU-në, sinjalet e kontrollit dhe detajet e realizimit fizik.

Qasja hierarkike e bën më të qartë edhe analizën: në çdo nivel pyeten dy gjëra. Së pari, si janë të lidhura pjesët mes vete; kjo është struktura. Së dyti, çfarë bën secila pjesë; ky është funksioni. Kjo logjikë përshkon krejt lëndën: nga kompjuteri si sistem, te CPU-ja, te njësia e kontrollit, e deri te mënyra si ekzekutohet një instruksion i vetëm.

# 2. Arkitektura kundrejt organizimit

Arkitektura e kompjuterit përfshin ato veti që janë të dukshme për programuesin dhe që ndikojnë drejtpërdrejt në ekzekutimin logjik të programit. Këtu hyn seti i instruksioneve, formatet e instruksioneve, numri i bitëve me të cilët paraqiten të dhënat, mënyrat e adresimit të memories dhe mekanizmat bazë të komunikimit me hyrje/daljen.

Organizimi i kompjuterit tregon si realizohen në praktikë këto kërkesa arkitekturore. Këtu hyjnë detajet harduerike që zakonisht programuesi nuk i sheh drejtpërdrejt: sinjalet e kontrollit, teknologjia e memories, bus-at, njësitë funksionale, ndërfaqet me periferitë dhe mënyra konkrete e realizimit të operacioneve brenda procesorit.

Shembulli klasik është shumëzimi. Pyetja “a ekziston instruksioni MUL?” i takon arkitekturës, sepse programuesi duhet të dijë nëse ka një instruksion të tillë në ISA. Pyetja “a bëhet shumëzimi me një njësi të veçantë harduerike apo duke ripërdorur mbledhjen?” i takon organizimit, sepse kjo është mënyra konkrete e realizimit.

Ky dallim ka rëndësi sepse shumë sisteme mund të kenë të njëjtën arkitekturë, por organizim të ndryshëm. Kjo do të thotë se mund të ekzekutojnë të njëjtin program, por me shpejtësi, kosto dhe efikasitet energjetik të ndryshëm. Pikërisht kjo ide përmendet edhe te familjet si Intel x86 dhe IBM System/370: baza arkitekturore mund të mbetet e njëjtë, ndërsa teknologjia dhe organizimi ndryshojnë me kalimin e kohës.

# 3. Struktura dhe funksioni i kompjuterit

Struktura e kompjuterit është mënyra si ndërlidhen komponentët kryesorë. Në nivelin më të lartë, kompjuteri shihet si një sistem që lidhet me rrethinën e jashtme përmes periferive dhe linjave komunikuese. Brenda tij, pjesët kryesore janë procesori, memoria kryesore, hyrja/dalja dhe ndërlidhjet e sistemit.

Funksioni i kompjuterit ka të bëjë me operacionet që kryhen brenda kësaj strukture. Si në slajde ashtu edhe te Stallings, katër funksionet bazë janë: përpunimi i të dhënave, ruajtja e të dhënave, bartja e të dhënave dhe kontrolli. Këto katër funksione janë themeli i çdo sistemi kompjuterik, pavarësisht madhësisë apo teknologjisë së tij.

Kjo do të thotë se edhe një mikro-kontroller shumë i vogël, edhe një superkompjuter shumë i fuqishëm, në esencë duhet të bëjë të njëjtën gjë: të marrë të dhëna, t’i ruajë kur duhet, t’i përpunojë sipas një grupi instruksionesh dhe t’i kontrollojë këto veprime në rendin e duhur.

# 4. Modeli funksional i kompjuterit

Bartja e të dhënave nënkupton lëvizjen e të dhënave ndërmjet kompjuterit dhe mjedisit të jashtëm, ose ndërmjet pjesëve të brendshme të kompjuterit. Kur të dhënat merren ose dërgohen te një pajisje e lidhur drejtpërdrejt, procesi njihet si hyrje/dalje (I/O), ndërsa kur lëvizja bëhet në distanca më të mëdha, flitet për komunikim të të dhënave.

Ruajtja e të dhënave nënkupton mbajtjen e informacionit për përdorim të mëvonshëm. Kjo përfshin si ruajtjen afatshkurtër të operandëve dhe rezultateve gjatë ekzekutimit të programit, ashtu edhe ruajtjen më afatgjatë të programeve dhe të dhënave në memorie. Termat bazë që lidhen me këtë funksion janë leximi dhe shkrimi.

Përpunimi i të dhënave nënkupton transformimin e tyre. Një vlerë mund të mblidhet me një tjetër, të krahasohet, të zhvendoset, të shumëzohet, të ndahet ose t’i nënshtrohet operacioneve logjike. Përpunimi kryhet kryesisht nga ALU-ja, por gjithmonë nën drejtimin e njësisë së kontrollit.

Kontrolli është funksioni që i lidh të tre funksionet e tjera në një rrjedhë koherente. Njësia e kontrollit vendos se cili instruksion do të merret nga memoria, cilat regjistra do të përdoren, kur do të bëhet leximi ose shkrimi dhe cilat sinjale duhet të aktivizohen që të kryhet veprimi i kërkuar. Pa kontroll, nuk do të kishte as rend, as koordinim.

# 5. Komponentët kryesorë të strukturës së kompjuterit

CPU-ja është pjesa qendrore që kontrollon operacionet e kompjuterit dhe kryen funksionet bazë të përpunimit. Ajo është komponenta që ekzekuton instruksionet e programit dhe koordinon rrjedhën e punës së pjesëve të tjera.

Memoria kryesore ruan të dhënat dhe instruksionet që CPU-ja duhet t’i përdorë shpejt gjatë ekzekutimit. Kjo është memoria që punon më afër me procesorin dhe që furnizon vazhdimisht ciklin e instruksioneve.

Hyrja/dalja shërben si ura midis botës së brendshme të kompjuterit dhe rrethinës së jashtme. Tastiera, miu, disku, ekrani, rrjeti dhe pajisje të tjera i japin ose marrin kompjuterit të dhëna përmes mekanizmave të I/O-së.

Ndërlidhjet e sistemit, zakonisht të menduara si system bus, janë mekanizmat që mundësojnë komunikimin mes CPU-së, memories dhe I/O-së. Busi nuk është thjesht një vijë e vetme, por një bashkësi rrugësh për bartjen e adresave, të dhënave dhe sinjaleve të kontrollit. Nëse këto lidhje janë të dobëta ose të ngadalta, edhe komponentët individualë të mirë nuk e japin performancën që pritet.

# 6. Përbërja e CPU-së

ALU-ja, ose Njësia Aritmetike dhe Logjike, është pjesa ku kryhen operacionet aritmetike dhe logjike. Ajo merret me mbledhje, zbritje, krahasime, zhvendosje bitësh dhe vendime logjike si AND, OR dhe NOT. Kur themi se procesori “llogarit”, në thelb po flasim për punën e ALU-së.

Njësia e kontrollit është dirigjenti i CPU-së. Ajo interpreton instruksionet që vijnë nga memoria, i dekodon dhe nxjerr sinjalet që u tregojnë pjesëve të tjera të procesorit se çfarë duhet bërë. Kjo njësi nuk bën llogaritjen vetë; ajo organizon rrjedhën e saj.

Regjistrat janë memoriet më të vogla, më të shpejta dhe më afër ekzekutimit. Për shkak se janë shumë të shpejtë, procesori i përdor për të mbajtur përkohësisht adresa, operandë, rezultate dhe gjendje kontrolli. Sa më shumë punë të mund të kryhet duke përdorur regjistra, aq më pak nevojitet qasje e kushtueshme në memorien kryesore.

Ndërlidhjet e brendshme të CPU-së janë rrugët që i lidhin këto tri pjesë. Edhe kur në skema paraqiten si “internal bus”, ideja është e njëjtë: të sigurohet rrjedhje e shpejtë dhe e kontrolluar e të dhënave dhe sinjaleve brenda vetë procesorit.

# 7. Njësia e kontrollit si pjesë më e imët e hierarkisë

Në slajde, njësia e kontrollit zbërthehet më tej në logjikë sekuencore, memorien e kontrollit dhe regjistra/dekodues. Kjo tregon se edhe vetë kontrolli është një sistem i organizuar, jo vetëm një “buton komande”.

Logjika sekuencore merret me rendin e hapave, pra me kalimin nga një gjendje në tjetrën gjatë ekzekutimit të instruksioneve. Dekoduesit dhe regjistrat përkthejnë instruksionin në forma të përdorshme dhe mbajnë gjendjen e përkohshme të kontrollit. Memoria e kontrollit lidhet me idenë e mikroprogramimit: sinjalet e kontrollit mund të organizohen si sekuenca mikroinstruksionesh që drejtojnë pjesët e procesorit.

# 8. Gjeneratat e hershme të kompjuterëve

Gjenerata e parë lidhet me gypat me vakum. Shembulli bazë është ENIAC: një sistem shumë i madh, me konsum të lartë energjie, me peshë të madhe dhe programim manual përmes ndërprerësve. Nga këto karakteristika kuptohet pse kompjuterët e parë ishin të shtrenjtë, të vështirë për t’u mirëmbajtur dhe fizikisht të papërshtatshëm për përdorim të gjerë.

Kalimi te transistorët në gjeneratën e dytë e bëri kompjuterin më të vogël, më të besueshëm dhe më efikas. Gjenerata e tretë, me qarqet e integruara, e rriti më tej densitetin e komponentëve dhe uli kostot. Më pas, mikroprocesori e çoi kompjuterin në një fazë ku një procesor i tërë mund të vendosej në një çip të vetëm. Ky është kalimi kyç drejt kompjuterëve personalë dhe pajisjeve moderne digjitale.

# 9. Makina e John von Neumann-it dhe kompjuteri IAS

Kontributi më i rëndësishëm i von Neumann-it është stored-program concept: programi dhe të dhënat ruhen në të njëjtën memorie dhe trajtohen si informacion binar. Kjo e bën kompjuterin fleksibil, sepse programi mund të ndryshohet pa ndërruar vetë makinën fizike.

Kompjuteri IAS përfaqëson këtë model në formë klasike. Në të, ALU-ja vepronte mbi të dhëna binare, njësia e kontrollit i merrte instruksionet nga memoria dhe pajisjet hyrëse/dalëse menaxhoheshin nga kontrolli. Pra, memoria nuk ruante vetëm të dhëna “pasive”, por edhe vetë udhëzimet sipas të cilave punonte sistemi.

Te Stallings, struktura e IAS-it shpjegohet edhe në mënyrë më të detajuar: një fjalë memories kishte 40 bita dhe mund të mbante dy instruksione nga 20 bita, secili i përbërë nga opcode dhe fushë adrese. Kjo tregon se edhe në një sistem historik, organizimi i memories dhe formati i instruksionit janë thelbësorë për të kuptuar si ekzekutohet programi.

# 10. Regjistrat kryesorë të IAS-it

MAR (Memory Address Register) mban adresën e lokacionit të memories që duhet lexuar ose shkruar. Kur procesori duhet të marrë një fjalë nga memoria, MAR tregon saktësisht se nga cila adresë do të bëhet qasja.

MBR (Memory Buffer Register) mban fjalën që po vjen nga memoria ose që po dërgohet në memorie apo I/O. Në një kuptim praktik, ai është regjistri ndërmjetës ku kalon përmbajtja gjatë lëvizjes nga dhe drejt memories.

IR (Instruction Register) mban opcode-in e instruksionit që po ekzekutohet. Ai e përfaqëson pyetjen “çfarë duhet bërë tani?”. Pasi opcode vendoset në IR, njësia e kontrollit e dekodon dhe e shndërron në sinjale konkrete.

IBR (Instruction Buffer Register) ruan përkohësisht instruksionin tjetër kur një fjalë memories përmban dy instruksione. Kjo lidhet me faktin se në IAS një fjalë 40-bitëshe mund të ndahej në instruksionin e majtë dhe të djathtë; prandaj njëri mund të ekzekutohej, ndërsa tjetri të mbahej për më pas.

PC (Program Counter) mban adresën e instruksionit që do të merret më pas. Ai është treguesi i rrjedhës së programit. Nëse nuk ka degëzim, PC ecën përpara; nëse ka jump ose branch, PC ndryshohet sipas instruksionit.

AC (Accumulator) dhe MQ (Multiplier Quotient) përdoren për të mbajtur operandë dhe rezultate të ALU-së. Në shumëzim, për shembull, rezultati mund të jetë më i madh se një fjalë e vetme; prandaj pjesa më e rëndësishme dhe ajo më pak e rëndësishme mund të shpërndahen mes këtyre regjistrave.

# 11. Cikli i instruksionit te IAS

Ekzekutimi i programit ndodh në mënyrë të përsëritur përmes ciklit të instruksionit. Në fetch cycle, procesori merr instruksionin e radhës nga memoria. Në execute cycle, ai e zbaton atë. Kjo ndarje është shumë e rëndësishme, sepse shpjegon ritmin themelor me të cilin punon çdo CPU.

Kur instruksioni merret, opcode vendoset në IR, adresa përkatëse në MAR, ndërsa vetë fjala e memories kalon përmes MBR. Nëse ka mbetur një instruksion në IBR, ai mund të përdoret pa një qasje të re në memorie. Pastaj njësia e kontrollit e dekodon opcode-in dhe nxjerr sinjalet që lëvizin të dhëna ose aktivizojnë ALU-në.

Kjo skemë historike është themeli i mënyrës si kuptohet sot cikli i procesorit: marrja e instruksionit, dekodimi, qasja në operandë, ekzekutimi dhe përditësimi i gjendjes së sistemit.

# 12. Ligji i Moore-it dhe miniaturizimi

Ligji i Moore-it shpreh idenë se numri i transistorëve në një çip rritet me ritëm shumë të shpejtë, tradicionalisht afërsisht dyfishim në një periudhë të rregullt. Në slajde theksohet pasoja praktike: për të njëjtin çmim fitohet më shumë fuqi procesuese.

Rëndësia reale e këtij zhvillimi nuk është vetëm “më shumë transistorë”, por ajo që kjo sjell në nivel sistemi. Rrugët elektrike bëhen më të shkurtra, prandaj sinjalet lëvizin më shpejt. Kompjuterët bëhen më të vegjël dhe mund të futen në pajisje të larmishme. Ndërlidhjet në qarqet e integruara bëhen më të besueshme. Në shumë raste mund të optimizohet edhe konsumi i energjisë për njësi pune.

Megjithatë, ky miniaturizim sjell edhe kufij praktikë: nxehtësinë, konsumimin e energjisë, vështirësinë e disipimit termik dhe kompleksitetin e organizimit të brendshëm. Pikërisht këto kufizime ndihmuan kalimin nga rritja lineare e frekuencës te shumëbërthamësia.

# 13. Mikroprocesorët modernë, ARM dhe embedded systems

Evolucioni i mikroprocesorëve modernë tregon kalimin nga çipat e hershëm me kapacitete modeste te familje shumë të pasura si Intel x86, PowerPC dhe ARM. Ideja që duhet mbajtur është se rritja e densitetit të transistorëve dhe përmirësimet arkitekturore e organizative e kanë shndërruar procesorin në një sistem shumë më kompleks se sa ALU plus kontroll i thjeshtë.

ARM ka rëndësi të veçantë sepse lidhet me efikasitetin energjetik dhe përdorimin e gjerë në pajisje mobile e embedded. Në këtë kontekst, embedded systems janë sisteme kompjuterike të ndërtuara për një rol të caktuar brenda një pajisjeje më të madhe. Ato gjenden në pajisje shtëpiake, automjete, printerë, pajisje rrjeti, sensorë dhe shumë produkte të tjera.

Kjo do të thotë se “kompjuter” nuk duhet kuptuar vetëm si laptop ose desktop. Në praktikë, shumica numerike e kompjuterëve sot janë sisteme të mbjella, shpesh të vogla, të lira, të optimizuara për energji dhe të projektuara për një funksion të specializuar.

# 14. Arkitektura Harvard dhe dallimi nga von Neumann

Në arkitekturën von Neumann, instruksionet dhe të dhënat ruhen në të njëjtën memorie. Kjo e bën sistemin të thjeshtë dhe fleksibil, por do të thotë se i njëjti kanal i memories ndahet për marrjen e instruksioneve dhe për qasjen te të dhënat.

Në arkitekturën Harvard, memoria e instruksioneve dhe memoria e të dhënave janë fizikisht të ndara. Kjo bën të mundur që procesori, në parim, të lexojë një instruksion dhe njëkohësisht të qaset në të dhënat, sepse po përdor rrugë të ndara. Kjo është arsyeja pse Harvard lidhet me qasje paralele dhe shmangie të disa ngushticave të memories.

Një dallim praktik që përmendet në slajde është se memoria e programit shpesh është vetëm për lexim, ndërsa memoria e të dhënave lejon lexim dhe shkrim. Prandaj, kur pyetja është “një memorie e vetme apo dy të ndara?”, von Neumann dhe Harvard duhen dalluar pikërisht mbi këtë bazë.

# 15. Cloud computing si ide bazë

Cloud computing, në kuptimin e thjeshtuar të prezantuar në material, është ofrimi i resurseve kompjuterike si shërbim. Në vend që përdoruesi të blejë dhe të menaxhojë vetë gjithë infrastrukturën, ai i konsumon resurset nga larg sipas nevojës.

Kjo qasje lidhet me fleksibilitetin, shkallëzimin dhe ndarjen e kostos. Përdoruesi ose organizata mund të marrë fuqi procesuese, ruajtje, platformë zhvillimi ose aplikacione pa pasur domosdoshmërisht pronësinë direkte të të gjithë harduerit. Edhe kur slajdet e trajtojnë vetëm si hyrje, ideja thelbësore është se kompjuteri modern nuk kufizohet më te një makinë fizike e vetme në tavolinë.

# 16. Problemet themelore të performancës

Performanca nuk varet vetëm nga shpejtësia e CPU-së. Një sistem i balancuar kërkon që procesori, memoria dhe hyrje/dalja të jenë në një raport të arsyeshëm. Nëse CPU-ja përmirësohet shumë, por memoria dhe I/O mbeten të ngadalta, atëherë përfitimi i vërtetë i sistemit mbetet i kufizuar.

Kjo është arsyeja pse rritja e performancës është problem i gjithë sistemit. Koha e ekzekutimit ndikohet nga sa instruksione duhet të ekzekutohen, sa cikle harxhohen për çdo instruksion dhe sa shpejt kalojnë vetë ciklet e klokut. Prandaj performanca është kombinim i arkitekturës, organizimit dhe teknologjisë.

Te materialet e këtij kapitulli del qartë edhe çështja e fuqisë dhe nxehtësisë. Me rritjen e frekuencës dhe të densitetit të transistorëve, nuk mjafton vetëm të thuhet “e bëjmë më të shpejtë CPU-në”; duhet parë nëse kjo rritje është termikisht dhe energjetikisht e përballueshme.

# 17. Koha e CPU-së, IC, CPI dhe frekuenca

Masa më e rëndësishme e performancës është koha e ekzekutimit. Një kompjuter konsiderohet më i shpejtë vetëm nëse e përfundon të njëjtin punim në kohë më të shkurtër. Kjo është më themelore se çdo metrikë e ndërmjetme.

Instruction Count (IC) është numri i instruksioneve që ekzekutohen për një program. Ky numër nuk është domosdoshmërisht i njëjtë për çdo arkitekturë ose për çdo implementim, sepse të njëjtin problem mund ta zgjidhin programe ose kompajlerë të ndryshëm me numër të ndryshëm instruksionesh.

CPI (Clock Cycles Per Instruction) është numri mesatar i cikleve të klokut për instruksion. Nëse një program kërkon shumë cikle për instruksion, atëherë edhe me frekuencë të lartë mund të mos jetë aq i shpejtë sa duket. Frekuenca e klokut tregon sa cikle ndodhin për sekondë, ndërsa koha e ciklit është reciproku i saj.

Këta tre faktorë lidhen nga formula themelore: koha e CPU-së = IC × CPI × koha e ciklit. Meqë koha e ciklit = 1/frekuenca, formula mund të shkruhet edhe si koha e CPU-së = (IC × CPI)/frekuenca. Kjo formulë shpjegon pse nuk mjafton të krahasohen vetëm GHz: një procesor me frekuencë më të ulët mund të dalë më i shpejtë nëse ka CPI më të mirë ose ekzekuton më pak instruksione për të njëjtën detyrë.

# 18. MIPS si metrikë

MIPS shpreh numrin e milionave instruksioneve për sekondë. Në shikim të parë duket intuitiv: sa më i madh MIPS, aq më i shpejtë procesori. Por kjo nuk është gjithmonë e mjaftueshme si krahasim i drejtë.

Arsyeja është se jo çdo instruksion bën të njëjtën sasi pune. Dy procesorë mund të kenë MIPS të ndryshëm, por instruksionet e njërit mund të jenë më “të pasura” ose programi mund të kërkojë numër tjetër instruksionesh. Prandaj MIPS mund të përdoret si tregues ndihmës, por jo si prova e vetme e performancës.

Më e sigurt është të kthehesh gjithmonë te koha reale e ekzekutimit dhe te lidhja ndërmjet IC, CPI dhe frekuencës.

# 19. Speedup dhe krahasimi i sistemeve

Speedup është raporti mes kohës së vjetër dhe kohës së re. Nëse një sistem e kryen një punë në 10 sekonda dhe një sistem tjetër në 5 sekonda, speedup është 10/5 = 2. Kjo do të thotë se sistemi i ri është dy herë më i shpejtë për atë punë.

Ky raport është i dobishëm sepse e lidh drejtpërdrejt performancën me kohën. Performanca rritet kur koha zvogëlohet, prandaj formulimi “sa herë është më i shpejtë?” duhet parë gjithmonë në raport me kohën e ekzekutimit, jo vetëm me një komponent të sistemit.

# 20. Multi-core dhe paralelizmi

Kur rritja e frekuencës së një bërthame të vetme hasi kufij praktikë, industria filloi të rrisë performancën duke vendosur disa bërthama në të njëjtin çip. Kjo është logjika e multicore: jo domosdoshmërisht një bërthamë shumë më e shpejtë, por disa bërthama që mund të punojnë në paralel.

Përfitimi real varet nga programi. Nëse puna mund të ndahet në pjesë të pavarura që ekzekutohen njëkohësisht, shumëbërthamësia mund të japë rritje të dukshme. Por nëse programi ka pjesë të mëdha serike, pritje, sinkronizim ose qasje të kufizuar në memorie, rritja e performancës mbetet më e ulët se sa numri teorik i bërthamave.

Prandaj multicore nuk është magji automatike. Është mundësi harduerike për paralelizëm, por shfrytëzimi i saj varet nga natyra e problemit dhe nga mënyra si është shkruar programi.

# 21. Pipeline

Pipeline e ndan ekzekutimin e instruksionit në faza, p.sh. marrja, dekodimi, qasja në operandë, ekzekutimi dhe shkrimi i rezultatit. Në vend që një instruksion të kalojë krejt rrugën i vetëm para se të fillojë tjetri, disa instruksione mund të jenë njëkohësisht në faza të ndryshme të së njëjtës tubacion.

Përfitimi kryesor i pipeline-it është rritja e throughput-it, domethënë rritja e numrit të instruksioneve të përfunduara për njësi kohe. Kjo nuk do të thotë domosdoshmërisht që një instruksion i vetëm bëhet shumë më i shpejtë; përfitimi vjen nga mbivendosja e fazave.

Efikasiteti i pipeline-it kufizohet nga hazard-et. Hazard-et e të dhënave ndodhin kur një instruksion varet nga rezultati i tjetrit. Hazard-et e kontrollit dalin kryesisht te degëzimet, kur nuk dihet me siguri cili instruksion vjen më pas. Hazard-et strukturore dalin kur dy veprime duan të përdorin të njëjtin resurs në të njëjtën kohë. Sa më shumë ndërprerje ose boshllëqe në pipeline, aq më pak i afrohet ai përfitimit ideal.

# 22. Ligji i Amdahl-it

Ligji i Amdahl-it thotë se përfitimi i përgjithshëm nga një përmirësim kufizohet nga pjesa e sistemit ose e programit që nuk përmirësohet. Nëse vetëm një pjesë e punës mund të përshpejtohet, atëherë pjesa e mbetur bëhet kufiri i shpejtësisë totale.

Në kontekstin e paralelizmit kjo do të thotë se edhe nëse një pjesë e madhe e programit mund të ndahet në shumë procesorë ose bërthama, pjesa serike vendos tavanin teorik të speedup-it. Sa më e madhe pjesa që mbetet serike, aq më shpejt arrihet ky kufi.

Interpretimi praktik është shumë i rëndësishëm: shtimi i pafund i bërthamave nuk e jep pafund speedup-in. Përmirësimi ka kthime gjithnjë e më të vogla sapo pjesa serike fillon të dominojë. Kjo është arsyeja pse paralelizmi duhet menduar bashkë me strukturën e problemit, jo vetëm me numrin e njësive përpunuese.

# 23. Përmbledhja e formulave kryesore

Këto formula përmbledhin lidhjet që janë përdorur në pjesën e performancës. Qëllimi nuk është vetëm t’i mësosh përmendësh, por të kuptosh çfarë tregon secila dhe si lidhet me të tjerat.

|   |   |   |
|---|---|---|
|**Madhësia**|**Formula**|**Kuptimi**|
|Koha e CPU-së|T_CPU = IC × CPI × T_ciklit|Sa kohë i duhet CPU-së për të ekzekutuar programin.|
|Koha e CPU-së|T_CPU = (IC × CPI) / f|E njëjta formulë e shkruar me frekuencë në vend të kohës së ciklit.|
|Frekuenca dhe cikli|f = 1 / T_ciklit|Frekuenca dhe koha e ciklit janë reciproke.|
|CPI|CPI = numri i cikleve / numri i instruksioneve|Mesatarja e cikleve që harxhohen për çdo instruksion.|
|Performanca|Performanca ∝ 1 / Koha|Kur koha bie, performanca rritet.|
|Speedup|Speedup = T_vjetër / T_re|Sa herë është përmirësuar një sistem ose një program.|

MIPS = IC / (T × 10^6). Kjo metrikë tregon miliona instruksione për sekondë, por duhet lexuar me kujdes sepse nuk tregon vetvetiu sa punë reale bën çdo instruksion.

# 24. Përmbyllje e përmbajtjes

Në thelb, i gjithë materiali lidhet nga një vijë e vetme logjike. Fillimisht përcaktohen nocionet bazë: arkitekturë, organizim, strukturë dhe funksion. Pastaj shpjegohet si kompjuteri përpunon, ruan, bart dhe kontrollon të dhëna. Më tej zbërthehet struktura e tij në CPU, memorie, I/O dhe bus, si dhe vetë CPU-ja në ALU, njësi kontrolli dhe regjistra. Në planin historik, modeli von Neumann dhe kompjuteri IAS japin themelin klasik të stored-program machine. Në planin teknologjik, ligji i Moore-it, mikroprocesorët modernë, ARM-i dhe sistemet embedded tregojnë si është zhvilluar hardueri. Në planin organizativ e performues, koha e CPU-së, CPI, frekuenca, MIPS, pipeline, multicore dhe ligji i Amdahl-it shpjegojnë pse një sistem është i shpejtë ose pse has kufizime.

Kur këto tema kuptohen si një tërësi, materiali nuk duket më si listë slajdesh të ndara, por si një histori e vetme: si ndërtohet kompjuteri, si punon, si u zhvillua dhe si matet fuqia e tij.