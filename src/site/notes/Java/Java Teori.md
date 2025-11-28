---
{"dg-publish":true,"permalink":"/java/java-teori/"}
---

# Modifiers në Java – Përmbledhje

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

|Përshkrimi|Escape seq.|Unicode|
|---|---|---|
|Backspace|``|``|
|Tab|||
|Linefeed (New line)|`||
|`|`||
|`|||
|Carriage return|`||
|`|`||
|`|||
|Escape|`\`|`\`|

## ✔️ Shembuj

```java
char tab = '	';
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