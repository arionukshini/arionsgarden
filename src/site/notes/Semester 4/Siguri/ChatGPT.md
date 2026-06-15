---
{"dg-publish":true,"permalink":"/semester-4/siguri/chat-gpt/"}
---

# Siguria e te dhenave - permbledhje per provim

## Qellimi i lendes

Lenda merret me mbrojtjen e te dhenave permes kriptografise, menaxhimit te celesave, certifikatave digjitale, nenshkrimeve digjitale, smart kartelave dhe aplikimeve praktike. Ne provim zakonisht duhet me dit:

- konceptet baze te kriptografise dhe kriptoanalizes
- dallimin mes enkriptimit simetrik dhe asimetrik
- si punojne DES, 3DES, RSA, DHM, hash funksionet dhe nenshkrimet digjitale
- pse duhen certifikatat, PKI dhe menaxhimi i celesave
- cka jane XML signatures dhe pse XML canonicalization eshte e rendesishme
- si punojne smart kartelat ne nivel fizik, logjik dhe aplikativ
- detyrat praktike: Caesar, Atbash, transpozicion, OTP, DES/3DES, RSA, DHM, hash, salted hash, digital signature, steganografi

Testi ka rreth 17-20 pyetje. Pergjigja e sakte jep rreth 3 pike, pergjigja e pjesshme 1 ose 2 pike, ndersa pa pergjigje ose gabim jep 0 pike.

# Hyrje ne sigurine e te dhenave

## Kriptografia, kriptoanaliza dhe kriptologjia

Kriptografia eshte shkenca dhe teknika qe merret me fshehjen dhe mbrojtjen e informacionit. Mesazhi fillestar quhet `plaintext`, ndersa mesazhi i transformuar quhet `ciphertext`.

Enkriptimi eshte procesi:

```text
E(M, K) = C
```

ku `M` eshte mesazhi, `K` eshte celesi dhe `C` eshte ciphertext. Dekriptimi eshte procesi i kundert:

```text
D(C, K) = M
```

Kriptoanaliza merret me thyerjen ose analizimin e informacionit te enkriptuar pa e pasur celesin. Kriptologjia eshte termi i perbashket per kriptografine dhe kriptoanalizen.

## Objektivat kryesore te sigurise

Kriptografia nuk perdoret vetem per fshehje. Ajo synon disa veti:

- Confidentiality / fshehtesia: vetem palet e autorizuara mund ta lexojne mesazhin.
- Integrity / integriteti: ndryshimi i te dhenave duhet te detektohet.
- Authentication / autentikimi: palet duhet te verifikojne identitetin e njera-tjetres.
- Non-repudiation / mos-mohimi: nje pale nuk mund ta mohoje me vone nje veprim, p.sh. nenshkrimin e nje dokumenti.

Ne provim eshte me rendesi me dallu keto. Enkriptimi kryesisht jep fshehtesi. Hash funksioni jep integritet. Nenshkrimi digjital jep autenticitet, integritet dhe mos-mohim. Certifikatat lidhin celesin publik me identitetin real.

## Kerckhoff dhe Shannon

Parimi i Kerckhoff-it thote se siguria e nje sistemi nuk duhet te varet nga fshehtesia e algoritmit, por nga fshehtesia e celesit. Pra algoritmi mund te jete publik, i analizuar dhe i standardizuar; nese celesi ruhet, sistemi duhet te mbetet i sigurt.

Claude Shannon i dha dy ide themelore per dizajnin e shifrave moderne:

- Confusion: ta beje lidhjen mes plaintext, ciphertext dhe celesit sa me te paqarte.
- Diffusion: statistikat e plaintext-it te shperndahen neper ciphertext, qe nje ndryshim i vogel ne hyrje te ndikoje ne shume pjese te daljes.

DES, AES dhe shifrat moderne i perdorin keto ide me zevendesime, permutacione, raunde dhe feedback.

## Kodi i Cezarit

Kodi i Cezarit eshte shembull klasik i substitution cipher. Cdo shkronje zevendesohet me nje shkronje tjeter duke u zhvendosur me `k` pozita ne alfabet.

Nese shkronjat i shenojme si numra:

```text
A = 0, B = 1, ..., Z = 25
```

atehere:

```text
Enkriptimi:  E_k(x) = (x + k) mod 26
Dekriptimi:  D_k(x) = (x - k) mod 26
```

Kodi i Cezarit eshte i dobet sepse keyspace eshte shume i vogel. Per alfabetin latin ka vetem 26 zhvendosje te mundshme, prandaj brute force eshte i lehte. Mund te thyhet edhe me analize frekuencore, sepse shkronjat me te shpeshta ne gjuhe vazhdojne te shfaqin modele edhe pas zhvendosjes.

## Rot13

Rot13 eshte rast special i Caesar cipher me zhvendosje 13. Pasi alfabeti ka 26 shkronja:

```text
Rot13(Rot13(x)) = x
```

Kjo do te thote se i njejti transformim perdoret edhe per enkriptim edhe per dekriptim. Nuk eshte metode sigurie reale, por shembull i mire per te kuptuar substitution.

## Atbash cipher

Atbash eshte tjeter substitution cipher klasik. Nuk perdor zhvendosje, por e kthen alfabetin mbrapsht:

```text
A -> Z
B -> Y
C -> X
...
```

Matematikisht, per alfabet me madhesi 26:

```text
E(x) = 25 - x
D(x) = 25 - x
```

Edhe Atbash thyhet lehte sepse ruan frekuencat dhe modelet e gjuhes.

## Transpozicioni

Te transpozicioni, shkronjat nuk zevendesohen me shkronja te tjera. Teksti mbetet me te njejtat simbole, por ndryshohet renditja e tyre.

Shembull nga ligjerata:

```text
Plaintext:  PRISHTINA ESHTE QYTET I BUKUR
```

Teksti mund te vendoset ne tabele dhe pastaj te lexohet ne rend tjeter. Kjo prodhon ciphertext ku shkronjat jane te njejta, por pozicionet jane te perziera. Transpozicioni i vetem nuk e fsheh mire frekuencen e shkronjave, por i fsheh pozicionet dhe strukturat lokale.

## Kodimi, shifrimi dhe enkriptimi

Ne ligjerata ndahet komunikimi i fshehte ne steganografi dhe kriptografi. Brenda kriptografise permenden:

- substitution: zevendesim i simboleve
- transposition: ndryshim i renditjes se simboleve
- coding: ndarje e informacionit ne blloqe me gjatesi te caktuar
- ciphering: shnderrim i simboleve sipas nje rregulli dhe celesi

Per provim, mos i perziej: steganografia e fsheh ekzistencen e mesazhit, kriptografia e ben permbajtjen te palexueshme.

# Steganografia

## Ideja

Steganografia eshte fshehja e informacionit brenda nje informacioni tjeter. Qellimi nuk eshte domosdoshmerisht ta beje mesazhin te pakuptueshem, por ta beje te padukshem qe mesazhi ekziston.

Shembuj:

- tekst i bardhe ne flete te bardhe
- mesazh i fshehur ne shkronjat e para te fjalive
- mesazh ne audio, video ose fotografi
- ndryshim i biteve me peshe me te vogel ne nje imazh

## Steganografia ne imazhe

Imazhet 24-bit zakonisht kane 8 bit per red, 8 bit per green dhe 8 bit per blue. Nese ndryshojme vetem bitin me peshe me te vogel (`least significant bit`), ndryshimi nuk verehet lehte nga syri i njeriut.

Shembull:

```text
0xAB 0x33 0xF0
0xAB 0x33 0xF1
```

Ngjyra ndryshon shume pak, por ne bitin e fundit mund te ruhet informacion.

## Kapaciteti i fshehjes

Formula e pergjithshme:

```text
Total pixels = width * height
Total bits   = total pixels * bits_per_pixel_used
Total bytes  = total bits / 8
```

Shembuj nga ligjeratat:

- Full HD: `1920 * 1080 = 2,073,600` pixel.
- Nese perdoret 1 bit per pixel: `2,073,600 / 8 = 259,200` byte, afersisht 253-260 kB tekst.
- Nese perdoren 3 bit per pixel: rreth 777,600 byte, pra rreth 760 kB.
- Foto `1024 * 768 = 786,432` pixel. Me 1 bit per pixel: `786,432 / 8 = 98,304` byte, afersisht 96-98 kB.

## Shembulli me tekst te fshehur

Teksti mund te kthehet ne hex dhe binar. P.sh. mesazhi:

```text
Shihemi ne Route...
```

fillon me hex:

```text
53 68 69 68 65 6D 69 ...
```

Pastaj bitet e mesazhit vendosen ne LSB te piksellave. Per te rikthyer mesazhin, lexohen LSB-te ne te njejtin rend.

## Steghide dhe Stegcracker

Ne ushtrime perdoret `steghide` per fshehje dhe nxjerrje te te dhenave:

```bash
steghide embed -ef info.txt -cf img.jpg -sf img1.jpg
steghide extract -sf img1.jpg -xf secret.txt --verbose
```

`stegcracker` perdoret per brute force te fjalekalimeve te steganografise:

```bash
stegcrack info.jpg wordlist -o hidden_info
stegcrack info.jpg wordlist -o hidden_info -t 4
```

Pyetje tipike: llogarit kapacitetin e fshehjes per nje rezolucion, ose gjej sa pixel duhen per nje tekst te caktuar.

# Enkriptimi klasik dhe DES

## Llojet e celesave

Ne ligjerata permenden disa lloje celesash:

- Secret key (`Ks`): celes sekret i ndare mes paleve, perdoret ne enkriptim simetrik.
- Session key (`Kt`): celes i perkohshem per nje sesion komunikimi.
- Derived key (`Kd`): celes i derivuar nga nje celes tjeter ose nga nje master key.
- Private key (`Kpr`): celes privat ne kriptografi asimetrike.
- Public key (`Kpb`): celes publik ne kriptografi asimetrike.

Celesat session jane te rendesishem sepse edhe nese komprometohet nje sesion, nuk komprometohen domosdoshmerisht te gjitha komunikimet e tjera.

## Enkriptimi simetrik

Ne enkriptim simetrik i njejti celes perdoret per enkriptim dhe dekriptim:

```text
C = E(K, M)
M = D(K, C)
```

Avantazhi eshte shpejtesia. Problemi kryesor eshte shperndarja e celesave. Nese kemi `n` persona dhe secili cift ka celes te vecante, duhen:

```text
n * (n - 1) / 2
```

celesa.

## DES - historiku

DES u zhvillua ne SHBA ne vitet 1970. NBS, sot NIST, kerkoi nje algoritm per mbrojtje te te dhenave. IBM propozoi algoritmin Lucifer, i cili u standardizua si DES ne vitin 1976 dhe u adoptua nga ANSI ne vitin 1981.

Kerkesat kryesore ishin:

- siguri e larte
- pershkrim publik dhe i verifikueshem
- siguria te jete ne celes, jo ne fshehtesine e algoritmit
- implementim efikas, sidomos ne hardware
- mundesi certifikimi dhe eksportimi

## Parametrat e DES

DES eshte:

- block cipher
- algoritm simetrik
- blloku hyrjes: 64 bit
- celesi nominal: 64 bit
- celesi efektiv: 56 bit, sepse cdo bit i 8-te perdoret per parity
- 16 raunde Feistel

DES perdor dy parimet e Shannon-it:

- konfuzioni, sidomos permes S-Box-ave
- difuzioni, permes permutacioneve dhe perzierjes se biteve ne raunde

## Struktura Feistel

Pas permutacionit fillestar, blloku 64-bit ndahet ne dy gjysma 32-bit:

```text
L0, R0
```

Per cdo raund:

```text
Li = Ri-1
Ri = Li-1 XOR f(Ri-1, Ki)
```

Kjo strukture eshte e rendesishme sepse i njejti algoritm mund te perdoret edhe per dekriptim; ndryshon vetem renditja e nencelesave.

## Funksioni f ne DES

Funksioni `f` ka kater hapa kryesore:

1. Expansion permutation: zgjeron `Ri` nga 32 bit ne 48 bit.
2. XOR me nencelesin `Ki` 48-bit.
3. S-Box substitution: 8 S-Box-a marrin nga 6 bit dhe japin nga 4 bit, pra 48 bit kthehen ne 32 bit.
4. P-Box permutation: permuton daljen 32-bit per difuzion.

S-Box-at jane pjesa me kritike e sigurise se DES. Ato jane jolineare dhe prishin lidhjen lineare mes hyrjes dhe daljes.

## S-Box

Nje S-Box ne DES eshte matrice `4 x 16`. Hyrja eshte 6 bit:

```text
b1 b2 b3 b4 b5 b6
```

Rreshti merret nga `b1b6`, ndersa kolona nga `b2b3b4b5`. Dalja eshte numer 4-bit.

Shembull:

```text
hyrja 011011
rreshti = 01
kolona  = 1101
```

Pra merret elementi ne rreshtin 1 dhe kolonen 13.

## Celesat e DES

Celesi 64-bit reduktohet ne 56 bit duke hequr cdo bit te 8-te te paritetit. Pastaj ndahet ne dy gjysma 28-bit. Ne secilin raund gjysmat zhvendosen majtas 1 ose 2 bit, pastaj zgjidhen 48 bit per nencelesin.

Per enkriptim perdoret rendi:

```text
K1, K2, ..., K16
```

Per dekriptim perdoret rendi i kundert:

```text
K16, K15, ..., K1
```

## Celesat e dobet

DES ka celesa te dobet ku:

```text
E(K, E(K, M)) = M
```

Kjo ndodh kur nencelesat perseriten ne menyre te vecante, p.sh. kur gjysmat e celesit kane vetem 0 ose vetem 1 pas zhvendosjeve.

Ka edhe semi-weak keys: cifte celesash `K1` dhe `K2` ku enkriptimi me njerin dhe pastaj me tjetrin e kthen mesazhin ne gjendjen fillestare.

## Siguria e DES

Problemi kryesor i DES nuk eshte struktura, por gjatesia e celesit: 56 bit. Sot kjo eshte shume e vogel per brute force. Ligjeratat permendin makinat per thyerje:

- EFF DES cracker me kosto rreth 250,000 USD
- COPACOBANA me FPGA me kosto shume me te ulet

Kjo tregon se rritja e fuqise kompjuterike e ben te pasigurte nje keyspace qe dikur ishte i mjaftueshem.

## Modelet e sulmeve

Tre modele qe permenden:

- Known-plaintext attack (KPA): sulmuesi ka plaintext dhe ciphertext perkates.
- Chosen-plaintext attack (CPA): sulmuesi mund te zgjedhe plaintext dhe te marre ciphertext.
- Chosen-ciphertext attack (CCA): sulmuesi zgjedh ciphertext dhe merr dekriptimin.

Sa me shume kontroll ka sulmuesi mbi hyrjet dhe daljet, aq me i fuqishem eshte modeli i sulmit.

## Triple DES

Triple DES e aplikon DES disa here. Forma tipike eshte EDE:

```text
C = E(K3, D(K2, E(K1, P)))
```

Per dekriptim behet ne rend te kundert:

```text
P = D(K1, E(K2, D(K3, C)))
```

Raste:

- 3DES: `K1 != K2 != K3`
- 2DES-EDE: `K1 = K3`, `K1 != K2`

3DES rrit sigurine krahasuar me DES, por eshte me i ngadalte. Sot standardi modern eshte AES.

# Modet e algoritmeve kriptografike

## Block cipher dhe stream cipher

Algoritmet simetrike ndahen ne:

- Block ciphers: perpunojne blloqe me gjatesi fikse, p.sh. DES me 64 bit, AES me 128 bit.
- Stream ciphers: perpunojne bit pas biti ose bajt pas bajti.

Block cipher ka nevoje per mode te operimit kur mesazhi eshte me i gjate se nje bllok.

## Electronic Code Book - ECB

ECB eshte modi me i thjeshte:

```text
Ci = E(K, Pi)
```

Problemi: i njejti bllok plaintext jep gjithmone te njejtin bllok ciphertext me te njejtin celes. Kjo ruan modele. Prandaj, nese enkriptohet nje imazh me ECB, forma e imazhit mund te mbetet e dallueshme.

Dobesi:

- zbulon perseritje
- blloqet jane te pavarura
- sulmuesi mund te nderroje ose riorganizoje blloqe nese e di formatin
- nuk jep integritet

ECB mund te kete perdorim vetem per te dhena te vogla, te rastesishme dhe pa perseritje, por ne praktike shmanget.

## Cipher Block Chaining - CBC

CBC lidh cdo bllok me ciphertext-in paraprak:

```text
Ci = E(K, Pi XOR Ci-1)
Pi = D(K, Ci) XOR Ci-1
```

Per bllokun e pare perdoret `IV`:

```text
C0 = IV
```

IV nuk ka nevoje te jete sekret, por duhet te jete unik dhe i paparashikueshem. Qellimi eshte qe dy mesazhe te njejta te mos japin ciphertext te njejte.

Avantazhe:

- fsheh perseritjet
- cdo bllok varet nga blloqet paraprake
- blloku i fundit mund te perdoret si ide per MAC ne disa skema klasike

Kujdes: CBC vetem nuk mjafton per integritet. Duhet MAC ose mode autentikuese moderne.

## Stream cipher

Stream cipher gjeneron nje keystream:

```text
k1, k2, ..., kn
```

Pastaj:

```text
ci = pi XOR ki
pi = ci XOR ki
```

Nese keystream eshte vertet i rastesishem, ka gjatesi sa mesazhi, perdoret vetem nje here dhe mbahet sekret, kemi one-time pad, i cili eshte teorikisht shume i sigurt.

Nese `ki = 0`, atehere ciphertext eshte i njejte me plaintext. Prandaj cilesia dhe fshehtesia e keystream eshte gjithcka.

## One Time Pad

One Time Pad kombinon plaintext-in me nje celes me gjatesi te njejte:

```text
C = P XOR K
P = C XOR K
```

Kushtet per siguri:

- celesi duhet te jete plotesisht i rastesishem
- celesi duhet te kete gjatesi sa mesazhi
- celesi duhet te perdoret vetem nje here
- celesi duhet te ruhet sekret

Problemi praktik eshte shperndarja dhe ruajtja e celesit. Nese celesi riperdoret, siguria bie shume.

## A5/1

A5/1 eshte shembull i stream cipher me shift registers, i perdorur historikisht ne GSM. Ai ka tre regjistra:

- X: 19 bit
- Y: 22 bit
- Z: 23 bit

Ne cdo iterim merret nje bit shumice:

```text
m = maj(x8, y10, z10)
```

Regjistri leviz vetem nese biti i tij i kontrollit eshte i barabarte me `m`. Keystream bit del nga XOR i biteve te fundit:

```text
keystream = x18 XOR y21 XOR z22
```

Ideja e rendesishme: shift-register crypto eshte efikase ne hardware, por dizajni duhet te jete i kujdesshem sepse modelet periodike mund te sulmohen.

## AES

AES eshte standardi modern simetrik dhe zevendesuesi praktik i DES. Nga ligjeratat:

- block size: 128 bit
- key length: 128, 192 ose 256 bit
- 10 deri 14 raunde, varesisht nga gjatesia e celesit

AES perdoret gjeresisht sepse eshte i shpejte, i standardizuar dhe me siguri shume me te larte se DES.

# Shkembimi i celesave dhe KDC

## Problemi i shperndarjes se celesave

Ne enkriptim simetrik, palet duhet te kene te njejtin celes sekret para komunikimit. Kjo krijon problem praktik: si e dergojme celesin pa u pergjuar?

Nese perdorim nje Key Distribution Center (KDC), secili perdorues ka celes me KDC-ne. Kur Alice do te flase me Bob:

1. Alice kerkon nga KDC nje celes per komunikim me Bob.
2. KDC gjeneron `Ktemp`.
3. KDC dergon `E(KA, Ktemp)` per Alice dhe `E(KB, Ktemp)` per Bob.
4. Alice dhe Bob e dekriptojne me celesat e tyre.
5. Te dy perdorin `Ktemp` si session key.

Kjo ul numrin e celesave qe duhet te ruhen, por KDC behet pike shume e rendesishme besimi.

## Shkembimi me celes publik

Ne enkriptim asimetrik:

1. Alice merr celesin publik te Bob.
2. Alice gjeneron nje celes session `Ktemp`.
3. Alice dergon `E(KpubB, Ktemp)`.
4. Bob e dekripton me celesin privat.
5. Te dy perdorin `Ktemp` per enkriptim simetrik.

Kjo perdoret sepse RSA/asimetriku eshte i ngadalte per te dhena te medha, ndersa simetriku eshte i shpejte. Prandaj ne praktike shpesh perdoret kombinim: asimetriku per shkembim celesi, simetriku per mesazhet.

## Man-in-the-middle

Nese celesat publik nuk autentikohen, sulmuesi mund te nderroje celesat:

- Alice mendon se po merr celesin publik te Bob, por merr celesin e sulmuesit.
- Bob mendon se po merr celesin publik te Alice, por merr celesin e sulmuesit.
- Sulmuesi dekripton, lexon, ndryshon dhe ri-enkripton mesazhet.

Kjo quhet man-in-the-middle. Zgjidhja eshte nenshkrimi i celesave publik me certifikata X.509 dhe infrastrukture PKI.

# RSA dhe enkriptimi asimetrik

## Pse duhet enkriptimi asimetrik

Enkriptimi simetrik eshte i shpejte, por ka problem me shperndarjen e celesave. Enkriptimi asimetrik perdor cift celesash:

- celes publik: mund te shperndahet
- celes privat: mbahet sekret

Per te derguar mesazh sekret te Bob, Alice e enkripton me celesin publik te Bob. Vetem Bob e dekripton me celesin privat.

## Bazat matematikore

RSA bazohet ne faktorizimin e numrave te medhenj. Lehte eshte me shumezu dy prime te medhenj, por shume veshtire me faktorizu produktin.

Koncepte qe duhen:

- prime number: ka vetem faktoret 1 dhe vetveten
- coprime: dy numra kane gcd 1
- modulo: mbetja pas pjesetimit
- Euler totient `phi(n)`: numri i numrave me te vegjel ose te barabarte me `n` qe jane coprime me `n`

Nese:

```text
n = p * q
```

ku `p` dhe `q` jane prime, atehere:

```text
phi(n) = (p - 1) * (q - 1)
```

## Teorema Fermat-Euler

Per `m` relativisht te thjeshte me `n`:

```text
m^phi(n) mod n = 1
```

Kur `n = p*q`:

```text
m^((p-1)(q-1)) mod n = 1
```

Kjo eshte baza qe e ben RSA te funksionoje.

## Algoritmi RSA

Hapat:

1. Zgjidh dy numra te thjeshte `p` dhe `q`.
2. Llogarit `n = p*q`.
3. Llogarit `phi(n) = (p-1)(q-1)`.
4. Zgjidh `e` te tille qe `gcd(e, phi(n)) = 1`.
5. Gjej `d` te tille qe:

```text
e*d mod phi(n) = 1
```

6. Celesi publik eshte `(e, n)`.
7. Celesi privat eshte `d` dhe praktikisht ruhen edhe `p`, `q` per optimizim.

Enkriptimi:

```text
c = m^e mod n
```

Dekriptimi:

```text
m = c^d mod n
```

## Shembull RSA

Nga ligjerata:

```text
p = 5
q = 11
n = p*q = 55
phi(n) = (5-1)(11-1) = 40
e = 3
```

Gjejme `d`:

```text
3*d mod 40 = 1
d = 27
```

Pra:

```text
Celesi publik: (3, 55)
Celesi privat: 27
```

Per mesazhin `m = 26`:

```text
c = 26^3 mod 55 = 31
m = 31^27 mod 55 = 26
```

Kjo eshte shembull i vogel per llogaritje ne provim. Ne praktike `p` dhe `q` jane shume te medhenj.

## Shpejtesia e RSA

RSA eshte shume me i ngadalte se DES/AES:

- ne hardware mund te jete rreth 1000 here me i ngadalte se DES
- ne software mund te jete rreth 100 here me i ngadalte

Prandaj nuk perdoret zakonisht per enkriptim te te dhenave te medha. Perdoret per:

- shkembim session key
- nenshkrim digjital
- verifikim identiteti

Eksponente publik te shpeshte jane:

```text
3, 7, 65537
```

`65537 = 2^16 + 1` perdoret shpesh sepse eshte efikas dhe praktikisht i sigurt kur perdoret me padding korrekt.

## Siguria e RSA

Siguria varet nga veshtiresia e faktorizimit te `n = p*q`. Nese sulmuesi gjen `p` dhe `q`, mund te llogarise `phi(n)` dhe pastaj `d`.

Duhet me dit:

- `n` eshte pjese e celesit publik
- `e` eshte publik
- `d`, `p`, `q` jane sekret
- madhesia e celesit ka rendesi shume te madhe

RSA pa padding te sigurt nuk duhet perdorur ne praktike. Standardet PKCS e definojne si duhet te paketohet dhe perdoret RSA.

## PKCS

PKCS jane Public-Key Cryptography Standards te dizajnuara nga RSA Data Security. Disa te rendesishme:

- PKCS #1: RSA Cryptography Standard
- PKCS #3: Diffie-Hellman Key Agreement
- PKCS #5: Password-Based Cryptography
- PKCS #7: Cryptographic Message Syntax
- PKCS #8: Private-Key Information Syntax
- PKCS #10: Certification Request Syntax
- PKCS #11: Cryptographic Token Interface, i rendesishem per smart cards/tokens
- PKCS #12: Personal Information Exchange, p.sh. ruajtja e certifikatave dhe celesave
- PKCS #15: Cryptographic Token Information Format

# Diffie-Hellman-Merkle

## Ideja

Diffie-Hellman-Merkle (DHM) lejon dy pale te krijojne nje celes simetrik mbi nje kanal publik pa e derguar vete celesin.

Nuk eshte enkriptim mesazhi ne vetvete. Eshte shkembim celesi.

## Hapat

Alice dhe Bob bien dakord publikisht per:

```text
p = numer prime
g = baze/gjenerator
```

Alice zgjedh sekretin `a`, Bob zgjedh sekretin `b`.

Alice dergon:

```text
A = g^a mod p
```

Bob dergon:

```text
B = g^b mod p
```

Alice llogarit:

```text
K = B^a mod p
```

Bob llogarit:

```text
K = A^b mod p
```

Te dy marrin te njejtin rezultat sepse:

```text
(g^b)^a mod p = (g^a)^b mod p = g^(ab) mod p
```

## Shembull DHM

Nga ligjerata:

```text
p = 23
g = 5
a = 6
b = 15
```

Alice:

```text
5^6 mod 23 = 8
```

Bob:

```text
5^15 mod 23 = 19
```

Alice:

```text
19^6 mod 23 = 2
```

Bob:

```text
8^15 mod 23 = 2
```

Celesi i perbashket eshte `2`.

## Dobesia kryesore

DHM pa autentikim eshte i cenueshem nga man-in-the-middle. Sulmuesi mund te beje shkembim te vecante me Alice dhe shkembim te vecante me Bob. Zgjidhja eshte autentikimi i vlerave publike me certifikata ose nenshkrime digjitale.

# Hash funksionet

## Funksionet njekaheshe

Funksioni hash merr hyrje me gjatesi arbitrare dhe jep dalje me gjatesi fikse:

```text
h = H(M)
```

Vetite kryesore:

- kompresim: dalje fikse edhe per hyrje te gjata
- efikasitet: llogaritet shpejt
- preimage resistance: nga `h` eshte veshtire te gjendet `M`
- second preimage resistance: per `M` te dhene, veshtire te gjendet `M'` me te njejtin hash
- collision resistance: veshtire te gjenden dy mesazhe te ndryshme me te njejtin hash

Nje ndryshim i vetem bit ne mesazh duhet ta ndryshoje shume hash-in.

## Perdorimet

Hash funksionet perdoren per:

- integritet te dokumenteve
- verifikim te shkarkimit te fajllave
- ruajtje te fjalekalimeve ne forme hash
- nenshkrime digjitale
- fingerprint te te dhenave
- verifikim teksti, fajlli ose folderi

Hash nuk jep fshehtesi. Nese dikush e ka mesazhin, mund ta llogarise hash-in. Hash vetem ndihmon me verifiku nese mesazhi ka ndryshuar.

## MD5

MD5:

- dizajnuar nga Ron Rivest
- dalje 128 bit = 16 byte
- punon me blloqe 512 bit
- ka 4 raunde me nga 16 operacione, gjithsej 64 operacione
- perdor 4 variabla 32-bit: A, B, C, D
- pershkruar ne RFC 1321

MD5 nuk konsiderohet me i sigurt per collision resistance. Mund te perdoret vetem per kontroll jo-sigurie, por jo per nenshkrime, certifikata ose password security.

## SHA-1

SHA-1:

- dalje 160 bit = 20 byte
- punon me blloqe 512 bit
- perdor 5 variabla 32-bit: A, B, C, D, E
- ka 4 raunde me nga 20 operacione, gjithsej 80 operacione

Edhe SHA-1 sot konsiderohet i dobet per collision resistance. Ne praktike preferohen SHA-256, SHA-384, SHA-512 ose SHA-3.

## SHA-2 dhe SHA-3

Nga ushtrimet:

- SHA-1: 160 bit
- SHA-2: 224, 256, 384, 512 bit
- SHA-3: 224, 256, 384, 512 bit

Gjatesia e daljes ndikon ne:

- collision resistance: dalje me e gjate do te thote me shume mundesi te mundshme
- performance: dalje dhe strukture me e madhe mund te kerkoje me shume pune

Per programim praktik shpesh kerkohet CLI si:

```bash
--alg=MD5 hash-text DiteEMire
--alg=SHA256 hash-file path/to/file
--alg=SHA1 hash-dir path/to/folder
```

## Birthday problem dhe collision

Per hash me `n` bit, brute force per preimage eshte rreth `2^n`, por gjetja e collision ka kompleksitet rreth `2^(n/2)` per shkak te birthday paradox. Prandaj 128-bit hash nuk jep 128-bit collision security, por rreth 64-bit.

Kjo eshte arsye pse MD5 u be i pasigurt.

# Ruajtja e fjalekalimeve

## Gabimi: plain text passwords

Mos ruaj fjalekalime ne plain text:

```text
UserName | Password
Blerim   | 12345678
Arbena   | abcdef
```

Nese databaza rrjedh, sulmuesi i merr direkt fjalekalimet.

## Hash pa salt

Me mire:

```text
UserName | PasswordHash
Blerim   | H(12345678)
```

Por nese dy perdorues kane te njejtin password, do ta kene te njejtin hash. Sulmuesi mund te perdore rainbow tables ose dictionary attack.

## Salted hash

Me salt:

```text
Salt = random value
Stored = H(password + salt)
```

Tabela ruan:

```text
UserName | Salt | SaltedPasswordHash
```

Edhe nese dy perdorues kane te njejtin password, salt i ndryshem prodhon hash te ndryshem.

## Procesi i autentikimit

Hapat:

1. Klienti dergon username.
2. Serveri kontrollon nese ekziston perdoruesi.
3. Serveri merr `salt` dhe `salted password hash`.
4. Nga forma e login-it merret password.
5. Llogaritet `H(password + salt)`.
6. Krahasohet me vleren e ruajtur.
7. Nese jane identike, login OK; perndryshe login NOK.

## PBKDF2

PBKDF2 eshte Password-Based Key Derivation Function. Ai perdor:

- password
- salt
- HMAC ose funksion pseudorandom
- shume iterime

Qellimi eshte ta beje brute force me te shtrenjte. Standardi lidhet me PKCS #5 dhe RFC 8018. Ne praktike, per password hashing perdoren edhe bcrypt, scrypt ose Argon2, por ne ligjerata theksohet PBKDF2.

# Nenshkrimet digjitale

## Cka siguron nenshkrimi digjital

Nenshkrimi digjital perdoret per:

- autenticitet: e dime kush e ka nenshkruar
- integritet: ndryshimi i dokumentit zbulohet
- mos-mohim: nenshkruesi nuk mund ta mohoje lehte
- lidhje me dokumentin: nenshkrimi nuk mund te bartet ne dokument tjeter

Nenshkrimi digjital nuk jep privatesi. Dokumenti mund te jete i lexueshem. Per privatesi duhet enkriptim.

## Si krijohet nenshkrimi

Ne praktike nuk enkriptohet i gjithe dokumenti me celes privat, sepse kjo eshte e ngadalte. Behet:

```text
h = H(M)
S = E(Kprivate_sender, h)
```

Pra nenshkruhet hash-i i dokumentit.

Verifikimi:

1. Marresi llogarit `h1 = H(M)` nga dokumenti i pranuar.
2. Marresi dekripton nenshkrimin me celesin publik te derguesit dhe merr `h2`.
3. Nese `h1 == h2`, nenshkrimi verifikohet.

## Pse timestamp ka rendesi

Nenshkrimi mund te perfshije timestamp per te parandaluar replay attack. Kjo eshte e rendesishme ne pagesa elektronike, kontrata dhe transaksione, ku nje mesazh i vjeter nuk duhet te riperdoret.

## Nenshkrimi dhe enkriptimi bashke

Vetem nenshkrimi nuk mjafton per privatesi. Rend i zakonshem:

1. Derguesi nenshkruan mesazhin ose hash-in me celesin privat.
2. Pastaj enkripton permbajtjen/nenshkrimin me celesin publik te marresit.
3. Marresi dekripton me celesin privat te vet.
4. Marresi verifikon nenshkrimin me celesin publik te derguesit.

Nga ushtrimet, notacioni:

```text
[M]Alice = nenshkrimi i M me celesin privat te Alice
{M}Alice = enkriptimi i M me celesin publik te Alice
```

Ne praktike shpesh perdoren dy cifte celesash:

- nje cift per enkriptim
- nje cift per nenshkrim

Arsye juridike: dokumenti qe nenshkruhet duhet te jete i lexueshem para nenshkrimit.

## Nenshkrimi elektronik dhe nenshkrimi digjital

Nenshkrimi elektronik eshte koncept me i gjere juridik: cdo e dhene elektronike e lidhur me dokumentin per te treguar pajtim ose identitet.

Nenshkrimi digjital eshte metode kriptografike konkrete qe perdor hash, celes privat/publik dhe verifikim matematik.

## eIDAS

eIDAS rregullon sherbimet e besimit ne BE:

- electronic signatures
- electronic seals
- timestamps
- electronic delivery services
- website authentication

Tri nivele:

- Electronic signature: forme e pergjithshme elektronike.
- Advanced electronic signature: lidhur unike me nenshkruesin, e identifikon ate, krijohet nen kontrollin e tij, dhe ndryshimet ne dokument zbulohen.
- Qualified electronic signature: advanced signature e krijuar me pajisje te kualifikuar dhe certifikate te kualifikuar.

eIDAS v2 permend edhe EUDI Wallet, self-sovereign identity dhe sherbime te reja te kualifikuara.

# Certifikatat, PKI dhe menaxhimi i celesave

## Pse duhen certifikatat

Problemi i celesit publik eshte: si e di qe ky celes publik i takon vertet Bob-it?

Certifikata digjitale lidh:

- identitetin e subjektit
- celesin publik
- afatin e vlefshmerise
- algoritmin
- nenshkrimin e autoritetit certifikues

Kjo e ben te mundur verifikimin e celesit publik.

## X.509

Certifikata X.509 v3 permban:

- version
- serial number
- signature algorithm identifier
- issuer
- validity period
- subject
- subject public key
- issuer/subject ID opsional
- extensions opsionale
- digital signature te CA-se

CA (Certification Authority) e nenshkruan certifikaten me celesin e vet privat.

## PKI

Public Key Infrastructure perfshin:

- CA
- RA (Registration Authority)
- certifikata
- CRL (Certificate Revocation List)
- repository per certifikata dhe CRL
- procedura per gjenerim, regjistrim, revokim dhe freskim celesash

PKI e zvogelon rrezikun e man-in-the-middle sepse celesat publik jane te nenshkruar dhe te verifikueshem.

## PGP vs X.509

PGP perdor Web of Trust:

- perdoruesi mund ta nenshkruaje vet celesin e vet
- perdorues te tjere mund ta nenshkruajne celesin
- nje celes mund te kete shume nenshkrime

X.509 perdor hierarki:

- issuer zakonisht eshte CA
- subject eshte pronari i certifikates
- zakonisht ka nje nenshkrim nga issuer
- root CA mund te jete self-signed

## Modelet e besimit

Nga ushtrimet:

- Monopoly: nje CA e vetme e besueshme.
- Oligarchy: disa CA kryesore, perdoruesi zgjedh kujt i beson.
- Anarchy: secili mund te jete CA, perdoruesi vendos kujt i beson.

## Verifikimi i celesave

Per celesa publik pa certifikate mund te behet:

- kontrollim byte per byte
- krahasim i fingerprint/thumbprint
- verifikim out-of-band, p.sh. ne telefon ose takim fizik

Thumbprint eshte hash i celesit/certifikates qe krahasohet me vlere te pritur.

## Ruajtja e celesave

Vendet e mundshme:

- fajll ne disk
- leter ne safe
- USB/CD
- smart card me PIN
- mental key

Vendi me i sigurt praktik per celes privat eshte pajisje ku celesi gjenerohet brenda dhe nuk e leshon pajisjen, p.sh. smart card ose token hardware.

## Backup dhe rikuperimi

Nese humbet celesi privat, mund te humbet qasja ne te dhena ose mundesia e nenshkrimit. Por nese ka mekanizem rikuperimi, ai mund te jete security hole. Prandaj key recovery duhet te rregullohet me politika te qarta.

## Gjenerimi i celesave

Celesat duhet te jene te rastesishem. Zgjedhje te dobeta, p.sh. fjale nga fjalori, jane te cenueshme nga dictionary attack.

Per DES, hapesira teorike eshte `2^56`, por nese perdoruesi zgjedh fjale te thjeshta, hapesira reale eshte shume me e vogel.

## Base64

Base64 perdoret per ta paraqitur te dhena binare ne ASCII. Ka 64 simbole:

```text
A-Z
a-z
0-9
+ /
```

Perdorimi tipik: certifikata, celesa, nenshkrime, attachment-e, XML/JSON ku duhen te dhena binare ne tekst.

# XML nenshkrimet digjitale

## XML

XML (eXtensible Markup Language) eshte gjuhe per pershkrimin dhe bartjen e te dhenave. Ndryshe nga HTML, XML nuk fokusohet ne pamje, por ne strukture dhe kuptim te te dhenave.

XML tags nuk jane te paradefinuara. Dokumenti mund te jete vetepershkrues me DTD ose XML Schema.

Shembull:

```xml
<studenti>
  <emri>Filan Fisteku</emri>
  <ditelindja>1980-11-01</ditelindja>
  <indexi>55555</indexi>
</studenti>
```

## Rregulla per XML elemente

Elementet:

- mund te permbajne shkronja dhe numra
- nuk duhet te fillojne me numer ose shenje pikesimi
- nuk duhet te fillojne me `xml`, `XML` ose `Xml`
- nuk duhet te permbajne hapesira
- `:` perdoret per namespaces

Well-formed XML do te thote se dokumenti ka sintakse valide: tag-et mbyllen, struktura eshte korrekte, atributet jane ne rregull.

## DTD dhe XSD

DTD dhe XML Schema definojne strukturen legale te dokumentit.

XML Schema (XSD):

- definon elementet dhe atributet qe lejohen
- definon renditjen dhe numrin e elementeve
- tregon cilat jane child elements
- definon nese nje element mund te jete bosh
- definon tipe te dhenash dhe vlera standarde

## Pse XML signature eshte problem me vete

Mund ta kthejme nje XML dokument ne byte array dhe ta enkriptojme, por rezultati nuk eshte me XML well-formed. Ne praktike duhen:

- nenshkrime te pjesshme te XML dokumentit
- enkriptim i pjesshem i elementeve
- disa nenshkrime per pjese te ndryshme
- ruajtje e hash values dhe certifikatave ne dokument
- verifikim edhe kur dokumenti ka namespaces, whitespace ose forma te ndryshme sintaksore

## XML canonicalization

XML eshte fleksibil. Dy dokumente mund te duken te ndryshem ne tekst, por te kene kuptim te njejte. P.sh. hapesirat, renditja e atributeve, ose forma e elementeve mund te ndryshojne.

Per nenshkrim kjo eshte problem: hash-i varet nga byte-at. Prandaj XML kthehet ne forme kanonike para hash-it dhe nenshkrimit.

Canonicalization e ben dokumentin ne forme standarde, qe verifikimi te mos deshtoje vetem per shkak te ndryshimeve sintaksore pa ndryshim semantik.

## Struktura e XML Signature

Sipas RFC 3275 / XML Signature, struktura eshte:

```xml
<Signature>
  <SignedInfo>
    <CanonicalizationMethod/>
    <SignatureMethod/>
    <Reference URI="">
      <Transforms/>
      <DigestMethod/>
      <DigestValue/>
    </Reference>
  </SignedInfo>
  <SignatureValue/>
  <KeyInfo/>
  <Object/>
</Signature>
```

Kuptimi i pjeseve:

- `SignedInfo`: tregon cka eshte nenshkruar dhe si.
- `CanonicalizationMethod`: algoritmi per forme kanonike.
- `SignatureMethod`: algoritmi i nenshkrimit, p.sh. RSA ose DSA.
- `Reference`: tregon te dhenat qe jane nenshkruar; mund te jene ne te njejtin dokument ose dokument te jashtem.
- `Transforms`: transformimet para hash-it.
- `DigestMethod`: algoritmi hash, p.sh. SHA.
- `DigestValue`: hash-i.
- `KeyInfo`: opsional, celes publik ose certifikate per verifikim.
- `Object`: te dhena te futura brenda nenshkrimit ose objekt i lidhur.

## XML signatures ne .NET

Ne .NET perdoret:

```text
System.Security.Cryptography.Xml
```

Klasa kryesore:

```text
SignedXml
```

Metodat:

```text
ComputeSignature()
CheckSignature()
```

Ideja praktike: krijohet reference per elementin qe nenshkruhet, caktohen transformimet/canonicalization, llogaritet digest, nenshkruhet me celes privat dhe verifikohet me celes publik/certifikate.

# Smart kartelat

## Cka jane smart kartelat

Smart kartela eshte kartele plastike me chip qe mund te ruaje dhe shpesh te procesoje te dhena. Jo cdo kartele eshte e njejte:

- memory card: ruan te dhena, logjike e kufizuar, p.sh. kartela telefonike
- microprocessor card: ka CPU dhe mund te procesoje, gjeneroje/ruaje celesa
- contactless card: komunikon me lexuesin permes antenes
- dual interface: mund te kete edhe kontakt edhe pa kontakt

## Standardet fizike

Formate:

- ID-1: 85.6 x 54 mm, madhesi e zakonshme kartele
- ID-000: format SIM

Material tipik: PVC.

Kontaktet sipas ISO 7816 perfshijne:

- Vcc
- GND
- RST
- CLK
- I/O
- Vpp
- RFU

## Vetite elektrike

Sipas ISO 7816-3:

- tension furnizimi 5V ose 3V
- rryme me e vogel se rreth 10 mA
- fuqia rreth `P = U*I`
- clock zakonisht vjen nga jashte, p.sh. 4-8 MHz
- transmetim nga rreth 9600 bps deri 112000 bps

Smart kartela ka burime te kufizuara, prandaj sistemi operativ dhe aplikacionet duhet te jene shume kompakte.

## Arkitektura e brendshme

Komponentet tipike:

- CPU
- ROM per sistem operativ
- EEPROM per te dhena jo-volative dhe aplikacione
- RAM per te dhena te perkohshme
- crypto coprocessor
- I/O
- per contactless: antene, modulator/demodulator, clock extractor

EEPROM eshte me i shtrenjte ne siperfaqe se ROM, prandaj perdoret me kujdes.

## Card Operating System - COS

Smart karta ka sistem operativ te vogel. Shembull historik: STARCOS. COS vendoset kryesisht ne ROM, por pjese mund te jene edhe ne EEPROM.

Detyrat e COS:

- menaxhim i memories
- menaxhim i fajllave
- kontroll i qasjes
- PIN verification
- komanda APDU
- funksione kriptografike

## Struktura e fajllave

Fajllat organizohen si peme:

- MF (Master File): rrenja, p.sh. ID `3F 00`
- DF (Dedicated File): si directory
- EF (Elementary File): fajll me te dhena

Lloje EF:

- transparent
- linear fixed
- linear variable
- cyclic

Kjo i ngjan filesystem-it, por eshte e optimizuar per kartele.

## PIN dhe siguria

PIN zakonisht ka 4 deri 12 karaktere. Pas disa tentimeve te gabuara, p.sh. 3, kartela mund te bllokohet.

Ka nivele:

- User PIN
- Administrator PIN

Rrezik i permendur: dergimi i PIN-it plain text neper rrjet ose deri te pajisja pa kanal te sigurt.

## Komunikimi fizik

Komunikimi eshte half-duplex sepse ekziston vetem nje linje I/O. Terminali eshte master, kartela eshte slave.

Transmetimi mund te jete:

- direct convention: 3/5V si logjike 1
- inverse convention: 0V si logjike 1

Paketa bazike:

- 1 start bit
- 8 bit data
- 1 parity bit
- 2 stop bits

ETU (Elementary Time Unit) varet nga clock dhe pjestuesi `F`. Shembull:

```text
3.5712 MHz / 372 = 9600 bit/s
```

## ATR dhe protokollet

ATR (Answer To Reset) eshte pergjigjja e karteles pas reset. Mund te jete deri 33 byte dhe tregon parametra te komunikimit.

Protokollet:

- T=0: asinkron, half-duplex, byte-oriented
- T=1: asinkron, half-duplex, block-oriented

## APDU

APDU (Application Protocol Data Unit) eshte formati kryesor i komandave sipas ISO 7816-4.

Command APDU:

```text
CLA INS P1 P2 [Lc] [Data] [Le]
```

Ku:

- CLA: class
- INS: instruction
- P1/P2: parametra
- Lc: gjatesia e te dhenave qe dergohen
- Data: te dhenat
- Le: numri i byte-ve qe priten ne pergjigje

Response APDU:

```text
Data SW1 SW2
```

`SW1 SW2` jane status words. Shembull:

```text
90 00 = sukses
61 XX = ka ende te dhena per t'u marre
```

## Rastet e APDU

Command APDU:

- Case 1: vetem header
- Case 2: header + Le
- Case 3: header + Lc + Data
- Case 4: header + Lc + Data + Le

Response APDU:

- vetem `SW1 SW2`
- `Data + SW1 SW2`

## Komandat tipike

Komanda te rendesishme:

- `SelectFile`: zgjedh MF/DF/EF sipas file ID ose application ID
- `ReadBinary`: lexon byte nga EF me offset
- `WriteBinary`: shkruan, nese ACL/PIN e lejon
- `Verify`: verifikon PIN user ose administrator
- authenticate/read/write ne aplikacione specifike

Standardet:

- ISO 7816-4 per komanda te pergjithshme
- ISO 7816-8 per funksione kriptografike
- EMV per pagesa elektronike
- EN 1546 per electronic purse
- GSM 11.11 per telekomunikacion

## Secure Messaging

Secure Messaging mbron transferin e te dhenave mes terminalit dhe karteles. Mund te perdore:

- algoritme kriptografike
- celesa
- random challenges
- initial data
- logical channels

Qellimi eshte konfidencialitet dhe/ose integritet per APDU.

## Menaxhimi i celesave ne smart kartela

Nga ligjerata:

- Master Key: nuk ruhet ne kartele.
- Derived Key: derivuar, p.sh. `E(CID, MasterKey)`.
- Diversified Key: nje celes per aplikacion ose kartele.
- Session Key: p.sh. `E(DerivedKey, RND)`.
- Versioning: per rotacion dhe menaxhim.

Ideja eshte qe komprometimi i nje celesi te kete ndikim minimal.

## PC/SC

PC/SC synon qe aplikacioni te jete i pavarur nga lexuesi dhe kartela konkrete.

Pjesemarres:

- smart card
- reader
- reader driver
- smart card resource manager
- service provider
- user application

Hapat tipike:

1. `SCardEstablishContext`
2. `SCardListReaders`
3. `SCardGetStatusChange`
4. `SCardConnect`
5. `SCardTransmit`
6. `SCardDisconnect`
7. `SCardReleaseContext`

## Smart kartelat pa kontakt

Lloje:

- Close coupling: 0-1 cm, ISO 10536.
- Proximity coupling: 0-10 cm, ISO 14443, shume i perdorur per karta multi-aplikative.
- Vicinity coupling: deri rreth 1 m, ISO 15693, i pershtatshem per tracking.

Contactless card ka antene dhe merr energji/komunikim nga fusha e lexuesit.

## Aplikimet

Smart kartelat perdoren ne:

- GSM/SIM
- banka
- pagesa elektronike
- para elektronike
- qasje fizike
- login ne Windows
- ruajtje fjalekalimesh / Single Sign-On
- bileta transporti
- tracking i objekteve
- pasaporta biometrike me RFID
- ID kartela

# Ushtrimet praktike sipas javeve

## Jave 1 - konceptet dhe planprogrami

Duhet te dish termat:

- cryptography
- cryptanalysis
- cryptology
- plaintext
- ciphertext
- cipher
- encryption
- decryption

Ushtrimet kerkojne GitHub repository, editor si Visual Studio Code, gjuhe programuese sipas kerkeses se ushtrimeve, dhe Cryptool 2.

## Jave 2 - Caesar dhe Atbash

Per Caesar duhet me implementu:

- enkriptim me `E(x) = (x + k) mod 26`
- dekriptim me `D(x) = (x - k) mod 26`
- brute force duke provuar te gjitha celesat
- analize frekuencore

Per Atbash:

```text
E(x) = 25 - x
D(x) = 25 - x
```

Pyetje qe mund te dali: cka eshte keyspace dhe si ndikon ne shpejtesine e brute force?

## Transposition ciphers

Nga planprogrami permenden:

- simple transposition
- columnar transposition
- double transposition

Duhet me kuptu se transpozicioni nuk i ndryshon simbolet, vetem renditjen. Brute force varet nga numri i renditjeve te mundshme.

## Jave 4 - OTP, DES dhe Triple DES

One Time Pad:

```text
C = A XOR k
A = C XOR k
```

Kushti kryesor: celesi gjatesi sa plaintext dhe te perdoret vetem nje here.

DES:

- 64-bit block
- 64-bit key me 8 parity bit, efektiv 56 bit
- 16 Feistel rounds
- 16 nencelesa 48-bit
- S-Box merr 6 bit dhe jep 4 bit

Triple DES:

```text
Encryption: ciphertext = E(D(E(plaintext, k1), k2), k1)
Decryption: plaintext  = D(E(D(ciphertext, k1), k2), k1)
```

## Jave 5 - RSA dhe DHM

RSA practical:

1. Zgjidh `p`, `q`.
2. Llogarit `n = p*q`.
3. Llogarit `phi(n) = (p-1)(q-1)`.
4. Zgjidh `e`.
5. Gjej `d` ku `d*e mod phi(n) = 1`.
6. Publik: `(e, n)`.
7. Privat: `d`.

Detyre tipike: enkripto/dekripto `m = 123` me `p = 23` dhe `q = 5`.

DHM practical:

1. Zgjidhen publikisht `p` dhe `g`.
2. Alice zgjedh `a`, Bob zgjedh `b`.
3. Alice dergon `g^a mod p`.
4. Bob dergon `g^b mod p`.
5. Te dy llogarisin sekretin e perbashket.

Duhet me dit edhe man-in-the-middle per DHM.

## Jave 7 - hash program

Detyra kerkon program qe llogarit hash per:

- tekst
- fajll
- folder

Algoritmet:

- MD5
- SHA1
- SHA256

Parametra tipike:

```text
--alg=MD5 hash-text DiteEMire
```

Duhet me kontrollu:

- algoritmin si parameter opsional
- komanden: `hash-text`, `hash-file`, `hash-dir`
- hyrjen: string, file path, directory path

## Jave 7 - salted hash login

Detyra tjeter: regjistrim dhe autentikim i perdoruesit me salted hash.

Regjistrim:

1. Merret password.
2. Gjenerohet salt random.
3. Ruhet `salt`.
4. Ruhet `H(password + salt)`.

Login:

1. Merret username.
2. Merret salt dhe hash nga databaza.
3. Llogaritet `H(password_input + salt)`.
4. Krahasohet me hash-in e ruajtur.

## Jave 8 - digital signature

Duhet me kuptu dhe implementu:

1. Gjenerohet cift celesash RSA.
2. Gjenerohet hash i dokumentit.
3. Hash-i enkriptohet/nenshkruhet me celesin privat.
4. Marresi e verifikon me celesin publik.
5. Marresi llogarit vet hash-in e dokumentit.
6. Nese hash-et perputhen, dokumenti eshte i pandryshuar dhe nenshkrimi eshte valid.

Pyetje e rendesishme: nenshkrimi nuk jep privatesi. Ai jep autenticitet dhe integritet.

## Jave 8 - certifikatat

Certifikata digjitale permban te dhena shtese per celesin publik dhe emrin e perdoruesit. CA eshte pale e trete e besuar qe krijon dhe nenshkruan certifikata.

PKI perfshin:

- CA
- CRL
- menaxhim celesash
- modele besimi: monopoly, oligarchy, anarchy

## Jave 12/13 - steganografia

Duhet me dit:

- dallimin kriptografi vs steganografi
- fshehjen ne tekst, audio, video, imazh
- LSB ne imazhe
- llogaritjen e kapacitetit
- perdorimin baze te `steghide`
- brute force me `stegcracker`

Formula per detyra:

```text
pixels = width * height
bits_capacity = pixels * bits_changed_per_pixel
bytes_capacity = bits_capacity / 8
kB_capacity = bytes_capacity / 1024
```

# Pyetje dhe pergjigje te shpejta per provim

## Cili eshte dallimi mes hash dhe encryption?

Enkriptimi eshte i kthyeshem me celes: ciphertext mund te kthehet ne plaintext. Hash eshte njekahesh: nga hash nuk duhet te gjendet mesazhi. Hash perdoret per integritet, jo per fshehtesi.

## Pse nuk duhet ECB?

Sepse blloqet e njejta plaintext japin blloqe te njejta ciphertext. Modelet mbeten te dukshme dhe blloqet mund te riorganizohen.

## Pse duhet IV ne CBC?

Qe blloku i pare te mos jete gjithmone i njejte per mesazhe te njejta. IV e ben enkriptimin unik edhe me te njejtin celes.

## Pse DES nuk eshte me i sigurt?

Sepse celesi efektiv eshte vetem 56 bit. Brute force eshte praktikisht i mundshem me hardware modern.

## Pse RSA nuk perdoret per fajlla te medhenj?

Sepse eshte shume me i ngadalte se enkriptimi simetrik. Zakonisht RSA perdoret per session key ose nenshkrim, pastaj AES/DES-like cipher perdoret per te dhenat.

## Pse certifikata e ndal MITM?

Sepse celesi publik lidhet me identitetin dhe nenshkruhet nga CA. Sulmuesi nuk mund te zevendesoje celesin publik pa pasur certifikate valide per identitetin e viktimes.

## Pse salted hash eshte me i mire se hash i thjeshte?

Sepse dy password-e te njejta japin hash te ndryshem nese salt eshte i ndryshem. Gjithashtu veshtireson rainbow tables dhe sulmet masive.

## Cka eshte non-repudiation?

Mos-mohimi. Nese nje dokument eshte nenshkruar digjitalisht me celes privat, nenshkruesi nuk mund ta mohoje lehte qe e ka nenshkruar, perderisa celesi privat ka qene nen kontrollin e tij.

## Pse XML signature ka nevoje per canonicalization?

Sepse XML mund te kete forma te ndryshme tekstuale me kuptim te njejte. Pa canonicalization, hash-i mund te ndryshoje per shkak te whitespace ose renditjes se atributeve, jo per shkak te ndryshimit real te te dhenave.

## Cka eshte APDU?

APDU eshte njesia e komandes/pergjigjes mes aplikacionit/lexuesit dhe smart karteles. Command APDU ka `CLA INS P1 P2 Lc Data Le`; Response APDU ka `Data SW1 SW2`.

## Cka eshte ATR?

Answer To Reset. Eshte pergjigjja fillestare e smart karteles pas reset dhe tregon parametra te komunikimit/protokollit.

## Cka eshte secret sharing me XOR?

Mesazhi ndahet ne pjese duke krijuar vargje random. Per dy persona:

```text
S = M XOR R
M = S XOR R
```

As `S` as `R` vetem nuk zbulojne mesazhin. Duhen te dyja.

# Formula qe duhet t'i mbash mend

## Caesar

```text
E_k(x) = (x + k) mod 26
D_k(x) = (x - k) mod 26
```

## DES Feistel

```text
Li = Ri-1
Ri = Li-1 XOR f(Ri-1, Ki)
```

## CBC

```text
Ci = E(K, Pi XOR Ci-1)
Pi = D(K, Ci) XOR Ci-1
```

## Stream cipher / OTP

```text
ci = pi XOR ki
pi = ci XOR ki
```

## RSA

```text
n = p*q
phi(n) = (p-1)(q-1)
e*d mod phi(n) = 1
c = m^e mod n
m = c^d mod n
```

## Diffie-Hellman-Merkle

```text
A = g^a mod p
B = g^b mod p
K = B^a mod p = A^b mod p
```

## Hash

```text
h = H(M)
```

## Digital signature

```text
h = H(M)
S = E(Kprivate_sender, h)
Verify: D(Kpublic_sender, S) == H(M)
```

## Steganography capacity

```text
pixels = width * height
bits = pixels * bits_per_pixel_used
bytes = bits / 8
kB = bytes / 1024
```
