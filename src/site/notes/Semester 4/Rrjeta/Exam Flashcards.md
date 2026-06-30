---
{"dg-publish":true,"permalink":"/semester-4/rrjeta/exam-flashcards/","tags":["university/rrjeta","anki","exams"]}
---


# Exam Flashcards

> [!info] Anki import
> Import **`Exam Flashcards.apkg`**. It includes the cards and all exam-question images. This Markdown file is the readable Obsidian version.

- Cards: **268**
- Cards with source images: **103**
- Duplicate/near-identical exam occurrences are grouped when the normalized question text is the same; all sources are listed on the card.

## EX-001

### Front

Qka eshte Interneti? Përshkruani me fjalë të juaja si funksionon? Prej çka përbehet?

### Back

Interneti eshte rrjet i rrjeteve. Interneti paraqet bashkesine e kompjutereve, servereve,
aplikacioneve, routereve dhe linjave per komunikim. Te gjitha pajisjet e lidhura ne internet
njihen si hosta apo sisteme fundore te cilat lidhen mes veti permes linjave komunikuese dhe
packet switches.

### Sources

- Afate me zgjidhje 2.pdf Q1

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-002

### Front

Cilat jane klasat e IP adresave dhe rangu i tyre?

### Back

Klasat klasike IPv4: A `1.0.0.0-126.255.255.255`, B `128.0.0.0-191.255.255.255`, C `192.0.0.0-223.255.255.255`, D `224.0.0.0-239.255.255.255` multicast, E `240.0.0.0-255.255.255.255` rezervë/eksperimentale. `127.0.0.0/8` është loopback.

### Sources

- Afate me zgjidhje 2.pdf Q2

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-003

### Front

Ne qka bazohet funksionimi themelor i internetit ?

### Back

Funksionimi themelor i internetit bazohet ne Packet Switching Network.

### Sources

- Afate me zgjidhje 2.pdf Q3

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-004

### Front

Qka jane aplikacionet hybrid dhe permendni nje shembull?

### Back

Aplikacionet hybrid jane edhe aplikacione klient/server edhe aplikacione P2P(Peer-To-Peer).
Shembuj te aplikacionit hybrid eshte Microsoft Messenger, Telnet etj.

### Sources

- Afate me zgjidhje 2.pdf Q4

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-005

### Front

Qka jane “Socekts” dhe per qka perdoren?

### Back

Sockets perdoren per komunikim te proceseve ne rrjete. Nje proces dergon dhe pranon te
dhena ne rrjeta permes interface-ave te quajtur sockets. Pra paraqet interface-in ne mes
application dhe transport layer brenda nje hosti.

### Sources

- Afate me zgjidhje 2.pdf Q5

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-006

### Front

Qka jane “cookies” ?

### Back

“Cookies” jane metode per identifikimin e shfrytezuesve. Cookies jane te dhena te vogla qe
dergohen prej nje web sajti dhe ruhen ne shfletuesin e shfrytezuesit, te cilat e lejojne nje sajt me i
mbajt ne mend te dhenat e atij shfrytezuesi.

### Sources

- Afate me zgjidhje 2.pdf Q6

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-007

### Front

Qka eshte DNS? Qka do te ndodhte ne intenet nese nuk do te ekzistonte DNS?

### Back

.DNS-i(Domain Name System) eshte nje sherbim ne internet i cili eshte pergjegjes per
konvertimin e emrit te web sajtit ne IP adrese. Nese DNS nuk do te ekzistonte atehere do te
duhej qe nje web sajti ti qasemi me IP adresen e tij perkatese.

### Sources

- Afate me zgjidhje 2.pdf Q7

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-008

### Front

Qka eshte VPN?

### Back

VPN(Virtual Private Network) eshte nje rrjete virtuale nepermjet nje rrjete tjeter, sic eshte
interneti.

### Sources

- Afate me zgjidhje 2.pdf Q8

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-009

### Front

Cilat janë dallimet në mes të TCP dhe UDP protokollit?

### Back

TCP protokoli eshte “Reliable Transport Service”, pra ofron siguri te transmetimit te te
dhenave permes implementimit te three-way handshake, si dhe siguron qe te dhenat do te arrijne
ne destinacionin e duhur. TCP protokilli ofron nje abstraksion te nje stream te bajtave ku mund
te shkruhen dhe te lexohen te dhenat.
Ndersa UDP protokoli eshte “Unreliable Transport Service”, pra nuk ofron siguri te transmetimit
te te dhenave si dhe nuk siguron qe te dhenat do te arrine me sukses ne destinacionin e duhur.

### Sources

- Afate me zgjidhje 2.pdf Q9

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-010

### Front

Qka eshte SSID te rrjetat Wireless?

### Back

SSID eshte shprehje qe perdoret kur konfigurojme WLAN. SSID eshte nje numer unik 32
karakteresh qe perdoret per emerimin e wireless networks. Kur shume wireless networks gjinden
ne te njejtin lokacion, SSID-at sigurohen qe te dhenat te arrijne ne destiancionin e duhur. Pa
SSID, dergimi dhe pranimi i paketave ne nje lokacion me shume rrjeta wireless do te ishte i
paparashikueshem.

### Sources

- Afate me zgjidhje 2.pdf Q10

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-011

### Front

Shkruani nje IP adrese private?

### Back

192.168.1.1
IP adresat private kane rangjet e me poshtme:
10.0.0.0 - 10.255.255.255
172.16.0.0 - 172.31.255.255
192.168.0.0 - 192.168.255.255

### Sources

- Afate me zgjidhje 2.pdf Q11

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-012

### Front

Qka percakton TTL ne IP datagramin dhe qka ndodhe me TTL gjate IP packet
forwarding?

### Back

Ne IP datagram, TTL percakton numrin maksimal te routereve/switcheve qe paketa e
shenimeve mund ti pershkoj. Gjatë kohës së udhëtimit të paketës (IP packet forwarding) nepër
rutera, TTL ndryshohet.

### Sources

- Afate me zgjidhje 2.pdf Q12

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-013

### Front

Qka eshte DHCP?

### Back

Sherbimi ne Internet i cili eshte pergjgjes per dhenien automatike te IP adresave pajisjeve
kompjuterike eshte DHCP.

### Sources

- Afate me zgjidhje 2.pdf Q13

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-014

### Front

Sa biteshe eshte MAC adresa e karteles se rrjetes?

### Back

MAC adresa e kartelës se rrjetës është 48 biteshe.

### Sources

- Afate me zgjidhje 2.pdf Q14

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-015

### Front

Përshkruani llojet e vonesave të paketave të shënimeve?

![assets/exam-flashcards/2019qershor-p04-q20.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p04-q20.png)

### Back

Dallojm keto lloje te vonesave te paketave : processing delay, queuing delay, transmission
delay dhe propagation delay.
Processing delay-koha e nevojshme per ekzaminimin e header-it te paketes dhe percaktimin se
ku te drejtohet paketa.
Queuing delay-koha qe paketa pret per tu vendosur ne lidhje(link).
Transmission delay-koha e nevojshme per vendosjen e te gjitha paketave në lidhje.
Propagation delay-koha e nevojshme per te kaluar paketa nga fillimi i lidhjes deri tek routeri
ardhshem.

### Sources

- Afate me zgjidhje 2.pdf Q15
- 2019Qershor.pdf Q20 p.4

Tags: rrjeta exam solved_bank exam_form source::afate_me_zgjidhje_2 source::2019qershor

## EX-016

### Front

Përshkruani se si punon “Trace route” programi?

![assets/exam-flashcards/afati-shkurt-2023-p02-q08.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p02-q08.png)

### Back

Programi trace route dergon shume paketa te vecanta nga hosti burimor drejt nje hostname
destinues. Duke kaluar rruges drejte destinacionit, paketat kalojn neper nje numer te router-ve.
Kur nje router pranon nje nga keto paketa te vecanta, ai dergon tek burimi nje mesazh te shkurte
qe permban emrin dhe adresen e routerit. Hosti i burimit te paketave regjistron kohen qe kalon
nga fillimi i dergimit te paketave e deri te pranimi i mesazheve perkatese si dhe regjistron emrin
dhe adresen e routerit qe kthen mesazhin. Ne kete form hosti burimor mund te konstruktoj rrugen
e paketave nga burimi tek destinacioni, dhe vonesat e tyre.

### Sources

- Afate me zgjidhje 2.pdf Q16
- Afate me zgjidhje 1.pdf Q75
- Afati shkurt 2023.pdf Q8 p.2
- download. (5).pdf Q8 p.2
- 2019Qershor.pdf Q5 p.1
- 2019Shtatore.pdf Q5 p.1
- 2023Janar.pdf Q8 p.2

Tags: rrjeta exam solved_bank exam_form source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1 source::afati_shkurt_2023 source::download_5 source::2019qershor source::2019shtatore source::2023janar

## EX-017

### Front

Ku ekzekutohen aplikacionet ne Internet?

### Back

Aplikcaionet ne Internet ekzekutohen ne pajisje fundore(end systems).

### Sources

- Afate me zgjidhje 2.pdf Q17

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-018

### Front

Sa kohe nevojitet për të dërguar një fajll nga hosti A deri ne hostin B me madhësi 640k bita,
nëpër rrjetën TDM që ka 24 slote dhe ka “bandwidth” 1536 kbps. Le të supozojmë se 1 sekond
nevojitet për të krijuar lidhjen nga hosti A deri ne hostin B :

### Back

1536kbps/24=64kbps, 640kb/64kbps=10 sekonda, 10 sekonda+1 sekonde(vonesa)=11
sekonda.

### Sources

- Afate me zgjidhje 2.pdf Q18

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-019

### Front

Çka është protokolli (në kuptim të rrjetave kompjuterike)?

### Back

Protkolli definon formatin dhe radhitjen e te dhenave te shkembyera mes dy apo me shume
pajisjeve komunikuese, si dhe definon veprimet e ndermarra ne transmetimin dhe pranimin e
atyre te dhenave.

### Sources

- Afate me zgjidhje 2.pdf Q19

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-020

### Front

Renditni shtate(7) shtresat e ISO modelit?

### Back

Application, Presentation, Session, Transport, Network, Link, Physical.

### Sources

- Afate me zgjidhje 2.pdf Q20

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-021

### Front

Cilat janë pesë shtresat e protokollit të Internetit, prej lartë poshtë (vizato skicën) dhe si
quhet paketa e proceduar në atë shtresë?

### Back

Pese(5) shtresat e protokollit te Internetit prej larte poshte jane: Application, Transport,
Network, Data-Link dhe Physical.
Paketat ne shtresat perkatese quhen:
Application(pakete), Transport(segment), Network(datagram), Data-Link(frame), Physical(bits).

### Sources

- Afate me zgjidhje 2.pdf Q21

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-022

### Front

Qfare lloji IP adrese eshte 127.168.1.1? Qfare lloji IP adrese eshte 127.0.0.1? Pse?

### Back

Keto IP adrese ben pjese ne rangun e IP adresave “loopback address” qe sherbejne vetem per
testim te protokollit TCP/IP.

### Sources

- Afate me zgjidhje 2.pdf Q22

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-023

### Front

Nje DNS “resource record”(Name, Value, Type, TTL) eshte i tipit A(pra Type=A). Qka
permban atehere “Value”?

### Back

Një DNS resource record ka formatin `(Name, Value, Type, TTL)`. Kuptimi i `Value` varet nga `Type`: A -> IP address; NS -> authoritative DNS server; CNAME -> canonical name; MX -> mail server.

### Sources

- Afate me zgjidhje 2.pdf Q23

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-024

### Front

Ku është i implementuar “Link Layer”?

### Back

Eshte i implementuar ne software si driver per NIC(Network Interface Card).

### Sources

- Afate me zgjidhje 2.pdf Q24

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-025

### Front

Përshkruani dy teknikat themelore FDM dhe TDM lidhur me transmetimin e
shënimeve ne rrjete; ngjashmëritë dhe dallimet?

### Back

TDM (Time Division Multiplexing) dhe FDM (Frequency Division Multiplexing) jane dy
metoda te multipleximit te shume sinjaleve ne nje bartes te vetem. Dallimi mes FDM dhe TDM
qendron ne menyren se si e ndajne kanalin. FDM e ndan kanalin ne dy apo me shume rangje te
frekuencave qe nuk mbivendosen, perderisa TDM ndan periudha te caktuara kohore tek secili
kanal. Nga ky fakt mund te themi per TDM qe secili kanal perdor te gjithe bandwithin brenda nje
kohe te caktuar, ndersa per FDM secili kanal perdor nje pjese te caktuar te bandwithit gjate gjithe
kohes.TDM ofron me shume fleksibilitet, mirepo permes FDM te dhenat arrijne me shpejte ne
destinacion.

### Sources

- Afate me zgjidhje 2.pdf Q25

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-026

### Front

Për çka përdoret protokolli ARP? Si punon?

### Back

ARP protokolli sherben per perkthimin e IP adresave ne MAC adresa. Kur deshrojm te bejme
ping nje IP adrese ne rrjeten lokale, atehere sistemi duhet ta ktheje IP adresen ne MAC adrese.
Kjo perfshin perdorimin e ARP-se per gjetjen e MAC adresave. Sistemi mban nje ARP tabele ku
jane te ruajtura IP adresat dhe MAC adresat perkatese. Kur deshirojm te dergojm nje pakete tek
nje IP adrese, sistemi se pari konsultohet me ARP tabelen nese ekziston nje MAC adrese per ate
IP adrese. Nese ekziston, ARP protkolli nuk perdoret. Nese nuk ekziston atehere dergohet nje
broadcast packet(255.255.255.255) ne rrjete permes ARP protokolit qe pyet se kush e ka IP
adresen perkatese. Pajisja me IP adresen perkatese me pas kthen nje ARP pakete duke perfshire
MAC adresen e pajisjes.

### Sources

- Afate me zgjidhje 2.pdf Q26

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-027

### Front

Pershkruani se si punon “NAT”-i, per çka perdoret, si?

### Back

NAT lejon shumë hostë me IP private të përdorin një IP publike. Router-i NAT zëvendëson source private IP/port me public IP/port kur paketa del në Internet dhe ruan mapping në NAT table. Kur kthehet përgjigjja, router-i përdor portin publik për ta gjetur hostin privat dhe e rikthen destination IP/port. Portet janë çelësi që dallon lidhjet e shumë hostëve pas të njëjtës IP publike.

### Sources

- Afate me zgjidhje 2.pdf Q27

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-028

### Front

Qka duhet te dijne dy procese qe te komunikojne ne rrjete?

### Back

Që dy procese të komunikojnë në rrjete ato duhet të dine: IP adresat dhe numrat e porteve.

### Sources

- Afate me zgjidhje 2.pdf Q28

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-029

### Front

Çka është dallimi në mes të “persistent” dhe “non-persistent” HTTP lidhjes?

### Back

Lidhjet persistent nenkupton qe gjate komunikimit klient-sever permes nje lidhje TCP, te
gjitha kerkesat dhe pergjigjet koresponduese dergohen permes te njejtes lidhje TCP.
Ndersa lidhja non-persistent nenkupton qe gjate komunikimit klient-server permes nje lidhje
TCP, cdo cift kerkese/pergjigje transmetohet permes nje lidhje TCP te vecant.

### Sources

- Afate me zgjidhje 2.pdf Q29

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-030

### Front

Çka është “Proxy serveri”?

### Back

Proxy server eshte server qe sillet si ndermjetsues i kerkesave te klientve per informacione
apo sherbime nga servere tjere. Pra Proxy serveri i ploteson kerkesat e klienteve ne vend te
serverit origjinal. Proxy serevri eshte server dhe klient ne te njejten kohe.

### Sources

- Afate me zgjidhje 2.pdf Q30

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-031

### Front

Nëse supozojmë se dprop është me e madhe se dtrans në kohen t = dtrans, ku është biti i pare
i paketës?

### Back

Biti i pare i paketes eshte rruges per tek routeri tjeter.

### Sources

- Afate me zgjidhje 2.pdf Q31

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-032

### Front

Nëse supozojmë se dprop është me e vogël se dtrans në kohen t = dtrans, ku është biti i pare i
paketës?

### Back

Ka mberritur tek tjetri ruter(destinacion).

### Sources

- Afate me zgjidhje 2.pdf Q32

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-033

### Front

Çka përshkruan standardi IEEE 802.11?

### Back

802.11 standardi pershkruan specifikacionet mbi te cilat implementohet WLAN(Wireless
Local Area Network). Ky standard specifikon lidhjet e pajisjeve ne rrjetat pa tela.

### Sources

- Afate me zgjidhje 2.pdf Q33

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-034

### Front

Ne TCP sekuencën si ne figurë e (rrumbullakuar) pse ACK ka vlerën 43 (jo 42, 41, ose jo 44,
45 etj)?

### Back

ACK ka vleren 43 tek segmenti i derguar nga Hosti B tek Hosti A sepse e dijm qe
acknowledgment number eshte sequence number i bajtave te ardhshem qe pret hosti, keshtu
Hosti B deshiron ti tregoj hostit A se deri tani ka pranuar te gjithe byte-t deri tek byte 42 dhe tani
eshte duke pritur per 43 bajtat e tutje.

### Sources

- Afate me zgjidhje 2.pdf Q34
- Afate me zgjidhje 1.pdf Q57

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-035

### Front

Këngën me gjatësi 4 minuta (me madhësi 4 MByte) e ngarkoni (upload) përmes lidhjes
1Mbps te Internetit. Sa kohe ju nevojitet për te ngarkuar (upload-our) këtë këngë, nëse linja ka
kapacitetit te shkarkimit (download) prej 744Kbps?

### Back

4 Mbyte = 4 * 8 Mbit = 32 Mbit. 1 Mbps = 1000 Kbps. Shkarkim = 744 Kbps =>
Ngarkim = 1000 Kbps – 744 Kbps = 256 Kbps. Tash kemi: 32 Mbit / 256 Kbps = 32 * 10^6 s /
256 * 10^3 = 32000 s / 256 = 125 sekonda.

### Sources

- Afate me zgjidhje 2.pdf Q35

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-036

### Front

Vizatojeni IPv4 datagram formatin? Ku eshte ketu MAC adresa? Sa eshte “overhead”-i ndaj
shtreses se TCP-se?

### Back

IP datagrami nuk permban MAC adrese. Nese datagrami permban nje TCP segment, atehere
secili datagram ka 40 bajta te headerit(20 bajta te IP headerit dhe 20 bajta te TCP headerit).

### Sources

- Afate me zgjidhje 2.pdf Q37

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-037

### Front

Nëse aplikacioni gjeneron paketa 40 bajtëshe të shënimeve çdo 20 msec dhe secila paket
enkapsulohet në TCP segment dhe pastaj në IP datagram, sa % e shënimeve janë overhead dhe sa
% janë shënime të aplikacionit?

### Back

50% overhead, 50% shenime.

### Sources

- Afate me zgjidhje 2.pdf Q38

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-038

### Front

Cili eshte dallimi ne mes te SMTP protokollit dhe POP3?

### Back

SMTP protokolli transferon te dhenat nga mail serveri i derguesit tek mail serveri i pranuesit.
Ndersa POP3 sherben per marrjen e emailave nga mail serveri ne pajisjen lokale(PC).

### Sources

- Afate me zgjidhje 2.pdf Q39

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-039

### Front

Cili eshte dallimi ne mes te IMAP dhe POP3?

### Back

Dallimi kryesor mes tyre eshte se POP3 i shkarkon emailat ne pajisjen tone(kompjuter) dhe
zakonisht i fshin email-at nga remote server ndersa IMAP lejojne perdoruesit ti ruajn email-at e
tyre edhe ne remote server.

### Sources

- Afate me zgjidhje 2.pdf Q40

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-040

### Front

Si mund ta dijmë IP adresën e ueb faqes www.uni-pr.edu ?

### Back

Hapim command prompt dhe shenojm “tracert www.uni-pr.edu” dhe IP adresa eshte ajo qe
shfaqet pas “tracing route to(website)(ip adresa)”.

### Sources

- Afate me zgjidhje 2.pdf Q41

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-041

### Front

Si ndodh “Congestions” ne rrjeta kompjuetrike?

### Back

Congestion ndodh zakonisht kur trafiku ne hyrje te nyjes(routerit) e tejkalon bandwithin
dales, pra vijn me shum paketa sesa qe mund te procesohen dhe keshtu ato krijojn queue ne
bufferin dales te routerit para se te transmetohen dhe disa prej tyre edhe behen drop ne rast te
zenies se tere bufferit.

### Sources

- Afate me zgjidhje 2.pdf Q42

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-042

### Front

Cilet jane komponentët e arkitekturës së rrjetave celulare(GSM 2G) :

### Back

Base transceiver station(BTS), Base station controller(BSC), Mobile switching
center(MSC),Base station system(BSS), Mobile subscribers.

### Sources

- Afate me zgjidhje 2.pdf Q43

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-043

### Front

Çka është CSMA/CD protokolli?

### Back

CSMA/CD eshte nje media access protokoll qe perdoret ne LAN dhe paraqet nje grup
rregullash qe percaktojne se si pajisjet e rrjetes reagojne kur dy pajisje tentojne te perdorin nje
kanal transmetues te njejte te te dhenave ne te njejten kohe(qe nihet si collision).

### Sources

- Afate me zgjidhje 2.pdf Q44

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-044

### Front

Shënoni dy mënyra se si e përcaktoni se çfarë IP adresa ka kompjuteri juaj (sistemi operativ
është Windows)?

### Back

1) Ne Run e hapim command prompt-in, pastaj shenojme ipconfig dhe IPv4 eshte IP adresa e
kompjuterit tone.
2) Ne web browser shenojme: What’s my IP address?

### Sources

- Afate me zgjidhje 2.pdf Q45

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-045

### Front

Si e përcaktoni se rrugëtimin paketave neper rrjeta kompjuterike nëse i qasemi serverit www.uni-
pr.edu (sistemi operativ është Windows)?

![assets/exam-flashcards/2019shtatore-p03-q11.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019shtatore-p03-q11.png)

### Back

Pergjigjja e njejte si ne pytjen 41), po nuk eshte e sigurte.

### Sources

- Afate me zgjidhje 2.pdf Q45
- 2019Shtatore.pdf Q11 p.3

Tags: rrjeta exam solved_bank exam_form source::afate_me_zgjidhje_2 source::2019shtatore

## EX-046

### Front

Shenoni disa(te pakten dy) protokolle per qasje ne email(Mail Access Protocol)

### Back

Protokollet per qasje ne email jane: POP3, SMTP, IMAP dhe HTTP.

### Sources

- Afate me zgjidhje 2.pdf Q46
- Afate me zgjidhje 1.pdf Q22

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-047

### Front

Çka eshë dallimi ne mes “stop-and-wait” dhe “pipeline” protokollit?

### Back

Sipas stop-and-wait protokolit, pas dergimit te cdo pakete, derguesi duhet te ndaloj dhe te
pret per reagim nga pranuesi(acknowledgment) ashtu qe te tregoj se ka pranuar paketen.
Ndersa sipas pipleline protokolit, derguesi lejohet te dergoje shume paketa pa pritur per
acknowledgments.

### Sources

- Afate me zgjidhje 2.pdf Q47

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-048

### Front

Te TCP protokolli, si eshte ndërlidhja ne mes te “Sequence number” dhe “Acknowledgment
Number”?

### Back

Acknowledgment Number qe Hosti A vendos ne segment eshte Sequence Number i bajtave
te ardhshem qe hosti A pret nga Hosti B.

### Sources

- Afate me zgjidhje 2.pdf Q48

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-049

### Front

Çka është MTU (Maximum Transmission Unit)? Sa është vlera e tij?

### Back

MTU paraqet madhesine maksimale te nje frame qe mund te transmetohet nga hosti. Tek
Etherneti, MTU eshte 1500 bajta qe nenkupton se madhesia maksimale e nje IP pakete qe nje
Ehernet frame mund te permbaje eshte 1500 bajta.

### Sources

- Afate me zgjidhje 2.pdf Q49

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-050

### Front

Përshkruani katër hapat e ndërveprimit ne mes te DHCP serverit dhe klientit?

### Back

1) DHCP server discovery - se pari duhet te gjindet DHCP serveri me te cilen do te
nderveproj hosti dhe kjo arrihet permes nje DHCP discover message, i cili enkapsulohet ne nje
datagram me IP adrese destinuese 255.255.255.255 dhe me adresen e burimit 0.0.0.0.
2) DHCP server offer(s) - DHCP serveri e pranon DHCP discover message dhe i pergjigjet
klientit me nje DHCP offer message, ku secili offer message permban: transaction ID te discover
message te pranuar, IP adresen e propozuar, subnet-masken dhe kohezgjatjen per sa do te vleje
IP adresa.
3) DHCP request - klienti perzgjedh nje nga ofertat e serverit dhe i pergjigjet ofertes se
perzgjedhur me nje DHCP request message.
4) DHCP ACK – serveri i pergjigjet DHCP request message me nje DHCP ACK message.

### Sources

- Afate me zgjidhje 2.pdf Q50

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-051

### Front

Çka është dallimi ne mes “Link State” dhe “Distance Vector” algoritmit për rrugëtim
(routing)?

### Back

Link-State: çdo router mëson topologjinë/koston e linkeve dhe llogarit rrugët me Dijkstra; ka pamje më globale. Distance-Vector: router-at shkëmbejnë me fqinjët distancat e tyre deri te destinacionet dhe përditësojnë me Bellman-Ford; është më i thjeshtë, por mund të ketë count-to-infinity/konvergjencë më të ngadaltë.

### Sources

- Afate me zgjidhje 2.pdf Q51

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-052

### Front

Këngën me madhësi 4.5 Mbyte e shkarkoni përmes lidhjes simetrike DSL 2 [Mbps]. Sa kohe
ju nevojitmet për te shkarkuar këtë këngë?

### Back

4.5Mbyte = 4.5M * 8 bit = 36Mbit / 2 Mbps = 18 sekonda.

### Sources

- Afate me zgjidhje 2.pdf Q52

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-053

### Front

Dy hoste(pajisje) A dhe B te lidhura me një linje të vetme R[bps] dhe të larguara m[metra].
Hosti A fillon te transmetoj paketën me gjatësi L[bit] ne kohen t=0. Në kohen t=dtrans, ku është
biti i fundit i paketës?

### Back

Sapo e ka leshuar hostin A.

### Sources

- Afate me zgjidhje 2.pdf Q53

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-054

### Front

Dy hoste(pajisje) A dhe B te lidhura me nje linje te vetme R[bps] dhe te larguara m[metra].
Hosti A fillon te transmeton paketen me gjatesi L[bit] ne kohen t=0. Ne kohen t=dtrans, ku eshte
biti i pare i paketes?

### Back

Ne kanalin transmetues.

### Sources

- Afate me zgjidhje 2.pdf Q54

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-055

### Front

Çka shërben HLR dhe VLR te GSM rrjetat mobile?

### Back

HLR eshte nje komponente e CDMA, TDMA dhe GSM networks. HLR eshte nje databaze
qe mban numrat mobil dhe informacionet tjera te permanent subscribers te nje rrjete mobile.
VLR eshte databaze e rrjetes se vizituar qe permban shenime per secilen pajisje mobile qe
eshte aktualisht pjese e rrjetes.

### Sources

- Afate me zgjidhje 2.pdf Q55

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-056

### Front

Qka sherben komanda ping 8.8.8.8 – t ?

### Back

Ping 8.8.8.8 sherben per testimin e lidhjes ne internet, ku 8.8.8.8 eshte IP adresa e DNS
serverit te Google-t.

### Sources

- Afate me zgjidhje 2.pdf Q56

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-057

### Front

Çka është “Web Cashing”? Çka shërben? Sa kushton?

### Back

Një Web cache ështe një njësi rrjeti që plotëson kërkesat e HTTP si përfaqsues e nje Web serveri
origjinues. Web cache ka hapësirën e vet të ruajtjes dhe mban kopje të objekteve më të vonshme të
kërkuara në këtë hapësirë ruajtjeje. Web caching është pozicionuar mirë në Internet për dy arsye. E
para, një Web cache mund ta zvogëlojë substancialisht kohën e përgjigjes ndaj një kërkese klienti,
veçanërisht nëse ngadalësimi i bandwidthit mes klientit dhe serverit origjinues është shumë më i
vogël se ngadalësimi i bandwidthit mes klientit dhe cache-it, siç është shpesh, dhe nëse cache-i e ka
objektin e kërkuar, atëherë cache-i do të mund t’ia dorëzojë shumë shpejtë objektin klientit. E dyta
Web cache-at mund ta ulin substancialisht trafikun në kyqjen e një institucioni në Internet.

### Sources

- Afate me zgjidhje 2.pdf Q57
- Afate me zgjidhje 1.pdf Q69

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-058

### Front

Qka duhet te konfigurohet qe nje kompjuter te kete qasje ne internet?

### Back

Qe nje kompjuter te kete casje ne internet duhet te ndahet nje IP adrese per ate kompjuter, te
konfigurohet default gateway dhe DNS serveri.

### Sources

- Afate me zgjidhje 2.pdf Q58

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-059

### Front

Çka janë A-Records? Çka përmban “Value” tek një A-Record? A mund të konfigurohen më shumë se një A-Record për një domain name?

### Back

konfigurohen me shume se nje A-Records per nje domain name.
A-Records jane DNS resource records, pra shenime qe ruhen ne databaze te DNS Serverit
Value eshte IP Adresa e hostname-it.
Per nje domain name mund te konfigurohen me shume e nje A-record, sepse shpesh nje website,
permban me shume se nje web server.

### Sources

- Afate me zgjidhje 2.pdf Q59
- Afate me zgjidhje 1.pdf Q50

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-060

### Front

Çka janë sulmet “DoS – Denial of Service”? Pse ndodhin? Si mbrohemi nga këto sulme?

### Back

DoS – Denial of Service është një sulm në internet ku sulmuesi përpiqet të bëjë rrjete(network)
padisponueshme për përdoruesit e saj të synuar nga ndërprerja e përkohshme ose edhe e pafundme
e shërbimeve të një hosti të lidhur në internet.Kryhet duke përmbytur burimin e synuar me kërkesa
të tepërta në një përpjekje për të mbingarkuar sistemet dhe me qellim për të parandaluar disa ose të
gjitha kërkesat legjitime për t'u përmbushur .Ndodhin per shkak te mbrojtje se dobet nga sulmet ne
web site te ndryshme . Mbrohemi permes Firewalls , Aplikacione te ndryshme te sigurise etj .

### Sources

- Afate me zgjidhje 2.pdf Q60
- Afate me zgjidhje 1.pdf Q87

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-061

### Front

Përshkruani se çka është ‘Virtual Circuit Network’ dhe çka ‘Datagram Network’.
Cilën nga këto e përdorë Interneti?

### Back

‘Virtual Circuit Network’ është sherbim për transportimin e të dhënave në një rrjet kompjuterik të
ndërlidhur me paketa në mënyrë të tillë që të duket sikur ekziston një lidhje e dedikuar e shtresës
fizike midis burimeve dhe sistemeve fundore të destinacionit të këtyre të dhënave .
‘Datagram Network’ është sherbim për transportimin e të dhënave në një rrjet kompjuterik të
ndërlidhur me paketa pa egzistuar një lidhje e dedikuar e shtresës fizike midis burimeve dhe
sistemeve fundore të destinacionit të këtyre të dhënave . Interneti perdore Datagram Network .

### Sources

- Afate me zgjidhje 2.pdf Q61
- Afate me zgjidhje 1.pdf Q88

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-062

### Front

Çka është Flow Control e qka Congestion Control?

### Back

Flow control sherben per perputhjen e shkalles me te cilen derguesi i dergon te dhenat ne
krahasim me shkallen me te cilen i pranon te dhenat. Kurse congestion control sherben si metode
e kontrollimit qe te gjithe pajisjet ne rrjete kane nje casje te barabarte ne burimet e rrjetes, gjate
nje kohe te caktuar.

### Sources

- Afate me zgjidhje 2.pdf Q62

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-063

### Front

Cilat janë dy funksionet kyçe të shtresës se rrjetës? Përshkruani secilën me kujdes.

### Back

Dy funksionet kyqe te shtreses se rrjetes jane ‘Forwading’ dhe ‘Routing’ . Forwarding- ben
zhvendosjen e paketave nga porti hyres ne portin e dedikuar dales te routerit.
Routing- percakton rrugetimin qe do te beje paketa ne rrjet prej burimit deri ne destinacion.

### Sources

- Afate me zgjidhje 2.pdf Q63
- Afate me zgjidhje 1.pdf Q90

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-064

### Front

Sa subneta jane ne figure?

### Back

Ne figure ndodhen 6 subneta.

### Sources

- Afate me zgjidhje 2.pdf Q64

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-065

### Front

Pershkruani një rekord ne Switch table?

### Back

Kolona e pare paraqet pacadresen e hostit te lidhur ne ate switch qe dergon paket perkatese .
Kolona e dyte paraqet interfacin ne te cilin eshte I lidhur ai host . ‘Time to live’ është fushë 8-
bitësh dhe funksioni I saj tek Ipv4 është që të mos e lejojë një datagram të rrugëtojë nëpër rrjet
pambarimisht nëse ai datagram nuk ka arritur tek caku/destinacioni . TTL ka nje vlere te
caktuar qe paraqet numrin e kercimeve neper routera , cdoher qe datagrami kercen ne nje router
TTL do te zvoglohet per 1 .

### Sources

- Afate me zgjidhje 2.pdf Q65
- Afate me zgjidhje 1.pdf Q91

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-066

### Front

Përshkruani vetitë kryesore të WiFi, Bluetooth dhe WiMAX. Zgjidhjen e mendoni në
aspektin e distancës dhe ‘data rate’-it?

### Back

Bluetooth, WiFi, WiMAX jane teknologji wireless qe iu mundesojn pajisjeve komunikimin
ne mes veti. Bluetooth-i sherben per komunikime ne distanca te vogla dhe ofron data rate deri ne
3 Mbps. WiFi sherben per komunikime ne distanca deri 100 m dhe lejon data rate me te madh,
10-54 Mbps. WiMAX mbulon distanca shume te medha, deri ne 50km me nje data rate 80 Mbps.

### Sources

- Afate me zgjidhje 2.pdf Q66

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-067

### Front

Vizatoni strukturen e Frame Ethernetit?

### Back

Ethernet frame: Preamble 7B, SFD 1B, Destination MAC 6B, Source MAC 6B, Type/Length 2B, Payload 46-1500B, FCS/CRC 4B.

### Sources

- Afate me zgjidhje 2.pdf Q67
- Afate me zgjidhje 1.pdf Q61

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-068

### Front

Çka është UMTS? Sa është shpejtësia e komunikimit (Uplink/Downlink)?

### Back

UMTS(Universal Mobile Telecommunications System) eshte nje 3G standard qe ofron
sherbime te internetit per ‘mobile computer’ dhe ‘phone users’ pa marre parasysh se ku gjinden.
Kur UMTS eshte i disponueshem, kompjuteret dhe perdoruesit e telefonit mund te kycen
konstant ne internet pa marre parasysh ku gjinden. Shpejtesia e komunikimit per downlink eshte
deri ne 14.4 Mbps, ndersa per uplink eshte deri ne 5.76 Mbps.

### Sources

- Afate me zgjidhje 2.pdf Q68
- Afate me zgjidhje 1.pdf Q78

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-069

### Front

Kur një paketë e shënimeve kalon nëper një SWITCH, a zvogëlohet vlera e TTL?

### Back

Jo, nuk zvogelohet.

### Sources

- Afate me zgjidhje 2.pdf Q69
- Afate me zgjidhje 1.pdf Q62

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2 source::afate_me_zgjidhje_1

## EX-070

### Front

Pershkruani evoluimin e sistemit GSM?

### Back

Kur flitet per teknologjine celulare, zakonisht klasifikohet ne disa gjenerata. Gjenarata
pare(1G) ishte e dizajnuar vetem per trafik zanor. Gjenerata e dyte(2G) ishte gjithashtu e
dizajnuar per trafik zanor por me vone u zgjerua ne 2.5G per te perkrahur internetin si dhe
sherbimet zanore. Gjenerata e trete(3G) perkrahin zerin dhe internetin por me nje shpejtsi dhe
fuqi me te madhe. Sot ekziston edhe gjenerata e katert(4G) e cila oftron internetin me te shpejte
per pajisje telefonike, diku deri ne 10 here me te shpejte se 3G.

### Sources

- Afate me zgjidhje 2.pdf Q70

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-071

### Front

Cili eshte dallimi ne mes te “forwarding” dhe “routing” ne rrjeta kompjuterike?

### Back

Forwarding është veprimi lokal në router: merr paketën nga input port dhe e dërgon në output port sipas forwarding table. Routing është procesi global që llogarit rrugën/forwarding tables duke përdorur algoritme dhe protokolle routing.

### Sources

- Afate me zgjidhje 2.pdf Q71

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-072

### Front

Qka eshte “Apache Web Server”? Sa kushton?

### Back

“Apache Web Server” eshte web serveri me i njohur dhe me i perdorur i cili eshte krijuar dhe
mirembahet nga ‘Apache Sowftare Foundation’. Apache eshte softuer open souce, pra kushton
fale.

### Sources

- Afate me zgjidhje 2.pdf Q72

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-073

### Front

Te Go-Back(GBN) protokolli sa “timer” jane? Qfare eshte roli I tyre?

### Back

Te GBN derguesi mund te transmetoj deri ne n paketa pa mare acknowledgment. Pranuesi
dergon comulative acknowledgments => p.sh nese dergon ack. per paketen n kjo d.m.th se ai ka
pranuar paketat paraprake n-1, n-2 e keshtu me rradhe. Eshte vetem nje timer te derguesi per
paketen me te vjeter per te cilen nuk eshte pranuar ack. Nese timer-it i mbaron koha
ritransmetohen te gjitha unack. paketat.

### Sources

- Afate me zgjidhje 2.pdf Q73

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-074

### Front

Shenoni disa akplikacione qe i “durojne”(jane tolerante) humbjet e bitave(shenimeve) gjate
transmetimit?

### Back

1) Skype
2) Aplikacionet multimediale
3) Video/voice streaming
4) Viber etj.

### Sources

- Afate me zgjidhje 2.pdf Q74

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-075

### Front

Kengen me gjatesi 6 min.(me madhesi 6MByte) e ngarkoni(upload) perms lidhjes simetrike 6
Mbps te Internetit.Sa kohe ju duhet per te ngarkuar kete kenge?

### Back

Pasiqe lidhja eshte simetrike sa ndahen per upload aq ndahen edhe per download, per kete
arsye kemi per upload 3Mbps, ndersa 6Mbyte mundem ta shenojme si 6M*8bit = 48Mbit dhe
kemi 48Mbit/3Mbps = 16 s.

### Sources

- Afate me zgjidhje 2.pdf Q75

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-076

### Front

Qka eshte RTT(Round Trip Time)?

### Back

RTT (Round Trip Time) është koha që i duhet një pakete/mesazhi të shkojë nga klienti te serveri dhe që përgjigjja/ACK të kthehet prapë te klienti.

### Sources

- Afate me zgjidhje 2.pdf Q76

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-077

### Front

Qka sherben “Virtual Local Area Network”(VLAN) switch-i?

### Back

LAN-i virtual ose shkurtimisht VLAN-i sherben per te i lejuar administratoret e rrjetit qe t’i
grupojne dy e me shume hoste se bashku edhe nese ato hoste nuk jane te konektuara direkt ne te
njejtin rrjet-switch.

### Sources

- Afate me zgjidhje 2.pdf Q77

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-078

### Front

Ju merrni sherbimin e Internetit nga IPKO. IP adresa qe IPKO iu ndan eshte reale
91.187.99.206. Ju duhet ta dizajnoni rrjeten per nje kompani me 5 kompjuter, nje
shtypes(network enabled), nje web server dhe nje ftp server. Vizatojeni skemen e lidhjes se
ketyre kompjutereve, shtypesit ne LAN dhe serveret ne Internet se bashku me te gjitha IP adresat
e pajisjeve te lidhura.(Kjo detyre ka 4 pike. Shfrytezo faqen mbrapa per skica!)

### Back

Zgjidhje tipike: vendos router-in në kufi me WAN/public IP `91.187.99.206` dhe LAN privat p.sh. `192.168.0.0/24`.
- Router LAN/default gateway: `192.168.0.1`
- PC-të: `192.168.0.10-192.168.0.15`
- Printer: `192.168.0.20`
- Web server: `192.168.0.80`
- Email server: `192.168.0.25` ose FTP server: `192.168.0.21`, varësisht nga pyetja
- Të gjithë hostët përdorin gateway `192.168.0.1`.
Router-i bën NAT/PAT për klientët. Për qasje nga jashtë te serverët, konfiguro port forwarding/static NAT.

### Sources

- Afate me zgjidhje 2.pdf Q78

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-079

### Front

Qka duhet te konfigurohet shtese te routeri nga detyra paraprake ashtu qe web servei dhe ftp
serveri te punojne korrekt?

### Back

Qe ftp serveri dhe web server-i te punojne korrekt duhet qe porti per ftp te jete 21, ndersa per
web server porti duhet te jete 80.

### Sources

- Afate me zgjidhje 2.pdf Q79

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-080

### Front

Cila është adresa e ueb dhe ftp serverit tuaj (nga detyra 78) për shfrytëzuesit nga jashtë (nga
Interneti) dhe nga brenda rrjetit (Intraneti)?

### Back

Nga jashtë/shtëpia i qasesh përmes IP publike të router-it/ISP-së ose domain-it publik. Brenda LAN-it mund t'i qasesh me IP private të serverëve, p.sh. web `192.168.0.80` dhe FTP `192.168.0.21`, ose me domain nëse DNS/NAT loopback është konfiguruar.

### Sources

- Afate me zgjidhje 2.pdf Q80

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-081

### Front

Qka eshte dallimi ne mes te hub-it, switch-it dhe router-it?

### Back

Routeri eshte pajisje me dy e me shume kartela te rrjetës e cila bene vendosjen e paketave
nga një rrjetë në tjetrën.
Paisja e cila pranon paketat dhe i percjell ato te destinacioni i tyre perkates ne nje LAN quhet
Switch.
Paisja hardverike e cila transmeton te dhenat e komunikimit quhet Hub.
Hub-i transmeton te dhenat e paketave(frames) ne te gjitha pajisjet e lidhura ne te, ku me pas
pajisjet per te cilat nuk eshte i destinuar informacioni e bejne discard, kurse switchi meson se
cilat pajisje jane te lidhura ne portet e tij dhe i percjell paketat vetem ne portin e destinuar. Hub-i
transmeton frames, ndersa switchi ne anen tjeter transmeton sinjale elektrike. Hub-i sherben per
zgjerimin e rrjetes duke ofruar me shume porte ndersa switchi e ndan rrjeten ne pjese me te vogla
ku kemi me pak congestion.

### Sources

- Afate me zgjidhje 2.pdf Q81

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-082

### Front

Sa eshte koha e transmetimit te shenimeve(data rate) tek 802.11 standardi?? Si ndahet brezi
frekuencor? A duhet licence për këtë brez frekuencor?

### Back

Ofron deri ne 11 Mbps per standardin 802.11b ndersa per standardet 802.11a dhe 802.11g
ofron deri ne 54 Mbps, por standard pra eshte 54Mbps.
Brezi frekuencor :
802.11b: 2.4–2.485 GHz deri ne 11 Mbps
802.11a: 5.1–5.8 GHz deri ne 54 Mbps
802.11g: 2.4–2.485 GHz deri ne 54 Mbps
802.11AC 5.8GHz deri 1300Mbps max data rate 6.93gbps
Nuk nevojitet license.

### Sources

- Afate me zgjidhje 2.pdf Q82

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-083

### Front

E ciles pajisje eshte IP adresa 127.127.127.127?

### Back

Eshte e hostit tone.

### Sources

- Afate me zgjidhje 2.pdf Q83

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-084

### Front

Nese TTL(Time To Live) ka vleren nje(1), qka ndodhe me paketen e shenimeve?

### Back

Paketa mund te pershkoj vetem edhe nje router tjeter, e pastaj pasi vlera e saj te zbritet per
nje(1) ajo behet drop.

### Sources

- Afate me zgjidhje 2.pdf Q84

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-085

### Front

Sa eshte numri maksimal i porteve qe kemi ne TCP/IP protokollin? Pse jane aq porte?

### Back

Numri maksimal i porteve ne protokollin TCP/IP eshte 2^16 – 1 = 65536 – 1 = 65535 porte.
Numri i porteve eshte kaq pasiqe numri i portit per nje TCP/IP lidhje percaktohet me 16 bita.

### Sources

- Afate me zgjidhje 2.pdf Q85

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-086

### Front

Qka eshte “throughput”-i ne rrjeta kompjuterike?

### Back

Troughput-i eshte shpejtesia(qe shprehet ne bps) me te cilen transmetohen bitat nga derguesi
tek pranuesi.

### Sources

- Afate me zgjidhje 2.pdf Q86

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-087

### Front

Qka ndodh me paketen e shenimeve nese (traffic intensity) L*a/R>1?

### Back

Nese L*a/R>1 atehere vonesa e arritjes se paketes eshte infinit qe d.m.th se paketa humbe.

### Sources

- Afate me zgjidhje 2.pdf Q87

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-088

### Front

Nese deshirojme te kemi rrjeten private me numer maksimal te shfrytezuesve, duhet te
perdorim brezin e IP adresave? __.__.__.__/__
Shenoni dy IP adresa te qfaredoshme nga ky brez?
__.__.__.__ dhe __.__.__.__

### Back

Pergjigjja:
Nëse dëshirojmë të kemi rrjetën private me numër maksimal të shfrytëzuesve, duhet të përdorim
brezin e IP adresave: 10.0.0.0/8
Shënoni 2 IP adresa te çfarëdoshme nga ky brez:
10.0.0.10 dhe 10.10.0.11

### Sources

- Afate me zgjidhje 2.pdf Q88

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-089

### Front

Nese deshirojme te kemi rrjeten private me numer minimal te shfrytezuesve, duhet te
perdorim brezin e IP adresave? __.__.__.__/__
Shenoni dy IP adresa te qfaredoshme nga ky brez?
__.__.__.__ dhe __.__.__.__

### Back

Pergjigjja:
. Nëse dëshirojmë të kemi rrjetën private me numër minimal të shfrytëzuesve, duhet të përdorim
brezin e IP adresave: 192.168.1.0/8
Shënoni 2 IP adresa te çfarëdoshme nga ky brez:
192.168.1.10 dhe 192.168.1.11

### Sources

- Afate me zgjidhje 2.pdf Q89

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-090

### Front

Si eshte ndare brezi frekuencor te qasja ne Internet me DSL?

### Back

- High-speed downstream channel, ne rangun 50 kHz-1 MHz
- Medium-speed upstream channel, ne rangun 4 kHz-50 kHz
- Ordinary two-way telephone channel, ne rangun 0-4 kHz
Punoi: Ismail Sekiraqa

### Sources

- Afate me zgjidhje 2.pdf Q90

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_2

## EX-091

### Front

IP (IP v4) adresa eshte biteshe ndersa IP v6 eshte biteshe?

### Back

IPv4 eshte 32 biteshe.
IPv6 eshte 128 biteshe.

### Sources

- Afate me zgjidhje 1.pdf Q1

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-092

### Front

Sa eshte IP Adresa e local host-it?

### Back

Ip adresa e local hostit eshte 127.0.0.1 dhe I takon klases A.

### Sources

- Afate me zgjidhje 1.pdf Q2

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-093

### Front

Internet protokolli sipas renditjes (top-down) perbehet nga cilat shtresa?

### Back

1. Application
2.Transport
3.Network
4.Link
5.Physical

### Sources

- Afate me zgjidhje 1.pdf Q3

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-094

### Front

Cka eshte Interneti?

### Back

Internetin mund ta kuptojme si:
-miliona paisje llogaritese te konektuara,
-rrjet e rrjetave,
-infrastrukture qe ofron sherbime per aplikacione
-ofron nderfaqe programuese per aplikacionet

### Sources

- Afate me zgjidhje 1.pdf Q4

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-095

### Front

Si eshte I ndare brezi frekuencor te DSL?

### Back

High Speed downstream 50Khz-1MHz
Medium Speed upstream 4Khz-50MHz
Two way telephone channel 0-4Khz

### Sources

- Afate me zgjidhje 1.pdf Q5

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-096

### Front

Si e percaktoni rrugetimin e paketave neper rrjeta kompjuterike nese I qasemi erverit
www.uni.pr.edu (sistemi operativ eshte Windows)?

### Back

Per te percaktuar rrugetimin e paketave te web faqes www.uni-pr.edu percjellim keto hapa:
cmd
tracert www.uni-pr.edu
enter

### Sources

- Afate me zgjidhje 1.pdf Q6

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-097

### Front

Cka eshte throughput ne rrjeta kompjuterike?

### Back

Throughput: Shpejtesia (bit/njesi kohe) me te cilen transferohen bitat prej derguesit tek pranuesi.
-i menjehershem
-mesatar

### Sources

- Afate me zgjidhje 1.pdf Q7

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-098

### Front

cka eshte dallimi ne mes te multipleksimit FDM dhe TDM?

### Back

FDM eshte shkurtes per Frequency Division Multiplexing. Ne secilen lidhje ndahet nje brez
frekuencor I caktuar.
TDM eshte shkurtes per Time Division Multiplexing. Koha ndahet ne frames me kohezgjatje fikse.
Frame ndahet ne nje numer fiks te sloteve qe varet nga numri I shfryteyuesve.

### Sources

- Afate me zgjidhje 1.pdf Q8

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-099

### Front

Sheno disa ISP ne KOSOVE?

### Back

Ipko, kujetsa, artmotion, etj.

### Sources

- Afate me zgjidhje 1.pdf Q9

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-100

### Front

Cka eshte dallimi ne mes te forwarding dhe routing ne rrjeta kompjuterike?

### Back

Forwarding është veprimi lokal në router: merr paketën nga input port dhe e dërgon në output port sipas forwarding table. Routing është procesi global që llogarit rrugën/forwarding tables duke përdorur algoritme dhe protokolle routing.

### Sources

- Afate me zgjidhje 1.pdf Q10

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-101

### Front

Nje DNS resource record (name,value,type,ttl) eshte I tipit MX ( pra type=MX). Cka
permban ateher Value?

### Back

Për DNS RR me Type=MX, `Value` përmban emrin canonical/hostname të mail serverit për domain-in.

### Sources

- Afate me zgjidhje 1.pdf Q11
- Afate me zgjidhje 1.pdf Q41

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-102

### Front

Cka sherben DHCP serveri?

### Back

DHCP serveri lejon hostin qe ne menyre dinamike te marre IP Adresen e tij nga serveri I rrjetit , kur
ai bashkangjitet ne rrjet.

### Sources

- Afate me zgjidhje 1.pdf Q12

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-103

### Front

Si punon NAT-i ?

### Back

NAT lejon shumë hostë me IP private të përdorin një IP publike. Router-i NAT zëvendëson source private IP/port me public IP/port kur paketa del në Internet dhe ruan mapping në NAT table. Kur kthehet përgjigjja, router-i përdor portin publik për ta gjetur hostin privat dhe e rikthen destination IP/port. Portet janë çelësi që dallon lidhjet e shumë hostëve pas të njëjtës IP publike.

### Sources

- Afate me zgjidhje 1.pdf Q13

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-104

### Front

Cfare bene pjesa e kodimit te meposhtem tek komunikimi klient-server me ndihmen e

### Back

protokollit TCP:
readThread = new Thread ( new ThreadStart(EkzekutoServerin));
readThread.Start();
Me ane te kesaj pjese te kodit krijohet instanca e Thread-it readThread me parameter
EkzekutoServerin. Me kete rast behet edhe startimi I Serverit.

### Sources

- Afate me zgjidhje 1.pdf Q14

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-105

### Front

Cka eshte CSMA/CD protokolli?

### Back

CSMA/CD eshte protokol qe bene zbulimin e nderhyrjeve (collisons) qe ndodhin ne kanalin
Transmetues te paisjeve te rrjetit. Kur dy nyje perdorin te njejtin kanal ateher shfaqen keto
Nderhyrje. Zbulimi I nderhyrjeve behet per kohe shume te shkurte. Kur keto nderhyrje zbulohen
CSMA/CD adapteri e nderpren transmetimin deri sa kanali eshte I hapur

### Sources

- Afate me zgjidhje 1.pdf Q15

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-106

### Front

Pershkruani permbajtjen e nje ARP tabele te nje nyje kompjuterike te cfardoshme?

### Back

ARP tabela ruan mapping `IP address -> MAC address` për hostët në LAN dhe një TTL/age për secilin rekord. Kolona `???` është MAC Address. Shembull:
`IP Address | MAC Address | TTL`
`10.20.30.1 | aa:bb:cc:dd:ee:ff | 120s`
`10.20.30.41 | 11:22:33:44:55:66 | 120s`

### Sources

- Afate me zgjidhje 1.pdf Q16

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-107

### Front

Cka sherben SSID ne rrjeta kompjuterike?

### Back

SSID eshte shkurtes per Service Set Identifier. Te gjitha paisjet ne rrjet duhet te perdorin kete case-
sensitive name, per te komunikuar ne Wifi, I cili eshte nje string text deri ne 32 bytes I gjate.

### Sources

- Afate me zgjidhje 1.pdf Q17

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-108

### Front

Nese supozojme se d prop eshte me e madhe se d trans, ne kohen t =d trans, ku eshte biti I
pare I paketes?

### Back

Biti I pare eshte ne link, dhe ene nuk ka arritu ne destinacion.

### Sources

- Afate me zgjidhje 1.pdf Q18
- Afate me zgjidhje 1.pdf Q36

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-109

### Front

Cka sherben VLR te mobile GSM rrjetat?

### Back

VLR-ja te mobile GSM rrjetat sherben si nje databaze me regjistra per secilin perdorues qe gjendet
momentalisht ne rrjet.

### Sources

- Afate me zgjidhje 1.pdf Q19

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-110

### Front

Kur TTL do te kete vleren zero? Cka ndodh ateher me paketen e shenimeve?

### Back

Kur TTL nuk do te kete regjistrime. Kur TTL ka vleren zero, pakoja behet DROP.

### Sources

- Afate me zgjidhje 1.pdf Q20

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-111

### Front

Shenoni dy menyra te percaktimit se cfare IP adrese ka kompjuteri juaj (sistemi
operativ eshte Windows)?

### Back

Ekzisotjne disa menyra te percaktimit te IP adreses se kompjuterit:
a) Start > Run > cmd > ipconfig > enter
b) Control Pannel > Internet and Network > Network and Sharing Center > Network and
Connection Status > Details

### Sources

- Afate me zgjidhje 1.pdf Q21

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-112

### Front

Sa eshte numri maksimal I portave qe kemi ne TCP/IP protokollin? Pse jane aq porta?

### Back

Cilat guxojme ti perdorim?
Numri maksimal I portave qe kemi ne TCP/IP protokollin eshte 65535, sepse port numri eshte 16
bitesh. 2^16 – 1 = 65535.
0-1023 te kontaktit
1024-41151 te regjistruar
41152-65535 dinamik

### Sources

- Afate me zgjidhje 1.pdf Q21

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-113

### Front

Cka eshte dallimi ne mes te TCP dhe UDP?

### Back

TCP eshte transport I besueshem (reliable) mes procesit te dergimit dhe te pranimit te mesazheve.
Derguesi nuk ka ndikim tek marresi. Nuk I perkrah : throughput, timing,minimum, security.
UDP eshte transport jo I besueshem (un reliable) mes procesit te dergimit dhe pranimit te mesazhit.
Nuk I perkrah : thorughput, flow control. Congestion control, security.

### Sources

- Afate me zgjidhje 1.pdf Q23

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-114

### Front

Cka eshte dallimi ne mes “stop and wait” dhe “pipeline” protokollit?

### Back

Me ante te “stop and wait” protokollit, paketa dergohet edhe pret per ACK pergjigje nga pranuesi,
dhe pastaj dergon paketen tjeter.
Me ane te “pipeline” protokolit, shume paketa dergohen njekohesisht, pa mar ACK pergjigje nga
pranuesi.

### Sources

- Afate me zgjidhje 1.pdf Q24

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-115

### Front

Te TCP protokolli , si nderlidhja ne mes te “Sequence number” dhe “Acknowledgment

### Back

number”
Sequence number perdoret per te kontrolluar sa shume segmente ka derguar, dhe per te I
identifikuar ato.
Acknowledgment number perdoret per te informuar derguesin se paketa e nisur ka arritur.
Pranuesi e perdor sequence number per te radhitur segmentet qe arrijne te parenditura, si dhe
te kalkuloj nje ACK number.

### Sources

- Afate me zgjidhje 1.pdf Q25

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-116

### Front

Cka eshte MTU (Maximum Transmission Unit)? Sa eshte vlera e tij?

### Back

MTU eshte shkurtes per Maximum Transmission Unit, perdoret per te percaktuar madhesin me te
madhe te paketave gjate ndonje transmetimi. Shumica e Cisco routerave perdorin MTU te madhesin
7740 bytes.

### Sources

- Afate me zgjidhje 1.pdf Q26

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-117

### Front

Pershkruani kater hapat e nderveprimit ne mes te DHCP serverit dhe klientit?

### Back

a)DHCP DISCOVERY behet lidhja e klientit me serverin
b)DHCP OFFER klienti mer ip adresen nga serveri
c)DHCP REQUEST kerkesat per ip adresa nga klienti
d)DHCP ACKNOELEDGMENT serveri e lajmron klientin per kerkesat e pranuara.

### Sources

- Afate me zgjidhje 1.pdf Q27

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-118

### Front

Pershkruani ngjashmerite dhe ndryshimet ne mes te switch-it dhe router-it?

### Back

Switchi eshte nje paisje e cila punon ne Link Layer, varesisht nga Mac adresa, switch e din se ne
cilin port te bej zhvendosjen e paketave.
Routeri eshte nje paisje e cila punon ne Net Layer, ben transferimin e te dhenave ndermjet dy
rrjetave te ndryeshme, procesi I tille njihet si routing.

### Sources

- Afate me zgjidhje 1.pdf Q28

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-119

### Front

Cka eshte dallimi ndermjet “Link State” dhe “Distance Vector” algorimit per
routing (rrugetim)?

### Back

Link-State: çdo router mëson topologjinë/koston e linkeve dhe llogarit rrugët me Dijkstra; ka pamje më globale. Distance-Vector: router-at shkëmbejnë me fqinjët distancat e tyre deri te destinacionet dhe përditësojnë me Bellman-Ford; është më i thjeshtë, por mund të ketë count-to-infinity/konvergjencë më të ngadaltë.

### Sources

- Afate me zgjidhje 1.pdf Q29

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-120

### Front

Dy hoste (paisje) A dhe B te lidhura me nje linje te vetme R [bps] dhe te larguara m
[metra]. Hosti A fillon te transmettoj paketen me gjatesi L [bit] ne kohen t=0. Ne kohen
t= d trans, ku eshte biti I fundit?

### Back

Biti posa po e leshon hostin A.

### Sources

- Afate me zgjidhje 1.pdf Q30

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-121

### Front

Kur TTL do te kete vleren nje cka ndodh me paketen e shenimeve?

### Back

Kur TTL ka vleren nje, pakoja mund te shkoje tek ndonje router tjeter dhe te zvogeloj TTL per nje
(pra behet zero) dhe pakoja behet DROP.

### Sources

- Afate me zgjidhje 1.pdf Q31

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-122

### Front

Cka eshte RTT (Round Trip Time )?

### Back

RTT (Round Trip Time) është koha që i duhet një pakete/mesazhi të shkojë nga klienti te serveri dhe që përgjigjja/ACK të kthehet prapë te klienti.

### Sources

- Afate me zgjidhje 1.pdf Q32

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-123

### Front

Ku eshte I implementuar “Link Layer”?

### Back

Link Layer eshte I implementuar ne “adaptor” (aka Network Interface Card NIC), ose ne chip.

### Sources

- Afate me zgjidhje 1.pdf Q33

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-124

### Front

Cka eshte dallimi ne mes te hubit, switch-it dhe router-it ?

### Back

Hub-i eshte nje paisje e cila punon ne Physicall Layer, ai e shyqrton pakteten qe pranon bit per bit,
qdo bit qe pranon ne hyrje e transmeton ne te gjitha portes dalese, te dhenat qe I mer gjithmon I ben
broadcast.
Switchi eshte nje paisje e cila punon ne Link layer, varesisht nga MAC adresa e din se ne cilin port
te zhvendos paketen.
Routeri eshte nje paisje e cila punon ne Net layer, ben transferimin e te dhenave ndermjet dy
rrjetave te ndryeshme, procesi I tille njihet si routing.

### Sources

- Afate me zgjidhje 1.pdf Q34

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-125

### Front

Nese supozojme se dprop eshte me e vogel se dtrans, ne kohen t=dtrans ku eshte biti I
pare I paketes?

### Back

Biti I pare I paketes posa e ka arritur Hostin B.

### Sources

- Afate me zgjidhje 1.pdf Q35

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-126

### Front

127.168.1.1 eshte IP Adresa

### Back

e :
eshte IP Adresa e loopback
address qe perdoret per testimin e
tcp/ip.

### Sources

- Afate me zgjidhje 1.pdf Q37

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-127

### Front

Cka eshte dallimi ne mes te POP3 dhe SMTP?

### Back

SMTP, POP3 dhe IMAP jane protokole te cilat perdoren per dergime te mail-ave.
SMTP- eshte shkurtes per Simple Mail Transfer Protocol dhe perdoret kur email dergohet nga nje
email klient, psh Outlook Express, tek nje email server, ose kur nje email dergohet nga nje email
server tek tjetri. SMTP perdor portin 25.
POP3- eshte shkurtes per Post Office Protocol, lejon qe nje email klient te download-oj nje email
prej nje email serveri. POP3 perdor portin 110.

### Sources

- Afate me zgjidhje 1.pdf Q38

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-128

### Front

Nese deshirojme te kemi rrjeten private me numer minimal te shfrytezuesve, duhet te
perdorim brezin e IP adresave ? Si dhe shenoni 2 ip adresa te cfardoshme nga ky

### Back

brez:
192.168.0.0 / 30 Lejon vetem dy shfrutezues
192.168.0.1 dhe 192.168.0.2

### Sources

- Afate me zgjidhje 1.pdf Q39

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-129

### Front

Nëse dëshirojmë të kemi rrjetën private me numër maksimal të shfrytëzuesve, duhet të

### Back

përdorim brezin e IP adresave: Shënoni 2 IP adresa te çfarëdoshme nga ky brez:
10.0.0.0 / 8 Lejon 16777214 shfrytezues
10.0.0.1 10.111.6.2

### Sources

- Afate me zgjidhje 1.pdf Q40

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-130

### Front

Si ndodh “Congestions” ne rrjetat kompjuterike?

### Back

Kjo dukuri ndodh kur shume burime te ndryeshme dergojne shume shpejte shume te dhena qe te
trajtohen. Si rezultat ka humbje te paketave dhe vonesa te medha ne baferin e routerit.

### Sources

- Afate me zgjidhje 1.pdf Q42

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-131

### Front

127.192.168.1 eshte IP

### Back

Adresa e :
eshte IP Adresa e klases A

### Sources

- Afate me zgjidhje 1.pdf Q43

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-132

### Front

Per te komunikuar dy kopmjuter ndermjet veti ata duhet te dine:

### Back

1. IP Adresen
2. Portin

### Sources

- Afate me zgjidhje 1.pdf Q44

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-133

### Front

Cka eshte DNS dhe per cka perdoret? Nese te gjithe DNS Serveret do te ishin

### Back

jashte funskionit (offline), cka do te ndodhte me Internetin?
DNS eshte shkurtes per Domain Name Server, e cila ben perkthimin e hostname-ave ne IP
Adresa perkatese. Nese te gjithe DNS do ti ishin jashte funksionit te tyre ne do te mund te ju
qasemi web faqeve vetem permes IP Adresave (jo me hostname).

### Sources

- Afate me zgjidhje 1.pdf Q45

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-134

### Front

Cili aplikacion degjon ne portin 66666?

### Back

Ne portin 66666 nuk degjon asnje aplikacion, sepse port numri maksimal eshte 65535, sepse port
numri eshte 16 bites, 2^16 – 1 = 65535.

### Sources

- Afate me zgjidhje 1.pdf Q46

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-135

### Front

Nese aplikacioni gjeneron paketa 40 bajteshe te shenimeve cdo 20 msec dhe secila
paket enkapsulohet ne TCP segment dhe pastaj ne IP datagram. Sa per qind e
shenimeve jane overhead(mbingarkes) dhe sa perqind jane shenime te aplikacionit?

### Back

Gjate enkapsulimit ne TCP segment, te dhenave I shtohet 20 bajte overhead, ndersa gjate
enkapsulimit me IP datagram ketyre shenimeve u shtohen 20 bajte te tjer overhead duke rezultuar
ne nje overhead prej 40 bajtesh. Ne kete raste 40 bajte jane overhead dhe 40 bajte per shenime
aplikacioni dmth nga 50% per csecilen

### Sources

- Afate me zgjidhje 1.pdf Q47

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-136

### Front

Shenoni emrat e dy produkteve per ueb server dhe nese keto dy produkte I instalojme

### Back

ne kopmjuterin lokal shenoni edhe portet e tyre:
1. IIS (nje port I cfardosshem )
2. APACHE portin 80

### Sources

- Afate me zgjidhje 1.pdf Q48

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-137

### Front

Cka duhet te konfigurohet ne nje kopmjuter qe ai te kete qasje ne Internet?

### Back

Ne kompjuter duhet te konfigurohet Ip Adresa e Hostit, Subnetmask-a, IP Adresa e DNS serverit
dhe Ip Adresa e default gateway.

### Sources

- Afate me zgjidhje 1.pdf Q49

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-138

### Front

Plotesoje ARP tabelen per kompjuterin me IP adrese 192.168.1.100?

### Back

ARP tabela ruan mapping `IP address -> MAC address` për hostët në LAN dhe një TTL/age për secilin rekord. Kolona `???` është MAC Address. Shembull:
`IP Address | MAC Address | TTL`
`10.20.30.1 | aa:bb:cc:dd:ee:ff | 120s`
`10.20.30.41 | 11:22:33:44:55:66 | 120s`

### Sources

- Afate me zgjidhje 1.pdf Q51

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-139

### Front

Cili aplikacion dëgjon në portin 99999?

### Back

Ne portin 99999 nuk degjon asnje aplikacion, sepse port numri maksimal eshte 65535, sepse port
numri eshte 16 bites, 2^16 – 1 = 65535.

### Sources

- Afate me zgjidhje 1.pdf Q52

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-140

### Front

Sa bitëshe është MAC adresa e kartelës së rrjetës?

### Back

MAC adresa është 48 bitëshe, pra 6 bajtë.

### Sources

- Afate me zgjidhje 1.pdf Q53

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-141

### Front

Shkruani pjesën e kodit ne gjuhen programuese ne C# që starton threadin krijuar?

### Back

readThread = new Thread ( new ThreadStart(EkzekutoServerin));
readThread.Start();

### Sources

- Afate me zgjidhje 1.pdf Q54

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-142

### Front

Serveri që implementon SMTP protokollin dëgjon në portin?

### Back

Portin 25.

### Sources

- Afate me zgjidhje 1.pdf Q55

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-143

### Front

10.127.192.256 është IP adresa e ?

### Back

Nuk eshte ip adrese valide .

### Sources

- Afate me zgjidhje 1.pdf Q56

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-144

### Front

Gjeni rrugën me peshën (koston) me te ulët në mes të nyjës v dhe z, si ne figurë? Dv(z) =

### Back

V-X-Y-Z Pesha 5 .

### Sources

- Afate me zgjidhje 1.pdf Q58

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-145

### Front

Gjeni rrugën me peshën (koston) me te ulët në mes të nyjës w dhe z, si ne figurë? Dw(z) =

### Back

W-V-Y-Z Pesha 9 . Dijkstra .

### Sources

- Afate me zgjidhje 1.pdf Q59

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-146

### Front

Gjeni rrugën me peshën (koston) me te ulët në mes të nyjës u dhe w, si ne figurë? Du(w) =

### Back

U-X-Y-W Pesha 3 .

### Sources

- Afate me zgjidhje 1.pdf Q60

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-147

### Front

Çka është ARP protokolli?

### Back

ARP (Address resolution protocol) është një protokoll për hartimin e një IP adrese ,në një adresë të
makinës fizike(physical machine address) që njihet në rrjetin lokal(localnetwork). Ky protokoll
operon nen shtresen e rrjetit(network layer) si pjese e interfejsit ndermjet OSI network dhe OSI link
layer .

### Sources

- Afate me zgjidhje 1.pdf Q63

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-148

### Front

Përshkruani se si punon ARP (në LAN)?

### Back

ARP (Address resolution protocol) është një protokoll për hartimin e një IP adrese ,në një adresë të
makinës fizike(physical machine address) që njihet në rrjetin lokal(localnetwork).
P.sh A deshiron te dergoj nje datagram tek B . Mac adresa e B nuk gjendet ne ARP tabelen e A .
A transmeton nje ARP query paket , qe permban IP adressen e B’s dhe e dergon ne broadcast Mac
adressen FF-FF-FF-FF-FF .Te gjitha nyjet e pranojne ARP query paketen .B e pranon paketen dhe i
pergjigjet A-se me Mac adresen e saj , dhe ky frame dergohet te Mac adresa e A-se . A-ja e ruan
qiftin IP-MAC/adrese ne ARP table derisa informacioni te behet i vjeter .

### Sources

- Afate me zgjidhje 1.pdf Q64

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-149

### Front

. Plotësoje ARP tabelën për kompjuterin me IP adresë 10.10.10.10 ‘

### Back

ARP tabela ruan mapping `IP address -> MAC address` për hostët në LAN dhe një TTL/age për secilin rekord. Kolona `???` është MAC Address. Shembull:
`IP Address | MAC Address | TTL`
`10.20.30.1 | aa:bb:cc:dd:ee:ff | 120s`
`10.20.30.41 | 11:22:33:44:55:66 | 120s`

### Sources

- Afate me zgjidhje 1.pdf Q65

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-150

### Front

Vizatoni IPv4 datagram formatin (përdorni edhe faqen prapa!). Sa është “overhead”-i
ndaj shtresës se TCP-së?

### Back

20 bytes of TCP ch4

### Sources

- Afate me zgjidhje 1.pdf Q66

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-151

### Front

Sa SUBNET-a janë në figurë?

### Back

6 Subneta .

### Sources

- Afate me zgjidhje 1.pdf Q67

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-152

### Front

Çka është “Apache Web Server”? Sa kushton?

### Back

Apache Web Server është një open-source Web server , per shpërndarjen dhe menaxhimin e
softwerit . Nuk kushton fare sepse eshte open-source.

### Sources

- Afate me zgjidhje 1.pdf Q68

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-153

### Front

Çka janë TCP dhe UDP protokollet? Beni një përshkrim te shkurtër për secilën prej

### Back

tyre?
TCP dhe UDP jane protokolle per komunikim klient server.
TCP është protokoll që siguron një kanal tëbesueshëm të komunikimit në mes klientit dhe serverit
ndërsa protokolli UDP nuk siguron nje kanal të tillë dhe rrjedha e informatave bëhet pa garancionin
se ato do të arrijnë në destinacion.

### Sources

- Afate me zgjidhje 1.pdf Q70

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-154

### Front

Çka shërben komanda: ping 8.8.8.8 –t ?

### Back

Komanda ping sherben per te testuar lidhjen me rrjeten(internetin) . 8.8.8.8 eshte ip adresa e DNS
serverit publik te Google . Ndersa ping 8.8.8.8 –t ben qe komanda ping te ekzekutohet deri sa ta
ndalim vet p.sh Ctrl+C .

### Sources

- Afate me zgjidhje 1.pdf Q71

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-155

### Front

Çka ndodhe me paketat e shënimeve nëse (traffic intensity) L*a/R > 1?

### Back

Raporti La/R i quajtur intensiteti i trafikut shpesh luan një rol të rëndësishëm ne vlerësimin e nivelit
të vonesës në radhë. Nese La/R > 1 atëherë shkalla mesatare me të cilën bitat arrijën në radhë
tejkalon shakllën me të cilën bitat mund të transmetohen nga radha. Në këtë gjendje fatkeqe, radha
do të tentoj të rritet pakufi dhe vonesa ne radhë do t’i afrohet pafundësisë! Prandaj, nja nga rregullat
e arta ne inxhinierinë e trafikut është: Dizajnoni sitetim tuaj ashtu që intensiteti i trafikut të mos jetë
më i madh se 1.

### Sources

- Afate me zgjidhje 1.pdf Q72

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-156

### Front

Shënoni disa aplikacione që i “durojnë” (janë tolerante) humbjet e bitave (shënimeve)

### Back

gjate transmetimit:
1. Real Time audio/video aplikacionet (livestream)
2.Skype
3.Interactive Games

### Sources

- Afate me zgjidhje 1.pdf Q73

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-157

### Front

Çka janë “Cookies”?

### Back

Kur një web server këron një faqe në një shfletues, lidhja mbyllet dhe serveri harron gjithçka rreth
përdoruesit . Pikerisht per kete arsye jane krijuar cookies . Cookies janë të dhëna, të ruajtura në
tekst fajlla vogla, në kompjuterin e perdoruesve .Cookies i lejojnë site-ve të ruajnë gjurmët e
përdoruesve.

### Sources

- Afate me zgjidhje 1.pdf Q74

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-158

### Front

A është ‘SOCKETS’ protokoll apo interface? Me kujdesë përshkruani pse.

### Back

Socket eshte interface softwerik e cila i hap lidhjet ne rrjetë për t’i lejuar aplikacionet që të mund të
shkruajnë dhe të lexojnë nëpermjet rrjetës. Socket janë një pikë fundore (ang. Endpoint) e
komunikimit në mes të dy programeve në rrjetë. Një Socket perbehet prej numrit te portit (ang. port
number) dhe prej një IP adresë dhe këto dy komponente e identifikojnë në mënyrë unike Socket-in.

### Sources

- Afate me zgjidhje 1.pdf Q76

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-159

### Front

Çka është Flow Control e qka Congestion Control“PROXY Serveri”?

### Back

(Flow Control). Nyjet në secilën anë të lidhjes kanë një sasi të limituar të frejmave që mund ti
bartin. Kjo gjë paraqet një shqetësim kur nyja pranuese mund pranon shumë frejma me një
shpejtësi më të madhe se sa që mund ti procesoj ndersa me ane te flow control kontrollohet rrjedha
e tyre. Kështu që pa flow control buferi i pranuesit mund të mbingarkohet ashtu që frejmat të
humbasin.
TCP ka një congestion-control mechanism që ul shpejtësinë e shtresës së transportit të dërguesit
TCP kur një apo më shumë linçe mes burimit dhe destinacionit të pritësit tejmbushen..

### Sources

- Afate me zgjidhje 1.pdf Q77

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-160

### Front

Llogarite kohen që nevojitet për të dërguar një fajll nga hosti A deri ne hostin B me
madhësi 6400k bita, nëpër rrjetën TDM që ka 24 slote dhe ka “bandwidth” 1536 kbps. Le
të supozojmë se 1 sekondë nevojitet për të krijuar lidhjen nga hosti A deri në hostin B?

### Back

Bm=BW/Sl=1536kb/s//24=64kb/s
T=S/Bm+1s=6400*10^3b/64*10^3b/s+1s=100s+1s=101s

### Sources

- Afate me zgjidhje 1.pdf Q79

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-161

### Front

Llogarite kohen që nevojitet për të dërguar një fajll nga hosti A deri ne hostin B me
madhësi 12800k bita, nëpër rrjetën TDM që ka 24 slote dhe ka “bandwidth” 1536 kbps.
Le të supozojmë se 0.5 sekondë nevojitet për të krijuar lidhjen nga hosti A deri në hostin
B?

### Back

Bm=BW/Sl=1536kb/s//24=64kb/s
T=S/Bm+0.5s=12800*10^3b/64*10^3b/s+0.5s=200s+0.5s=200.5s

### Sources

- Afate me zgjidhje 1.pdf Q80

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-162

### Front

Këngën me madhësi 4.5 Mbyte e shkarkoni përmes lidhjes simetrike DSL 2 [Mbps]. Sa
kohe ju nevojitet për te shkarkuar këtë këngë?

### Back

T=S/BW=4.5MByte//2Mbit/s=4.5*8*10^6 bit // 2*10^6 bit/s = 18s

### Sources

- Afate me zgjidhje 1.pdf Q81

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-163

### Front

Këngën me madhësi 7.5 Mbyte e shkarkoni përmes lidhjes simetrike DSL 3 [Mbps]. Sa
kohe ju nevojitet për te shkarkuar këtë këngë?

### Back

T=S/BW=7.5MByte//3Mbit/s=7.5*8*10^6 bit // 3*10^6 bit/s = 20s

### Sources

- Afate me zgjidhje 1.pdf Q82

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-164

### Front

Këngën me gjatësi 6 minuta (me madhësi 6 MByte) e ngarkoni (upload) përmes lidhjes
simetrike 6 Mbps te Internetit. Sa kohe ju nevojitet për te ngarkuar këtë këngë?

### Back

T=S/BW=6MByte//6Mbit/s=6*8*10^6 bit // 6*10^6 bit/s = 8s

### Sources

- Afate me zgjidhje 1.pdf Q83

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-165

### Front

Këngën me gjatësi 8 minuta (me madhësi 6 MByte) e ngarkoni (upload) përmes lidhjes
asimetrike 10Mbps të Internetit, me download (shkarkim) 8 Mbps. Sa kohë ju nevojitet
për ta ngarkuar këtë këngë?

### Back

Nese lidhja eshte asimetrike atehere download dhe upload kan vlera te ndryshme ku shuma e tyre e
jep trasmision rate te rrjetit . Nese lidhja eshte 10Mbps dhe download eshte 8Mbps atehere upload
eshte 2Mbps .
K=S/BW=6MByte//6Mbit/s=6*8*10^6 bit // 2*10^6 bit/s = 24s

### Sources

- Afate me zgjidhje 1.pdf Q84

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-166

### Front

Çka është dhe si punon VPN?

### Back

VPN (Virtual Private Network ) është një rrjete e përdorur për të shtuar sigurinë dhe privatësinë në
rrjetet private dhe publike, si WiFi Hotspots dhe Internet. VPN-të përdoren më shpesh nga
korporatat për të mbrojtur të dhëna të sensitive .

### Sources

- Afate me zgjidhje 1.pdf Q85

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-167

### Front

Çka shërben “Virtual Local Area Network” (VLAN) switch-i?

### Back

Vlan eshte ndarje virtuale e switch-it qe mundeson me 1 pasisje te vetme switch te bejme me
shume se nje rrjete .

### Sources

- Afate me zgjidhje 1.pdf Q86

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-168

### Front

. Çka shërben VLR dhe HLR te mobile GSM rrjetat?

### Back

HLR te GSM rrjetat mobile sherben si nje ‘Home Network databaze’, I cili permban numrin
permanet te tel, informacionet e profilit, informacionet me vendndodhjen momentale, mund te jete
edhe network tjeter . VLR-ja te mobile GSM rrjetat sherben si nje databaze me regjistra per secilin
perdorues qe gjendet momentalisht ne rrjet.

### Sources

- Afate me zgjidhje 1.pdf Q89

Tags: rrjeta exam solved_bank source::afate_me_zgjidhje_1

## EX-169

### Front

Sa është shkalla e penetrimit të Internetit në Kosovë? Pse është ashtu sipas mendimit tuaj?

![assets/exam-flashcards/afati-shkurt-2023-p01-q01.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p01-q01.png)

### Back

Për provim jep përgjigje arsyetuese: shkalla është e lartë sepse Kosova ka përdorim të gjerë të smartphone-ve, rrjete mobile/fiber dhe popullsi të re; por mund të ketë dallime mes zonave urbane dhe rurale, të ardhurave dhe cilësisë së infrastrukturës. Nëse kërkohet numër fiks, kontrollo statistikën më të fundit nga ARKEP/ASK.

### Sources

- Afati shkurt 2023.pdf Q1 p.1
- download. (5).pdf Q1 p.1
- 2023Janar.pdf Q1 p.1

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_5 source::2023janar

## EX-170

### Front

Internet protokolli sipas renditjes (top-down) përbehet nga këto 5 shtresa:
1. ______________________
2. ______________________
3. ______________________
4. ______________________
5. ______________________

![assets/exam-flashcards/afati-shkurt-2023-p01-q02.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p01-q02.png)

### Back

Pesë shtresat top-down janë: Application, Transport, Network, Link, Physical.

### Sources

- Afati shkurt 2023.pdf Q2 p.1
- Afati shkurt 2024.pdf Q2 p.1
- Afati shkurt 2025.pdf Q2 p.1
- download. (1).pdf Q2 p.1
- download. (5).pdf Q2 p.1
- 2023Janar.pdf Q2 p.1

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::afati_shkurt_2024 source::afati_shkurt_2025 source::download_1 source::download_5 source::2023janar

## EX-171

### Front

Çka është RTT (Round Trip Time)?

![assets/exam-flashcards/afati-shkurt-2023-p01-q03.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p01-q03.png)

### Back

RTT (Round Trip Time) është koha që i duhet një pakete/mesazhi të shkojë nga klienti te serveri dhe që përgjigjja/ACK të kthehet prapë te klienti.

### Sources

- Afati shkurt 2023.pdf Q3 p.1
- download. (5).pdf Q3 p.1
- 2023Janar.pdf Q3 p.1

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_5 source::2023janar

## EX-172

### Front

Si punon NAT-i? (përdore faqen mbrapa, sipas nevojës, për skica)

![assets/exam-flashcards/afati-shkurt-2023-p01-q04.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p01-q04.png)

### Back

NAT lejon shumë hostë me IP private të përdorin një IP publike. Router-i NAT zëvendëson source private IP/port me public IP/port kur paketa del në Internet dhe ruan mapping në NAT table. Kur kthehet përgjigjja, router-i përdor portin publik për ta gjetur hostin privat dhe e rikthen destination IP/port. Portet janë çelësi që dallon lidhjet e shumë hostëve pas të njëjtës IP publike.

### Sources

- Afati shkurt 2023.pdf Q4 p.1
- Afati shkurt 2024.pdf Q4 p.1
- download. (1).pdf Q4 p.1
- download. (2).pdf Q4 p.1
- download. (3).pdf Q4 p.1
- download. (5).pdf Q4 p.1
- 2019Qershor.pdf Q4 p.1
- 2019Shtatore.pdf Q4 p.1
- 2020Qershor.pdf Q4 p.1
- 2023Janar.pdf Q4 p.1

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::afati_shkurt_2024 source::download_1 source::download_2 source::download_3 source::download_5 source::2019qershor source::2019shtatore

## EX-173

### Front

Nëse aplikacioni gjeneron paketa 40 bajtëshe (bytes) të shënimeve çdo 20 msec dhe secila paket
enkapsulohet në TCP segment dhe pastaj në IP datagram. Sa për qind (%) e shënimeve janë
overhead (mbingarkesë) dhe sa për qind (%) janë shënime të aplikacionit?

![assets/exam-flashcards/afati-shkurt-2023-p02-q05.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p02-q05.png)

### Back

50% overhead, 50% shenime.

### Sources

- Afati shkurt 2023.pdf Q5 p.2
- download. (5).pdf Q5 p.2
- 2023Janar.pdf Q5 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_5 source::2023janar

## EX-174

### Front

Tek DHCP protokolli, i klienti i sapo ardhur në rrejt, dërgon paketën e parë me “destination
address: 255.255.255.255”. Pse?

![assets/exam-flashcards/afati-shkurt-2023-p02-q06.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p02-q06.png)

### Back

Klienti i ri ende nuk ka IP adresë dhe nuk e di adresën e DHCP serverit. Prandaj dërgon DHCPDISCOVER si broadcast me destination `255.255.255.255`, që ta dëgjojë çdo DHCP server në LAN.

### Sources

- Afati shkurt 2023.pdf Q6 p.2
- Afati shkurt 2024.pdf Q6 p.2
- Afati shkurt 2025.pdf Q6 p.2
- download. (1).pdf Q6 p.2
- download. (5).pdf Q6 p.2
- 2023Janar.pdf Q6 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::afati_shkurt_2024 source::afati_shkurt_2025 source::download_1 source::download_5 source::2023janar

## EX-175

### Front

Tek MAC shtresa, gjatë dërgimit te datagramit ne Internet, nga kompjuteri A tek kompjuteri B,
dërguesi (kompjuteri A) si MAC adrese vendosë ________________________?

![assets/exam-flashcards/afati-shkurt-2023-p02-q07.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p02-q07.png)

### Back

Nëse B është jashtë LAN-it lokal, kompjuteri A vendos si destination MAC adresën e default gateway/router-it në LAN, jo MAC adresën finale të B. Nëse B është në të njëjtin LAN, A vendos MAC adresën e B.

### Sources

- Afati shkurt 2023.pdf Q7 p.2
- Afati shkurt 2024.pdf Q7 p.2
- download. (1).pdf Q7 p.2
- download. (5).pdf Q7 p.2
- 2023Janar.pdf Q7 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::afati_shkurt_2024 source::download_1 source::download_5 source::2023janar

## EX-176

### Front

Pse përdorim sot CDN?

![assets/exam-flashcards/afati-shkurt-2023-p02-q09.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p02-q09.png)

### Back

CDN përdoret për ta vendosur përmbajtjen më afër përdoruesve në serverë të shpërndarë. Kjo ul latency/RTT, rrit throughput-in, zvogëlon ngarkesën në origin server dhe e bën shërbimin më rezistent ndaj trafikimit të lartë ose dështimeve.

### Sources

- Afati shkurt 2023.pdf Q9 p.2
- download. (1).pdf Q9 p.2
- download. (2).pdf Q9 p.2
- download. (3).pdf Q9 p.2
- download. (5).pdf Q9 p.2
- 2020Qershor.pdf Q9 p.2
- 2023Janar.pdf Q9 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_1 source::download_2 source::download_3 source::download_5 source::2020qershor source::2023janar

## EX-177

### Front

Një DNS “resource record” (Name, Value, Type, TTL) është i tipit MX (pra Type=MX). Çka
përmban atëherë “Value”?

![assets/exam-flashcards/afati-shkurt-2023-p02-q10.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p02-q10.png)

### Back

Për DNS RR me Type=MX, `Value` përmban emrin canonical/hostname të mail serverit për domain-in.

### Sources

- Afati shkurt 2023.pdf Q10 p.2
- download. (1).pdf Q10 p.2
- download. (5).pdf Q10 p.2
- 2019Qershor.pdf Q9 p.2
- 2023Janar.pdf Q10 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_1 source::download_5 source::2019qershor source::2023janar

## EX-178

### Front

Çka është ndryshimi ne mes te “Routing” dhe “Forwarding”. Përshkruani shkurtimisht secilin
prej tyre.

![assets/exam-flashcards/afati-shkurt-2023-p03-q11.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p03-q11.png)

### Back

Forwarding është veprimi lokal në router: merr paketën nga input port dhe e dërgon në output port sipas forwarding table. Routing është procesi global që llogarit rrugën/forwarding tables duke përdorur algoritme dhe protokolle routing.

### Sources

- Afati shkurt 2023.pdf Q11 p.3
- download. (1).pdf Q11 p.2
- download. (5).pdf Q11 p.3
- 2023Janar.pdf Q11 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_1 source::download_5 source::2023janar

## EX-179

### Front

Përshkruaj dallimet kryesore ne mes Link-State (LS) vs. Distance-Vector (DV) Routing
Algorithm ?

![assets/exam-flashcards/afati-shkurt-2023-p03-q12.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p03-q12.png)

### Back

Link-State: çdo router mëson topologjinë/koston e linkeve dhe llogarit rrugët me Dijkstra; ka pamje më globale. Distance-Vector: router-at shkëmbejnë me fqinjët distancat e tyre deri te destinacionet dhe përditësojnë me Bellman-Ford; është më i thjeshtë, por mund të ketë count-to-infinity/konvergjencë më të ngadaltë.

### Sources

- Afati shkurt 2023.pdf Q12 p.3
- download. (1).pdf Q12 p.3
- download. (2).pdf Q12 p.3
- download. (3).pdf Q12 p.3
- download. (4).pdf Q12 p.3
- download. (5).pdf Q12 p.3
- 2019Qershor.pdf Q12 p.3
- 2019Shtatore.pdf Q12 p.3
- 2020Qershor.pdf Q12 p.3
- 2022Qershor.pdf Q12 p.3
- 2023Janar.pdf Q12 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_1 source::download_2 source::download_3 source::download_4 source::download_5 source::2019qershor source::2019shtatore

## EX-180

### Front

Të kompletohet kodi në vijim për implementimi e një UDP serveri të thjeshtë në Python:
from socket import *
port = 9000
serverSocket = socket(AF_INET, _______________)
serverSocket.bind(('',port))
while True:
message, client = serverSocket.recvfrom(2048)
serverSocket.sendto(____________, _______)

![assets/exam-flashcards/afati-shkurt-2023-p03-q13.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p03-q13.png)

### Back

Përdoret UDP socket, pra `SOCK_DGRAM`.

Kodi i plotësuar:
```python
from socket import *
port = 9000
serverSocket = socket(AF_INET, SOCK_DGRAM)
serverSocket.bind(('', port))
while True:
    message, client = serverSocket.recvfrom(2048)
    serverSocket.sendto(message.upper(), client)
```
Nëse kërkohet vetëm echo, rreshti i fundit mund të jetë `serverSocket.sendto(message, client)`.

### Sources

- Afati shkurt 2023.pdf Q13 p.3
- download. (5).pdf Q13 p.3
- 2023Janar.pdf Q13 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_5 source::2023janar

## EX-181

### Front

Çka dallon SMTP me POP3 protokollin?

![assets/exam-flashcards/afati-shkurt-2023-p03-q14.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p03-q14.png)

### Back

CSMA/CD eshte nje media access protokoll qe perdoret ne LAN dhe paraqet nje grup
rregullash qe percaktojne se si pajisjet e rrjetes reagojne kur dy pajisje tentojne te perdorin nje
kanal transmetues te njejte te te dhenave ne te njejten kohe(qe nihet si collision).

### Sources

- Afati shkurt 2023.pdf Q14 p.3
- download. (5).pdf Q14 p.3
- 2023Janar.pdf Q14 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_5 source::2023janar

## EX-182

### Front

Plotësoje ARP tabelën për nyjën (kompjuterin) me IP adresë 10.20.30.40
IP Address ??? TTL

![assets/exam-flashcards/afati-shkurt-2023-p03-q15.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p03-q15.png)

### Back

ARP tabela ruan mapping `IP address -> MAC address` për hostët në LAN dhe një TTL/age për secilin rekord. Kolona `???` është MAC Address. Shembull:
`IP Address | MAC Address | TTL`
`10.20.30.1 | aa:bb:cc:dd:ee:ff | 120s`
`10.20.30.41 | 11:22:33:44:55:66 | 120s`

### Sources

- Afati shkurt 2023.pdf Q15 p.3
- Afati shkurt 2025.pdf Q15 p.3
- download. (4).pdf Q16 p.4
- download. (5).pdf Q15 p.3
- 2022Qershor.pdf Q16 p.4
- 2023Janar.pdf Q15 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::afati_shkurt_2025 source::download_4 source::download_5 source::2022qershor source::2023janar

## EX-183

### Front

Përshkruaj te paktën 3 standarde nga IEEE 802.11?

![assets/exam-flashcards/afati-shkurt-2023-p04-q16.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p04-q16.png)

### Back

802.11 standardi pershkruan specifikacionet mbi te cilat implementohet WLAN(Wireless
Local Area Network). Ky standard specifikon lidhjet e pajisjeve ne rrjetat pa tela.

### Sources

- Afati shkurt 2023.pdf Q16 p.4
- download. (1).pdf Q16 p.4
- download. (5).pdf Q16 p.4
- 2023Janar.pdf Q16 p.4

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_1 source::download_5 source::2023janar

## EX-184

### Front

Ju merrni shërbimin e Internetit nga Kujtesa. IP adresa që Kujtesa iu ndan është reale fikse
82.114.86.203. Ju duhet ta dizajnoni rrjetën për një kompani me 6 kompjuter, një shtypës
(network enabled) dhe ueb dhe email server. Vizatoni skemën e lidhjes se këtyre kompjuterëve,
shtypësit në LAN dhe serverëve ne Internet se bashku me te gjitha IP adresat e pajisjeve te
lidhura
(Shfrytëzo faqen mbrapa për skica! Kjo detyrë ka max. 6 pikë!)

![assets/exam-flashcards/afati-shkurt-2023-p04-q17.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p04-q17.png)

### Back

Zgjidhje tipike: vendos router-in në kufi me WAN/public IP `82.114.86.203` dhe LAN privat p.sh. `192.168.0.0/24`.
- Router LAN/default gateway: `192.168.0.1`
- PC-të: `192.168.0.10-192.168.0.15`
- Printer: `192.168.0.20`
- Web server: `192.168.0.80`
- Email server: `192.168.0.25` ose FTP server: `192.168.0.21`, varësisht nga pyetja
- Të gjithë hostët përdorin gateway `192.168.0.1`.
Router-i bën NAT/PAT për klientët. Për qasje nga jashtë te serverët, konfiguro port forwarding/static NAT.

### Sources

- Afati shkurt 2023.pdf Q17 p.4
- Afati shkurt 2023.pdf Q18 p.4
- download. (5).pdf Q17 p.4
- download. (5).pdf Q18 p.4
- 2023Janar.pdf Q17 p.4
- 2023Janar.pdf Q18 p.4

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_5 source::2023janar

## EX-185

### Front

Çka duhet të konfigurohet shtesë te routeri nga detyra paraprake qe te kemi qasje ne ueb server
nga çdo kompjuter të lidhur në Internet.

![assets/exam-flashcards/afati-shkurt-2023-p04-q19.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p04-q19.png)

### Back

Duhet port forwarding/static NAT nga IP publike e router-it te IP private e web serverit. Minimalisht hap/forward portin TCP 80 për HTTP dhe zakonisht 443 për HTTPS. Nëse ka DNS publik, A-record duhet të tregojë te IP publike e router-it.

### Sources

- Afati shkurt 2023.pdf Q19 p.4
- Afati shkurt 2024.pdf Q19 p.4
- Afati shkurt 2025.pdf Q19 p.4
- download. (5).pdf Q19 p.4
- 2023Janar.pdf Q19 p.4

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::afati_shkurt_2024 source::afati_shkurt_2025 source::download_5 source::2023janar

## EX-186

### Front

Shkruani formulën për vonesat ne Internet. Përshkruaj secilën komponentë.

![assets/exam-flashcards/afati-shkurt-2023-p04-q20.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2023-p04-q20.png)

### Back

Vonesa nodale totale:
`d_nodal = d_proc + d_queue + d_trans + d_prop`
- `d_proc`: processing delay, kontroll header/checksum dhe vendim forwarding.
- `d_queue`: pritja në queue/buffer.
- `d_trans = L/R`: koha për ta futur paketën L-bit në link me rate R.
- `d_prop = d/s`: koha që sinjali udhëton në medium.

### Sources

- Afati shkurt 2023.pdf Q20 p.4
- download. (5).pdf Q20 p.4
- 2023Janar.pdf Q20 p.4

Tags: rrjeta exam exam_form source::afati_shkurt_2023 source::download_5 source::2023janar

## EX-187

### Front

Cilët janë dy protokollet mbi te cilët është ndërtuar Interneti?

![assets/exam-flashcards/afati-shkurt-2024-p01-q01.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p01-q01.png)

### Back

Dy protokollet bazë mbi të cilat është ndërtuar Interneti janë TCP dhe IP, shpesh të quajtura TCP/IP.

### Sources

- Afati shkurt 2024.pdf Q1 p.1

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-188

### Front

Çka është DOCSIS?

![assets/exam-flashcards/afati-shkurt-2024-p01-q03.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p01-q03.png)

### Back

DOCSIS = Data Over Cable Service Interface Specification. Është standard për qasje në Internet përmes rrjeteve kabllore/HFC, ku cable modem komunikon me CMTS-in e operatorit.

### Sources

- Afati shkurt 2024.pdf Q3 p.1

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-189

### Front

Përshkruani vonesat router-in A:

![assets/exam-flashcards/afati-shkurt-2024-p02-q05.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p02-q05.png)

### Back

Katër vonesat kryesore janë:
- Processing delay: router-i lexon header-in, kontrollon gabime dhe vendos dalje.
- Queueing delay: paketa pret në buffer nëse linku dalës është i zënë.
- Transmission delay: `L/R`, koha për t'i vendosur bitat në link.
- Propagation delay: `d/s`, koha e përhapjes së sinjalit në medium.

### Sources

- Afati shkurt 2024.pdf Q5 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-190

### Front

Çka është “average throughput” në rrjeta kompjuterike?

![assets/exam-flashcards/afati-shkurt-2024-p02-q08.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p02-q08.png)

### Back

Average throughput është mesatarja e shpejtësisë reale të dorëzimit të bitave gjatë një intervali kohe: `throughput mesatar = bitat e transferuar / koha totale`. Varet nga bottleneck link, congestion dhe protokollet.

### Sources

- Afati shkurt 2024.pdf Q8 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-191

### Front

Shpjegoni, me te paktën 3 fjali, si punon “Conditional GET”

![assets/exam-flashcards/afati-shkurt-2024-p02-q09.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p02-q09.png)

### Back

Conditional GET përdoret për cache validation. Klienti/proxy dërgon kërkesë HTTP GET me `If-Modified-Since` ose `If-None-Match` (ETag). Nëse objekti nuk ka ndryshuar, serveri kthen `304 Not Modified` pa e dërguar objektin prapë. Nëse ka ndryshuar, kthen `200 OK` me versionin e ri.

### Sources

- Afati shkurt 2024.pdf Q9 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-192

### Front

Çka janë “fake emails”? Pse është e mundur? Si mund të mbrohemi?

![assets/exam-flashcards/afati-shkurt-2024-p03-q10.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p03-q10.png)

### Back

Fake email/spoofing është email ku fusha si `From:` falsifikohet. Është e mundur sepse SMTP historikisht nuk e verifikon fort identitetin e dërguesit dhe header-at mund të manipulohen. Mbrojtja: SPF, DKIM, DMARC, filtra anti-spam/phishing, TLS, verifikim i domain-it dhe kujdes ndaj linkeve/attachments.

### Sources

- Afati shkurt 2024.pdf Q10 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-193

### Front

Si quhet TLD e Kosovës?

![assets/exam-flashcards/afati-shkurt-2024-p03-q11.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p03-q11.png)

### Back

Kosova nuk ka ccTLD zyrtar të deleguar në DNS root. `XK`/`.xk` përdoret shpesh si kod jozyrtar/teknik, por nuk është ccTLD zyrtar si p.sh. `.al` ose `.de`.

### Sources

- Afati shkurt 2024.pdf Q11 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-194

### Front

What is the HOL blocking issue in HTTP/1.1? How does HTTP/2 attempt to
solve it?

![assets/exam-flashcards/afati-shkurt-2024-p03-q12.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p03-q12.png)

### Back

HOL blocking në HTTP/1.1 ndodh kur një përgjigje e ngadalshme në një lidhje TCP bllokon përgjigjet pas saj, sidomos me pipelining. HTTP/2 e zbut këtë duke përdorur binary framing dhe multiplexing: shumë streams ndajnë të njëjtën lidhje TCP. Kujdes: HTTP/2 ende mund të vuajë nga TCP-level HOL blocking në rast humbjeje paketash.

### Sources

- Afati shkurt 2024.pdf Q12 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-195

### Front

Why do HTTP, SMTP, and IMAP run on top of TCP rather than on UDP?

![assets/exam-flashcards/afati-shkurt-2024-p03-q13.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p03-q13.png)

### Back

Sepse HTTP, SMTP dhe IMAP kanë nevojë për transmetim të besueshëm, të renditur dhe pa humbje të stream-it të bajtave. TCP ofron reliability, ACK/retransmission, flow control dhe congestion control. Me UDP këto do duhej t'i implementonte vetë aplikacioni.

### Sources

- Afati shkurt 2024.pdf Q13 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-196

### Front

Source dhe destination port jane vlera:_______________

![assets/exam-flashcards/afati-shkurt-2024-p03-q14.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p03-q14.png)

### Back

Source port dhe destination port janë fusha 16-bitëshe në header-in TCP/UDP. Ato identifikojnë procesin/aplikacionin dërgues dhe pranues në hosta.

### Sources

- Afati shkurt 2024.pdf Q14 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-197

### Front

Plotësoje ARP tabelën për nyjën (kompjuterin) me IP adresë 192.168.1.10
IP Address ??? TTL

![assets/exam-flashcards/afati-shkurt-2024-p03-q15.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p03-q15.png)

### Back

ARP tabela ruan mapping `IP address -> MAC address` për hostët në LAN dhe një TTL/age për secilin rekord. Kolona `???` është MAC Address. Shembull:
`IP Address | MAC Address | TTL`
`10.20.30.1 | aa:bb:cc:dd:ee:ff | 120s`
`10.20.30.41 | 11:22:33:44:55:66 | 120s`

### Sources

- Afati shkurt 2024.pdf Q15 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-198

### Front

Përshkruaj si arrin TCP ta implementoj “reliability”

![assets/exam-flashcards/afati-shkurt-2024-p04-q16.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p04-q16.png)

### Back

TCP arrin reliability me checksum, sequence numbers, ACK, timer/timeout, ri-transmetim, sliding window, flow control dhe congestion control. Marrësi i përdor sequence numbers për renditje dhe deduplikim; dërguesi ri-transmeton segmentet që nuk konfirmohen.

### Sources

- Afati shkurt 2024.pdf Q16 p.4

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-199

### Front

Çka është dallimi ne mes algoritmeve te routimit: Link State vs. Distance Vector?

![assets/exam-flashcards/afati-shkurt-2024-p04-q17.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p04-q17.png)

### Back

Link-State: çdo router mëson topologjinë/koston e linkeve dhe llogarit rrugët me Dijkstra; ka pamje më globale. Distance-Vector: router-at shkëmbejnë me fqinjët distancat e tyre deri te destinacionet dhe përditësojnë me Bellman-Ford; është më i thjeshtë, por mund të ketë count-to-infinity/konvergjencë më të ngadaltë.

### Sources

- Afati shkurt 2024.pdf Q17 p.4
- Afati shkurt 2025.pdf Q17 p.4

Tags: rrjeta exam exam_form source::afati_shkurt_2024 source::afati_shkurt_2025

## EX-200

### Front

Ju merrni shërbimin e Internetit nga Kujtesa. IP adresa që Kujtesa iu ndan është reale fikse
9.9.9.9. Ju duhet ta dizajnoni rrjetën për një kompani me 6 kompjuter, një shtypës (network
enabled) dhe ueb dhe email server. Vizatoni skemën e lidhjes se këtyre kompjuterëve, shtypësit
në LAN dhe serverëve ne Internet se bashku me te gjitha IP adresat e pajisjeve te lidhura
(Shfrytëzo faqen mbrapa për skica!)

![assets/exam-flashcards/afati-shkurt-2024-p04-q18.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2024-p04-q18.png)

### Back

Zgjidhje tipike: vendos router-in në kufi me WAN/public IP `9.9.9.9` dhe LAN privat p.sh. `192.168.0.0/24`.
- Router LAN/default gateway: `192.168.0.1`
- PC-të: `192.168.0.10-192.168.0.15`
- Printer: `192.168.0.20`
- Web server: `192.168.0.80`
- Email server: `192.168.0.25` ose FTP server: `192.168.0.21`, varësisht nga pyetja
- Të gjithë hostët përdorin gateway `192.168.0.1`.
Router-i bën NAT/PAT për klientët. Për qasje nga jashtë te serverët, konfiguro port forwarding/static NAT.

### Sources

- Afati shkurt 2024.pdf Q18 p.4

Tags: rrjeta exam exam_form source::afati_shkurt_2024

## EX-201

### Front

Çka është Interneti?

![assets/exam-flashcards/afati-shkurt-2025-p01-q01.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p01-q01.png)

### Back

Internetin mund ta kuptojme si:
-miliona paisje llogaritese te konektuara,
-rrjet e rrjetave,
-infrastrukture qe ofron sherbime per aplikacione
-ofron nderfaqe programuese per aplikacionet

### Sources

- Afati shkurt 2025.pdf Q1 p.1

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-202

### Front

Pse teknikat e “packet switching” përdoren per transmetim të shënimeve në Internet?

![assets/exam-flashcards/afati-shkurt-2025-p01-q03.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p01-q03.png)

### Back

Përdoret sepse Interneti bart trafik bursty nga shumë aplikacione. Packet switching ndan rrjetin në paketa, lejon ndarje statistikore të bandwidth-it, përdor rrugë alternative kur ka dështime dhe nuk kërkon krijim të qarkut të dedikuar për çdo komunikim.

### Sources

- Afati shkurt 2025.pdf Q3 p.1

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-203

### Front

Si punon NAT-i? (përdore faqen mbrapa për skica)

![assets/exam-flashcards/afati-shkurt-2025-p01-q04.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p01-q04.png)

### Back

NAT lejon shumë hostë me IP private të përdorin një IP publike. Router-i NAT zëvendëson source private IP/port me public IP/port kur paketa del në Internet dhe ruan mapping në NAT table. Kur kthehet përgjigjja, router-i përdor portin publik për ta gjetur hostin privat dhe e rikthen destination IP/port. Portet janë çelësi që dallon lidhjet e shumë hostëve pas të njëjtës IP publike.

### Sources

- Afati shkurt 2025.pdf Q4 p.1

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-204

### Front

Përshkruani 4 llojet e vonesave ne rrjeta kompjuterike:

![assets/exam-flashcards/afati-shkurt-2025-p02-q05.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p02-q05.png)

### Back

Katër vonesat kryesore janë:
- Processing delay: router-i lexon header-in, kontrollon gabime dhe vendos dalje.
- Queueing delay: paketa pret në buffer nëse linku dalës është i zënë.
- Transmission delay: `L/R`, koha për t'i vendosur bitat në link.
- Propagation delay: `d/s`, koha e përhapjes së sinjalit në medium.

### Sources

- Afati shkurt 2025.pdf Q5 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-205

### Front

Tek MAC shtresa, gjatë dërgimit te datagramit në Internet, nga kompjuteri A tek kompjuteri B,
dërguesi (kompjuteri A) si MAC adresë vendosë vlerën: ________________________?

![assets/exam-flashcards/afati-shkurt-2025-p02-q07.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p02-q07.png)

### Back

Nëse B është jashtë LAN-it lokal, kompjuteri A vendos si destination MAC adresën e default gateway/router-it në LAN, jo MAC adresën finale të B. Nëse B është në të njëjtin LAN, A vendos MAC adresën e B.

### Sources

- Afati shkurt 2025.pdf Q7 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-206

### Front

Çka shërben komanda:
C:\Users\Blerim Rexha>ipconfig /all

![assets/exam-flashcards/afati-shkurt-2025-p02-q08.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p02-q08.png)

### Back

Komanda ping sherben per te testuar lidhjen me rrjeten(internetin) . 8.8.8.8 eshte ip adresa e DNS
serverit publik te Google . Ndersa ping 8.8.8.8 –t ben qe komanda ping te ekzekutohet deri sa ta
ndalim vet p.sh Ctrl+C .

### Sources

- Afati shkurt 2025.pdf Q8 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-207

### Front

Shpjegoni dallimin kryesor në mes të HTTP 1.1 vs. HTTP 2 protokollit?

![assets/exam-flashcards/afati-shkurt-2025-p02-q09.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p02-q09.png)

### Back

HTTP/1.1 është tekstual dhe zakonisht përdor lidhje persistent, por kërkesat/përgjigjet mund të bllokohen nga HOL blocking. HTTP/2 përdor binary framing, multiplexing të shumë streams mbi një TCP connection dhe header compression (HPACK), prandaj shfrytëzon më mirë lidhjen dhe ul vonesën aplikative.

### Sources

- Afati shkurt 2025.pdf Q9 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-208

### Front

SMTP protokolli bazohet me UDP, çka do të thotë kjo?

![assets/exam-flashcards/afati-shkurt-2025-p02-q10.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p02-q10.png)

### Back

Kjo fjali është gabim për SMTP real: SMTP normalisht punon mbi TCP, jo UDP (porti 25 për server-server, 587 për submission, 465 për SMTPS). Nëse do të ishte mbi UDP, do të ishte connectionless dhe pa garanci të renditjes/dorëzimit, gjë që nuk i përshtatet email-it.

### Sources

- Afati shkurt 2025.pdf Q10 p.2

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-209

### Front

Çka përmban një DNS rekord?

![assets/exam-flashcards/afati-shkurt-2025-p03-q11.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p03-q11.png)

### Back

Një DNS resource record ka formatin `(Name, Value, Type, TTL)`. Kuptimi i `Value` varet nga `Type`: A -> IP address; NS -> authoritative DNS server; CNAME -> canonical name; MX -> mail server.

### Sources

- Afati shkurt 2025.pdf Q11 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-210

### Front

Tek “Reliable data transfer protocol (rdt)” çka shërben timer-i?

![assets/exam-flashcards/afati-shkurt-2025-p03-q12.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p03-q12.png)

### Back

Timer-i përdoret për të zbuluar humbjen e paketës ose ACK-ut. Dërguesi e nis timer-in kur dërgon paketë; nëse ACK nuk arrin para timeout-it, paketa ri-transmetohet.

### Sources

- Afati shkurt 2025.pdf Q12 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-211

### Front

Shënoni tri dallime ne mes te Go-Back-N vs. Selective repart?

![assets/exam-flashcards/afati-shkurt-2025-p03-q13.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p03-q13.png)

### Back

Dallimet kryesore:
- Go-Back-N pranon vetëm paketat në rend dhe i hedh ato jashtë rendit; Selective Repeat i buffer-on.
- Go-Back-N pas humbjes ri-transmeton nga paketa e humbur e tutje; Selective Repeat ri-transmeton vetëm paketat e humbura.
- Go-Back-N përdor cumulative ACK; Selective Repeat përdor ACK selektiv për secilën paketë.
- Zakonisht GBN ka një timer për paketën më të vjetër pa ACK; SR ka timer për çdo paketë të pa-konfirmuar.

### Sources

- Afati shkurt 2025.pdf Q13 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-212

### Front

Shenoni vleren per Seq:_____ dhe ACK =______

![assets/exam-flashcards/afati-shkurt-2025-p03-q14.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p03-q14.png)

### Back

Segmenti final është ACK nga Host A pas pranimit të echoed `C` nga Host B. A kishte dërguar një bajt me `Seq=42`, prandaj sekuenca e radhës e A është `43`. B dërgoi një bajt me `Seq=79`, prandaj ACK i radhës është `80`.

Përgjigjja: `Seq = 43`, `ACK = 80`.

### Sources

- Afati shkurt 2025.pdf Q14 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-213

### Front

Çka kushtëzon rregulla: “Longest prefix matching”?

![assets/exam-flashcards/afati-shkurt-2025-p03-q16.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p03-q16.png)

### Back

Longest prefix matching do të thotë që router-i zgjedh hyrjen në forwarding table me prefiksin më të gjatë që përputhet me IP adresën e destinacionit. Rregulli kushtëzon daljen/interfejsin e paketës kur disa rreshta përputhen njëkohësisht.

### Sources

- Afati shkurt 2025.pdf Q16 p.3

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-214

### Front

Ju merrni shërbimin e Internetit nga ISP Broadcast. IP adresa që iu ndan është reale, fikse:
185.188.217.233. Ju duhet ta dizajnoni rrjetën për një kompani me 6 kompjuter, një shtypës
(network enabled) dhe ueb dhe email server. Vizatoni skemën e lidhjes se këtyre kompjuterëve,
shtypësit në LAN dhe serverëve ne Internet se bashku me te gjitha IP adresat e pajisjeve te lidhura
ne LAN.
(Shfrytëzo faqen mbrapa për skica!)

![assets/exam-flashcards/afati-shkurt-2025-p04-q18.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/afati-shkurt-2025-p04-q18.png)

### Back

Zgjidhje tipike: vendos router-in në kufi me WAN/public IP `185.188.217.233` dhe LAN privat p.sh. `192.168.0.0/24`.
- Router LAN/default gateway: `192.168.0.1`
- PC-të: `192.168.0.10-192.168.0.15`
- Printer: `192.168.0.20`
- Web server: `192.168.0.80`
- Email server: `192.168.0.25` ose FTP server: `192.168.0.21`, varësisht nga pyetja
- Të gjithë hostët përdorin gateway `192.168.0.1`.
Router-i bën NAT/PAT për klientët. Për qasje nga jashtë te serverët, konfiguro port forwarding/static NAT.

### Sources

- Afati shkurt 2025.pdf Q18 p.4

Tags: rrjeta exam exam_form source::afati_shkurt_2025

## EX-215

### Front

Shëno emrin e plotë të shkurtesave:
IP -
CSMA -
DOCSIS -

![assets/exam-flashcards/download-1-p01-q01.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p01-q01.png)

### Back

- IP = Internet Protocol
- CSMA = Carrier Sense Multiple Access
- DOCSIS = Data Over Cable Service Interface Specification

### Sources

- download. (1).pdf Q1 p.1

Tags: rrjeta exam exam_form source::download_1

## EX-216

### Front

Interneti, qe e njohim, bazohet ne komutimin me paketa (packet switching). Pse komutimi me
paketa është me efecientë se komutimi me qarqe?

![assets/exam-flashcards/download-1-p01-q03.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p01-q03.png)

### Back

Packet switching është më efikas për trafik bursty sepse burimet ndahen statistikisht: lidhja përdoret vetëm kur ka paketa për t'u dërguar. Circuit switching rezervon kapacitet të dedikuar edhe kur përdoruesi është idle, prandaj mund të harxhojë bandwidth.

### Sources

- download. (1).pdf Q3 p.1
- download. (2).pdf Q3 p.1
- download. (3).pdf Q3 p.1
- 2019Qershor.pdf Q3 p.1
- 2019Shtatore.pdf Q3 p.1
- 2020Qershor.pdf Q3 p.1

Tags: rrjeta exam exam_form source::download_1 source::download_2 source::download_3 source::2019qershor source::2019shtatore source::2020qershor

## EX-217

### Front

Cili aplikacion i njohur dëgjon në portin 66666?

![assets/exam-flashcards/download-1-p02-q05.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p02-q05.png)

### Back

Ne portin 66666 nuk degjon asnje aplikacion, sepse port numri maksimal eshte 65535, sepse port
numri eshte 16 bites, 2^16 – 1 = 65535.

### Sources

- download. (1).pdf Q5 p.2

Tags: rrjeta exam exam_form source::download_1

## EX-218

### Front

Tek komunikimi klient-server çka paraqet RTT?

![assets/exam-flashcards/download-1-p02-q08.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p02-q08.png)

### Back

RTT (Round Trip Time) është koha që i duhet një pakete/mesazhi të shkojë nga klienti te serveri dhe që përgjigjja/ACK të kthehet prapë te klienti.

### Sources

- download. (1).pdf Q8 p.2
- download. (2).pdf Q8 p.2
- download. (3).pdf Q8 p.2
- 2020Qershor.pdf Q8 p.2

Tags: rrjeta exam exam_form source::download_1 source::download_2 source::download_3 source::2020qershor

## EX-219

### Front

Ku është i implementuar “Link layer” protokolli?

![assets/exam-flashcards/download-1-p03-q13.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p03-q13.png)

### Back

Eshte i implementuar ne software si driver per NIC(Network Interface Card).

### Sources

- download. (1).pdf Q13 p.3

Tags: rrjeta exam exam_form source::download_1

## EX-220

### Front

Plotëso vlerat e munguara për X,
Y dhe Z në figurë.

![assets/exam-flashcards/download-1-p03-q14.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p03-q14.png)

### Back

Nga figura: A dërgon 1 bajt me `Seq=42`, prandaj B kthen `ACK=43`. B dërgon 1 bajt me `Seq=79`, prandaj A kthen `ACK=80`.

Pra: `X = 43`, `Y = 43`, `Z = 80`.

### Sources

- download. (1).pdf Q14 p.3
- download. (2).pdf Q14 p.3
- download. (3).pdf Q14 p.3
- 2020Qershor.pdf Q14 p.3

Tags: rrjeta exam exam_form source::download_1 source::download_2 source::download_3 source::2020qershor

## EX-221

### Front

Plotësoje ARP tabelën për nyjën (kompjuterin) me IP adresë 10.10.100.100
IP Address ??? TTL

![assets/exam-flashcards/download-1-p03-q15.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p03-q15.png)

### Back

ARP tabela ruan mapping `IP address -> MAC address` për hostët në LAN dhe një TTL/age për secilin rekord. Kolona `???` është MAC Address. Shembull:
`IP Address | MAC Address | TTL`
`10.20.30.1 | aa:bb:cc:dd:ee:ff | 120s`
`10.20.30.41 | 11:22:33:44:55:66 | 120s`

### Sources

- download. (1).pdf Q15 p.3

Tags: rrjeta exam exam_form source::download_1

## EX-222

### Front

Ju merrni shërbimin e Internetit nga IPKO. IP adresa që IPKO iu ndan është reale 20.30.40.50. Ju
duhet ta dizajnoni rrjetën për një kompani me 5 kompjuter, ne brezin 192.168.0.1/24, një shtypës
(network enabled), një ueb server dhe një ftp server. Vizatoni skemën e lidhjes se këtyre
kompjuterëve, shtypësit në LAN dhe serverëve ne Internet se bashku me te gjitha IP adresat e
pajisjeve te lidhura.
(Shfrytëzo faqen mbrapa për skica! Kjo detyrë ka max. 6 pikë!)

![assets/exam-flashcards/download-1-p04-q17.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p04-q17.png)

### Back

Zgjidhje tipike: vendos router-in në kufi me WAN/public IP `20.30.40.50` dhe LAN privat p.sh. `192.168.0.0/24`.
- Router LAN/default gateway: `192.168.0.1`
- PC-të: `192.168.0.10-192.168.0.15`
- Printer: `192.168.0.20`
- Web server: `192.168.0.80`
- Email server: `192.168.0.25` ose FTP server: `192.168.0.21`, varësisht nga pyetja
- Të gjithë hostët përdorin gateway `192.168.0.1`.
Router-i bën NAT/PAT për klientët. Për qasje nga jashtë te serverët, konfiguro port forwarding/static NAT.

### Sources

- download. (1).pdf Q17 p.4
- download. (1).pdf Q18 p.4

Tags: rrjeta exam exam_form source::download_1

## EX-223

### Front

Me çfarë adrese i qaseni ueb dhe ftp serverit tuaj (nga detyra 17 & 18) nge shtëpia.

![assets/exam-flashcards/download-1-p04-q19.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p04-q19.png)

### Back

Nga jashtë/shtëpia i qasesh përmes IP publike të router-it/ISP-së ose domain-it publik. Brenda LAN-it mund t'i qasesh me IP private të serverëve, p.sh. web `192.168.0.80` dhe FTP `192.168.0.21`, ose me domain nëse DNS/NAT loopback është konfiguruar.

### Sources

- download. (1).pdf Q19 p.4
- download. (2).pdf Q19 p.4
- download. (3).pdf Q19 p.4
- 2019Shtatore.pdf Q19 p.4
- 2020Qershor.pdf Q19 p.4

Tags: rrjeta exam exam_form source::download_1 source::download_2 source::download_3 source::2019shtatore source::2020qershor

## EX-224

### Front

Nëse supozojmë se d është me e madhe se d në kohen t = d , ku është biti i pare i
prop trans trans
paketës?

![assets/exam-flashcards/download-1-p04-q20.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-1-p04-q20.png)

### Back

Biti i pare i paketes eshte rruges per tek routeri tjeter.

### Sources

- download. (1).pdf Q20 p.4

Tags: rrjeta exam exam_form source::download_1

## EX-225

### Front

Çka shërben TCP/IP protokolli?

![assets/exam-flashcards/download-2-p01-q01.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p01-q01.png)

### Back

ARP (Address resolution protocol) është një protokoll për hartimin e një IP adrese ,në një adresë të
makinës fizike(physical machine address) që njihet në rrjetin lokal(localnetwork). Ky protokoll
operon nen shtresen e rrjetit(network layer) si pjese e interfejsit ndermjet OSI network dhe OSI link
layer .

### Sources

- download. (2).pdf Q1 p.1
- download. (3).pdf Q1 p.1
- 2020Qershor.pdf Q1 p.1

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2020qershor

## EX-226

### Front

Si i qasemi remote (nga distanca) kompjuterit qe ka IP adresën: 127. 0.0.1?

![assets/exam-flashcards/download-2-p01-q02.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p01-q02.png)

### Back

IP Adress MAC address TTL
10.10.10.11 A1-38-EF-20-CE-0F 18:28:00
10.10.10.12 45-AF-32-6D-57-00 15:00:00

### Sources

- download. (2).pdf Q2 p.1
- download. (3).pdf Q2 p.1
- 2020Qershor.pdf Q2 p.1

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2020qershor

## EX-227

### Front

Përshkruani se si punon “ping” programi?

![assets/exam-flashcards/download-2-p01-q05.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p01-q05.png)

### Back

Programi trace route dergon shume paketa te vecanta nga hosti burimor drejt nje hostname
destinues. Duke kaluar rruges drejte destinacionit, paketat kalojn neper nje numer te router-ve.
Kur nje router pranon nje nga keto paketa te vecanta, ai dergon tek burimi nje mesazh te shkurte
qe permban emrin dhe adresen e routerit. Hosti i burimit te paketave regjistron kohen qe kalon
nga fillimi i dergimit te paketave e deri te pranimi i mesazheve perkatese si dhe regjistron emrin
dhe adresen e routerit qe kthen mesazhin. Ne kete form hosti burimor mund te konstruktoj rrugen
e paketave nga burimi tek destinacioni, dhe vonesat e tyre.

### Sources

- download. (2).pdf Q5 p.1
- download. (3).pdf Q5 p.1
- 2020Qershor.pdf Q5 p.1

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2020qershor

## EX-228

### Front

Çka është DOCSIS? Ku përdoret, pse?

![assets/exam-flashcards/download-2-p02-q06.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p02-q06.png)

### Back

DOCSIS = Data Over Cable Service Interface Specification. Është standard për qasje në Internet përmes rrjeteve kabllore/HFC, ku cable modem komunikon me CMTS-in e operatorit.

### Sources

- download. (2).pdf Q6 p.2
- download. (3).pdf Q6 p.2
- download. (4).pdf Q6 p.2
- 2020Qershor.pdf Q6 p.2
- 2022Qershor.pdf Q6 p.2

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::download_4 source::2020qershor source::2022qershor

## EX-229

### Front

Cilat janë pesë shtresat e protokollit të Internetit, prej lartë poshtë (vizato skicën) dhe si quhet
paketa (shënimi i) e proceduar në atë shtresë? (përdore faqen mbrapa për skica)

![assets/exam-flashcards/download-2-p02-q07.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p02-q07.png)

### Back

Pese(5) shtresat e protokollit te Internetit prej larte poshte jane: Application, Transport,
Network, Data-Link dhe Physical.
Paketat ne shtresat perkatese quhen:
Application(pakete), Transport(segment), Network(datagram), Data-Link(frame), Physical(bits).

### Sources

- download. (2).pdf Q7 p.2
- download. (3).pdf Q7 p.2
- 2020Qershor.pdf Q7 p.2

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2020qershor

## EX-230

### Front

Nëse dëshirojmë të kemi rrjetën private me numër minimal të shfrytëzuesve, duhet të përdorim
brezin e IP adresave:
___.___.___.___/___
Shënoni 2 IP adresa te çfarëdoshme nga ky brez:
___.___.___.___ dhe ___.___.___.___

![assets/exam-flashcards/download-2-p02-q10.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p02-q10.png)

### Back

Pergjigjja:
. Nëse dëshirojmë të kemi rrjetën private me numër minimal të shfrytëzuesve, duhet të përdorim
brezin e IP adresave: 192.168.1.0/8
Shënoni 2 IP adresa te çfarëdoshme nga ky brez:
192.168.1.10 dhe 192.168.1.11

### Sources

- download. (2).pdf Q10 p.2
- download. (3).pdf Q10 p.2
- 2019Qershor.pdf Q10 p.2
- 2020Qershor.pdf Q10 p.2

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2019qershor source::2020qershor

## EX-231

### Front

(Për)Shkruaje përgjigjen e komandës:
C:\>tracert www.uni-pr.edu

![assets/exam-flashcards/download-2-p02-q11.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p02-q11.png)

### Back

Komanda `tracert www.uni-pr.edu` në Windows shfaq hop-at/router-at deri te destinacioni dhe vonesat RTT për secilin hop. Përdoret për të parë rrugëtimin dhe ku mund të ketë vonesë/problem.

### Sources

- download. (2).pdf Q11 p.2
- download. (3).pdf Q11 p.2
- 2020Qershor.pdf Q11 p.2

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2020qershor

## EX-232

### Front

Çka është praktikisht “link cost” në rrjeta kompjuterike?

![assets/exam-flashcards/download-2-p03-q13.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p03-q13.png)

### Back

Protkolli definon formatin dhe radhitjen e te dhenave te shkembyera mes dy apo me shume
pajisjeve komunikuese, si dhe definon veprimet e ndermarra ne transmetimin dhe pranimin e
atyre te dhenave.

### Sources

- download. (2).pdf Q13 p.3
- download. (3).pdf Q13 p.3
- 2020Qershor.pdf Q13 p.3

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2020qershor

## EX-233

### Front

Plotësoje ARP tabelën për nyjën (kompjuterin) me IP adresë 192.168.0.1
IP Address ??? TTL

![assets/exam-flashcards/download-2-p03-q15.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p03-q15.png)

### Back

ARP tabela ruan mapping `IP address -> MAC address` për hostët në LAN dhe një TTL/age për secilin rekord. Kolona `???` është MAC Address. Shembull:
`IP Address | MAC Address | TTL`
`10.20.30.1 | aa:bb:cc:dd:ee:ff | 120s`
`10.20.30.41 | 11:22:33:44:55:66 | 120s`

### Sources

- download. (2).pdf Q15 p.3
- download. (3).pdf Q15 p.3
- 2020Qershor.pdf Q15 p.3

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2020qershor

## EX-234

### Front

WLAN routeri, i blerë rishtazi, në shtëpi mbështet standardin 802.11 AC. Çka do të thotë kjo nga
këndvështrimi i performancës dhe brezit frekuencor?

![assets/exam-flashcards/download-2-p04-q16.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p04-q16.png)

### Back

IEEE 802.11ac është Wi-Fi 5. Punon në brezin 5 GHz, përdor kanale më të gjera dhe MIMO, dhe ka throughput teorik deri rreth 1.3 Gbps në konfigurime të zakonshme (më shumë në konfigurime me më shumë spatial streams).

### Sources

- download. (2).pdf Q16 p.4
- download. (3).pdf Q16 p.4
- 2019Qershor.pdf Q11 p.3
- 2020Qershor.pdf Q16 p.4

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2019qershor source::2020qershor

## EX-235

### Front

Ju merrni shërbimin e Internetit nga IPKO. IP adresa që IPKO iu ndan është reale 20.30.40.50. Ju
duhet ta dizajnoni rrjetën për një kompani me 5 kompjuter, ne brezin 10.20.30.40/24, një shtypës
(network enabled), një ueb server dhe një ftp server. Vizatoni skemën e lidhjes se këtyre
kompjuterëve, shtypësit në LAN dhe serverëve ne Internet se bashku me te gjitha IP adresat e
pajisjeve te lidhura. (Shfrytëzo faqen mbrapa për skica! Kjo detyrë ka max. 6 pikë!)

![assets/exam-flashcards/download-2-p04-q17.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p04-q17.png)

### Back

Zgjidhje tipike: vendos router-in në kufi me WAN/public IP `20.30.40.50` dhe LAN privat p.sh. `192.168.0.0/24`.
- Router LAN/default gateway: `192.168.0.1`
- PC-të: `192.168.0.10-192.168.0.15`
- Printer: `192.168.0.20`
- Web server: `192.168.0.80`
- Email server: `192.168.0.25` ose FTP server: `192.168.0.21`, varësisht nga pyetja
- Të gjithë hostët përdorin gateway `192.168.0.1`.
Router-i bën NAT/PAT për klientët. Për qasje nga jashtë te serverët, konfiguro port forwarding/static NAT.

### Sources

- download. (2).pdf Q17 p.4
- download. (2).pdf Q18 p.4
- download. (3).pdf Q17 p.4
- download. (3).pdf Q18 p.4
- 2020Qershor.pdf Q17 p.4
- 2020Qershor.pdf Q18 p.4

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2020qershor

## EX-236

### Front

Përshkruaj llojet e vonesave në rrjeta kompjuterike? Cilat janë me të mëdha? Pse?

![assets/exam-flashcards/download-2-p04-q20.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-2-p04-q20.png)

### Back

Dallojm keto lloje te vonesave te paketave : processing delay, queuing delay, transmission
delay dhe propagation delay.
Processing delay-koha e nevojshme per ekzaminimin e header-it te paketes dhe percaktimin se
ku te drejtohet paketa.
Queuing delay-koha qe paketa pret per tu vendosur ne lidhje(link).
Transmission delay-koha e nevojshme per vendosjen e te gjitha paketave në lidhje.
Propagation delay-koha e nevojshme per te kaluar paketa nga fillimi i lidhjes deri tek routeri
ardhshem.

### Sources

- download. (2).pdf Q20 p.4
- download. (3).pdf Q20 p.4
- 2020Qershor.pdf Q20 p.4

Tags: rrjeta exam exam_form source::download_2 source::download_3 source::2020qershor

## EX-237

### Front

Çka është Internet-i? Prej çka përbehet? Përshkruani me fjalë të juaja si funksionon?

![assets/exam-flashcards/download-4-p01-q01.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p01-q01.png)

### Back

Interneti eshte rrjet i rrjeteve. Interneti paraqet bashkesine e kompjutereve, servereve,
aplikacioneve, routereve dhe linjave per komunikim. Te gjitha pajisjet e lidhura ne internet
njihen si hosta apo sisteme fundore te cilat lidhen mes veti permes linjave komunikuese dhe
packet switches.

### Sources

- download. (4).pdf Q1 p.1
- 2022Qershor.pdf Q1 p.1

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-238

### Front

IP adresat private janë:
Klasa A: 10.___.___.___. deri ___.___.___.255
Klasa B: 172.16.0.0 deri 172.31.___.____
Klasa C: 192.___.___.___ deri 192.168.___.___

![assets/exam-flashcards/download-4-p01-q02.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p01-q02.png)

### Back

Rangjet private IPv4 janë:
- Klasa A: `10.0.0.0 - 10.255.255.255` (`10.0.0.0/8`)
- Klasa B: `172.16.0.0 - 172.31.255.255` (`172.16.0.0/12`)
- Klasa C: `192.168.0.0 - 192.168.255.255` (`192.168.0.0/16`)

### Sources

- download. (4).pdf Q2 p.1
- 2022Qershor.pdf Q2 p.1

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-239

### Front

Çka është RTT ?

![assets/exam-flashcards/download-4-p01-q03.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p01-q03.png)

### Back

RTT (Round Trip Time) është koha që i duhet një pakete/mesazhi të shkojë nga klienti te serveri dhe që përgjigjja/ACK të kthehet prapë te klienti.

### Sources

- download. (4).pdf Q3 p.1
- 2022Qershor.pdf Q3 p.1

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-240

### Front

Skiconi se si punon NAT-i? Çfarë roli kanë portet?(përdore faqen mbrapa, sipas nevojës, për skica)

![assets/exam-flashcards/download-4-p01-q04.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p01-q04.png)

### Back

NAT lejon shumë hostë me IP private të përdorin një IP publike. Router-i NAT zëvendëson source private IP/port me public IP/port kur paketa del në Internet dhe ruan mapping në NAT table. Kur kthehet përgjigjja, router-i përdor portin publik për ta gjetur hostin privat dhe e rikthen destination IP/port. Portet janë çelësi që dallon lidhjet e shumë hostëve pas të njëjtës IP publike.

### Sources

- download. (4).pdf Q4 p.1
- 2022Qershor.pdf Q4 p.1

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-241

### Front

Cila fushë e IP datagramit zvogëlohet për një, sa herë që router-i e përpunon datagramin? Pse?

![assets/exam-flashcards/download-4-p01-q05.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p01-q05.png)

### Back

Fusha është TTL (Time To Live). Çdo router e zvogëlon TTL për 1; kur TTL bëhet 0, paketa hidhet. Kjo parandalon qarkullimin e pafund të datagrameve në rast loop-i në routing.

### Sources

- download. (4).pdf Q5 p.1
- 2022Qershor.pdf Q5 p.1

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-242

### Front

Tek kumutimi i paketave është supozuar që shfrytëzuesi është vetëm 10% te kohës aktiv. A është
ky supozim i drejtë? Pse?

![assets/exam-flashcards/download-4-p02-q07.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p02-q07.png)

### Back

Po, si model është i arsyeshëm për trafik Interneti sepse përdoruesit zakonisht janë bursty: kanë periudha të shkurtra aktiviteti dhe shumë kohë idle. Kjo e bën packet switching efikas me statistical multiplexing, por nëse shumë përdorues bëhen aktivë njëkohësisht krijohet queueing/congestion.

### Sources

- download. (4).pdf Q7 p.2
- 2022Qershor.pdf Q7 p.2

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-243

### Front

Shëno emrat (shkurtesat) e protokolleve të përdoruara.
Tek lidhja 2 përdoret protokolli: _____
Tek lidhja 4 përdoret protokolli: _____
Tek lidhja 6 përdoret protokolli: _____

![assets/exam-flashcards/download-4-p02-q08.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p02-q08.png)

### Back

Lidhja 2: SMTP. Lidhja 4: SMTP. Lidhja 6: POP3 nëse pyetja supozon POP3; në praktikë mund të jetë IMAP ose HTTP/webmail.

### Sources

- download. (4).pdf Q8 p.2
- 2022Qershor.pdf Q8 p.2

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-244

### Front

Tek DHCP protokolli, i klienti i sapo ardhur në rrjet, dërgon paketën e parë me “destination
address: 255.255.255.255”. Pse?

![assets/exam-flashcards/download-4-p02-q09.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p02-q09.png)

### Back

Klienti i ri ende nuk ka IP adresë dhe nuk e di adresën e DHCP serverit. Prandaj dërgon DHCPDISCOVER si broadcast me destination `255.255.255.255`, që ta dëgjojë çdo DHCP server në LAN.

### Sources

- download. (4).pdf Q9 p.2
- 2022Qershor.pdf Q9 p.2

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-245

### Front

Shënoni tri parimet themelore të “Network Neutrality”?

![assets/exam-flashcards/download-4-p03-q10.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p03-q10.png)

### Back

Tri parime bazë të network neutrality:
- No blocking: ISP nuk duhet të bllokojë përmbajtje/aplikacione legale.
- No throttling: ISP nuk duhet të ngadalësojë në mënyrë diskriminuese trafik të caktuar.
- No paid prioritization/discrimination: ISP nuk duhet të favorizojë trafik sepse dikush paguan më shumë.
Shpesh përmendet edhe transparenca ndaj përdoruesit.

### Sources

- download. (4).pdf Q10 p.3
- 2022Qershor.pdf Q10 p.3

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-246

### Front

WLAN routeri, i blerë rishtazi, në shtëpi mbështet standardin IEEE 802.11 AX. Çka do të thotë
kjo nga këndvështrimi i performancës dhe brezit frekuencor?

![assets/exam-flashcards/download-4-p03-q11.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p03-q11.png)

### Back

IEEE 802.11ax është Wi-Fi 6. Punon kryesisht në 2.4 GHz dhe 5 GHz (Wi-Fi 6E shton 6 GHz), përdor OFDMA dhe MU-MIMO për efikasitet më të lartë, latencë më të ulët dhe throughput teorik deri rreth 9.6 Gbps.

### Sources

- download. (4).pdf Q11 p.3
- 2022Qershor.pdf Q11 p.3

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-247

### Front

Në figurë është paraqitur rasti ri-trammetimit te shënimeve,
plotëso fushat?
Seq=____, ___ bytes of data
ACK = ____

![assets/exam-flashcards/download-4-p03-q13.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p03-q13.png)

### Back

ACK-i `100` humbet, prandaj Host A e ri-transmeton të njëjtin segment. Segmenti origjinal kishte `Seq=92` dhe `8 bytes of data`, kështu që edhe ri-transmetimi ka `Seq=92, 8 bytes of data`. Host B e pranon dublikatën dhe kthen përsëri `ACK=100`.

### Sources

- download. (4).pdf Q13 p.3
- 2022Qershor.pdf Q13 p.3

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-248

### Front

Dy hoste (pajisje) A dhe B te lidhura me një linje të vetme R [bps] dhe të larguara d [metra].
Hosti A fillon te transmetoj paketën me gjatësi L [bit] ne kohen t = 0. Në
kohen t = d , ku është biti i fundit i paketës?
trans

![assets/exam-flashcards/download-4-p03-q14.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p03-q14.png)

### Back

Sapo e ka leshuar hostin A.

### Sources

- download. (4).pdf Q14 p.3
- 2022Qershor.pdf Q14 p.3

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-249

### Front

Kompjuteri A dhe B jane lidhur sikurse ne figure, permes router-it R. Cfare MAC adrese vendose
kompjueri A ne datagrame-in e vet ?
IP src: 111.111.111.111, MAC src: 74-29-9C-E8-FF-55
IP dest: 222.222.222.222, MAC dest: _________________________

![assets/exam-flashcards/download-4-p04-q15.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p04-q15.png)

### Back

Meqë A dhe B janë në rrjete të ndryshme dhe komunikimi kalon përmes router-it R, A vendos si MAC destination MAC adresën e interfejsit të router-it R në LAN-in e A. IP destination mbetet IP e B; MAC ndryshon hop pas hop-i.

### Sources

- download. (4).pdf Q15 p.4
- 2022Qershor.pdf Q15 p.4

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-250

### Front

Videon me madhësi 320 MByte e ngarkoni (upload) përmes lidhjes asimetrike 200Mbps të
Internetit, me download (shkarkim) 180 Mbps. Sa kohë ju nevojitet për ta ngarkuar këtë këngë?

![assets/exam-flashcards/download-4-p04-q17.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p04-q17.png)

### Back

Nese lidhja eshte asimetrike atehere download dhe upload kan vlera te ndryshme ku shuma e tyre e
jep trasmision rate te rrjetit . Nese lidhja eshte 10Mbps dhe download eshte 8Mbps atehere upload
eshte 2Mbps .
K=S/BW=6MByte//6Mbit/s=6*8*10^6 bit // 2*10^6 bit/s = 24s

### Sources

- download. (4).pdf Q17 p.4
- 2022Qershor.pdf Q17 p.4

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-251

### Front

Ju merrni shërbimin e Internetit nga IPKO. IP adresa që IPKO iu ndan është reale 91.187.99.206.
Ju duhet ta dizajnoni rrjetën për një kompani me 5 kompjuter, një shtypës (network enabled), një
ueb server dhe një ftp server. Vizatoni skemën e lidhjes se këtyre kompjuterëve, shtypësit në
LAN dhe serverëve ne Internet se bashku me te gjitha IP adresat e pajisjeve te lidhura. (Shfrytëzo
faqen mbrapa për skica!)

![assets/exam-flashcards/download-4-p04-q18.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p04-q18.png)

### Back

Zgjidhje tipike: vendos router-in në kufi me WAN/public IP `91.187.99.206` dhe LAN privat p.sh. `192.168.0.0/24`.
- Router LAN/default gateway: `192.168.0.1`
- PC-të: `192.168.0.10-192.168.0.15`
- Printer: `192.168.0.20`
- Web server: `192.168.0.80`
- Email server: `192.168.0.25` ose FTP server: `192.168.0.21`, varësisht nga pyetja
- Të gjithë hostët përdorin gateway `192.168.0.1`.
Router-i bën NAT/PAT për klientët. Për qasje nga jashtë te serverët, konfiguro port forwarding/static NAT.

### Sources

- download. (4).pdf Q18 p.4
- download. (4).pdf Q19 p.4
- 2022Qershor.pdf Q18 p.4
- 2022Qershor.pdf Q19 p.4

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-252

### Front

Cila është adresa e ueb dhe ftp serverit tuaj (nga detyra 18 dhe 19) për shfrytëzuesit nga jashtë
(nga Interneti) dhe nga brenda rrjetit (Intraneti)?

![assets/exam-flashcards/download-4-p04-q20.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/download-4-p04-q20.png)

### Back

Nga jashtë/shtëpia i qasesh përmes IP publike të router-it/ISP-së ose domain-it publik. Brenda LAN-it mund t'i qasesh me IP private të serverëve, p.sh. web `192.168.0.80` dhe FTP `192.168.0.21`, ose me domain nëse DNS/NAT loopback është konfiguruar.

### Sources

- download. (4).pdf Q20 p.4
- 2022Qershor.pdf Q20 p.4

Tags: rrjeta exam exam_form source::download_4 source::2022qershor

## EX-253

### Front

Si ka mundësi ne Internet qe me miliarda pajisje (softeurike dhe harduerike), te prodhuesve te
ndryshëm, te lidhen se bashku dhe te komunikojnë?

![assets/exam-flashcards/2019qershor-p01-q01.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p01-q01.png)

### Back

Sepse Interneti përdor protokolle të hapura dhe të standardizuara (TCP/IP, DNS, HTTP, routing protocols) dhe arkitekturë me shtresa. Çdo prodhues mjafton të implementojë të njëjtat formate paketash, adresa dhe rregulla protokollare që pajisjet të ndërveprojnë.

### Sources

- 2019Qershor.pdf Q1 p.1
- 2019Shtatore.pdf Q1 p.1

Tags: rrjeta exam exam_form source::2019qershor source::2019shtatore

## EX-254

### Front

Si quhet kompjuteri qe ka IP adresën: 127. 0.0.1?

![assets/exam-flashcards/2019qershor-p01-q02.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p01-q02.png)

### Back

IP Adress MAC address TTL
10.10.10.11 A1-38-EF-20-CE-0F 18:28:00
10.10.10.12 45-AF-32-6D-57-00 15:00:00

### Sources

- 2019Qershor.pdf Q2 p.1
- 2019Shtatore.pdf Q2 p.1

Tags: rrjeta exam exam_form source::2019qershor source::2019shtatore

## EX-255

### Front

Si është ndare brezi frekuencor te DSL?

![assets/exam-flashcards/2019qershor-p02-q06.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p02-q06.png)

### Back

High Speed downstream 50Khz-1MHz
Medium Speed upstream 4Khz-50MHz
Two way telephone channel 0-4Khz

### Sources

- 2019Qershor.pdf Q6 p.2
- 2019Shtatore.pdf Q6 p.2

Tags: rrjeta exam exam_form source::2019qershor source::2019shtatore

## EX-256

### Front

Cilat janë pesë shtresat e protokollit të Internetit, prej lartë poshtë (vizato skicën) dhe si quhet
paketa (shënimi i) e proceduar në atë shtresë?

![assets/exam-flashcards/2019qershor-p02-q07.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p02-q07.png)

### Back

Pese(5) shtresat e protokollit te Internetit prej larte poshte jane: Application, Transport,
Network, Data-Link dhe Physical.
Paketat ne shtresat perkatese quhen:
Application(pakete), Transport(segment), Network(datagram), Data-Link(frame), Physical(bits).

### Sources

- 2019Qershor.pdf Q7 p.2
- 2019Shtatore.pdf Q7 p.2

Tags: rrjeta exam exam_form source::2019qershor source::2019shtatore

## EX-257

### Front

Alice përdor emalin për të komunikuar me Bob, nën supozimin se përdor POP3 dhe SMTP
protokollin, plotëso figurën me poshtë se ku përdoret cili protokoll?
Tek lidhja 2 përdoret protokolli: _____
Tek lidhja 4 përdoret protokolli: _____
Tek lidhja 6 përdoret protokolli: _____

![assets/exam-flashcards/2019qershor-p02-q08.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p02-q08.png)

### Back

Në skemën klasike të email-it:
- Lidhja 2: SMTP (user agent i Alice -> mail server i Alice)
- Lidhja 4: SMTP (mail server i Alice -> mail server i Bob)
- Lidhja 6: POP3 (mail server i Bob -> user agent i Bob)
Në sisteme moderne, lidhja 6 mund të jetë edhe IMAP/HTTP, por në këtë pyetje supozohet POP3.

### Sources

- 2019Qershor.pdf Q8 p.2
- 2019Shtatore.pdf Q8 p.2

Tags: rrjeta exam exam_form source::2019qershor source::2019shtatore

## EX-258

### Front

Përshkruaj principet se si arrihet besueshmëri e transmetimit të shënimeve në nivelin TCP-së?

![assets/exam-flashcards/2019qershor-p03-q13.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p03-q13.png)

### Back

TCP arrin reliability me checksum, sequence numbers, ACK, timer/timeout, ri-transmetim, sliding window, flow control dhe congestion control. Marrësi i përdor sequence numbers për renditje dhe deduplikim; dërguesi ri-transmeton segmentet që nuk konfirmohen.

### Sources

- 2019Qershor.pdf Q13 p.3
- 2019Shtatore.pdf Q13 p.3

Tags: rrjeta exam exam_form source::2019qershor source::2019shtatore

## EX-259

### Front

Pershkruaj rolin e ketyre parametrave: base, nextseqnum dhe N.

![assets/exam-flashcards/2019qershor-p03-q14.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p03-q14.png)

### Back

Në sliding-window/GBN:
- `base`: numri i sekuencës së paketës më të vjetër të dërguar por ende pa ACK.
- `nextseqnum`: numri i sekuencës që do t'i jepet paketës së ardhshme.
- `N`: madhësia e dritares, pra maksimumi i paketave që mund të jenë outstanding pa ACK.

### Sources

- 2019Qershor.pdf Q14 p.3
- 2019Shtatore.pdf Q14 p.3

Tags: rrjeta exam exam_form source::2019qershor source::2019shtatore

## EX-260

### Front

Plotësoje ARP tabelën për nyjën (kompjuterin) me IP adresë 10.10.10.10
IP Address ??? TTL

![assets/exam-flashcards/2019qershor-p04-q15.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p04-q15.png)

### Back

ARP tabela ruan mapping `IP address -> MAC address` për hostët në LAN dhe një TTL/age për secilin rekord. Kolona `???` është MAC Address. Shembull:
`IP Address | MAC Address | TTL`
`10.20.30.1 | aa:bb:cc:dd:ee:ff | 120s`
`10.20.30.41 | 11:22:33:44:55:66 | 120s`

### Sources

- 2019Qershor.pdf Q15 p.4

Tags: rrjeta exam exam_form source::2019qershor

## EX-261

### Front

Përshkruani me te paktën tri fjali CSMA/CD protokollin.

![assets/exam-flashcards/2019qershor-p04-q16.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p04-q16.png)

### Back

CSMA/CD eshte nje media access protokoll qe perdoret ne LAN dhe paraqet nje grup
rregullash qe percaktojne se si pajisjet e rrjetes reagojne kur dy pajisje tentojne te perdorin nje
kanal transmetues te njejte te te dhenave ne te njejten kohe(qe nihet si collision).

### Sources

- 2019Qershor.pdf Q16 p.4
- 2019Shtatore.pdf Q16 p.4

Tags: rrjeta exam exam_form source::2019qershor source::2019shtatore

## EX-262

### Front

Ju merrni shërbimin e Internetit nga IPKO. IP adresa që IPKO iu ndan është reale 77.88.99.100.
Ju duhet ta dizajnoni rrjetën për një kompani me 5 kompjuter, ne brezin 192.168.1.0/24, një
shtypës (network enabled), një ueb server dhe një ftp server. Vizatoni skemën e lidhjes se këtyre
kompjuterëve, shtypësit në LAN dhe serverëve ne Internet se bashku me te gjitha IP adresat e
pajisjeve te lidhura. (Shfrytëzo faqen mbrapa për skica! Kjo detyrë ka max. 6 pikë!)

![assets/exam-flashcards/2019qershor-p04-q17.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p04-q17.png)

### Back

Zgjidhje tipike: vendos router-in në kufi me WAN/public IP `77.88.99.100` dhe LAN privat p.sh. `192.168.0.0/24`.
- Router LAN/default gateway: `192.168.0.1`
- PC-të: `192.168.0.10-192.168.0.15`
- Printer: `192.168.0.20`
- Web server: `192.168.0.80`
- Email server: `192.168.0.25` ose FTP server: `192.168.0.21`, varësisht nga pyetja
- Të gjithë hostët përdorin gateway `192.168.0.1`.
Router-i bën NAT/PAT për klientët. Për qasje nga jashtë te serverët, konfiguro port forwarding/static NAT.

### Sources

- 2019Qershor.pdf Q17 p.4
- 2019Qershor.pdf Q18 p.4

Tags: rrjeta exam exam_form source::2019qershor

## EX-263

### Front

Cila është adresa e ueb dhe ftp serverit tuaj (nga detyra 17 & 18) për shfrytëzuesit nga jashtë (nga
Interneti) dhe nga brenda rrjetit (Intraneti)?

![assets/exam-flashcards/2019qershor-p04-q19.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019qershor-p04-q19.png)

### Back

Nga jashtë/shtëpia i qasesh përmes IP publike të router-it/ISP-së ose domain-it publik. Brenda LAN-it mund t'i qasesh me IP private të serverëve, p.sh. web `192.168.0.80` dhe FTP `192.168.0.21`, ose me domain nëse DNS/NAT loopback është konfiguruar.

### Sources

- 2019Qershor.pdf Q19 p.4

Tags: rrjeta exam exam_form source::2019qershor

## EX-264

### Front

Një DNS “resource record” (Name, Value, Type, TTL) është i tipit CNAME (pra Type=
CNAME). Çka përmban atëherë “Value”?

![assets/exam-flashcards/2019shtatore-p02-q09.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019shtatore-p02-q09.png)

### Back

Një DNS resource record ka formatin `(Name, Value, Type, TTL)`. Kuptimi i `Value` varet nga `Type`: A -> IP address; NS -> authoritative DNS server; CNAME -> canonical name; MX -> mail server.

### Sources

- 2019Shtatore.pdf Q9 p.2

Tags: rrjeta exam exam_form source::2019shtatore

## EX-265

### Front

Nëse dëshirojmë të kemi rrjetën private me numër maximal të shfrytëzuesve, duhet të përdorim
brezin e IP adresave:
___.___.___.___/___
Shënoni 2 IP adresa te çfarëdoshme nga ky brez:
___.___.___.___ dhe ___.___.___.___

![assets/exam-flashcards/2019shtatore-p02-q10.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019shtatore-p02-q10.png)

### Back

Pergjigjja:
Nëse dëshirojmë të kemi rrjetën private me numër maksimal të shfrytëzuesve, duhet të përdorim
brezin e IP adresave: 10.0.0.0/8
Shënoni 2 IP adresa te çfarëdoshme nga ky brez:
10.0.0.10 dhe 10.10.0.11

### Sources

- 2019Shtatore.pdf Q10 p.2

Tags: rrjeta exam exam_form source::2019shtatore

## EX-266

### Front

Plotësoje ARP tabelën për nyjën (kompjuterin) me IP adresë 192.168.10.10
IP Address ??? TTL

![assets/exam-flashcards/2019shtatore-p04-q15.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019shtatore-p04-q15.png)

### Back

ARP tabela ruan mapping `IP address -> MAC address` për hostët në LAN dhe një TTL/age për secilin rekord. Kolona `???` është MAC Address. Shembull:
`IP Address | MAC Address | TTL`
`10.20.30.1 | aa:bb:cc:dd:ee:ff | 120s`
`10.20.30.41 | 11:22:33:44:55:66 | 120s`

### Sources

- 2019Shtatore.pdf Q15 p.4

Tags: rrjeta exam exam_form source::2019shtatore

## EX-267

### Front

Ju merrni shërbimin e Internetit nga IPKO. IP adresa që IPKO iu ndan është reale 20.30.40.50. Ju
duhet ta dizajnoni rrjetën për një kompani me 5 kompjuter, ne brezin 192.168.1.0/24, një shtypës
(network enabled), një ueb server dhe një ftp server. Vizatoni skemën e lidhjes se këtyre
kompjuterëve, shtypësit në LAN dhe serverëve ne Internet se bashku me te gjitha IP adresat e
pajisjeve te lidhura. (Shfrytëzo faqen mbrapa për skica! Kjo detyrë ka max. 6 pikë!)

![assets/exam-flashcards/2019shtatore-p04-q17.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019shtatore-p04-q17.png)

### Back

Zgjidhje tipike: vendos router-in në kufi me WAN/public IP `20.30.40.50` dhe LAN privat p.sh. `192.168.0.0/24`.
- Router LAN/default gateway: `192.168.0.1`
- PC-të: `192.168.0.10-192.168.0.15`
- Printer: `192.168.0.20`
- Web server: `192.168.0.80`
- Email server: `192.168.0.25` ose FTP server: `192.168.0.21`, varësisht nga pyetja
- Të gjithë hostët përdorin gateway `192.168.0.1`.
Router-i bën NAT/PAT për klientët. Për qasje nga jashtë te serverët, konfiguro port forwarding/static NAT.

### Sources

- 2019Shtatore.pdf Q17 p.4
- 2019Shtatore.pdf Q18 p.4

Tags: rrjeta exam exam_form source::2019shtatore

## EX-268

### Front

Nëse supozojmë se d është me e madhe se d në kohen t = d , ku është biti i parë i
prop trans trans
paketës?

![assets/exam-flashcards/2019shtatore-p04-q20.png|900](/img/user/Semester%204/Rrjeta/assets/exam-flashcards/2019shtatore-p04-q20.png)

### Back

Biti i pare i paketes eshte rruges per tek routeri tjeter.

### Sources

- 2019Shtatore.pdf Q20 p.4

Tags: rrjeta exam exam_form source::2019shtatore
