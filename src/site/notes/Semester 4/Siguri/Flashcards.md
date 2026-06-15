---
{"dg-publish":true,"permalink":"/semester-4/siguri/flashcards/"}
---

# Flashcards - Siguria e te dhenave

Generated from the three exam PDFs plus the lecture summary. The first block is exam-style coverage; later cards broaden the deck for studying.

For Anki import use `flashcards.csv` with fields: `Front`, `Back`, `Tags`. Enable HTML so `<br>` line breaks render nicely.

## Card 001

**Q:** Cilat jane kater shtyllat/vetite kryesore te kriptografise?

**A:** Confidentiality/fshehtesia, Integrity/integriteti, Authentication/autentikimi, Non-repudiation/jo-mohueshmeria. Keto mbulojne fshehjen, zbulimin e ndryshimit, verifikimin e paleve dhe pamundesine per ta mohuar nje veprim te nenshkruar.

**Tags:** `siguri exam core`

## Card 002

**Q:** Sipas Claude Shannon, cilat jane dy konceptet fondamentale te sigurise se shifrave?

**A:** Confusion dhe Diffusion. Confusion e fsheh lidhjen mes plaintext, ciphertext dhe celesit. Diffusion i shperndan statistikat e plaintext-it neper ciphertext, qe nje ndryshim i vogel ne hyrje te ndikoje ne shume pjese te daljes.

**Tags:** `siguri exam shannon`

## Card 003

**Q:** Cka eshte confusion sipas Shannon?

**A:** Confusion do te thote ta bejme lidhjen mes plaintext-it, ciphertext-it dhe celesit sa me te paqarte. S-Box-at ne DES jane shembull i mekanizmit qe krijon confusion.

**Tags:** `siguri shannon`

## Card 004

**Q:** Cka eshte diffusion sipas Shannon?

**A:** Diffusion do te thote qe statistikat dhe modelet e plaintext-it te shperndahen ne ciphertext. Nje ndryshim i vogel ne plaintext duhet te shkaktoje ndryshim te madh ne ciphertext.

**Tags:** `siguri shannon`

## Card 005

**Q:** Si shkruhet formula e Caesar cipher per alfabetin shqip?

**A:** Nese alfabeti ka m shkronja: E_n(X) = (X + n) mod m dhe D_n(X) = (X - n) mod m. Per alfabetin shqip zakonisht merret m = 36. Ideja eshte e njejte si mod 26 ne alfabetin latin klasik.

**Tags:** `siguri exam caesar`

## Card 006

**Q:** Pse Caesar cipher mbetet i dobet edhe nese perdoret me alfabetin shqip?

**A:** Sepse eshte monoalphabetic substitution: cdo shkronje zhvendoset me te njejtin celes. Keyspace eshte i vogel, mund te provohen te gjitha zhvendosjet, dhe frekuencat e gjuhes ende ndihmojne kriptoanalizen.

**Tags:** `siguri exam caesar`

## Card 007

**Q:** Cka dallon Caesar cipher nga Jefferson cylinder nga aspekti kriptografik?

**A:** Caesar eshte substitution monoalfabetik me nje zhvendosje fikse. Jefferson cylinder perdor disa disqe/alfabete dhe jep sjellje polialfabetike me keyspace shume me te madh. Pra ne parim Jefferson eshte me i forte; Caesar ne shqip vetem e rrit pak hapesiren e alfabetit, por mbetet i dobet.

**Tags:** `siguri exam caesar jefferson`

## Card 008

**Q:** Nese profesori pyet pse Caesar ne shqip mund te duket me i sigurt se nje shembull i thjeshte Jefferson, cka duhet theksuar?

**A:** Thuaj se alfabeti shqip ka me shume simbole se alfabeti klasik 26-shkronjesh, prandaj rritet pak keyspace dhe ndryshon analiza frekuencore. Por kriptografikisht, nje Jefferson cylinder i perdorur mire eshte me i forte se Caesar.

**Tags:** `siguri exam caesar jefferson`

## Card 009

**Q:** Pse low-order RGB bits dont matter ne steganografi?

**A:** Sepse bitet me peshe me te vogel ndryshojne ngjyren shume pak. Syri i njeriut zakonisht nuk e dallon ndryshimin, por programi mund t'i lexoje ato bite dhe te nxjerre mesazhin e fshehur.

**Tags:** `siguri exam steganografi`

## Card 010

**Q:** Si llogaritet kapaciteti i steganografise ne imazh?

**A:** Total pixels = width * height. Total bits = total pixels * bits_per_pixel_used. Total bytes = total bits / 8. Total kB = bytes / 1024.

**Tags:** `siguri exam steganografi`

## Card 011

**Q:** Ne steganografi, si fshihet shkronja A = 0x41 ne 4 piksela kur perdoren 2 LSB per pixel?

**A:** 0x41 = 01000001. Ndaje ne grupe 2-bit: 01 00 00 01. Vendosi keto grupe ne dy bitet me peshe me te vogel te secilit pixel/kanal te zgjedhur.

**Tags:** `siguri exam steganografi`

## Card 012

**Q:** Zgjidhe ushtrimin: 0x61 0x80 0x2F, 0x61 0x80 0x2E, 0x61 0x80 0x2D, 0x61 0x80 0x2C; fsheh A=0x41 me 2 LSB ne byte-in e fundit.

**A:** A = 01000001 -> 01 00 00 01. Byte-at e fundit behen: 0x2F -> 0x2D, 0x2E -> 0x2C, 0x2D -> 0x2C, 0x2C -> 0x2D. Pra pixelet: 0x61 0x80 0x2D; 0x61 0x80 0x2C; 0x61 0x80 0x2C; 0x61 0x80 0x2D.

**Tags:** `siguri exam steganografi`

## Card 013

**Q:** Cka jane S-Box-at ne DES?

**A:** S-Box-at jane tabela zevendesimi jolineare. Ne DES ka 8 S-Box-a; secili merr 6 bit hyrje dhe jep 4 bit dalje. Ato krijojne confusion dhe jane pjese kritike e sigurise se DES.

**Tags:** `siguri exam des`

## Card 014

**Q:** Si lexohet hyrja 6-bit ne nje S-Box te DES?

**A:** Per hyrjen b1 b2 b3 b4 b5 b6, rreshti merret nga b1b6, ndersa kolona nga b2b3b4b5. Dalja eshte vlera 4-bit ne ate pozite te S-Box-it.

**Tags:** `siguri des`

## Card 015

**Q:** Cilat jane hapat e Diffie-Hellman-Merkle?

**A:** Palet zgjedhin publikisht p dhe g. Alice zgjedh sekretin a dhe dergon A = g^a mod p. Bob zgjedh sekretin b dhe dergon B = g^b mod p. Alice llogarit K = B^a mod p, Bob llogarit K = A^b mod p. Te dy marrin K = g^(ab) mod p.

**Tags:** `siguri exam dhm`

## Card 016

**Q:** Diffie-Hellman me p=7, g=5, B=2, a=3: sa eshte A dhe sekreti s?

**A:** A = g^a mod p = 5^3 mod 7 = 125 mod 7 = 6. Sekreti s = B^a mod p = 2^3 mod 7 = 8 mod 7 = 1.

**Tags:** `siguri exam dhm calculation`

## Card 017

**Q:** Diffie-Hellman me p=10, g=3, B=2, a=4: sa eshte A dhe sekreti s?

**A:** A = 3^4 mod 10 = 81 mod 10 = 1. Sekreti s = 2^4 mod 10 = 16 mod 10 = 6. Shenim: ne praktike p duhet te jete prime, por ketu llogaritet sipas detyres.

**Tags:** `siguri exam dhm calculation`

## Card 018

**Q:** Ne cilin rast modet ECB/CBC/etc. nuk kane shume rendesi?

**A:** Kur enkriptohet vetem nje bllok i vetem. Modet e operimit kryesisht percaktojne si lidhen disa blloqe; per nje bllok te vetem nuk ka perseritje ose chaining mes blloqeve.

**Tags:** `siguri exam modes`

## Card 019

**Q:** Pse duhet perdorur CBC ne vend te ECB?

**A:** CBC e lidh cdo bllok me ciphertext-in paraprak: Ci = E(K, Pi XOR Ci-1). Keshtu blloqet e njejta plaintext nuk japin ciphertext te njejte dhe fshihen perseritjet qe ECB i zbulon.

**Tags:** `siguri exam cbc`

## Card 020

**Q:** Cilat jane formulat e CBC?

**A:** Enkriptimi: Ci = E(K, Pi XOR Ci-1). Dekriptimi: Pi = D(K, Ci) XOR Ci-1. Per bllokun e pare perdoret IV si C0.

**Tags:** `siguri exam cbc`

## Card 021

**Q:** Cka siguron me shume CBC krahasuar me ECB?

**A:** CBC fsheh modelet dhe perseritjet e blloqeve sepse cdo ciphertext varet nga blloku paraprak. Megjithate CBC vetem nuk siguron integritet; per ate duhet MAC ose mode autentikuese.

**Tags:** `siguri cbc`

## Card 022

**Q:** Tek RSA, cila eshte formula qe lidh celesin publik me ate privat?

**A:** e*d mod phi(N) = 1, ku phi(N) = (p-1)(q-1) kur N = p*q. Celesi publik eshte (e, N), celesi privat eshte d ose (d, N).

**Tags:** `siguri exam rsa`

## Card 023

**Q:** Ne shembullin RSA p=5, q=11, n=55, phi=40, e=3, d=27: cili eshte celesi publik dhe privat?

**A:** Celesi publik eshte (e, n) = (3, 55). Celesi privat eshte d = 27, ose ne forme me modul (27, 55).

**Tags:** `siguri exam rsa calculation`

## Card 024

**Q:** Me RSA parametrat n=55, e=3, d=27, enkripto m=5.

**A:** C = m^e mod n = 5^3 mod 55 = 125 mod 55 = 15. Pra ciphertext C = 15.

**Tags:** `siguri exam rsa calculation`

## Card 025

**Q:** Pse celesat RSA jane shume me te gjate se celesat simetrik?

**A:** Sepse siguria e RSA bazohet ne faktorizimin e N=p*q dhe sulmet ndaj tij jane ndryshe nga brute force simetrik. Per te arritur nivel te ngjashem sigurie, RSA ka nevoje per shume me shume bit se AES/DES.

**Tags:** `siguri exam rsa`

## Card 026

**Q:** Cka eshte PBKDF2 dhe per cka sherben?

**A:** PBKDF2 eshte Password-Based Key Derivation Function. Merr password, salt dhe numer iterimesh, pastaj prodhon nje derived key/hash. Qellimi eshte te ngadalesoje brute force dhe dictionary attacks.

**Tags:** `siguri exam pbkdf2`

## Card 027

**Q:** Cka eshte numri i perseritjeve/iterations ne PBKDF2 dhe si ndikon ne siguri?

**A:** Iterations tregojne sa here perseritet funksioni pseudorandom/HMAC. Sa me i madh numri, aq me i shtrenjte eshte cdo provim password-i per sulmuesin. Por rritet edhe koha per perdoruesin legjitim.

**Tags:** `siguri exam pbkdf2`

## Card 028

**Q:** Pse nuk duhet ta ruajme password-in vetem si PasswordHash pa salt?

**A:** Sepse password-et e njejta japin hash te njejte dhe sulmuesi mund te perdore rainbow tables/dictionary attacks. Salt unik per perdorues i ben hash-et te ndryshme dhe e veshtireson sulmin masiv.

**Tags:** `siguri exam passwords`

## Card 029

**Q:** Per HMAC, pervec mesazhit, cka duhet te dihet?

**A:** Duhet te dihet edhe celesi sekret. HMAC = keyed hash; pa celesin, sulmuesi nuk mund te krijoje MAC valid edhe nese e di mesazhin.

**Tags:** `siguri exam hmac`

## Card 030

**Q:** Cila fushe/veti eshte e obliguar si te PGP ashtu edhe te X.509 certifikatat?

**A:** Nenshkrimi/signature. Pa nenshkrim nuk ka certifikim te lidhjes mes identitetit dhe celesit publik. X.509 ka zakonisht nje nenshkrim nga CA; PGP ka te pakten nje dhe shpesh disa.

**Tags:** `siguri exam certificates`

## Card 031

**Q:** Sheno tri ngjashmeri mes PGP dhe X.509 certifikatave.

**A:** Te dyja lidhen identitetin me celes publik; te dyja permbajne ose mbeshteten ne nenshkrime; te dyja perdoren per verifikim/autentikim te celesave publik dhe per te shmangur MITM.

**Tags:** `siguri exam certificates`

## Card 032

**Q:** Sheno dy dallime dhe nje ngjashmeri mes SHA-1 dhe MD5.

**A:** Dallime: MD5 ka dalje 128 bit, SHA-1 ka dalje 160 bit. SHA-1 ka strukture/raunde te ndryshme dhe historikisht konsiderohej me i forte se MD5. Ngjashmeri: te dy jane hash funksione njekaheshe me hyrje arbitrare dhe dalje fikse; te dy sot nuk jane te rekomanduar per collision security.

**Tags:** `siguri exam hash`

## Card 033

**Q:** Sa eshte gjatesia e hash-it SHA-1 dhe MD5 per nje MP3 4.20 MB?

**A:** Gjatesia e hash-it nuk varet nga madhesia e fajllit. SHA-1 = 160 bit. MD5 = 128 bit.

**Tags:** `siguri exam hash`

## Card 034

**Q:** Pershkruaj matematikisht nenshkrimin digjital.

**A:** Derguesi llogarit h = H(M), pastaj S = E(Kpriv_dergues, h). Marresi llogarit H(M) vete dhe kontrollon nese D(Kpub_dergues, S) == H(M).

**Tags:** `siguri exam signature`

## Card 035

**Q:** Cka siguron nenshkrimi digjital dhe cka nuk siguron?

**A:** Siguron autenticitet, integritet dhe non-repudiation. Nuk siguron privatesi; per privatesi duhet enkriptim me celesin publik te marresit ose me session key simetrik.

**Tags:** `siguri exam signature`

## Card 036

**Q:** Cilat jane 3 tipet e nenshkrimeve elektronike sipas eIDAS?

**A:** Electronic signature, Advanced electronic signature, Qualified electronic signature. Qualified eshte advanced signature e krijuar me pajisje te kualifikuar dhe certifikate te kualifikuar.

**Tags:** `siguri exam eidas`

## Card 037

**Q:** Cka eshte EU eIDAS?

**A:** eIDAS eshte rregullorja e BE-se per identifikim elektronik dhe sherbime te besuara: nenshkrime elektronike, vula elektronike, timestamp, delivery services dhe website authentication, me vlefshmeri nderkufitare.

**Tags:** `siguri exam eidas`

## Card 038

**Q:** Cka eshte man-in-the-middle attack?

**A:** Sulmuesi vendoset mes dy paleve dhe u paraqitet seciles si pala tjeter. Ai mund te zevendesoje celesat publik, te lexoje, ndryshoje dhe ri-enkriptoje mesazhet pa u vene re.

**Tags:** `siguri exam mitm`

## Card 039

**Q:** Si i ikim man-in-the-middle attack ne shkembim celesash?

**A:** Me certifikata X.509/PKI, nenshkrime digjitale, authenticated Diffie-Hellman, verifikim te fingerprint-it out-of-band dhe kontroll te chain of trust.

**Tags:** `siguri exam mitm`

## Card 040

**Q:** Alice do t'i dergoje Bob-it mesazh privat. Me cilin celes e enkripton?

**A:** Me celesin publik te Bob-it. Vetem Bob mund ta dekriptoje me celesin e vet privat.

**Tags:** `siguri exam public-key`

## Card 041

**Q:** Bob merr mesazh te enkriptuar per te. Me cilin celes e dekripton?

**A:** Me celesin e vet privat. Mesazhi eshte enkriptuar me celesin publik te Bob-it.

**Tags:** `siguri exam public-key`

## Card 042

**Q:** Bob do t'i nenshkruaje digjitalisht mesazhet e veta. Cilin celes perdor?

**A:** Bob perdor celesin e vet privat per nenshkrim. Te tjeret e verifikojne nenshkrimin me celesin publik te Bob-it.

**Tags:** `siguri exam signature`

## Card 043

**Q:** Alice nenshkruan mesazhet e veta. Si e verifikon Bob autenticitetin?

**A:** Bob perdor celesin publik te Alice per te verifikuar nenshkrimin. Nese hash-i i verifikuar perputhet me hash-in e mesazhit, nenshkrimi eshte valid.

**Tags:** `siguri exam signature`

## Card 044

**Q:** Nese Bob do privatese kur i dergon Alice mesazh, cilin celes perdor?

**A:** Ai enkripton me celesin publik te Alice. Alice e dekripton me celesin e saj privat.

**Tags:** `siguri exam public-key`

## Card 045

**Q:** Ku ruhet PIN-i i smart karteles dhe pse?

**A:** Ne EEPROM ose memorie te brendshme jo-volative te karteles, sepse PIN duhet te ruhet edhe pa energji dhe mund te ndryshohet. Nuk ruhet ne RAM sepse RAM humbet; jo ne ROM sepse ROM eshte fikse; jo ne databaze te jashtme nese qellimi eshte verifikim brenda karteles.

**Tags:** `siguri exam smart-card`

## Card 046

**Q:** Ku ruhet sistemi operativ i smart karteles dhe pse?

**A:** Kryesisht ne ROM, sepse COS duhet te jete i qendrueshem, i mbrojtur dhe i gatshem pas cdo ndezjeje. Pjese te update-ueshme ose aplikacione mund te jene ne EEPROM.

**Tags:** `siguri exam smart-card`

## Card 047

**Q:** Pse smart kartelat konsiderohen pajisje te sigurta?

**A:** Sepse celesat privat mund te gjenerohen dhe ruhen brenda chip-it pa e lene pajisjen; ka PIN/access control; mund te kete crypto coprocessor; bllokohet pas tentimeve te gabuara; dhe eshte me rezistente ndaj kopjimit se nje fajll ne disk.

**Tags:** `siguri exam smart-card`

## Card 048

**Q:** Cka eshte SSL/TLS?

**A:** SSL eshte emri historik; TLS eshte pasardhesi modern. Eshte protokoll qe siguron komunikim mbi rrjet me autentikim, shkembim celesash, enkriptim dhe integritet, p.sh. HTTPS ne browser dhe web server.

**Tags:** `siguri exam ssl`

## Card 049

**Q:** Ku implementohet SSL/TLS dhe cka enkriptohet me te?

**A:** Implementohet mes aplikacionit dhe transportit, p.sh. ne browser/web server per HTTPS. Pas handshake, te dhenat e aplikacionit enkriptohen me celes simetrik session; certifikatat/asimetriku perdoren per autentikim dhe shkembim celesi.

**Tags:** `siguri exam ssl`

## Card 050

**Q:** Cfare shenime permban MRZ ne dokumentet biometrike?

**A:** MRZ zakonisht permban emrin/mbiemrin, numrin e dokumentit, shtetesine, daten e lindjes, gjinine, daten e skadimit dhe check digits. Formatet varen nga dokumenti.

**Tags:** `siguri exam biometric`

## Card 051

**Q:** Pse eshte e rendesishme MRZ tek dokumentet biometrike?

**A:** Sepse lexohet automatikisht nga makinat dhe perdoret per te derivuar celesa te qasjes si BAC. MRZ lidh dokumentin fizik me te dhenat elektronike ne chip.

**Tags:** `siguri exam biometric`

## Card 052

**Q:** Nga cka derivohet BAC key tek dokumentet biometrike?

**A:** BAC key derivohet nga te dhena te MRZ: document number, date of birth dhe date of expiry, zakonisht bashke me check digits. Keto perdoren per te krijuar celesa qe hapin komunikimin me chip-in.

**Tags:** `siguri exam biometric`

## Card 053

**Q:** Cilat jane tri format e XML nenshkrimit digjital?

**A:** Enveloped signature: nenshkrimi eshte brenda dokumentit qe nenshkruhet. Enveloping signature: objekti i nenshkruar eshte brenda elementit Signature. Detached signature: nenshkrimi eshte i ndare nga objekti qe nenshkruhet.

**Tags:** `siguri exam xml`

## Card 054

**Q:** Ne cka bazohet teknologjia Blockchain?

**A:** Blockchain bazohet ne blloqe te lidhura me hash kriptografik. Cdo bllok permban hash-in e bllokut paraprak, prandaj ndryshimi i nje blloku prish zinxhirin. Rrjeti perdor mekanizem konsensusi per te vendosur cila histori eshte valide dhe per ta bere ledger-in praktikisht te pandryshueshem.

**Tags:** `siguri exam blockchain`

## Card 055

**Q:** Zgjidhe lock puzzle: 291 one right/in place; 245 one right/wrong place; 463 two right/wrong place; 578 none; 569 one right/wrong place.

**A:** PIN = 394. 5,7,8 nuk jane ne kod. Nga 569 vetem 9 ose 6 eshte ne kod dhe gabim vendi. Nga 291 del 9 ne poziten 2. Nga 463 dy shifra jane korrekte gabim vendi; del 3 dhe 4. Rendi qe i ploteson te gjitha kushtet eshte 394.

**Tags:** `siguri exam logic`

## Card 056

**Q:** Zgjidhe lock puzzle: 682 one correct/well placed; 614 one correct/wrong place; 206 two correct/wrong place; 738 none; 780 one correct/wrong place.

**A:** PIN = 042. Nga 738 del se 7,3,8 nuk jane ne kod. Nga 780 del se 0 eshte ne kod por jo ne poziten 3. Nga 206 dy jane korrekte por gabim vendi: 0 dhe 2. Nga 682, 2 eshte ne poziten 3. Pastaj 4 ploteson kushtin e 614 gabim vendi.

**Tags:** `siguri exam logic`

## Card 057

**Q:** Cka eshte plaintext?

**A:** Plaintext eshte mesazhi origjinal/i lexueshem para enkriptimit.

**Tags:** `siguri basics`

## Card 058

**Q:** Cka eshte ciphertext?

**A:** Ciphertext eshte mesazhi pas enkriptimit, i cili nuk duhet te kuptohet pa celesin perkates.

**Tags:** `siguri basics`

## Card 059

**Q:** Cka eshte cryptography?

**A:** Kriptografia eshte shkenca/teknika per mbrojtjen e informacionit permes transformimeve matematikore dhe celesave.

**Tags:** `siguri basics`

## Card 060

**Q:** Cka eshte cryptanalysis?

**A:** Kriptoanaliza eshte analiza ose tentimi per ta rikonstruktuar plaintext-in/celesin pa pasur autorizim ose pa celesin e sakte.

**Tags:** `siguri basics`

## Card 061

**Q:** Cka eshte cryptology?

**A:** Kriptologjia eshte termi i perbashket per kriptografine dhe kriptoanalizen.

**Tags:** `siguri basics`

## Card 062

**Q:** Cka thote parimi i Kerckhoff-it?

**A:** Siguria nuk duhet te varet nga fshehtesia e algoritmit, por nga fshehtesia e celesit. Algoritmi mund te jete publik dhe prape sistemi duhet te jete i sigurt.

**Tags:** `siguri basics`

## Card 063

**Q:** Cka eshte substitution cipher?

**A:** Shifer ku simbolet zevendesohen me simbole te tjera sipas nje rregulli/celesi. Caesar dhe Atbash jane shembuj.

**Tags:** `siguri classic`

## Card 064

**Q:** Cka eshte transposition cipher?

**A:** Shifer ku simbolet nuk ndryshohen, por ndryshohet renditja e tyre. Pra permbajtja e shkronjave mbetet, pozicionet perzihen.

**Tags:** `siguri classic`

## Card 065

**Q:** Cka eshte Atbash cipher?

**A:** Atbash e kthen alfabetin mbrapsht: A->Z, B->Y, etj. Matematikisht E(x)=m-1-x dhe D(x)=m-1-x.

**Tags:** `siguri classic`

## Card 066

**Q:** Pse analiza frekuencore funksionon kunder Caesar/Atbash?

**A:** Sepse ato ruajne modelet statistikore te gjuhes. Shkronjat e shpeshta ne plaintext kthehen ne shkronja te tjera por frekuencat mbeten te dallueshme.

**Tags:** `siguri classic`

## Card 067

**Q:** Cka eshte keyspace?

**A:** Keyspace eshte numri i celesave te mundshem. Sa me i vogel keyspace, aq me i lehte brute force.

**Tags:** `siguri basics`

## Card 068

**Q:** Cka eshte brute force attack?

**A:** Sulm ku provohen sistematikisht celesat/password-et e mundshem derisa gjendet i sakti.

**Tags:** `siguri attacks`

## Card 069

**Q:** Cka eshte known-plaintext attack?

**A:** Sulm ku sulmuesi ka disa plaintext dhe ciphertext perkates dhe i perdor per te nxjerre celesin ose informacion tjeter.

**Tags:** `siguri attacks`

## Card 070

**Q:** Cka eshte chosen-plaintext attack?

**A:** Sulm ku sulmuesi mund te zgjedhe plaintext dhe te marre ciphertext perkates, per te mesuar rreth algoritmit/celesit.

**Tags:** `siguri attacks`

## Card 071

**Q:** Cka eshte chosen-ciphertext attack?

**A:** Sulm ku sulmuesi zgjedh ciphertext dhe merr dekriptimin e tij, per te nxjerre informacion sekret.

**Tags:** `siguri attacks`

## Card 072

**Q:** Cka eshte DES?

**A:** DES eshte algoritm simetrik block cipher me bllok 64-bit, celes efektiv 56-bit dhe 16 raunde Feistel.

**Tags:** `siguri des`

## Card 073

**Q:** Pse celesi DES eshte 56-bit edhe pse shenohet 64-bit?

**A:** Sepse cdo bit i 8-te perdoret si parity bit. 64 bit nominale - 8 bit parity = 56 bit efektive.

**Tags:** `siguri des`

## Card 074

**Q:** Cila eshte formula Feistel ne DES?

**A:** Li = Ri-1 dhe Ri = Li-1 XOR f(Ri-1, Ki). Kjo strukture lejon dekriptim me te njejtin algoritm duke perdorur nencelesat ne rend te kundert.

**Tags:** `siguri des`

## Card 075

**Q:** Cilat jane hapat kryesore te DES?

**A:** Initial permutation, ndarje ne L/R 32-bit, 16 raunde Feistel me nencelesa, bashkim i gjysmave dhe final permutation.

**Tags:** `siguri des`

## Card 076

**Q:** Cka ben expansion permutation ne DES?

**A:** Zgjeron gjysmen e djathte nga 32 bit ne 48 bit qe te mund te behet XOR me nencelesin 48-bit.

**Tags:** `siguri des`

## Card 077

**Q:** Pse initial permutation ne DES nuk konsiderohet burim kryesor sigurie?

**A:** Sepse eshte permutacion fiks dhe i njohur. Siguria reale vjen nga celesi, raundet, S-Box-at dhe perzierja jolineare.

**Tags:** `siguri des`

## Card 078

**Q:** Pse DES nuk eshte me i sigurt?

**A:** Celesi efektiv 56-bit eshte shume i vogel per hardware modern dhe mund te thyhet me brute force. Prandaj DES u zevendesua nga 3DES dhe pastaj AES.

**Tags:** `siguri des`

## Card 079

**Q:** Cka jane weak keys ne DES?

**A:** Celesa qe krijojne nencelesa te perseritur ose simetrik, duke bere qe E(K, E(K, M)) = M ne raste te caktuara.

**Tags:** `siguri des`

## Card 080

**Q:** Si funksionon Triple DES EDE?

**A:** Enkriptim: C = E(K3, D(K2, E(K1, P))). Varianti 2-key ka K1=K3; varianti 3-key ka tre celesa te ndryshem.

**Tags:** `siguri des`

## Card 081

**Q:** Cka eshte AES?

**A:** AES eshte standard modern simetrik me bllok 128-bit dhe celesa 128/192/256-bit. Eshte zevendesuesi praktik i DES.

**Tags:** `siguri aes`

## Card 082

**Q:** Cka eshte ECB?

**A:** Electronic Code Book: Ci = E(K, Pi). Blloqet enkriptohen pavaresisht, prandaj blloqet e njejta plaintext japin ciphertext te njejte.

**Tags:** `siguri modes`

## Card 083

**Q:** Cka eshte IV?

**A:** Initialization Vector eshte vlere fillestare per mode si CBC. Nuk duhet te jete sekret, por duhet te jete unik/paparashikueshem per te shmangur ciphertext te perseritur.

**Tags:** `siguri modes`

## Card 084

**Q:** Cka eshte stream cipher?

**A:** Algoritm qe gjeneron keystream dhe e kombinon me plaintext zakonisht me XOR: ci = pi XOR ki.

**Tags:** `siguri stream`

## Card 085

**Q:** Cka eshte One Time Pad?

**A:** Shifer ku celesi eshte vertet random, gjatesi sa mesazhi, sekret dhe perdoret vetem nje here. Me keto kushte eshte teorikisht i sigurt.

**Tags:** `siguri stream`

## Card 086

**Q:** Pse nuk duhet riperdorur celesi i One Time Pad?

**A:** Sepse XOR i dy ciphertext-eve me te njejtin key jep XOR te dy plaintext-eve, duke zbuluar modele dhe duke e bere sulmin praktik.

**Tags:** `siguri stream`

## Card 087

**Q:** Cka eshte A5/1?

**A:** Stream cipher historik i GSM qe perdor tre shift registers dhe majority clocking per te gjeneruar keystream.

**Tags:** `siguri stream`

## Card 088

**Q:** Cka eshte KDC?

**A:** Key Distribution Center eshte pale e besuar qe gjeneron/shperndan session keys per perdoruesit qe kane celesa afatgjate me KDC-ne.

**Tags:** `siguri key-management`

## Card 089

**Q:** Si punon shkembimi i session key me KDC?

**A:** Alice kerkon celes per Bob. KDC krijon Ktemp dhe dergon E(KA,Ktemp) per Alice dhe E(KB,Ktemp) per Bob. Pastaj Alice dhe Bob perdorin Ktemp.

**Tags:** `siguri key-management`

## Card 090

**Q:** Pse enkriptimi hibrid perdoret ne praktike?

**A:** Sepse asimetriku eshte i ngadalte per te dhena te medha, por i mire per shkembim celesi; simetriku eshte i shpejte per mesazhe. Prandaj perdoren bashke.

**Tags:** `siguri public-key`

## Card 091

**Q:** Cka eshte Euler phi function?

**A:** phi(n) tregon sa numra nga 1 deri ne n jane relativisht te thjeshte me n. Nese n=p*q me p,q prime, phi(n)=(p-1)(q-1).

**Tags:** `siguri rsa`

## Card 092

**Q:** Cka do te thote dy numra jane coprime?

**A:** Dy numra jane coprime nese nuk kane faktor te perbashket pervec 1, pra gcd(a,b)=1.

**Tags:** `siguri rsa`

## Card 093

**Q:** Cka eshte modulo?

**A:** Modulo jep mbetjen pas pjesetimit. P.sh. 78 mod 11 = 1, sepse 77 pjesetohet me 11 dhe mbetet 1. Ne pergjithesi a mod n eshte mbetja ne intervalin 0..n-1.

**Tags:** `siguri math`

## Card 094

**Q:** Cilat jane hapat e gjenerimit te RSA?

**A:** Zgjidh p,q prime; llogarit n=p*q; llogarit phi=(p-1)(q-1); zgjedh e coprime me phi; gjej d ku e*d mod phi=1; publik=(e,n), privat=d.

**Tags:** `siguri rsa`

## Card 095

**Q:** Pse RSA bazohet ne faktorizimin e numrave te medhenj?

**A:** Sepse n=p*q eshte publik, por per te gjetur d duhet phi(n), dhe per phi(n) duhen p dhe q. Faktorizimi i n te madh eshte shume i veshtire.

**Tags:** `siguri rsa`

## Card 096

**Q:** Pse RSA me p dhe q te vegjel eshte vetem demonstrim?

**A:** Sepse p dhe q te vegjel faktorizohen menjehere. Ne praktike perdoren prime shume te medhenj dhe padding i sigurt.

**Tags:** `siguri rsa`

## Card 097

**Q:** Cka jane PKCS standardet?

**A:** Public-Key Cryptography Standards: standarde per RSA, DH, password-based cryptography, certifikata, private keys, token interfaces dhe ruajtje/transport te celesave.

**Tags:** `siguri pkcs`

## Card 098

**Q:** Cka eshte PKCS #1?

**A:** Standardi per RSA cryptography: formatet dhe skemat per enkriptim/nenshkrim me RSA.

**Tags:** `siguri pkcs`

## Card 099

**Q:** Cka eshte PKCS #5?

**A:** Password-Based Cryptography Standard; lidhet me PBKDF2 dhe derivimin e celesave nga password + salt + iterations.

**Tags:** `siguri pkcs`

## Card 100

**Q:** Cka eshte PKCS #11?

**A:** Cryptographic Token Interface Standard. Definon API per tokena/smart cards/HSM qe ruajne celesa dhe kryejne operacione kriptografike.

**Tags:** `siguri pkcs`

## Card 101

**Q:** Cka eshte hash function?

**A:** Funksion qe merr hyrje me gjatesi arbitrare dhe jep dalje fikse h=H(M). Duhet te jete efikas, njekahesh dhe rezistent ndaj collision.

**Tags:** `siguri hash`

## Card 102

**Q:** Cka eshte preimage resistance?

**A:** Duke pasur hash-in h, te jete praktikisht e pamundur te gjendet M i tille qe H(M)=h.

**Tags:** `siguri hash`

## Card 103

**Q:** Cka eshte second preimage resistance?

**A:** Per nje mesazh M te dhene, te jete praktikisht e pamundur te gjendet M' tjeter me H(M')=H(M).

**Tags:** `siguri hash`

## Card 104

**Q:** Cka eshte collision resistance?

**A:** Te jete praktikisht e pamundur te gjenden dy mesazhe te ndryshme M1 dhe M2 me te njejtin hash.

**Tags:** `siguri hash`

## Card 105

**Q:** Pse MD5 nuk perdoret me per siguri?

**A:** Sepse ka collision attacks praktike. Mund te perdoret vetem per checksum jo-sigurie, jo per certifikata, nenshkrime apo integritet kritik.

**Tags:** `siguri hash`

## Card 106

**Q:** Pse SHA-1 nuk rekomandohet me?

**A:** Sepse edhe SHA-1 ka collision attacks dhe nuk konsiderohet i sigurt per perdorime te reja. Preferohen SHA-256/SHA-3.

**Tags:** `siguri hash`

## Card 107

**Q:** Cka eshte birthday paradox ne hash?

**A:** Per hash n-bit, collision pritet me rreth 2^(n/2) prova, jo 2^n. Prandaj gjatesia e hash-it duhet te jete mjaft e madhe.

**Tags:** `siguri hash`

## Card 108

**Q:** Cka eshte salt?

**A:** Salt eshte vlere random unike qe kombinohet me password para hash-it. Ajo ruhet publikisht bashke me hash-in dhe nuk ka nevoje te jete sekrete.

**Tags:** `siguri passwords`

## Card 109

**Q:** Cka eshte dictionary attack?

**A:** Sulm ku provohen fjale/password-e te zakonshem nga lista. Salt dhe PBKDF2 e veshtiresojne, por password-et e dobeta mbeten problem.

**Tags:** `siguri passwords`

## Card 110

**Q:** Cka eshte MAC?

**A:** Message Authentication Code eshte vlere autentikuese e llogaritur me celes sekret per te verifikuar integritetin dhe autenticitetin e mesazhit.

**Tags:** `siguri mac`

## Card 111

**Q:** Cka eshte dallimi mes hash dhe MAC?

**A:** Hash nuk ka celes dhe kushdo mund ta llogarise. MAC perdor celes sekret, prandaj vetem palet qe e dine celesin mund te krijojne vleren valide.

**Tags:** `siguri mac`

## Card 112

**Q:** Cka eshte timestamp ne nenshkrim dhe pse duhet?

**A:** Timestamp lidh nenshkrimin me nje kohe te caktuar dhe ndihmon kunder replay attack, sidomos ne transaksione/pagesa elektronike.

**Tags:** `siguri signature`

## Card 113

**Q:** Pse ne praktike nenshkruhet hash-i dhe jo i gjithe dokumenti?

**A:** Sepse hash-i ka gjatesi fikse dhe eshte shume me efikas per t'u nenshkruar. Nese dokumenti ndryshon, hash-i ndryshon dhe verifikimi deshton.

**Tags:** `siguri signature`

## Card 114

**Q:** Cka eshte certifikata digjitale?

**A:** Dokument digjital qe lidh nje identitet me nje celes publik dhe nenshkruhet nga nje CA ose nga nje pale e besuar.

**Tags:** `siguri certificates`

## Card 115

**Q:** Cka permban nje certifikate X.509 v3?

**A:** Version, serial number, signature algorithm, issuer, validity period, subject, subject public key, extensions dhe signature te CA-se.

**Tags:** `siguri certificates`

## Card 116

**Q:** Cka eshte CA?

**A:** Certification Authority eshte pale e besuar qe verifikon identitetin dhe nenshkruan certifikata digjitale.

**Tags:** `siguri certificates`

## Card 117

**Q:** Cka eshte CRL?

**A:** Certificate Revocation List eshte liste certifikatash te revokuara para skadimit, p.sh. kur komprometohet celesi privat.

**Tags:** `siguri certificates`

## Card 118

**Q:** Cka eshte PKI?

**A:** Public Key Infrastructure eshte infrastruktura e CA, RA, certifikatave, CRL-ve, rregullave dhe proceseve per menaxhim te celesave publik.

**Tags:** `siguri certificates`

## Card 119

**Q:** Cka eshte Web of Trust ne PGP?

**A:** Model ku perdoruesit nenshkruajne celesat e njeri-tjetrit dhe besimi ndertohet nga rrjeti i nenshkrimeve, jo domosdoshmerisht nga nje CA hierarkike.

**Tags:** `siguri pgp`

## Card 120

**Q:** Cka eshte thumbprint/fingerprint i certifikates?

**A:** Hash i certifikates ose celesit publik qe mund te krahasohet out-of-band per te verifikuar se celesi eshte i sakti.

**Tags:** `siguri certificates`

## Card 121

**Q:** Pse ruajtja e celesit privat ne smart card eshte me e mire se ne fajll?

**A:** Sepse celesi privat nuk duhet te dale nga karta; operacionet kriptografike kryhen brenda pajisjes dhe qasja kontrollohet me PIN.

**Tags:** `siguri smart-card`

## Card 122

**Q:** Cka eshte Base64?

**A:** Kodim tekstual per te paraqitur te dhena binare me 64 simbole: A-Z, a-z, 0-9, + dhe /. Perdoret per certifikata, celesa dhe XML/JSON.

**Tags:** `siguri encoding`

## Card 123

**Q:** Cka eshte XML?

**A:** eXtensible Markup Language: gjuhe per pershkrim dhe bartje te te dhenave, jo per pamje si HTML.

**Tags:** `siguri xml`

## Card 124

**Q:** Cka do te thote XML well-formed?

**A:** Dokumenti ka sintakse valide: tag-et hapen/mbyllen mire, struktura eshte e sakte, atributet jane te shkruara drejt.

**Tags:** `siguri xml`

## Card 125

**Q:** Cka eshte XML Schema/XSD?

**A:** Skeme qe definon elementet, atributet, tipet, renditjen dhe kufizimet qe lejohen ne nje XML dokument.

**Tags:** `siguri xml`

## Card 126

**Q:** Pse XML signature ka nevoje per canonicalization?

**A:** Sepse XML mund te kete forma tekstuale te ndryshme me kuptim te njejte. Canonicalization e kthen ne forme standarde para hash-it, qe verifikimi te mos deshtoje nga whitespace/rend atributesh.

**Tags:** `siguri xml`

## Card 127

**Q:** Cka eshte SignedInfo ne XML Signature?

**A:** Pjesa qe tregon cka eshte nenshkruar dhe me cfare metodash: canonicalization, signature method, reference, transforms dhe digest.

**Tags:** `siguri xml`

## Card 128

**Q:** Cka eshte DigestValue ne XML Signature?

**A:** Hash-i i te dhenave te referuara pas transformimeve te caktuara.

**Tags:** `siguri xml`

## Card 129

**Q:** Cka eshte KeyInfo ne XML Signature?

**A:** Element opsional qe mund te mbaje celes publik ose certifikate per verifikimin e nenshkrimit.

**Tags:** `siguri xml`

## Card 130

**Q:** Cilat jane llojet kryesore te smart kartelave?

**A:** Memory cards, microprocessor cards, contact cards, contactless cards dhe dual-interface cards.

**Tags:** `siguri smart-card`

## Card 131

**Q:** Cka eshte memory card krahasuar me microprocessor card?

**A:** Memory card kryesisht ruan te dhena dhe ka logjike te kufizuar. Microprocessor card ka CPU/COS dhe mund te kryeje operacione, perfshire kriptografi.

**Tags:** `siguri smart-card`

## Card 132

**Q:** Cka eshte COS ne smart kartela?

**A:** Card Operating System: sistem operativ i vogel ne kartele qe menaxhon file system, PIN, komanda APDU, access control dhe funksione kriptografike.

**Tags:** `siguri smart-card`

## Card 133

**Q:** Si organizohet memoria/fajllat ne smart kartele?

**A:** Si peme: MF (Master File) si rrenje, DF (Dedicated File) si direktorium, EF (Elementary File) si fajll me te dhena.

**Tags:** `siguri smart-card`

## Card 134

**Q:** Cka eshte APDU?

**A:** Application Protocol Data Unit: formati i komandave dhe pergjigjeve mes aplikacionit/lexuesit dhe smart karteles.

**Tags:** `siguri smart-card`

## Card 135

**Q:** Cilat fusha ka Command APDU?

**A:** CLA, INS, P1, P2, Lc, Data, Le. Header eshte CLA INS P1 P2; body mund te kete Lc/Data/Le.

**Tags:** `siguri smart-card`

## Card 136

**Q:** Cilat fusha ka Response APDU?

**A:** Data dhe status words SW1 SW2. SW1/SW2 tregojne suksesin ose gabimin, p.sh. 90 00 do te thote sukses.

**Tags:** `siguri smart-card`

## Card 137

**Q:** Cka eshte ATR?

**A:** Answer To Reset: pergjigjja fillestare e karteles pas reset, qe tregon parametra dhe protokoll komunikimi.

**Tags:** `siguri smart-card`

## Card 138

**Q:** Cka jane protokollet T=0 dhe T=1?

**A:** T=0 eshte asinkron, half-duplex, byte-oriented. T=1 eshte asinkron, half-duplex, block-oriented.

**Tags:** `siguri smart-card`

## Card 139

**Q:** Cka eshte PC/SC?

**A:** Arkitekture/API qe e ben aplikacionin te pavarur nga lexuesi dhe smart kartela konkrete. Perfshin Resource Manager, reader drivers dhe SCard* funksione.

**Tags:** `siguri smart-card`

## Card 140

**Q:** Cilat jane hapat tipike PC/SC?

**A:** SCardEstablishContext, SCardListReaders, SCardGetStatusChange, SCardConnect, SCardTransmit, SCardDisconnect, SCardReleaseContext.

**Tags:** `siguri smart-card`

## Card 141

**Q:** Cka eshte Secure Messaging ne smart kartela?

**A:** Mbrojtje e APDU-ve me kriptografi per konfidencialitet/integritet/autentikim mes terminalit dhe karteles.

**Tags:** `siguri smart-card`

## Card 142

**Q:** Cka eshte Master Key ne menaxhimin e celesave te karteles?

**A:** Celes kryesor nga i cili mund te derivohen celesa te tjere; zakonisht nuk ruhet direkt ne kartele per te kufizuar demin e komprometimit.

**Tags:** `siguri smart-card`

## Card 143

**Q:** Cka eshte Session Key ne smart cards?

**A:** Celes i perkohshem per nje sesion, shpesh i derivuar nga nje derived/diversified key dhe nje vlere random.

**Tags:** `siguri smart-card`

## Card 144

**Q:** Cilat jane llojet e contactless smart cards sipas distances?

**A:** Close coupling: 0-1 cm. Proximity: 0-10 cm, ISO 14443. Vicinity: deri rreth 1 m, ISO 15693.

**Tags:** `siguri smart-card`

## Card 145

**Q:** Cka eshte RFID ne pasaporta biometrike?

**A:** Teknologji pa kontakt qe lejon lexuesin te komunikoje me chip-in e pasaportes permes fushes radio, zakonisht me mekanizma sigurie si BAC/PACE.

**Tags:** `siguri biometric`

## Card 146

**Q:** Cka eshte BAC ne pasaporta biometrike?

**A:** Basic Access Control: mekanizem qe derivon celesa nga MRZ per te hapur kanal te sigurt me chip-in dhe per te penguar leximin pa qasje fizike te dokumentit.

**Tags:** `siguri biometric`

## Card 147

**Q:** Cka eshte steganografia?

**A:** Fshehja e ekzistences se mesazhit brenda nje mediumi tjeter, p.sh. imazh, audio, video ose tekst.

**Tags:** `siguri steganografi`

## Card 148

**Q:** Cili eshte dallimi mes kriptografise dhe steganografise?

**A:** Kriptografia e ben mesazhin te palexueshem; steganografia e fsheh faktin qe mesazhi ekziston. Mund te perdoren bashke.

**Tags:** `siguri steganografi`

## Card 149

**Q:** Sa tekst fsheh nje imazh Full HD me 1 bit per pixel?

**A:** 1920*1080 = 2,073,600 bits = 259,200 bytes, rreth 253 kB ose afersisht 260 kB ne llogaritje te rrumbullakesuar.

**Tags:** `siguri steganografi calculation`

## Card 150

**Q:** Cka ben steghide?

**A:** Mjet per te fshehur dhe nxjerre te dhena nga media si imazhe/audio, p.sh. steghide embed dhe steghide extract.

**Tags:** `siguri steganografi`

## Card 151

**Q:** Cka ben stegcracker/stegcrack?

**A:** Mjet per brute force te fjalekalimit te nje mesazhi steganografik, duke provuar wordlist.

**Tags:** `siguri steganografi`

## Card 152

**Q:** Cka eshte secret sharing me XOR per dy persona?

**A:** Gjenero R random sa M, llogarit S = M XOR R. Njerit i jep R, tjetrit S. Vetem bashke rikonstruktojne M = R XOR S.

**Tags:** `siguri secret-sharing`

## Card 153

**Q:** Pse secret sharing me XOR eshte i sigurt nese R eshte random?

**A:** Sepse secila pjese e vetme duket random dhe nuk jep informacion per M. Duhet te kombinohen te gjitha pjeset.

**Tags:** `siguri secret-sharing`

## Card 154

**Q:** Cka ndodh nese humbet nje pjese ne secret sharing me XOR?

**A:** Mesazhi nuk rikonstruktohet dot, sepse cdo pjese eshte e nevojshme ne skemen e thjeshte XOR.

**Tags:** `siguri secret-sharing`

## Card 155

**Q:** Cka eshte non-repudiation?

**A:** Jo-mohueshmeria: nje pale nuk mund ta mohoje lehte nje veprim/nenshkrim qe eshte lidhur kriptografikisht me celesin e saj privat.

**Tags:** `siguri core`

## Card 156

**Q:** Cka eshte authentication?

**A:** Verifikimi i identitetit te nje pale ose burimit te nje mesazhi para ose gjate komunikimit.

**Tags:** `siguri core`

## Card 157

**Q:** Cka eshte integrity?

**A:** Garancia qe te dhenat nuk jane ndryshuar pa u zbuluar. Hash, MAC dhe digital signatures ndihmojne per integritet.

**Tags:** `siguri core`

## Card 158

**Q:** Cka eshte confidentiality?

**A:** Garancia qe vetem palet e autorizuara mund te lexojne permbajtjen. Arrihet me enkriptim.

**Tags:** `siguri core`

## Card 159

**Q:** Cka duhet te pergjigjesh kur pyetja kerkon "skicen" e digital signature?

**A:** Vizato dy ane: Sender llogarit hash te plaintext, e nenshkruan hash-in me private key dhe dergon M+S. Receiver llogarit hash te M, verifikon S me public key, krahason digest-et.

**Tags:** `siguri exam-technique`

## Card 160

**Q:** Si ta dallosh ne provim kur duhet celes publik e kur privat?

**A:** Per fshehtesi drejt Bob-it perdor celesin publik te Bob-it. Per nenshkrim te Alice perdor celesin privat te Alice. Per verifikim te Alice perdor celesin publik te Alice. Per dekriptim Bob perdor privat te Bob-it.

**Tags:** `siguri exam-technique`

## Card 161

**Q:** Cili eshte gabimi klasik ne pyetjet me RSA/DHM?

**A:** Te harrohet mod ne cdo hap. Fuqite llogariten gjithmone modulo p ose n; mos e le numrin te rritet pa fund.

**Tags:** `siguri exam-technique`

## Card 162

**Q:** Cili eshte gabimi klasik ne pyetjet me hash?

**A:** Te mendosh se hash-i ka gjatesi sa fajlli. Hash-i ka dalje fikse: MD5 128 bit, SHA-1 160 bit, SHA-256 256 bit, pavaresisht madhesise se fajllit.

**Tags:** `siguri exam-technique`

## Card 163

**Q:** Cili eshte gabimi klasik ne pyetjet me smart card storage?

**A:** Te zgjedhesh RAM per te dhena qe duhet te mbeten pas fikjes. PIN dhe te dhena te ndryshueshme ruhen ne EEPROM; OS kryesisht ne ROM.

**Tags:** `siguri exam-technique`

## Card 164

**Q:** Cili eshte gabimi klasik ne pyetjet me eIDAS?

**A:** Te perzihen nenshkrimi elektronik dhe nenshkrimi digjital. eIDAS jep kategori juridike; digital signature eshte mekanizem kriptografik konkret.

**Tags:** `siguri exam-technique`

