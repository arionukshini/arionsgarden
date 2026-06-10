---
{"dg-publish":true,"permalink":"/archive/java/java-2-teori-2/"}
---

# Java OOP – Advanced Topics (Syllabus 10–15)

## Java 10: Abstraksioni – Klasat Abstrakte dhe Interface-at

### Polimorfizmi
Polimorfizmi na mundëson që një variabël e super-klasës të mund të ndryshoj tipin në njërën nga nënklasat që e trashëgojnë super klasën.

#### Polimorfizmi statik
Polimorfizmi statik (i quajtur edhe polimorfizëm në kohën e kompilimit) ndodh kur një metodë e një klase mund të ketë shumë forma, por vendimi për cilën metodë do të përdoret bëhet gjatë kompilimit, para se programi të ekzekutohet. Lidhet kryesisht me mbingarkimin e metodës (method overloading) dhe operatorëve (operator overloading).

```java
class PolimorfizmiStatik {
    public void print(int a) {
        System.out.println("Numri i dhënë është: " + a);
    }
    public void print(String a) {
        System.out.println("Fjala e dhënë është: " + a);
    }
    public void print(int a, String b) {
        System.out.println("Numri dhe fjala: " + a + ", " + b);
    }
}
```

**Karakteristikat:**

* Vendimi bëhet gjatë kompilimit.
* Metoda që do të thirret përcaktohet nga parametra.
* Nuk mund të përdoret objekti për zgjedhjen e metodave gjatë ekzekutimit.

#### Polimorfizmi dinamik

Polimorfizmi dinamik ndodh në kohën e ekzekutimit dhe lidhet me mbishkrimin e metodës (method overriding). JVM vendos se cila metodë do të ekzekutohet në mënyrë dinamike gjatë ekzekutimit.

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Polimorfizmi dinamik:");
        shtypDetajet(new ClassA());
        shtypDetajet(new ClassB());
        shtypDetajet(new ClassC());
    }

    public static void shtypDetajet(Object o) {
        System.out.println("Detajet: " + o.toString());
    }
}

class ClassA extends Object {
    @Override
    public String toString() { return "ClassA Object"; }
}
class ClassB extends ClassA {
    @Override
    public String toString() { return "ClassB Object"; }
}
class ClassC extends ClassB {
    @Override
    public String toString() { return "ClassC Object"; }
}
```

**Dallimi midis polimorfizmit statik dhe dinamik:**

* Statik: vendoset gjatë kompilimit, lidhet me mbingarkimin e metodës.
* Dinamik: vendoset gjatë ekzekutimit, lidhet me mbishkrimin e metodës dhe referencën e klasës bazë.

---

### Klasat Abstrakte

* Një klasë abstrakte nuk mund të instancohet drejtpërdrejt.
* Mund të ketë metoda abstrakte dhe konkrete.
* Përdoret si bazë për nënklasa.

```java
abstract class Profesor {
    int id;
    String emri;

    Profesor(int id, String emri){
        this.id = id;
        this.emri = emri;
    }

    public void shtypDetajet() {
        System.out.println("Id: " + this.id);
    }
}
```

#### Metodat abstrakte

* Nuk mund të përfshihen në klasë jo-abstrakte.
* Nënklasa jo-abstrakte duhet t'i implementojë të gjitha metodat abstrakte.

#### Klasa abstrakte si tip

* Nuk mund të krijoni instanca me `new`.
* Mund të përdoret si tip për variabla.

#### Shembull – Punetori, Menaxheri, Programeri

```java
abstract class Punetori {
    protected String emri;
    protected double pagaBaze;

    public Punetori(String emri, double pagaBaze) {
        this.emri = emri;
        this.pagaBaze = pagaBaze;
    }

    public abstract double llogaritPagen();
    public abstract void shfaqInfo();
}

class Menaxheri extends Punetori {
    private double bonus;

    public Menaxheri(String emri, double pagaBaze, double bonus) {
        super(emri, pagaBaze);
        this.bonus = bonus;
    }

    @Override
    public double llogaritPagen() {
        return pagaBaze + bonus;
    }

    @Override
    public void shfaqInfo() {
        System.out.println("Menaxheri Emri: " + emri);
        System.out.println("Paga bazë: €" + pagaBaze);
        System.out.println("Bonusi: €" + bonus);
        System.out.println("Total paga: €" + llogaritPagen());
    }
}

class Programeri extends Punetori {
    private int orejashteOrarit;
    private double normaPageses;

    public Programeri(String emri, double pagaBaze, int orejashteOrarit, double normaPageses) {
        super(emri, pagaBaze);
        this.orejashteOrarit = orejashteOrarit;
        this.normaPageses = normaPageses;
    }

    @Override
    public double llogaritPagen() {
        return pagaBaze + (orejashteOrarit * normaPageses);
    }

    @Override
    public void shfaqInfo() {
        System.out.println("Programeri Emri: " + emri);
        System.out.println("Paga bazë: €" + pagaBaze);
        System.out.println("Overtime Hours: " + orejashteOrarit);
        System.out.println("Hourly Rate: €" + normaPageses);
        System.out.println("Total paga: €" + llogaritPagen());
    }
}

public class Main {
    public static void main(String[] args) {
        Punetori m = new Menaxheri("Lis Mali", 3000, 1000);
        Punetori p = new Programeri("Lum Deti", 2000, 20, 25.0);

        m.shfaqInfo();
        System.out.println("---------------------");
        p.shfaqInfo();
    }
}
```

---

### Ndërfaqet (Interfaces)

* Përcaktojnë **çfarë** duhet të bëjë një klasë, jo **si** ta bëjë.
* Mund të implementohen shumëfishtë.
* Të gjitha fushat janë `public static final`.
* Të gjitha metodat janë `public abstract`.

```java
public interface Krahasueshmeria {
    int compareTo(Object o);
}
```

#### Shembull – Comparable dhe Cloneable

```java
class Fakulteti implements Comparable<Fakulteti> {
    public int id;
    private String emri;

    Fakulteti(int id, String emri){
        this.id = id;
        this.emri = emri;
    }

    @Override
    public int compareTo(Fakulteti o) {
        if(this.id != o.id) return -1;
        if(!this.emri.equals(o.emri)) return -1;
        return 0;
    }
}

class Universiteti implements Cloneable {
    public int uniId;

    Universiteti(int uniId) { this.uniId = uniId; }

    public Universiteti cloneObj() throws CloneNotSupportedException {
        return (Universiteti) this.clone();
    }
}
```

**Gabimet dhe Përjashtimet:**

* **Syntax errors** – zbulohen nga kompaileri.
* **Runtime errors** – ndodhin gjatë ekzekutimit (p.sh. `ArithmeticException`).
* **Logical errors** – nuk japin rezultatin e duhur.

**Shembull me try-catch:**

```java
public class Main {
    public static void main(String[] args) {
        shtypHeresin(10, 0);
    }

    public static void shtypHeresin(int num1, int num2) {
        try {
            System.out.println("Herësi: " + (num1 / num2));
        } catch(ArithmeticException e) {
            System.out.println("Nuk mund të pjesëtoni me zero. Vazhdon ekzekutimi...");
        }
    }
}
```

#### File I/O

* Përdorimi i `File` për vetitë e fajllit.
* `Scanner` për lexim.
* `FileWriter` për shkrim.

```java
File file = new File("resource/file.txt");
Scanner input = new Scanner(file);
while(input.hasNext()) {
    System.out.println(input.nextLine());
}
input.close();
```

```java
FileWriter fw = new FileWriter("log.txt", true);
fw.write("Log message\n");
fw.close();
```

---

### Përmbledhje

* Polimorfizmi, klasat abstrakte dhe ndërfaqet janë gurët bazë të OOP.
* Trajtimi i gabimeve dhe përjashtimeve rrit sigurinë dhe stabilitetin e programeve.
* `Comparable` dhe `Cloneable` ndihmojnë në krahasimin dhe kopjimin e objekteve.
* File I/O lejon ndërveprimin me të dhëna të jashtme.
