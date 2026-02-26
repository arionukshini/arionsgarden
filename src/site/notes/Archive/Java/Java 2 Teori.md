---
{"dg-publish":true,"permalink":"/archive/java/java-2-teori/"}
---

# Java OOP – Advanced Topics (Syllabus 10–15)

## 1. Abstraksioni – Klasat Abstrakte dhe Interface-at

### 1.1 Polimorfizmi

Polimorfizmi është koncepti kryesor i **Programimit të Orientuar në Objekte (POO)** që lejon që një variabël e një superklase të marrë forma të ndryshme përmes nënklasave të saj. Ai rrit fleksibilitetin dhe ripërdorshmërinë e kodit.

Polimorfizmi mund të ndahet në dy lloje kryesore:

#### 1.1.1 Polimorfizmi statik (Compile-time)

- Ndodh gjatë **kompilimit**, para se programi të ekzekutohet.
- Lidhet me **mbingarkimin e metodës (method overloading)** dhe **mbingarkimin e operatorëve (operator overloading)**.
- Metodat kanë **të njëjtin emër**, por ndryshojnë në **numrin ose tipin e parametrave**.
- JVM vendos gjatë kompilimit se cila metodë të thirret.
- Nuk mund të përdorim një objekt për të zgjedhur metodën në kohë ekzekutimi.

**Karakteristikat kryesore:**
- Vendimi për metodën bëhet në **kohën e kompilimit**.
- E bën kodin më të lexueshëm dhe të thjeshtë.
- Nuk ka fleksibilitet gjatë ekzekutimit.

#### 1.1.2 Polimorfizmi dinamik (Runtime)

- Ndodh gjatë **ekzekutimit** të programit.
- Lidhet me **mbishkrimin e metodës (method overriding)**.
- JVM vendos **në kohë ekzekutimi** se cila metodë e një objekti do të thirret.
- Polimorfizmi dinamik përdor referenca të tipit të klasës bazë për të thirrur metoda të nënklasave.
- Lidhja dinamike është "kupa e artë" e POO-së për përdorimin e trashëgimisë.

**Dallimi midis statik dhe dinamik:**
| Tipi             | Koha | Mënyra | Lidhja me metodën |
| | | | |
| Statik           | Kompilim | Parametrat | Mbingarkimi |
| Dinamik          | Ekzekutim | Referenca objekt | Mbishkrimi |

---

### 1.2 Klasat Abstrakte

- Një klasë që **nuk mund të instancohet drejtpërdrejt**.
- Mund të ketë metoda **abstrakte** dhe **konkrete**.
- Shërben si **bazë për nënklasa**.
- Mund të ketë **atribute** (variabla), që trashëgohen nga nënklasat.
- Një klasë abstrakte mund të ketë edhe **konstruktorë**, të cilët përdoren nga nënklasat.

**Karakteristikat kryesore:**
- Lejon trashëgimi të vetme.
- Përdoret për të përqendruar logjikën e përbashkët.
- Nuk mund të krijohet instancë me `new`.

**Metodat abstrakte:**
- Nuk kanë trup (body) në klasën bazë.
- Detyrojnë nënklasën **t’i implementojë**.
- Një nënklasë që nuk implementon të gjitha metodat abstrakte duhet të shpallet gjithashtu **abstrakte**.

---

### 1.3 Ndërfaqet (Interfaces)

- Një ndërfaqe është një kontratë që përcakton **sjelljen** e objekteve.
- Përmban vetëm **metoda abstrakte** dhe **konstante**.
- Një klasë mund të implementojë **shumë ndërfaqe**.
- Ndërfaqet nuk mund të instancohen me `new`.
- Të gjitha fushat e një ndërfaqe janë **public static final** dhe të gjitha metodat janë **public abstract**.

**Avantazhet:**
- Lejon **trashëgimi të shumëfishtë të sjelljes**.
- Ndihmon në krijimin e objekteve **krahasueshme, klonueshme, ose të editueshme**.
- Përdoret për **specifikimin e kontratave** pa logjikë konkrete.

**Shembuj konceptualë:**
- `Comparable` – për krahasimin e objekteve.
- `Cloneable` – për klonimin e objekteve.

**Krahasimi me klasat abstrakte:**

| Tipi           | Karakteristika                               | Trashëgimi | Përdorim |
|----------------|---------------------------------------------|------------|-----------|
| Klasa abstrakte | Metoda abstrakte + konkrete, atribute       | Vetëm një | Logjikë e përbashkët |
| Ndërfaqe       | Vetëm metoda abstrakte dhe konstante        | Shumëfishtë | Sjellje / kontrata |

---

### 1.4 Gabimet dhe Përjashtimet (Errors & Exceptions)

**Gabimet (Errors):**
- Ndodhin nga JVM.
- Nuk mund të trajtohen nga programi.
- Shembuj: `OutOfMemoryError`, `StackOverflowError`.

**Përjashtimet (Exceptions):**
- Ndodhin gjatë **ekzekutimit**.
- Mund të kapen dhe trajtohen me **try-catch**.
- Llojet kryesore:
  1. **Checked exceptions** – duhet të deklarohen me `throws`.
  2. **Unchecked exceptions** – `RuntimeException`, nuk kërkojnë deklarim.
  
**Gabimet më të shpeshta:**
- Sintaksore: zbulohen nga kompilatori.
- Gjatë ekzekutimit: ndalojnë programin, p.sh., ndarja me zero.
- Logjike: ekzekutohen por rezultati është gabim.

**Mjetet për trajtim:**
- **try-catch**: kap dhe trajton përjashtime.
- **throws**: deklaron që një metodë mund të hedhë përjashtim.
- **finally**: ekzekutohet gjithmonë, pavarësisht nëse ka gabim.

---

### 1.5 File I/O

- Menaxhimi i fajllave përmes klasës `File` dhe leximi/shkrimi me `Scanner` dhe `FileWriter`.
- **File** ofron vetëm informacione mbi fajllin (existencë, madhësi, lexim/shkrim).
- Për lexim/shkrim të të dhënave: `Scanner` (lexim) dhe `FileWriter` (shkrim).
- Ndihmon për ruajtjen e të dhënave, logimin e gabimeve dhe menaxhimin e informacionit.

---

### 1.6 Përmbledhje – Trajtimi i Gabimeve dhe Përjashtimeve

- Zhvillimi i softuerit kërkon **programim mbrojtës**.
- **Exception handling** e bën kodin më të besueshëm dhe më të sigurt.
- Diferenca kryesore mes **gabimeve të zhvillimit, gabimeve runtime dhe gabimeve logjike** është e rëndësishme.
- Përdorimi i try-catch dhe logimit e bën softuerin më të mirë dhe më të menaxhueshëm.

**The key takeaway:**  
Polimorfizmi, abstraksioni, ndërfaqet dhe trajtimi i gabimeve janë **bazat teorike** të POO-së. Kuptimi i tyre teorik bën kodin më fleksibël, ripërdorshëm dhe të qëndrueshëm.

---

