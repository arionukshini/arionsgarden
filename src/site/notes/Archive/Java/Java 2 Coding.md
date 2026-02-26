---
{"dg-publish":true,"permalink":"/archive/java/java-2-coding/"}
---

# Java OOP Complete Guide

Ky dokument përmban shembuj dhe teori mbi Java OOP:

- Klasat abstrakte
- Ndërfaqet
- Polimorfizmi
- Klonimi dhe krahasimi
- Trajtimi i gabimeve dhe përjashtimeve

---

## 1. Klasat Abstrakte

Një klasë abstrakte nuk mund të instancohet direkt. Ajo përdoret si bazë për nënklasa.

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
        System.out.println("Menaxheri: " + emri);
        System.out.println("Paga bazë: " + pagaBaze);
        System.out.println("Bonusi: " + bonus);
        System.out.println("Total paga: " + llogaritPagen());
    }
}

class Programeri extends Punetori {
    private int oreJashteOrarit;
    private double normaPageses;

    public Programeri(String emri, double pagaBaze, int oreJashteOrarit, double normaPageses) {
        super(emri, pagaBaze);
        this.oreJashteOrarit = oreJashteOrarit;
        this.normaPageses = normaPageses;
    }

    @Override
    public double llogaritPagen() {
        return pagaBaze + (oreJashteOrarit * normaPageses);
    }

    @Override
    public void shfaqInfo() {
        System.out.println("Programeri: " + emri);
        System.out.println("Paga bazë: " + pagaBaze);
        System.out.println("Overtime Hours: " + oreJashteOrarit);
        System.out.println("Hourly Rate: " + normaPageses);
        System.out.println("Total paga: " + llogaritPagen());
    }
}

public class Main {
    public static void main(String[] args) {
        Punetori menaxheri = new Menaxheri("Lis Mali", 3000, 1000);
        Punetori programeri = new Programeri("Lum Deti", 2000, 20, 25);

        menaxheri.shfaqInfo();
        System.out.println("---------------------");
        programeri.shfaqInfo();
    }
}
````

---

## 2. Ndërfaqet (Interfaces)

```java
interface StudentiInterface {
    String toFile();
}

class Studenti implements StudentiInterface {
    private int id;
    private String emri;
    private double notaMesatare;

    public Studenti(int id, String emri, double notaMesatare) {
        this.id = id;
        this.emri = emri;
        this.notaMesatare = notaMesatare;
    }

    @Override
    public String toFile() {
        return id + " " + emri + " " + notaMesatare;
    }
}
```

---

## 3. Polimorfizmi

### 3.1 Statik (Compile-time)

```java
class Printer {
    void print(int a) { System.out.println("Numri: " + a); }
    void print(String s) { System.out.println("Fjala: " + s); }
    void print(int a, String s) { System.out.println("Numri dhe fjala: " + a + ", " + s); }
}
```

### 3.2 Dinamik (Runtime)

```java
class ClassA { public String toString() { return "ClassA Object"; } }
class ClassB extends ClassA { public String toString() { return "ClassB Object"; } }
class ClassC extends ClassB { public String toString() { return "ClassC Object"; } }

public class MainPolimorfizmi {
    public static void main(String[] args) {
        ClassA a = new ClassA();
        ClassA b = new ClassB();
        ClassA c = new ClassC();

        System.out.println(a);
        System.out.println(b);
        System.out.println(c);
    }
}
```

---

## 4. Klonimi dhe Krahasimi

```java
class Provimi implements Cloneable, Comparable<Provimi> {
    String lenda;
    int nota;

    public Provimi(String lenda, int nota) {
        this.lenda = lenda;
        this.nota = nota;
    }

    @Override
    public Provimi clone() throws CloneNotSupportedException {
        return (Provimi) super.clone();
    }

    @Override
    public int compareTo(Provimi o) {
        return Integer.compare(this.nota, o.nota);
    }
}
```

---

## 5. Trajtimi i gabimeve

### 5.1 Përjashtim i personalizuar

```java
class joZanoreException extends Exception {
    public joZanoreException(String message) { super(message); }
}

public class KontrolloZanoret {
    public static void main(String[] args) {
        try {
            checkZanore("Bcd");
        } catch (joZanoreException e) {
            System.out.println("Gabim: " + e.getMessage());
        }
    }

    public static void checkZanore(String text) throws joZanoreException {
        String zanore = "aeiouAEIOU";
        for (int i = 0; i < text.length(); i++) {
            if (zanore.contains("" + text.charAt(i))) return;
        }
        throw new joZanoreException("Vargu nuk përmban asnjë zanore.");
    }
}
```

### 5.2 Kontroll për numra dublikatë

```java
class DuplicateNumberException extends Exception {
    public DuplicateNumberException(String message) { super(message); }
}

import java.util.*;

public class CheckDuplicate {
    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(1, 2, 3, 2);
        try {
            checkDuplicates(numbers);
        } catch (DuplicateNumberException e) {
            System.out.println("Gabim: " + e.getMessage());
        }
    }

    public static void checkDuplicates(List<Integer> numbers) throws DuplicateNumberException {
        Set<Integer> unique = new HashSet<>();
        for (int num : numbers) {
            if (!unique.add(num)) throw new DuplicateNumberException("Numër dublikatë: " + num);
        }
    }
}
```

---

## 6. Përfundim

- **Klasat abstrakte**: bazë logjike + metoda abstrakte
    
- **Ndërfaqet**: sjellje + implementim shumëfishtë
    
- **Polimorfizmi**: statik (compile-time), dinamik (runtime)
    
- **Klonimi dhe krahasimi**: `Cloneable`, `Comparable`
    
- **Përjashtimet**: `throw`, `try-catch`, klasat e përcaktuara nga përdoruesi
    