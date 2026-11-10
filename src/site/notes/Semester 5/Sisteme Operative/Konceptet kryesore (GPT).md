---
{"dg-publish":true,"permalink":"/semester-5/sisteme-operative/konceptet-kryesore-gpt/","tags":["universitet","semestri-5","sisteme-operative","perseritje"],"dg-note-properties":{"tags":["universitet","semestri-5","sisteme-operative","perseritje"]}}
---

# Sisteme Operative — konceptet kryesore

Përmbledhje për përsëritje nga [[Semester 5/Sisteme Operative/Notes (GPT)\|Notes (GPT)]] dhe [[Provimet - pyetje dhe mbulimi\|Provimet - pyetje dhe mbulimi]]. Lexo idetë, pastaj provo t'i shpjegosh shembujt pa e parë përgjigjen.

## Çfarë bën sistemi operativ?

Sistemi operativ menaxhon **CPU-në, memorien, fajllat dhe pajisjet**. **Kernel-i** është pjesa me privilegje të plota. Programet e zakonshme punojnë në *user mode*; kur u duhet një shërbim i kernel-it, bëjnë një **system call**. **API-ja** është ndërfaqja që përdor programuesi, shpesh përmes një biblioteke.

**Interrupt** e njofton CPU-në për një ngjarje, si përfundimi i I/O-së. **Multiprogramimi** mban disa programe gati që CPU-ja të mos rrijë pa punë; **ndarja e kohës** u jep proceseve intervale të shkurtra për përgjigje të shpejtë.

## Procesi dhe gjendjet e tij

**Programi** është kod i ruajtur në disk; **procesi** është programi gjatë ekzekutimit, me PID, memorie dhe burime të veta. Sistemi operativ mban të dhënat e tij në **PCB** (Process Control Block): gjendjen, regjistrat, numëruesin e programit, prioritetin, informacionin e memories dhe të I/O-së.

Rrjedha bazë: `new → ready → running → terminated`. Nga `running`, procesi mund të kalojë në `waiting/blocked` kur pret I/O ose një ngjarje, ose të kthehet në `ready` kur i merret CPU-ja. Pas përfundimit të ngjarjes, kalon `waiting → ready`; në modelin bazë nuk kalon drejtpërdrejt në `running`.

- **Ready:** pret vetëm CPU-në.
- **Waiting/blocked:** pret një ngjarje ose burim para se të mund të konkurrojë për CPU.

## Tre skeduluesit dhe dispeçeri

| Roli | Çfarë bën | Sa shpesh |
| --- | --- | --- |
| **Afatgjatë (job scheduler)** | Pranon punë nga disku në sistem; ndikon shkallën e multiprogramimit. | Më rrallë |
| **Afatmesëm (swapper)** | Pezullon procese, i zhvendos përkohësisht nga RAM-i dhe i rikthen. | Sipas nevojës |
| **Afatshkurtër (CPU scheduler)** | Zgjedh procesin e radhës nga radha `ready`. | Shumë shpesh |

**Skeduluesi zgjedh; dispeçeri e kalon CPU-në te procesi i zgjedhur.** Dispeçeri kryen ndërrimin e kontekstit, kalimin në mënyrën e përdoruesit dhe vazhdimin te instruksioni i ruajtur. **Context switch** ruan gjendjen e procesit aktual dhe rikthen atë të procesit tjetër; kjo merr kohë pa kryer punë të aplikacionit. **Dispatch latency** është koha e këtij kalimi deri sa procesi i ri nis ekzekutimin.

## `fork`, `exec`, `wait`: prindi dhe fëmija

- **`fork()`** krijon fëmijë. Pas suksesit, të dy proceset vazhdojnë nga rreshti pas thirrjes: prindi merr PID-in e fëmijës, fëmija merr `0`; `-1` tregon dështim.
- **`exec()`** zëvendëson programin brenda procesit thirrës. Nuk krijon proces të ri dhe, nëse ka sukses, nuk kthehet te kodi i vjetër.
- **`wait()` / `waitpid()`** lejon prindin të presë fëmijën dhe të marrë statusin e përfundimit.

Për detyrat e kodit, vizato pemën e proceseve dhe ndiq kushtet `pid == 0`, `pid > 0`, `pid < 0` rresht për rresht. Dy thirrje të njëpasnjëshme, pa kushte, të `fork()` krijojnë **4 procese gjithsej** nëse të gjitha kanë sukses; për `n` thirrje të tilla janë `2ⁿ` procese. Rendi i shtypjeve nga proceset nuk garantohet.

### Zombie kundrejt orphan

| | Zombie | Orphan (proces jetim) |
| --- | --- | --- |
| **Çfarë ka ndodhur?** | Fëmija ka përfunduar, por prindi ende nuk ia ka marrë statusin. | Prindi ka përfunduar, ndërsa fëmija ende jeton. |
| **A ekzekutohet?** | Jo; mbetet vetëm hyrja e statusit në tabelën e proceseve. | Mund të vazhdojë ekzekutimin. |
| **Çfarë ndodh më pas?** | Prindi përdor `wait()`/`waitpid()` për ta mbledhur statusin. | Në Linux adoptohet nga një proces kujdestar, zakonisht `init`/`systemd` ose një subreaper. |

**Mbaje mend:** zombie = *fëmija vdiq i pari*; orphan = *prindi vdiq i pari*.

## Komunikimi ndërmjet proceseve (IPC)

- **Shared memory:** proceset lexojnë/shkruajnë në një zonë të përbashkët. Mund të jetë e shpejtë, por kërkon sinkronizim për të shmangur *race conditions*.
- **Message passing:** proceset përdorin `send`/`receive`; nuk kërkohet hapësirë e përbashkët adresash. Mesazhet mund të kalojnë drejtpërdrejt ose përmes një *mailbox*.
- **Pipe anonim:** zakonisht komunikim njëdrejtimësh mes proceseve të lidhura. `pipe(fd)` jep `fd[0]` për lexim dhe `fd[1]` për shkrim; krijoje para `fork()` dhe mbyll skajet e papërdorura.
- **Socket:** pikë fundore për komunikim lokal ose në rrjet. **RPC:** thirrje procedure në makinë tjetër përmes një ndërfaqeje të ngjashme me funksionin lokal.

## Dallime të tjera që dalin shpesh

- **Bërthamë monolitike / mikrobërthamë:** e para mban shumë shërbime në hapësirën e kernelit; e dyta mban funksionet minimale aty dhe i kalon shërbimet e tjera në procese përdoruesi.
- **Proces / thread:** procesi ka hapësirën e vet të adresave; thread-et brenda tij ndajnë memorien dhe burimet, por secili ka stekun dhe gjendjen e vet të ekzekutimit.
- **RAM / disk:** RAM-i është i shpejtë dhe humbet përmbajtjen pa energji; disku/SSD-ja ruan të dhënat. **Cache** mban kopje të të dhënave të përdorura shpesh në memorie më të shpejtë.

## Komandat Linux që duhen njohur

| Komanda | Kuptimi |
| --- | --- |
| `pwd`, `cd folder/`, `ls -l` | Shfaq vendndodhjen; ndrysho folderin; listo fajllat me hollësi. |
| `mkdir emri`, `rm file`, `rm -r folder/` | Krijo folder; fshi fajll; fshi folder dhe përmbajtjen. |
| `cat file`, `grep "tekst" file`, `man komanda` | Shfaq fajllin; kërko tekst; hap manualin. |
| `echo "tekst" > file`, `echo "tekst" >> file` | Shkruaj duke zëvendësuar përmbajtjen; shto tekst në fund. |
| `cp a b`, `cmp a b` | Kopjo fajll; krahaso dy fajlla (`cmp` hesht kur janë identikë). |
| `ps -f`, `ps -ef --forest` | Shfaq procese me PID/PPID; shfaq pemën e proceseve. |
| `history`, `uptime`, `sort file \| uniq` | Historia e komandave; koha e punës/ngarkesa; largimi i rreshtave të përsëritur fqinjë. |
| `whoami`, `sudo komanda` | Shfaq përdoruesin; ekzekuto me privilegje të ngritura. |
| `gcc -Wall -Wextra kod.c -o program`, `./program` | Kompajlo kodin C; ekzekuto programin në folderin aktual. |

`./` duhet sepse folderi aktual zakonisht nuk është në `PATH`. Te `ps`, **PID** identifikon procesin dhe **PPID** prindin e tij; gjendja `Z` tregon zombie. `sudo` mund të krijojë fajlla në pronësi të `root`.

### Lejet e fajllave: `4 + 2 + 1`

Lejet ndahen në **pronari | grupi | të tjerët**. Në secilin grup, **`r = 4`** (lexim), **`w = 2`** (shkrim), **`x = 1`** (ekzekutim). Mblidh vlerat për secilin grup dhe shkruaji si tre shifra.

| Numri | Mbledhja | Lejet |
| --- | --- | --- |
| `7` | `4 + 2 + 1` | `rwx` |
| `6` | `4 + 2` | `rw-` |
| `5` | `4 + 1` | `r-x` |
| `4` | `4` | `r--` |
| `0` | `0` | `---` |

- **`chmod 600 file` → `rw- | --- | ---`:** vetëm pronari lexon dhe shkruan.
- **`chmod 644 file` → `rw- | r-- | r--`:** pronari shkruan; grupi dhe të tjerët vetëm lexojnë.
- **`chmod 755 program` → `rwx | r-x | r-x`:** pronari bën gjithçka; të tjerët lexojnë dhe ekzekutojnë.

Te `ls -l`, karakteri i parë është lloji (`-` fajll, `d` folder); pastaj vijnë nëntë karakteret e lejeve. Shembull: `-rw-r--r--` = fajll i zakonshëm me leje `644`.

## Formula dhe terma për detyrat

- **Skedulimi i CPU-së:** `turnaround = completion − arrival`; `waiting = turnaround − burst`. Te **FCFS** shkon i pari ai që ka ardhur i pari; te **SJF** zgjidhet puna më e shkurtër; te **Round Robin** secili merr një kuant kohe dhe, nëse nuk përfundon, kthehet në radhë.
- **Race condition:** rezultati ndryshon sipas rendit në të cilin proceset ose thread-et prekin të dhënat e përbashkëta. **Mutex** dhe **semafori** përdoren për sinkronizim.
- **Deadlock:** procese që presin burimet e mbajtura nga njëri-tjetri dhe nuk ecin përpara. Katër kushtet e nevojshme janë përjashtimi i ndërsjellë, mbaj-dhe-prit, mungesa e marrjes me forcë dhe pritja rrethore.
- **Paging:** memoria ndahet në faqe dhe korniza; mungesa e faqes në RAM shkakton *page fault*. Shumë zhvendosje faqesh me pak punë të dobishme quhen *thrashing*.

## Për provimin final: tema shtesë

[[Provimet - pyetje dhe mbulimi\|Provimet - pyetje dhe mbulimi]] tregon se fotot e provimeve kërkojnë edhe **threads/Pthreads, algoritmet e skedulimit, sinkronizim, deadlock dhe memorie virtuale**. Këtu janë vetëm përkujtesa të shkurtra; [[Semester 5/Sisteme Operative/Notes (GPT)\|Notes (GPT)]] i mbulon këto pjesërisht ose aspak, prandaj për finalin duhen edhe materiale të mëvonshme.
