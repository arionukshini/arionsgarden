---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/flashcards/"}
---

# Flashcards – Arkitektura e Kompjuterëve

## Çfarë studion arkitektura e kompjuterit?

Arkitektura e kompjuterit merret me veçoritë e sistemit që janë të dukshme për programuesin dhe që ndikojnë drejtpërdrejt në ekzekutimin e programit, si numri i bitëve, seti i instruksioneve dhe mënyrat e adresimit.

## Çfarë studion organizimi i kompjuterit?

Organizimi i kompjuterit merret me njësitë operacionale dhe ndërlidhjet me të cilat realizohen në praktikë kërkesat e arkitekturës, p.sh. sinjalet e kontrollit, teknologjia e memories dhe ndërfaqet me periferitë.

## Cili është dallimi kryesor mes arkitekturës dhe organizimit të kompjuterit?

Arkitektura përshkruan **çfarë** sheh programuesi, ndërsa organizimi përshkruan **si** realizohet kjo në harduer.

## Çfarë nënkupton struktura e kompjuterit?

Struktura e kompjuterit nënkupton mënyrën se si ndërlidhen komponentët kryesorë të tij.

## Çfarë nënkupton funksioni i kompjuterit?

Funksioni i kompjuterit nënkupton operacionet që kryejnë komponentët individualë brenda strukturës së sistemit.

## Cilat janë katër funksionet kryesore të kompjuterit?

- Përpunimi i të dhënave
- Ruajtja e të dhënave
- Bartja e të dhënave
- Kontrolli i këtyre funksioneve

## Çfarë është input-output (I/O)?

I/O është procesi i marrjes ose dërgimit të të dhënave te pajisjet e lidhura drejtpërdrejt me kompjuterin, pra periferitë.

## Çfarë është komunikimi i të dhënave?

Komunikimi i të dhënave është bartja e të dhënave në distanca më të gjata sesa I/O-ja e drejtpërdrejtë.

## Cilët janë katër komponentët kryesorë strukturorë të kompjuterit?

1. CPU
2. Memoria kryesore
3. Hyrja/Dalja (I/O)
4. Ndërlidhjet e sistemit (system bus)

## Çfarë roli ka CPU-ja?

CPU-ja kontrollon operacionet e kompjuterit dhe kryen funksionet kryesore të përpunimit të të dhënave.

## Çfarë roli ka memoria kryesore?

Memoria kryesore ruan të dhënat dhe instruksionet që CPU-ja duhet t’i përdorë gjatë ekzekutimit.

## Çfarë roli ka I/O-ja?

I/O-ja bart të dhënat ndërmjet kompjuterit dhe rrethinës së jashtme.

## Çfarë është system bus?

System bus është bashkësia e rrugëve/linjave që mundëson komunikimin ndërmjet CPU-së, memories dhe I/O-së për adresa, të dhëna dhe sinjale kontrolli.

## Cilat janë pjesët kryesore të CPU-së?

CPU-ja përbëhet kryesisht nga:
- ALU
- Njësia e kontrollit
- Regjistrat
- Ndërlidhjet e brendshme

## Çfarë bën ALU-ja?

ALU-ja (Njësia Aritmetike dhe Logjike) kryen operacione aritmetike dhe logjike si mbledhja, zbritja, krahasimi dhe operacionet Boolean.

## Çfarë bën njësia e kontrollit?

Njësia e kontrollit interpreton instruksionet, i dekodon ato dhe lëshon sinjalet që koordinojnë punën e pjesëve të tjera të procesorit.

## Pse regjistrat janë të rëndësishëm?

Regjistrat janë memoriet më të shpejta të CPU-së dhe mbajnë përkohësisht adresa, operandë, rezultate dhe informacione kontrolli.

## Çfarë karakterizonte gjeneratën e parë të kompjuterëve?

Gjenerata e parë përdorte gypa me vakum; kompjuterët ishin shumë të mëdhenj, konsumonin shumë energji dhe programoheshin në mënyrë manuale.

## Cila ishte rëndësia e transistorit në gjeneratën e dytë?

Transistori zëvendësoi gypat me vakum, duke i bërë kompjuterët më të vegjël, më të lirë, më të besueshëm dhe më efikasë energjetikisht.

## Çfarë solli gjenerata e tretë e kompjuterëve?

Gjenerata e tretë solli qarqet e integruara (IC), duke rritur densitetin e komponentëve dhe duke ulur koston e prodhimit.

## Pse Intel 4004 konsiderohet historik?

Sepse ishte çipi i parë që përmbante të gjitha komponentet kryesore të një CPU-je në një paketim të vetëm.

## Çfarë është koncepti stored-program i von Neumann-it?

Është ideja që programi dhe të dhënat ruhen në të njëjtën memorie dhe trajtohen në formë binare.

## Pse kompjuteri IAS është i rëndësishëm?

Sepse përfaqëson modelin klasik von Neumann me memorie për program dhe të dhëna, ALU, njësi kontrolli dhe I/O.

## Sa ishte madhësia e një fjale në memorien IAS?

Një fjalë e memories IAS kishte 40 bita.

## Si ruheshin instruksionet në një fjalë të memories IAS?

Një fjalë 40-bitëshe mund të përmbante dy instruksione nga 20 bita secili.

## Çfarë përmban Instruction Register (IR)?

IR mban kodin operues (opcode) të instruksionit që po ekzekutohet.

## Çfarë përmban Program Counter (PC)?

PC mban adresën e instruksionit që duhet të merret më pas.

## Çfarë bën Memory Address Register (MAR)?

MAR specifikon adresën e lokacionit të memories që duhet lexuar ose shkruar.

## Çfarë bën Memory Buffer Register (MBR)?

MBR mban përkohësisht fjalën që po lexohet nga memoria ose që po shkruhet në memorie/I/O.

## Çfarë bën Instruction Buffer Register (IBR)?

IBR ruan përkohësisht instruksionin tjetër, zakonisht pjesën e djathtë të një fjale që përmban dy instruksione.

## Çfarë bëjnë Accumulator (AC) dhe Multiplier Quotient (MQ)?

Ata ruajnë përkohësisht operandët dhe rezultatet e operacioneve të ALU-së; në shumëzim, rezultati mund të ndahet midis AC dhe MQ.

## Cilat janë dy nënciklet kryesore të ciklit të instruksionit?

1. Sjellja e instruksionit (fetch)
2. Ekzekutimi i instruksionit (execute)

## Çfarë ndodh në fetch cycle?

Procesori merr instruksionin e radhës nga memoria, vendos opcode-in në IR dhe adresën përkatëse në MAR.

## Çfarë ndodh në execute cycle?

Njësia e kontrollit dekodon opcode-in dhe aktivizon sinjalet e nevojshme për të kryer operacionin ose bartjen e të dhënave.

## Sa instruksione kishte kompjuteri IAS dhe si grupoheshin?

IAS kishte 21 instruksione, të grupuara në: transfer të dhënash, degëzim të pakushtëzuar, degëzim të kushtëzuar, aritmetikë dhe modifikim adrese.

## Çfarë thotë ligji i Moore-it?

Ligji i Moore-it thotë se numri i transistorëve në një çip priret të dyfishohet afërsisht çdo dy vjet.

## Cilat janë disa pasoja të ligjit të Moore-it?

- Rritje e fuqisë procesuese për të njëjtin çmim
- Kompjuterë më të vegjël
- Rrugë elektrike më të shkurtra dhe më të shpejta
- Në shumë raste ulje e kërkesave për energji

## Pse u ngadalësua rritja klasike e performancës së procesorëve?

Sepse u afruan kufijtë fizikë, veçanërisht problemet e fuqisë, nxehtësisë, vonesës RC dhe latencës së memories.

## Cili është dallimi kryesor mes Pentium dhe PowerPC?

Pentium lidhet me arkitekturën CISC, ndërsa PowerPC me arkitekturën RISC.

## Çfarë do të thotë CISC?

CISC (Complex Instruction Set Computer) përdor instruksione më komplekse që shpesh kërkojnë më shumë cikle CPU-je.

## Çfarë do të thotë RISC?

RISC (Reduced Instruction Set Computer) përdor instruksione më të thjeshta që synojnë ekzekutim më të shpejtë dhe shpesh më uniform.

## Çfarë është ARM?

ARM është një arkitekturë procesori e bazuar në parimet RISC, shumë e përdorur në sisteme të mbjella dhe pajisje mobile për shkak të efikasitetit energjetik.

## Çfarë është një sistem i mbjellë (embedded system)?

Një sistem i mbjellë është kombinim harduer-softuer i projektuar për një funksion të dedikuar brenda një produkti ose sistemi më të madh.

## Jep disa shembuj të sistemeve embedded.

Shembuj janë: mikrovala, makinat larëse, printerët, switchet e rrjetit, veturat moderne dhe shumë pajisje mobile.

## Çfarë është arkitektura e Harvardit?

Arkitektura e Harvardit përdor memorie të ndara fizikisht për instruksione dhe për të dhëna.

## Cili është dallimi mes von Neumann dhe Harvard?

Në von Neumann programi dhe të dhënat ndajnë të njëjtën memorie, ndërsa në Harvard përdoren dy memorie të ndara: një për instruksione dhe një për të dhëna.

## Cili është avantazhi praktik i arkitekturës Harvard?

Procesori mund të qaset njëkohësisht në memorien e programit dhe në memorien e të dhënave, duke shmangur disa ngushtica.

## Çfarë është cloud computing?

Cloud computing është ofrimi i resurseve kompjuterike si shërbim, ku përdoruesi i konsumon resurset nga larg sipas nevojës.

## Cilat janë tre modelet kryesore të cloud computing?

SaaS, PaaS dhe IaaS.

## Çfarë është SaaS?

SaaS (Software as a Service) ofron softuer si shërbim, p.sh. Gmail.

## Çfarë është PaaS?

PaaS (Platform as a Service) ofron një platformë mbi të cilën klienti mund të zhvillojë ose ekzekutojë aplikacione.

## Çfarë është IaaS?

IaaS (Infrastructure as a Service) ofron qasje në infrastrukturë bazë si makina virtuale, ruajtje dhe sisteme operative.

## Pse shpejtësia e procesorit vetëm nuk mjafton për performancë të lartë?

Sepse performanca e sistemit varet edhe nga memoria dhe hyrje/dalja; nëse ato mbeten të ngadalta, CPU-ja duhet të presë.

## Çfarë është latenca e memories?

Latenca e memories është koha ndërmjet fillimit të një qasjeje në memorie dhe përfundimit të saj.

## Si ndihmon cache-i në performancë?

Cache-i është një memorie e vogël dhe e shpejtë ndërmjet CPU-së dhe memories kryesore që zvogëlon kohën mesatare të qasjes në të dhëna.

## Cilat janë disa teknika përshpejtuese të mikroprocesorëve?

- Pipelining
- Cache në çip
- Parashikimi i degëzimit
- Analiza e rrjedhës së të dhënave
- Ekzekutimi spekulativ

## Çfarë është pipeline?

Pipeline është teknikë që ndan ekzekutimin e instruksionit në faza të ndryshme dhe lejon mbivendosjen e disa instruksioneve në kohë.

## Cili është përfitimi kryesor i pipeline-it?

Rritja e throughput-it, pra rritja e numrit të instruksioneve të përfunduara për njësi kohe.

## A është pipeline paralelizëm i vërtetë në uniprocessor?

Jo plotësisht; në një uniprocessor pipeline rrit mbivendosjen e fazave, por nuk do të thotë se disa instruksione të plota ekzekutohen si procese të pavarura.

## Çfarë janë hazard-et në pipeline?

Hazard-et janë pengesa që e ulin efikasitetin e pipeline-it. Ato mund të jenë hazard-e të të dhënave, të kontrollit ose strukturore.

## Cilat janë tri llojet kryesore të hazard-eve?

1. Hazard-e të të dhënave
2. Hazard-e të kontrollit
3. Hazard-e strukturore

## Pse fuqia dhe nxehtësia janë sfida të mëdha në mikroprocesorët modernë?

Sepse me rritjen e frekuencës dhe të densitetit të transistorëve rritet edhe dendësia e fuqisë, gjë që e vështirëson ftohjen dhe furnizimin me energji.

## Çfarë është fuqia dinamike në çipat CMOS?

Fuqia dinamike është fuqia e konsumuar gjatë komutimit të transistorëve nga 0 në 1 dhe nga 1 në 0.

## Si ndikon ulja e frekuencës së klokut në fuqi?

Ulja e frekuencës së klokut e redukton drejtpërdrejt fuqinë e konsumuar.

## Çfarë është DVFS?

DVFS (Dynamic Voltage-Frequency Scaling) është teknikë ku procesori ul ose rrit tensionin dhe frekuencën sipas ngarkesës për të kursyer energji.

## Çfarë nënkupton 'Do nothing well'?

Është ideja që modulet joaktive të procesorit të kenë klok të shkyçur ose aktivitet minimal për të kursyer energji.

## Çfarë është overclocking?

Overclocking është rritja e përkohshme ose e qëllimshme e frekuencës së procesorit mbi normën standarde për të marrë performancë më të lartë, me koston e rritjes së nxehtësisë dhe fuqisë.

## Çfarë janë procesorët me shumë bërthama?

Janë procesorë që përmbajnë disa bërthama përpunuese në të njëjtin çip, duke mundësuar paralelizëm më të madh.

## A rritet performanca gjithmonë proporcionalisht me numrin e bërthamave?

Jo. Përfitimi varet nga sa pjesë e programit mund të paralelizohet dhe nga kufizimet e memories, sinkronizimit dhe pjesëve serike.

## Si përkufizohet një kompjuter 'më i shpejtë' se një tjetër?

Kompjuteri X është më i shpejtë se Y nëse koha e ekzekutimit për të njëjtin task është më e vogël te X.

## Si lidhet performanca me kohën e ekzekutimit?

Performanca është në raport të zhdrejtë me kohën e ekzekutimit: sa më e vogël koha, aq më e lartë performanca.

## Cila është formula bazë e speedup-it?

$$Speedup = \frac{T_{vjetër}}{T_{ri}}$$

## Çfarë është koha e CPU-së?

Koha e CPU-së është koha ndërmjet fillimit dhe përfundimit të ekzekutimit të një programi nga procesori.

## Cila është formula bazë e kohës së CPU-së?

$$T_{CPU} = IC \cdot CPI \cdot T_{clk} = \frac{IC \cdot CPI}{f_{clk}}$$

## Çfarë është IC?

IC (Instruction Count) është numri i instruksioneve të ekzekutuara për një program.

## Çfarë është CPI?

CPI (Clock Cycles Per Instruction) është numri mesatar i cikleve të klokut për instruksion.
$$CPI = \frac{\text{numri i cikleve të klokut}}{\text{numri i instruksioneve}}$$

## Çfarë është frekuenca e klokut?

Frekuenca e klokut tregon sa cikle ndodhin për sekondë dhe është reciproke e kohës së ciklit.

## Si lidhen frekuenca dhe koha e ciklit?

$$f = \frac{1}{T_{clk}}$$

## Çfarë është MIPS?

MIPS (Millions of Instructions Per Second) tregon sa miliona instruksione ekzekutohen për sekondë.
$$MIPS = \frac{IC}{T_{CPU}\cdot 10^6} = \frac{f_{clk}}{CPI \cdot 10^6}$$

## Pse MIPS nuk është gjithmonë metrikë e mjaftueshme?

Sepse jo çdo instruksion bën të njëjtën sasi pune; dy procesorë mund të kenë MIPS të ndryshëm, por të kryejnë punë reale ndryshe.

## Nga cilët faktorë varet koha e CPU-së?

Koha e CPU-së varet nga:
1. IC
2. CPI
3. Koha e ciklit / frekuenca e klokut

## Nga çfarë përcaktohet IC?

IC përcaktohet nga programi, ISA-ja dhe teknologjia e kompajlerit.

## Nga çfarë përcaktohet CPI?

CPI përcaktohet kryesisht nga hardueri dhe organizimi i CPU-së.

## Nga çfarë përcaktohet koha e ciklit?

Koha e ciklit përcaktohet nga teknologjia e harduerit dhe organizimi i sistemit.

## Çfarë është ligji i Amdahl-it?

Ligji i Amdahl-it përdoret për të gjetur përmirësimin maksimal të mundshëm kur vetëm një pjesë e sistemit ose programit përmirësohet.

## Çfarë tregon speedup-i në kontekstin e ligjit të Amdahl-it?

Tregon sa më shpejt ekzekutohet një task pas përmirësimit krahasuar me sistemin origjinal.

## Si shprehet speedup-i paralel sipas Amdahl-it?

$$S(N) = \frac{1}{(1-P) + \frac{P}{N}}$$
ku $P$ është pjesa e paralelizueshme, ndërsa $(1-P)$ pjesa serike.

## Cili është mesazhi kryesor i ligjit të Amdahl-it?

Edhe nëse shton shumë procesorë ose bërthama, pjesa serike e programit vendos kufirin teorik të speedup-it.

## Çfarë ndodh nëse P është e vogël në ligjin e Amdahl-it?

Nëse pjesa e paralelizueshme $P$ është e vogël, përdorimi i shumë procesorëve jep përfitim të kufizuar.

## Çfarë ndodh kur N shkon drejt infinitit në ligjin e Amdahl-it?

Speedup-i maksimal kufizohet me:
$$S_{max} = \frac{1}{1-P}$$

## Pse multicore dhe Amdahl lidhen fort mes vete?

Sepse multicore ofron paralelizëm harduerik, ndërsa ligji i Amdahl-it tregon kufirin teorik të përfitimit real nga ai paralelizëm.
