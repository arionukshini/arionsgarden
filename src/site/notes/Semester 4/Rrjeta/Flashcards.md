---
{"dg-publish":true,"permalink":"/semester-4/rrjeta/flashcards/","tags":["university/rrjeta","anki"]}
---


# Rrjeta kompjuterike — Flashcards

> [!info] Import në Anki
> Përdor skedarin `Rrjeta — Anki.csv`. Mapo kolonat `Front`, `Back`, `Tags` te note type **Basic** dhe zgjidh UTF‑8. Kartat më poshtë janë burimi i lexueshëm; CSV-ja është gjeneruar prej tyre.

## Ligjerata 1 — Bazat

### 001
- **Front:** Çfarë është Interneti në “nuts-and-bolts view”?
- **Back:** Një network of networks: hosts/end systems, access networks, routers/switches dhe ISP të ndërlidhur që përdorin protokolle të përbashkëta.
- **Tags:** rrjeta::l1

### 002
- **Front:** Çfarë përcakton një network protocol?
- **Back:** Format/rendin e mesazheve midis entiteteve dhe veprimet që kryhen kur mesazhet dërgohen ose pranohen.
- **Tags:** rrjeta::l1

### 003
- **Front:** Cili është dallimi mes network edge dhe network core?
- **Back:** Edge përmban end systems (clients/servers) dhe access networks; core është mesh-i i routerëve që forward-on paketa mes rrjeteve.
- **Tags:** rrjeta::l1

### 004
- **Front:** Çfarë bën një host para se ta dërgojë një application message në rrjet?
- **Back:** E ndan në chunks të quajtur packets dhe i transmeton në access link me rate R.
- **Tags:** rrjeta::l1

### 005
- **Front:** Çfarë është store-and-forward packet switching?
- **Back:** Routeri duhet të marrë paketën e plotë përpara se të fillojë ta transmetojë atë në output link.
- **Tags:** rrjeta::l1

### 006
- **Front:** Formula e transmission delay dhe kuptimi i saj?
- **Back:** d_trans = L/R. L është gjatësia e paketës në bits, R është transmission rate i linkut në bps; është koha për ta futur paketën në link.
- **Tags:** rrjeta::l1

### 007
- **Front:** Dallimi mes transmission delay dhe propagation delay?
- **Back:** Transmission delay është L/R dhe varet nga madhësia/rate-i; propagation delay është distanca/shpejtësia e sinjalit dhe varet nga mediumi/distanca.
- **Tags:** rrjeta::l1

### 008
- **Front:** Cilat janë katër burimet e nodal delay?
- **Back:** Processing, queueing, transmission dhe propagation delay.
- **Tags:** rrjeta::l1

### 009
- **Front:** Kur ndodh packet loss në router?
- **Back:** Kur buffer-i/queue ka kapacitet të fundëm dhe mbushet; një paketë që arrin nuk ka vend dhe drop-ohet.
- **Tags:** rrjeta::l1

### 010
- **Front:** Çfarë tregon traffic intensity La/R?
- **Back:** Raportin mes punës që arrin dhe kapacitetit të linkut. Kur i afrohet 1, queueing delay rritet shumë; mbi 1, mesatarisht puna arrin më shpejt se shërbehet.
- **Tags:** rrjeta::l1

### 011
- **Front:** Çfarë është bottleneck link?
- **Back:** Linku me rate/kapacitet kufizues në path; ai kufizon end-to-end throughput.
- **Tags:** rrjeta::l1

### 012
- **Front:** Packet switching kundrejt circuit switching?
- **Back:** Packet switching ndan burime sipas kërkesës dhe është efikas për trafik bursty; circuit switching rezervon burime end-to-end, jep performance të parashikueshme por mund të lërë kapacitet bosh.
- **Tags:** rrjeta::l1

### 013
- **Front:** Çfarë janë FDM dhe TDM?
- **Back:** Teknikat e circuit switching: FDM ndan mediumin në frequency bands; TDM e ndan në time slots.
- **Tags:** rrjeta::l1

### 014
- **Front:** Dallimi mes forwarding dhe routing?
- **Back:** Forwarding është veprim lokal që çon paketën nga input në output port; routing llogarit rrugët dhe forwarding tables në shkallë rrjeti.
- **Tags:** rrjeta::l1

### 015
- **Front:** Cilat janë tri kërcënime bazë të sigurisë të paraqitura në ligjëratë?
- **Back:** Packet sniffing/interception, IP spoofing dhe denial of service (DoS).
- **Tags:** rrjeta::l1

### 016
- **Front:** Çfarë është encapsulation?
- **Back:** Shtimi i header-it të secilës shtresë rreth të dhënave nga shtresa sipër; në marrës header-at hiqen në rend të kundërt.
- **Tags:** rrjeta::l1

### 017
- **Front:** Cila është radha e PDU-ve në Internet stack?
- **Back:** Application message → transport segment → network datagram → link frame → bits.
- **Tags:** rrjeta::l1

### 018
- **Front:** Cilat janë pesë shtresat e Internet protocol stack?
- **Back:** Application, transport, network, link dhe physical.
- **Tags:** rrjeta::l1

## Ligjerata 2 — Application layer

### 019
- **Front:** Client-server kundrejt P2P?
- **Back:** Client-server ka server always-on që shërben klientë; P2P lejon peers të kërkojnë dhe të ofrojnë shërbim njëri-tjetrit, duke sjellë self-scalability.
- **Tags:** rrjeta::l2

### 020
- **Front:** Çfarë është socket në programimin e rrjetit?
- **Back:** “Dera” midis application process dhe transport layer; aplikacioni dërgon/pranon mesazhe përmes tij.
- **Tags:** rrjeta::l2

### 021
- **Front:** Çfarë përcakton një application-layer protocol?
- **Back:** Llojet e mesazheve, sintaksën e fushave, semantikën e informacionit dhe rregullat se kur/si proceset dërgojnë e përgjigjen.
- **Tags:** rrjeta::l2

### 022
- **Front:** Çfarë kërkesash transporti mund të ketë një aplikacion?
- **Back:** Data loss/reliability, throughput, timing/latency dhe security.
- **Tags:** rrjeta::l2

### 023
- **Front:** Çfarë është HTTP dhe cili model përdor?
- **Back:** Hypertext Transfer Protocol, application-layer protocol i Web-it; përdor client-server model ku browser-i kërkon objekte dhe web server-i i kthen.
- **Tags:** rrjeta::l2

### 024
- **Front:** Çfarë do të thotë që HTTP është stateless?
- **Back:** Serveri nuk ruan automatikisht informacion për request-et e mëparshme të klientit; state mund të shtohet p.sh. me cookies.
- **Tags:** rrjeta::l2

### 025
- **Front:** Non-persistent kundrejt persistent HTTP?
- **Back:** Non-persistent zakonisht hap/mbyll TCP connection për objekt; persistent ripërdor connection-in për disa objekte dhe ul overhead-in/latency-n.
- **Tags:** rrjeta::l2

### 026
- **Front:** Për një objekt me non-persistent HTTP, sa është response time i përafërt?
- **Back:** Rreth 2 RTT plus koha e transmetimit: një RTT për TCP setup dhe një RTT për request plus fillimin e response.
- **Tags:** rrjeta::l2

### 027
- **Front:** Çfarë përmban HTTP request i përgjithshëm?
- **Back:** Request line (method, URL, version), header lines dhe opsionalisht entity body.
- **Tags:** rrjeta::l2

### 028
- **Front:** Çfarë kuptojnë status codes 200, 301, 404 dhe 500?
- **Back:** 200 OK/sukses; 301 moved permanently/redirect; 404 not found; 500 server error.
- **Tags:** rrjeta::l2

### 029
- **Front:** Cilat janë katër komponentët e cookies?
- **Back:** Set-Cookie në response, Cookie në request-et pasuese, cookie file në browser dhe back-end database në server.
- **Tags:** rrjeta::l2

### 030
- **Front:** Çfarë bën Conditional GET dhe cili status përdoret kur cache është fresh?
- **Back:** Dërgon If-Modified-Since që serveri të mos dërgojë objektin e pandryshuar; përgjigjja është 304 Not Modified.
- **Tags:** rrjeta::l2

### 031
- **Front:** Pse HTTP/3 përdor QUIC mbi UDP?
- **Back:** Për të ofruar encryption dhe streams me recovery të pavarur, duke shmangur TCP head-of-line blocking mes objekteve.
- **Tags:** rrjeta::l2

### 032
- **Front:** Çfarë bën SMTP dhe cili port klasik përdor mes mail servers?
- **Back:** SMTP transferon e-mail nga sending mail server te receiving mail server mbi TCP; porti klasik është 25.
- **Tags:** rrjeta::l2

### 033
- **Front:** SMTP kundrejt IMAP?
- **Back:** SMTP dërgon/relay-on mail; IMAP i lejon user agent-it të lexojë e sinkronizojë mailbox-in që ruhet në server.
- **Tags:** rrjeta::l2

### 034
- **Front:** Cili është roli kryesor i DNS?
- **Back:** Përkthimi i hostname-ve në IP addresses dhe anasjelltas, përmes një database të shpërndarë/hierarkike.
- **Tags:** rrjeta::l2

### 035
- **Front:** Cilat janë nivelet tipike të DNS hierarchy gjatë lookup-ut?
- **Back:** Local resolver, root name server, TLD name server dhe authoritative name server.
- **Tags:** rrjeta::l2

### 036
- **Front:** Iterative kundrejt recursive DNS query?
- **Back:** Iterative: serveri jep referral te serveri tjetër; recursive: serveri i kontaktuar e kryen resolution-in në emër të kërkuesit.
- **Tags:** rrjeta::l2

### 037
- **Front:** Çfarë janë DNS caching dhe TTL?
- **Back:** Resolveri ruan përgjigje për t’i ripërdorur; TTL përcakton sa kohë entry konsiderohet i vlefshëm.
- **Tags:** rrjeta::l2

### 038
- **Front:** Si funksionon ideja kryesore e BitTorrent?
- **Back:** File-i ndahet në chunks; peers shkarkojnë chunks nga shumë peers dhe njëkohësisht i upload-ojnë te të tjerët.
- **Tags:** rrjeta::l2

### 039
- **Front:** Çfarë është DASH?
- **Back:** Dynamic Adaptive Streaming over HTTP: video ndahet në segmente në disa encoding rates dhe client zgjedh rate sipas bandwidth/buffer-it.
- **Tags:** rrjeta::l2

### 040
- **Front:** Pse përdoret client-side playout buffer për streaming video?
- **Back:** Për të kompensuar network-added delay dhe delay jitter, që video të luhet më pa ndërprerje.
- **Tags:** rrjeta::l2

## Ligjerata 3 — Transport layer

### 041
- **Front:** Transport layer kundrejt network layer?
- **Back:** Transport layer ofron logical communication process-to-process; network layer ofron logical communication host-to-host.
- **Tags:** rrjeta::l3

### 042
- **Front:** Çfarë është multiplexing/demultiplexing?
- **Back:** Multiplexing mbledh data nga shumë sockets dhe shton header; demultiplexing përdor header-in për t’ia dhënë segmentin socket-it të saktë.
- **Tags:** rrjeta::l3

### 043
- **Front:** Si identifikohet UDP socket për demultiplexing?
- **Back:** Kryesisht nga destination IP address dhe destination port number.
- **Tags:** rrjeta::l3

### 044
- **Front:** Si identifikohet TCP socket?
- **Back:** Nga 4-tuple: source IP, source port, destination IP dhe destination port.
- **Tags:** rrjeta::l3

### 045
- **Front:** Cilat janë tiparet kryesore të UDP?
- **Back:** Connectionless best-effort; segmentet mund të humbin ose të dalin out-of-order; header i vogël; pa flow/congestion control dhe pa setup handshake.
- **Tags:** rrjeta::l3

### 046
- **Front:** Çfarë kontrollon UDP checksum?
- **Back:** Zbulon gabime të rastësishme në segment (përfshirë header/payload sipas llogaritjes); nuk e garanton rikuperimin e të dhënave.
- **Tags:** rrjeta::l3

### 047
- **Front:** Pse duhen sequence numbers në reliable data transfer?
- **Back:** Për të dalluar paketat e reja nga duplicate retransmissions dhe për të ruajtur rendin e dorëzimit.
- **Tags:** rrjeta::l3

### 048
- **Front:** Pse duhet timeout në rdt3.0?
- **Back:** Sepse data packets ose ACK mund të humbin; sender-i duhet të retransmetojë kur ACK nuk arrin në kohë.
- **Tags:** rrjeta::l3

### 049
- **Front:** Pse stop-and-wait ka utilization të dobët në path me RTT të madh?
- **Back:** Sender-i pret ACK pas çdo pakete, kështu linku rri idle për pjesën më të madhe të RTT-së.
- **Tags:** rrjeta::l3

### 050
- **Front:** Çfarë sjell pipelining?
- **Back:** Lejon shumë paketa in flight para ACK-ve, duke rritur utilization/throughput; kërkon sequence range dhe buffering më të sofistikuar.
- **Tags:** rrjeta::l3

### 051
- **Front:** Si reagon Go-Back-N ndaj një pakete të humbur?
- **Back:** Receiver zakonisht dërgon duplicate cumulative ACK për last in-order; sender-i pas timeout-it retransmeton paketën e humbur dhe të gjitha pas saj që s’janë ACK-uar.
- **Tags:** rrjeta::l3

### 052
- **Front:** Si ndryshon Selective Repeat nga Go-Back-N?
- **Back:** SR buffer-on out-of-order packets dhe retransmeton vetëm paketën e humbur; GBN mund të retransmetojë një varg paketash.
- **Tags:** rrjeta::l3

### 053
- **Front:** Cilat shërbime ofron TCP?
- **Back:** Reliable, in-order byte stream; connection-oriented, full-duplex; flow control dhe congestion control.
- **Tags:** rrjeta::l3

### 054
- **Front:** Çfarë numëron TCP sequence number?
- **Back:** Byte-n e parë të data-s në segment, jo thjesht numrin e segmentit.
- **Tags:** rrjeta::l3

### 055
- **Front:** Çfarë tregon TCP ACK number?
- **Back:** Numrin e byte-it të ardhshëm që receiver-i pret; TCP ACK është cumulative.
- **Tags:** rrjeta::l3

### 056
- **Front:** Çfarë është fast retransmit në TCP?
- **Back:** Kur sender-i merr 3 duplicate ACK për të njëjtën data, inferon loss dhe retransmeton segmentin e munguar pa pritur timeout.
- **Tags:** rrjeta::l3

### 057
- **Front:** Çfarë problemi zgjidh TCP flow control dhe cili field përdor?
- **Back:** Parandalon mbushjen e receiver buffer kur aplikacioni lexon ngadalë; receiver reklam-on receive window (rwnd).
- **Tags:** rrjeta::l3

### 058
- **Front:** Radhit mesazhet e TCP 3-way handshake.
- **Back:** Client SYN(seq=x) → server SYN+ACK(seq=y, ack=x+1) → client ACK(ack=y+1).
- **Tags:** rrjeta::l3

### 059
- **Front:** Flow control kundrejt congestion control?
- **Back:** Flow control mbron receiver-in nga sender-i; congestion control mbron rrjetin/router buffers nga shumë trafik.
- **Tags:** rrjeta::l3

### 060
- **Front:** Çfarë është cwnd në TCP?
- **Back:** Congestion window: kufi i sender-it për bytes in flight sipas congestion-it të perceptuar në rrjet.
- **Tags:** rrjeta::l3

### 061
- **Front:** Çfarë është slow start?
- **Back:** Faza TCP ku cwnd rritet afërsisht eksponencialisht me ACK-të deri te ssthresh ose loss.
- **Tags:** rrjeta::l3

### 062
- **Front:** Çfarë është congestion avoidance?
- **Back:** Pas slow start, TCP rrit cwnd gradualisht, përafërsisht një MSS për RTT (additive increase).
- **Tags:** rrjeta::l3

### 063
- **Front:** Çfarë është AIMD dhe pse përdoret?
- **Back:** Additive Increase, Multiplicative Decrease; rrit ngadalë dërgimin dhe e ul shumë pas loss për stabilitet dhe fairness mes flows.
- **Tags:** rrjeta::l3

### 064
- **Front:** Si ndryshon reagimi klasik TCP Reno ndaj triple duplicate ACK dhe timeout?
- **Back:** Me triple duplicate ACK zakonisht ul cwnd përgjysmë; me timeout reagon më fort, zakonisht cwnd kthehet në 1 MSS.
- **Tags:** rrjeta::l3

### 065
- **Front:** Pse QUIC redukton head-of-line blocking të HTTP/2 mbi TCP?
- **Back:** QUIC implementon streams dhe recovery të ndarë mbi UDP; loss në një stream nuk bllokon domosdoshmërisht delivery në stream-et e tjera.
- **Tags:** rrjeta::l3

## Ligjerata 4 — Network layer data plane

### 066
- **Front:** Data plane kundrejt control plane?
- **Back:** Data plane kryen forwarding lokal të paketave; control plane llogarit/instalon forwarding state dhe routing policy.
- **Tags:** rrjeta::l4

### 067
- **Front:** Çfarë bën longest prefix matching?
- **Back:** Zgjedh forwarding-table entry me prefiksin më të gjatë, pra më specifik, që përputhet me destination IP.
- **Tags:** rrjeta::l4

### 068
- **Front:** Cilat janë tre llojet kryesore të switching fabric?
- **Back:** Switching via memory, via bus dhe via interconnection network.
- **Tags:** rrjeta::l4

### 069
- **Front:** Kur ndodh input queueing dhe çfarë është HOL blocking?
- **Back:** Kur input packets s’mund të kalojnë aq shpejt sa arrijnë; head-of-line blocking ndodh kur paketa e parë bllokon paketa pas saj edhe nëse ato mund të shkonin në output tjetër.
- **Tags:** rrjeta::l4

### 070
- **Front:** FIFO, priority dhe round-robin scheduling në një fjali secila?
- **Back:** FIFO: e para që vjen shërbehet e para; priority: klasa me prioritet më të lartë shërbehet e para; RR: klasat shërbehen në cikël me nga një paketë kur kanë data.
- **Tags:** rrjeta::l4

### 071
- **Front:** Çfarë identifikon një IPv4 address?
- **Back:** Një interface hosti ose routeri; IPv4 address ka 32 bits.
- **Tags:** rrjeta::l4

### 072
- **Front:** Çfarë është subnet dhe çfarë nënkupton /24?
- **Back:** Një grup interfaces që mund të komunikojnë pa kaluar router; /24 do të thotë 24 high-order bits janë network prefix/maskë.
- **Tags:** rrjeta::l4

### 073
- **Front:** Cilat janë katër mesazhet kryesore DHCP?
- **Back:** DHCP Discover, Offer, Request dhe ACK.
- **Tags:** rrjeta::l4

### 074
- **Front:** Çfarë konfigurimi merr zakonisht klienti nga DHCP?
- **Back:** IP address, subnet mask, IP e default gateway/first-hop router dhe emër/adresë DNS serveri.
- **Tags:** rrjeta::l4

### 075
- **Front:** Çfarë bën NAT?
- **Back:** Përkthen private IP addresses dhe shpesh portet e rrjetit lokal në public IP/ports kur trafiku del ose hyn në Internet.
- **Tags:** rrjeta::l4

### 076
- **Front:** Një avantazh dhe një kufizim i NAT?
- **Back:** Avantazh: kursen IPv4 public addresses dhe fsheh adresimin lokal; kufizim: prish end-to-end transparency dhe komplikon inbound connections.
- **Tags:** rrjeta::l4

### 077
- **Front:** Sa bits ka IPv6 dhe pse u krijua?
- **Back:** 128 bits; adreson mungesën e IPv4 dhe sjell header më të thjeshtuar/ekstensibilitet.
- **Tags:** rrjeta::l4

### 078
- **Front:** Çfarë është tunneling në migrimin IPv4/IPv6?
- **Back:** Encapsulation e një datagrami IPv6 si payload brenda IPv4 për ta kaluar një pjesë të rrjetit që ende përdor IPv4.
- **Tags:** rrjeta::l4

### 079
- **Front:** Çfarë është generalized forwarding/match+action?
- **Back:** Rregulla që bëjnë match mbi fusha header dhe kryejnë action si forward, drop, modify ose send-to-controller.
- **Tags:** rrjeta::l4

### 080
- **Front:** Pse IP quhet “thin waist” i Internetit?
- **Back:** Shumë aplikacione/protokolle transporti mund të punojnë mbi IP dhe IP mund të punojë mbi shumë link technologies; një shtresë e përbashkët lidh diversitetin sipër/poshtë.
- **Tags:** rrjeta::l4

## Ligjerata 5 — Network layer control plane

### 081
- **Front:** Çfarë kërkon të gjejë routing protocol?
- **Back:** Path-e të mira nga source te destination përmes routerëve sipas një metric/policy si cost, delay, congestion ose administrim.
- **Tags:** rrjeta::l5

### 082
- **Front:** Cila është ideja e link-state routing?
- **Back:** Çdo router merr topologjinë dhe link costs për gjithë rrjetin përmes link-state broadcast dhe llogarit shortest paths lokalisht me Dijkstra.
- **Tags:** rrjeta::l5

### 083
- **Front:** Cili është hapi përsëritës kryesor i Dijkstra-s?
- **Back:** Zgjedh nyjën jashtë N' me estimated cost minimal, e shton në N', pastaj relakson/update-on distancat e neighbours të saj.
- **Tags:** rrjeta::l5

### 084
- **Front:** Cila është Bellman-Ford equation për distance-vector?
- **Back:** D_x(y) = min_v { c(x,v) + D_v(y) }: për çdo neighbour v, cost-i për y përmes v; merret minimumi.
- **Tags:** rrjeta::l5

### 085
- **Front:** Cila është ideja e distance-vector routing?
- **Back:** Routeri mban cost-in e vet për destinacionet, shkëmben vector-in me neighbours dhe i përditëson kostot me Bellman-Ford.
- **Tags:** rrjeta::l5

### 086
- **Front:** Çfarë është count-to-infinity problem?
- **Back:** Pas rritjes së kostos/prishjes së linkut, distance-vector routers mund të besojnë gabimisht se neighbour-i ka rrugë dhe të rrisin gradualisht metric-un në loop; bad news travels slow.
- **Tags:** rrjeta::l5

### 087
- **Front:** Si ndihmon poisoned reverse?
- **Back:** Routeri i thotë neighbour-it se destinacioni i arritshëm përmes atij neighbour-i ka cost infinite; redukton loops të thjeshta me dy nyje.
- **Tags:** rrjeta::l5

### 088
- **Front:** Çfarë është Autonomous System (AS)?
- **Back:** Një rrjet/grup rrjetesh nën një administrim të përbashkët dhe routing policy të përbashkët.
- **Tags:** rrjeta::l5

### 089
- **Front:** OSPF kundrejt BGP?
- **Back:** OSPF është intra-AS link-state routing; BGP është inter-AS path-vector routing i drejtuar fort nga policy.
- **Tags:** rrjeta::l5

### 090
- **Front:** Çfarë reklamojnë BGP peers?
- **Back:** Paths drejt destination network prefixes, përfshirë AS-PATH; peer-i premton t’i forward-ojë datagramet drejt atij destinacioni.
- **Tags:** rrjeta::l5

### 091
- **Front:** eBGP kundrejt iBGP?
- **Back:** eBGP shkëmben routes mes AS-ve; iBGP shpërndan informacionin BGP brenda një AS-i.
- **Tags:** rrjeta::l5

### 092
- **Front:** Pse BGP nuk zgjedh domosdoshmërisht shortest path?
- **Back:** Inter-AS routing respekton policy ekonomike/administrative; një AS kontrollon kujt i ofron transit dhe cilat rrugë reklamon.
- **Tags:** rrjeta::l5

### 093
- **Front:** Çfarë do të thotë “logically centralized” control plane në SDN?
- **Back:** Control decisions merren nga controller me pamje/policy qendrore logjike, edhe nëse implementimi i tij është i shpërndarë fizikisht.
- **Tags:** rrjeta::l5

### 094
- **Front:** Çfarë mundëson SDN më lehtë se routing tradicional?
- **Back:** Programim dhe menaxhim më fleksibël i flow tables për routing, access control, load balancing dhe traffic engineering.
- **Tags:** rrjeta::l5

### 095
- **Front:** Çfarë është OpenFlow në kontekstin SDN?
- **Back:** Protokoll southbound që lejon controller-in dhe switch-in të shkëmbejnë mesazhe/control për flow rules; jo vetë API-ja e apps.
- **Tags:** rrjeta::l5

### 096
- **Front:** Çfarë përdoret ICMP për?
- **Back:** Error reporting dhe diagnostikim në network layer, p.sh. destination unreachable dhe TTL expired; e përdorin ping/traceroute.
- **Tags:** rrjeta::l5

### 097
- **Front:** SNMP manager/agent/MIB në një fjali?
- **Back:** Manager-i monitoron/konfiguron; agent-i në managed device ekspozon data; MIB përcakton objektet e menaxhueshme.
- **Tags:** rrjeta::l5

### 098
- **Front:** Çfarë bën YANG krahas NETCONF?
- **Back:** YANG është data-modeling language që specifikon strukturë, sintaksë, semantikë dhe constraints; NETCONF përdor RPC për të shkëmbyer/configuruar atë data.
- **Tags:** rrjeta::l5

## Ligjerata 6 — Link layer dhe LANs

### 099
- **Front:** Çfarë shërbimi kryesor ofron link layer?
- **Back:** Transferimin e datagramit midis network nodes fqinje në një link të vetëm; mund të ofrojë framing, access control dhe error detection/correction.
- **Tags:** rrjeta::l6

### 100
- **Front:** Ku implementohet zakonisht link layer në host?
- **Back:** Në NIC/network adapter, si kombinim hardware, firmware dhe software, pranë physical layer.
- **Tags:** rrjeta::l6

### 101
- **Front:** Parity, checksum dhe CRC — dallimi kryesor?
- **Back:** Parity është shumë i thjeshtë; checksum bazohet në one’s-complement sum; CRC përdor polynomial/modulo-2 dhe zbulon shumë mirë burst errors.
- **Tags:** rrjeta::l6

### 102
- **Front:** Cilat janë tri kategori të MAC protocols?
- **Back:** Channel partitioning, random access dhe taking turns.
- **Tags:** rrjeta::l6

### 103
- **Front:** Si funksionon slotted ALOHA në rast collision?
- **Back:** Node dërgon në fillim slot-i; kur collision ndodh, pret random number of slots pastaj provon përsëri.
- **Tags:** rrjeta::l6

### 104
- **Front:** Çfarë do të thotë CSMA?
- **Back:** Carrier Sense Multiple Access: node dëgjon kanalin para se të transmetojë; nëse është busy, defer-on.
- **Tags:** rrjeta::l6

### 105
- **Front:** Çfarë shton CSMA/CD dhe ku përdoret klasikisht?
- **Back:** Collision detection: zbulon collision gjatë transmetimit dhe aborton; përdoret në Ethernet shared/bus klasik.
- **Tags:** rrjeta::l6

### 106
- **Front:** Pse Wi‑Fi përdor CSMA/CA në vend të CSMA/CD?
- **Back:** Radio transmitter-i s’mund të dëgjojë me besueshmëri collision gjatë dërgimit dhe hidden terminals ekzistojnë; prandaj Wi‑Fi shmang collisions me backoff/ACK/RTS-CTS.
- **Tags:** rrjeta::l6

### 107
- **Front:** Çfarë është MAC address dhe sa bits ka?
- **Back:** Link-layer/LAN address për komunikim lokal mes interfaces fqinje; zakonisht 48 bits.
- **Tags:** rrjeta::l6

### 108
- **Front:** Çfarë bën ARP?
- **Back:** Zbulon MAC address-in e një interface-i në të njëjtin LAN për një IP address të dhënë; request broadcast, reply zakonisht unicast, pastaj cache me TTL.
- **Tags:** rrjeta::l6

### 109
- **Front:** Kur host-i dërgon paketë te një subnet tjetër, MAC-in e kujt gjen me ARP?
- **Back:** MAC-in e default gateway/first-hop router në LAN-in lokal, jo MAC-in e destination host-it të largët.
- **Tags:** rrjeta::l6

### 110
- **Front:** Cilat fusha kryesore ka Ethernet frame?
- **Back:** Preamble, destination MAC, source MAC, type, payload dhe CRC.
- **Tags:** rrjeta::l6

### 111
- **Front:** Si self-learns një Ethernet switch?
- **Back:** Kur pranon frame, ruan source MAC dhe incoming port me timestamp në switch table; pastaj përdor destination MAC për forward/flood.
- **Tags:** rrjeta::l6

### 112
- **Front:** Çfarë bën switch-i kur destination MAC nuk është në tabelë?
- **Back:** Flood-on frame-in në të gjitha portet e tjera në të njëjtin LAN/VLAN përveç portit hyrës.
- **Tags:** rrjeta::l6

### 113
- **Front:** Switch kundrejt router?
- **Back:** Switch është kryesisht link-layer dhe forward-on sipas MAC; router është network-layer, forward-on sipas IP dhe ndan subnets/broadcast domains.
- **Tags:** rrjeta::l6

### 114
- **Front:** Çfarë është VLAN dhe pse përdoret?
- **Back:** Virtual LAN krijon broadcast domains logjike mbi switch infrastructure të përbashkët; përdoret për segmentim, shkallëzim dhe administrim.
- **Tags:** rrjeta::l6

### 115
- **Front:** Çfarë është MPLS në një fjali?
- **Back:** Mekanizëm label-switched që lejon path/forwarding policy me labels, jo vetëm longest-prefix IP routing.
- **Tags:** rrjeta::l6

## Ligjerata 7 — Wireless dhe mobile

### 116
- **Front:** Wireless kundrejt mobility?
- **Back:** Wireless do të thotë komunikim pa tel; një host wireless mund të jetë i palëvizshëm, ndërsa mobility nënkupton ndryshim të pikës/rrjetit të lidhjes.
- **Tags:** rrjeta::l7

### 117
- **Front:** Cilat janë elementet kryesore të një wireless network me infrastrukturë?
- **Back:** Wireless hosts, base station/AP, wireless links dhe wired network infrastructure që AP-ja e lidh me Internetin.
- **Tags:** rrjeta::l7

### 118
- **Front:** Çfarë është path loss dhe si ndikon frekuenca/distanca?
- **Back:** Attenuation e signal-it gjatë propagimit; zakonisht humbja rritet me distancën dhe me frekuencë më të lartë.
- **Tags:** rrjeta::l7

### 119
- **Front:** Çfarë është SNR dhe ç’lidhje ka me BER?
- **Back:** Signal-to-noise ratio; SNR më i lartë e bën më të lehtë nxjerrjen e signal-it nga noise dhe zakonisht ul bit error rate.
- **Tags:** rrjeta::l7

### 120
- **Front:** Çfarë është hidden terminal problem?
- **Back:** Dy nodes nuk e dëgjojnë njëri-tjetrin, por transmetimet e tyre interferojnë te një receiver/AP i përbashkët.
- **Tags:** rrjeta::l7

### 121
- **Front:** Çfarë është CDMA në ide?
- **Back:** Nodes përdorin codes të ndryshme për të ndarë të njëjtin medium/frekuencë; receiver-i përdor kodin përkatës për të rikuperuar sinjalin e dërguesit.
- **Tags:** rrjeta::l7

### 122
- **Front:** Si lidhet një host i ri me 802.11 AP?
- **Back:** Skanon channels dhe dëgjon beacon frames me SSID/MAC, zgjedh AP, bën association/authentication dhe zakonisht DHCP për IP.
- **Tags:** rrjeta::l7

### 123
- **Front:** Cilat janë hapat bazë të 802.11 CSMA/CA kur mediumi është busy?
- **Back:** Zgjedh random backoff; timeri numëron vetëm kur kanali është idle dhe kur arrin zero, host-i transmeton; receiver-i ACK-on pas SIFS.
- **Tags:** rrjeta::l7

### 124
- **Front:** Çfarë roli kanë RTS dhe CTS në Wi‑Fi?
- **Back:** Mund të rezervojnë mediumin për data/ACK exchange dhe të reduktojnë collisions nga hidden terminals, me kosto overhead.
- **Tags:** rrjeta::l7

### 125
- **Front:** Çfarë është rate adaptation në 802.11?
- **Back:** AP/mobile ndryshon dinamikisht modulation/transmission rate sipas SNR/quality të linkut.
- **Tags:** rrjeta::l7

### 126
- **Front:** Cilat janë komponentët kryesorë të 4G LTE architecture?
- **Back:** UE/mobile device, eNodeB/base station, MME, Serving Gateway (S-GW), PDN Gateway (P-GW) dhe Home Subscriber Service (HSS).
- **Tags:** rrjeta::l7

### 127
- **Front:** Cili është roli i eNodeB në LTE?
- **Back:** Është base station në edge të carrier network; menaxhon radio resources dhe lidh UE-në me packet core.
- **Tags:** rrjeta::l7

### 128
- **Front:** Çfarë është OFDMA në LTE?
- **Back:** Orthogonal Frequency Division Multiple Access: ndan kohë/frekuencë në resource blocks/subcarriers që scheduler-i ia cakton UE-ve.
- **Tags:** rrjeta::l7

### 129
- **Front:** Çfarë bën GTP tunneling në mobile packet core?
- **Back:** Encapsulon mobile datagramet në GTP/UDP/IP për t’i bartur mes eNodeB, S-GW dhe P-GW duke ruajtur mobility/data path state.
- **Tags:** rrjeta::l7

### 130
- **Front:** Cilat janë katër detyrat kryesore të mobility management?
- **Back:** Association, authentication, location tracking/routing dhe handover mes base stations.
- **Tags:** rrjeta::l7

### 131
- **Front:** Çfarë është triangle routing në indirect mobility routing?
- **Back:** Datagrams kalojnë fillimisht nga home network te mobile edhe kur correspondent dhe mobile janë afër; është transparent, por jo efikas.
- **Tags:** rrjeta::l7

### 132
- **Front:** Pse TCP mund të performojë keq mbi wireless/mobile networks?
- **Back:** TCP interpreton loss nga bit errors ose handover si congestion dhe ul cwnd, edhe kur rrjeti nuk është domosdoshmërisht i mbingarkuar.
- **Tags:** rrjeta::l7
