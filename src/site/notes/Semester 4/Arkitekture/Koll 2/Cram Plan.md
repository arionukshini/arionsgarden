---
{"dg-publish":true,"permalink":"/semester-4/arkitekture/koll-2/cram-plan/","tags":["exam","arkitekture-kompjuterike","cram"]}
---


# Plan 2-ditor për provim - Arkitekturë Kompjuterike

Qëllimi: të kalosh, jo të lexosh bukur. Përdor active recall.

## Rregulli kryesor

Mos e rilexo materialin pasivisht për orë të tëra.

Bëje kështu:

1. Lexo pyetjen.
2. Përgjigju me zë pa e parë përgjigjen.
3. Kontrollo.
4. Shëno kartat që i gabon.
5. Kthehu vetëm te kartat e gabuara.

## Dita 1

### Blloku 1 - Kapitulli 3

Qëllimi: komponentet, regjistrat, cikli i instruksionit, interruptet.

Duhet t'i dish patjetër:

- PC = adresa e instruksionit vijues.
- IR = instruksioni aktual.
- MAR = adresa në memorie.
- MBR = të dhënat që hyjnë/dalin nga memoria.
- Fetch = sjell instruksionin.
- Execute = ekzekuton instruksionin.
- Interrupt = CPU ruan kontekstin dhe kalon te ISR.

### Blloku 2 - Kapitulli 4

Qëllimi: cache dhe pasqyrimet.

Duhet t'i dish patjetër:

- `EMAT = Tc + m * Tm`
- `miss rate = 1 - hit rate`
- Direct mapping = një bllok ka vetëm një linjë të caktuar.
- Associative mapping = blloku mund të shkojë në cilëndo linjë.
- Set-associative = blloku shkon në një set, por në cilëndo linjë brenda atij seti.
- Write-through = cache dhe memoria kryesore përditësohen menjëherë.
- Write-back = fillimisht përditësohet vetëm cache.

### Blloku 3 - Përsëritja

Përsërit vetëm kartat që i gabove nga Kapitulli 3 dhe 4.

Nëse një kartë e gabon dy herë, shkruaje përgjigjen me dorë ose në scratch note.

## Dita 2

### Blloku 1 - Kapitulli 5

Qëllimi: DRAM, SRAM, ROM, Flash, Hamming.

Duhet t'i dish patjetër:

- DRAM = kondensator + refresh + memorie kryesore.
- SRAM = latch/flip-flop + pa refresh + cache.
- ROM = jo e avullueshme.
- PROM = shkruhet një herë.
- EPROM = fshihet me UV.
- EEPROM = fshihet/shkruhet elektrikisht.
- Flash = fshirje në blloqe.
- Hamming = korrigjon gabime me një bit.

### Blloku 2 - Kapitulli 6

Qëllimi: disku, RAID/SSD, memoria virtuale.

Duhet t'i dish patjetër:

- Seek time = lëvizja e kokës.
- Rotational latency = pritja për sektorin.
- `Access time = seek time + rotational latency`
- Page = bllok virtual.
- Page frame = bllok fizik në RAM.
- Page fault = faqja nuk është në RAM.
- Adresa virtuale = page number + offset.
- Adresa fizike = frame number + offset.

### Blloku 3 - Karta kurth dhe detyra

Bëji kartat:

- Karta kurth
- Detyra të shkurtra

Nëse gabon më shumë se 20%, përsëriti vetëm ato që i gabove.

## Dy orët e fundit para provimit

Mos nis material të ri.

Vetëm:

- kartat high-yield,
- karta kurth,
- detyrat e shkurtra,
- formulat.

## Prioritet nëse nuk ka kohë

1. Regjistrat dhe cikli fetch-execute.
2. Interruptet.
3. Cache hit/miss, EMAT, pasqyrimet.
4. DRAM vs SRAM dhe llojet e ROM-it.
5. Disk timing dhe memoria virtuale.

