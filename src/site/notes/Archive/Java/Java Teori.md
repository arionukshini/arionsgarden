---
{"dg-publish":true,"permalink":"/archive/java/java-teori/"}
---

# Modifiers në Java – Përmbledhje

## Qysh more pi lexon pa pagu

Java përdor disa **modifikues (modifiers)** që ndryshojnë sjelljen e klasave, metodave dhe variablave. Ndahen në **access modifiers** dhe **non-access modifiers**.

---

## 🟦 Access Modifiers

### **1. public**

- I qasshëm nga çdo klasë dhe çdo paketë.
- Përdoret kur diçka duhet të jetë publike dhe e përdorshme kudo.

### **2. private**

- I qasshëm vetëm brenda të njëjtës klasë.
- Përdoret për fshehje të të dhënave (encapsulation).

### **3. protected**

- I qasshëm brenda paketës dhe në subklasa (edhe në paketa të tjera).
- Përdoret zakonisht për trashëgimi.

---

## 🟩 Non-Access Modifiers

### **4. static**

- I përket klasës, jo instancës.
- Mund të thirret pa krijuar objekt.

### **5. final**

- Bën diçka të pandryshueshme.
- Për variabla → vlera nuk ndryshohet.
- Për metoda → nuk mund të override-ohen.
- Për klasa → nuk mund të trashëgohen.

### **6. abstract**

- Klasa abstrakte → nuk mund të krijojmë objekt prej saj.
- Metoda abstrakte → pa trup (body) dhe duhet implementuar në subklasa.

---

## 📌 Tabelë Përmbledhëse

|Modifier|Ku përdoret|Përshkrimi|
|---|---|---|
|**public**|class, method, variable|Qasje kudo|
|**private**|method, variable|Qasje vetëm në klasë|
|**protected**|method, variable|Qasje në paketë + subklasa|
|**static**|method, variable|I përket klasës|
|**final**|class, method, variable|Nuk ndryshohet / nuk trashëgohet / nuk override-ohet|
|**abstract**|class, method|Klasë pa objekt, metodë pa body|

---

# Identifikatorët në Java

Identifikatorët janë **emrat** që u japim:

- variablave
- metodave
- klasave
- paketave
- ndërfaqeve (interfaces)

## ✔️ Rregullat për identifikatorët

- **Nuk mund të fillojë me numër.**
    Shembull i gabuar: `1name`
- **Nuk mund të jetë fjalë e rezervuar.**
    Shembull: `class`, `public`, `static`, etj.
- **Nuk mund të jetë:** `true`, `false`, `null`
- **Mund të ketë gjatësi të pakufizuar.**
    Nuk ka limit sa i gjatë mund të jetë një emër.
- **Lejohet të fillojë me shkronjë ose _ ose $.**
    Shembull i saktë: `_name`, `$value`, `emri1`
- **Java është case-sensitive.**
    `Name`, `name`, dhe `NAME` janë identifikatorë të ndryshëm.

---

# Tipi i të dhënave **char** në Java

Tipi **char** ruan **një karakter të vetëm**. Mund të jetë:

- shkronjë (`'A'`)
- numër si karakter (`'4'`)
- vlerë ASCII
- vlerë Unicode

## ✔️ Shembuj

```java
char shkronj = 'A';
char numChar = '4';         // ASCII
char shkronjUnicode = 'A'; // Unicode për 'A'
char numCharUnicode = '4'; // Unicode për '4'
```

---

# Karakteret Speciale në Java

Java lejon karaktere të veçanta (escape characters). Këto përdoren në stringje dhe char.

## ✔️ Lista e karaktereve speciale

| Përshkrimi          | Escape seq. | Unicode |
| ------------------- | ----------- | ------- |
| Backspace           | `\b`        | `\u0008` |
| Tab                 | `\t`        | `\u0009` |
| Linefeed (New line) | `\n`        | `\u000A` |
| Carriage return     | `\r`        | `\u000D` |
| Escape              | `\\`        | `\u005C` |

## ✔️ Shembuj

```java
char tab = '\t';
```

---

# Llojet e Metodave në Java

## ✔️ Metodat Void

- Nuk kthejnë asnjë vlerë.
- Shembull:

```java
void printoPershendetje() {}
```

## ✔️ Metodat Return

- Kthejnë një vlerë.
- Shembull:

```java
int shto(int a, int b) { return a + b; }
```

## ✔️ Metodat Static

- I përkasin klasës.
- Thirren me emrin e klasës.
- Shembull:

```java
static double sqrt(double x) { return x*x; }
```

## ✔️ Metodat e Instancës

- I përkasin një objekti.
- Shembull:
```java
obj.shto(5,3);
```

---
# Metodat e Klasës

Metodat e klasës janë funksione që i përkasin vetë klasës. Ato mund të jenë:

- **statike** (të lidhura me klasën)
- **jo statike** (të lidhura me objektin)

## Tabelë përmbledhëse

|Lloji i metodës|I përket|Si thirret|Shembull|
|---|---|---|---|
|Statike (static)|Klasës|Me emrin e klasës|`Math.sqrt(16)`|
|Instancë|Objektit|Përmes objektit|`obj.shto(5,8)`|

---
# Metodat Statike

- Kanë fjalën **static**.
- Mund të thirren pa krijuar objekt.
- I përkasin klasës, jo instancës.
- Shembull:

```java
public class Matematika {
    public static int shto(int a, int b) {
        return a + b;
    }
}

int rezultati = Matematika.shto(5, 3);
```

---
# Metodat e Instancës (Jo Statike)

- I përkasin një objekti.
- Duhet krijuar objekt për t’i thirrur.
- Shembull:

```java
public class Person {
    String emri;
    public void pershendetje() {
        System.out.println("Përshëndetje, unë jam " + emri);
    }
}

Person p1 = new Person();
p1.emri = "Lumi";
p1.pershendetje();
```

---

# Metodat Statike dhe Jo Statike në të Njëjtën Klasë

```java
public class Student {
    String emri;

    public void printoInfo() {
        System.out.println("Emri i studentit: " + emri);
    }

    public static void pershendetje() {
        System.out.println("Përshëndetje nga klasa Student!");
    }
}
```

---

# Metodat e Mbingarkuara (Method Overloading)

- Janë metoda me **të njëjtin emër**, por me **parametra të ndryshëm**.
- Dallohen sipas **nënshkrimit të metodës** (emri + parametrat).

## Shembull

```java
public class Kalkulatori {
    public int shto(int a, int b) { return a + b; }
    public int shto(int a, int b, int c) { return a + b + c; }
    public double shto(double a, double b) { return a + b; }
}
```

## Kur ndodh / nuk ndodh Overloading

- ✔️ Ndodh kur ndryshojnë parametrat.
- ❌ Nuk ndodh vetëm duke ndryshuar:
    - tipin e vlerës së kthyer
    - modifikuesit e qasjes

---

# Metodat Abstrakte

- Janë metoda pa trup (pa implementim).
- Mund të përkufizohen vetëm në **klasa abstrakte**.
- Duhet të implementohen nga klasat që trashëgojnë.

## Shembull

```java
abstract class Kafsha {
    abstract void benZhurme();
    void hec() { System.out.println("Kafsha po hec..."); }
}
```

---
# Implementimi i Metodave Abstrakte

```java
abstract class Kafsha { abstract void benZhurme(); }

class Qeni extends Kafsha {
    void benZhurme() { System.out.println("Ham ham!"); }
}

class Macja extends Kafsha {
    void benZhurme() { System.out.println("Mjaaaau!"); }
}
```

---

# Klasa Math

## Vlera konstante

- `Math.PI`
- `Math.E`

## Metodat kryesore

- Metoda trigonometrike
- Metoda eksponenciale
- Metoda logaritmike
- `min`, `max`, `abs`, `random`

---

# Metoda random()

- Jep një vlerë `double` **>= 0.0 dhe < 1.0**.

### Shembuj

```java
(int)(Math.random() * 10)          // 0 deri 9
50 + (int)(Math.random() * 50)     // 50 deri 99
a + Math.random() * b              // [a , a+b)
```

---

# Benefitet e Metodave

- Shkruhet një herë, përdoret kudo (reusability).
- Fsheh zbatimin (encapsulation).
- Ul kompleksitetin.

---

# Klasat dhe Objektet

Programimi i orientuar në objekte (POO/OOP) bazohet te konceptet e **klasave** dhe **objekteve**. Një objekt përfaqëson një njësi reale me gjendje (atribute) dhe sjellje (metoda). Një klasë është modeli (template) prej të cilit krijohen objektet.

- Objektet shkëmbejnë mesazhe dhe bashkëveprojnë në një program.
- Java është e dizajnuar si gjuhë plotësisht objekt-orientuar, duke thjeshtuar punën me objekte.
- Objektet kanë:
    - **Gjendje** – të dhëna, atributet (p.sh. ngjyra, madhësia e një veture)
    - **Sjellje** – metodat (p.sh. si lëviz makina)

---

# Shtyllat e Programimit të Orientuar në Objekte

Programimi i orientuar në objekte (OOP) mbështetet në **katër shtylla** themelore. Kuptimi i tyre i thellë është thelbësor për krijimin e aplikacioneve të sigurta, të mirëstrukturuara dhe të qëndrueshme.

Katër shtyllat kryesore të OOP janë:

1. **Abstraksioni (Abstraction)**
2. **Enkapsulimi (Encapsulation)**
3. **Trashëgimia (Inheritance)**
4. **Polimorfizmi (Polymorphism)**

---

# 1️⃣ Abstraksioni (Abstraction)

Abstraksioni përqendrohet në **tregimin e vetëm informatave të nevojshme**, duke fshehur detajet e brendshme të funksionimit.
Qëllimi i tij është **ulja e kompleksitetit** dhe krijimi i modeleve të qarta të objekteve.

### ✔️ Si realizohet abstraksioni

- Përmes **klasave abstrakte**
- Përmes **metodave abstrakte**
- Përmes **interface-ve**

### ✔️ Shembull me klasë abstrakte

```java
abstract class Pajisja {
    abstract void ndizet();  // metodë abstrakte

    void info() {            // metodë konkrete
        System.out.println("Pajisje elektronike");
    }
}

class Laptop extends Pajisja {
    void ndizet() {
        System.out.println("Laptopi u ndez...");
    }
}
```

### ✔️ Shembull me interface

```java
interface Transport {
    void leviz();
}

class Bicikleta implements Transport {
    public void leviz() {
        System.out.println("Bicikleta po lëviz");
    }
}
```

### ✔️ Pse përdoret abstraksioni

- Fsheh detaje të panevojshme
- Lehtëson zhvillimin
- Lejon modele të qarta për klasat
- Redukton kompleksitetin e kodit

---

# 2️⃣ Enkapsulimi (Encapsulation)

Enkapsulimi lidhet me **fshehjen e të dhënave** dhe kontrollimin e qasjes përmes metodave të posaçme.

Ky koncept përdor:

- **private** për variablat
- **public getters/setters** për qasje

### ✔️ Shembull

```java
class LlogariaBankare {
    private double bilanci;

    public void depozito(double shuma) {
        bilanci += shuma;
    }

    public double getBilanci() {
        return bilanci;
    }
}
```

### ✔️ Përfitimet e enkapsulimit

- Rrit sigurinë
- Parandalon qasjen e paautorizuar
- Kontrollon mënyrën e modifikimit të të dhënave
- Lehtëson mirëmbajtjen e kodit

---

# 3️⃣ Trashëgimia (Inheritance)

Trashëgimia mundëson krijimin e klasave të reja duke përdorur funksionalitetin e klasave ekzistuese.

### ✔️ Termat kryesorë

- **Superclass** → klasa prind
- **Subclass** → klasa fëmijë
- **extends** → fjala kyçe për trashëgim në Java

### ✔️ Shembull bazik

```java
class Kafsha {
    void ha() { System.out.println("Kafsha po ha"); }
}

class Qeni extends Kafsha {
    void leh() { System.out.println("Ham ham!"); }
}

Qeni q = new Qeni();
q.ha();  // trashëguar
q.leh(); // e klasës Qeni
```

### ✔️ Llojet e trashëgimisë në Java

Java **NUK** lejon trashëgimi të shumëfishtë të klasave (multiple inheritance), por lejon të interface-ve.

Llojet:

1. **Single inheritance** — një subclass trashëgon një superclass
2. **Multilevel inheritance** — një zinxhir trashëgimor
3. **Hierarchical inheritance** — një superclass ka disa subclass
4. **Multiple inheritance (vetëm me interfaces)**

### ✔️ Shembull Multilevel

```java
class A { void metodaA(){} }
class B extends A { void metodaB(){} }
class C extends B { void metodaC(){} }
```

---

# 4️⃣ Polimorfizmi (Polymorphism)

Polimorfizmi lejon që **e njëjta metodë të sillet ndryshe**, varësisht nga objekti që e thërret.

Dy lloje kryesore:

- **Polimorfizmi statik** (Compile-time) → Method Overloading
- **Polimorfizmi dinamik** (Run-time) → Method Overriding

---

## ✔️ Polimorfizmi statik – Method Overloading

Metoda ka të njëjtin emër por parametra të ndryshëm.

```java
class Kalkulator {
    int shto(int a, int b) { return a + b; }
    double shto(double a, double b) { return a + b; }
}
```

---

## ✔️ Polimorfizmi dinamik – Method Overriding

Metoda rishkruhet në subclass.

```java
class Kafsha {
    void benZhurme() { System.out.println("Kafsha bën zhurmë"); }
}
class Qeni extends Kafsha {
    @Override
    void benZhurme() { System.out.println("Ham ham!"); }
}

Kafsha k = new Qeni();
k.benZhurme();  // Ham ham!
```

### ✔️ Përfitimet e polimorfizmit

- Kod më i pastër dhe fleksibil
- Mbështet zëvendësimin e objekteve
- Zbaton konceptin "one interface, many implementations"

---

# ✔️ Përmbledhje Vizuale e 4 Shtyllave të OOP

|Shtylla|Qëllimi|Realizohet me|Shembull|
|---|---|---|---|
|**Abstraksioni**|Fsheh detajet|Abstract classes, interfaces|`abstract void metoda();`|
|**Enkapsulimi**|Mbron të dhënat|private + getters/setters|`private int x;`|
|**Trashëgimia**|Ripërdorim kodi|extends|`class B extends A`|
|**Polimorfizmi**|Sjellje të ndryshme|Overloading, Overriding|`@Override`|

---

në Objekte
Katër shtyllat kryesore të OOP janë:

1. **Abstraksioni**
2. **Enkapsulimi**
3. **Trashëgimia (Inheritance)**
4. **Polimorfizmi (Polymorphism)**

Këto shtylla janë thelbësore për ndërtimin e sistemeve stabile dhe të mirëorganizuar.

---

## 1️⃣ Abstraksioni

Abstraksioni paraqet vetëm informacionin e nevojshëm dhe fsheh detajet e panevojshme.

- Ul kompleksitetin.
- Përqendrohet në **çfarë bën** objekti, jo **si e bën**.
- Realizohet përmes:
    - **klasave abstrakte**
    - **metodave abstrakte**

Shembull i abstraksionit: një makinë ka pedale, por nuk e dimë implementimin e brendshëm të motorit.

---

## 2️⃣ Enkapsulimi

Enkapsulimi është procesi i mbajtjes së të dhënave dhe metodave brenda një njësie të vetme (klasa) dhe fshehja e tyre nga qasja e jashtme.

- Arrihet përmes **private fields** dhe **public getters/setters**.
- Rrit sigurinë.
- Kontrollon qasjen.
- Ul mundësinë e gabimeve.

```java
private int mosha;
public int getMosha() { return mosha; }
public void setMosha(int m) { mosha = m; }
```

---

## 3️⃣ Trashëgimia

Trashëgimia lejon një klasë të marrë atributet dhe metodat e një klase tjetër.

- Klasa prind → **superclass**
- Klasa fëmijë → **subclass**

Përfitimet:

- Ripërdorim i kodit
- Ndërtim i hierarkive
- Organizim më i mirë i strukturës

Shembull:

```java
class Kafsha {}
class Qeni extends Kafsha {}
```

---

## 4️⃣ Polimorfizmi

Polimorfizmi lejon një metodë të sjellë veprime të ndryshme varësisht objektit.

Dy lloje:

- **Polimorfizmi statik** (compile-time) → Method Overloading
- **Polimorfizmi dinamik** (run-time) → Method Overriding

Shembull i polimorfizmit dinamik:

```java
Kafsha k = new Qeni();
k.benZhurme();
```

---

# Informacione shtesë të rëndësishme që duhen ditur

## ✔️ Klasa vs Objekt

- **Klasa** = dizajni i objektit
- **Objekti** = instance reale e klasës

## ✔️ Konstruktorët

- Metoda speciale që inicializon objektin.
- Ka të njëjtin emër si klasa.
- Mund të jetë i mbingarkuar.

```java
class Person {
    Person() {}
    Person(String emri) {}
}
```

## ✔️ This keyword

Përdoret për të referuar instancën aktuale.

```java
this.emri = emri;
```

## ✔️ Super keyword

Përdoret për të thirrur konstruktorin ose metodat e superklasës.

```java
super();
super.metoda();
```

## ✔️ Fushat statike dhe jo statike

- **Static** → i përket klasës
- **Non-static** → i përket objektit

## ✔️ Heap dhe Stack në Java

- **Heap** → ku ruhen objektet
- **Stack** → ku ruhen variablat lokale + thirrjet e metodave

## ✔️ Referencat e objekteve

```java
Person p1 = new Person();
Person p2 = p1;  // p2 referon të njëjtin objekt
```

## ✔️ Garbage Collection

Java automatikisht largon objektet e pareferencuara.

## ✔️ Access Modifiers dhe Qasja në OOP

Këto janë thelbësore në dizajnin e klasave:

- public
- private
- protected
- default (pa modifier)

## ✔️ Composition vs Inheritance

- **Inheritance** = “is-a” (Qeni është Kafshë)
- **Composition** = “has-a” (Makina ka motor)

## ✔️ Encapsulation vs Abstraction

- Encapsulation fsheh _si_ ruhen të dhënat.
- Abstraction fsheh _detajet e panevojshme_.

---

# Përmbledhje e kapitullit

OOP në Java bazohet në:

- përdorimin e **klasave** dhe **objekteve**
- aplikimin e **4 shtyllave** të OOP
- krijimin e hierarkive të qarta
- ndarjen e përgjegjësive
- ripërdorimin e kodit
- rritjen e sigurisë dhe modularitetit
