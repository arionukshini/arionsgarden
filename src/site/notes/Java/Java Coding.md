---
{"dg-publish":true,"permalink":"/java/java-coding/"}
---

# Java Coding – Notes & Examples

Ky file është për anën praktike të Java-s: shembuj, pattern-e dhe shpjegime rreth kodit.

---

## 1. Ciklet (Loops)

### 1.1 `for`

Përdoret kur e dimë paraprakisht sa herë do të përsëritet cikli.

```java
for (int i = 0; i < 10; i++) {
    // logic ...
    System.out.println("i = " + i);
}
```

- `int i = 0;` → inicializimi
    
- `i < 10;` → kushti, sa kohë është true cikli vazhdon
    
- `i++` → inkrementimi pas çdo iterimi
    

---

### 1.2 `while`

Përdoret kur duam të përsëritet diçka **derisa** një kusht të jetë i vërtetë.

```java
int i = 0;
while (i < 10) {
    System.out.println("i = " + i);
    i++;
}
```

- Nëse kushti është false në fillim, trupi i ciklit nuk ekzekutohet fare.
    

---

### 1.3 `do-while`

Përdoret kur duam që trupi i ciklit të ekzekutohet **të paktën një herë**, pavarësisht kushtit.

```java
int i = 0;
do {
    System.out.println("Test");
    i += 2;
} while (i < 0);
```

- Këtu trupi ekzekutohet një herë edhe pse `i < 0` është false në fillim.
    

---

## 2. Arrays dhe Matrica

### 2.1 Arrays (vargjet 1D)

```java
int[] vargu = new int[5];  // indekset 0–4
vargu[0] = 5;
vargu[1] = 10;
```

- `vargu.length` → gjatësia e vargut
    
- indeksi fillon nga 0
    

---

### 2.2 Matricat (vargje 2D)

```java
int[][] matrix = new int[5][5];
matrix[0][1] = 12;
```

- `matrix.length` → numri i rreshtave
    
- `matrix[0].length` → numri i kolonave të rreshtit të parë
    

---

## 3. Input me `Scanner`

`Scanner` përdoret për të lexuar nga tastiera (`System.in`).

```java
import java.util.Scanner;

Scanner scanner = new Scanner(System.in);

System.out.print("Shtyp numrin: ");
int numri1 = scanner.nextInt();
int numri2 = scanner.nextInt();
int numri3 = scanner.nextInt();

System.out.println("Numri1: " + numri1);
System.out.println("Numri2: " + numri2);
System.out.println("Numri3: " + numri3);
```

### 3.1 Metodat kryesore të `Scanner`

- `nextInt()` → lexon `int`
    
- `nextDouble()` → lexon `double`
    
- `nextBoolean()` → lexon `boolean`
    
- `next()` → lexon një fjalë (deri tek hapsira)
    
- `nextLine()` → lexon të gjithë rreshtin (deri tek enter)
    

### 3.2 Problemi me `nextInt()` dhe `nextLine()`

Kur përdor `nextInt()`, në buffer mbetet `\n` (enter). Nëse direkt pastaj thërret `nextLine()`, ajo e lexon vetëm enter-in.

Shembull zgjidhjeje:

```java
int numri = scanner.nextInt();
scanner.nextLine(); // konsumon \n

System.out.print("Shtyp emrin: ");
String emri = scanner.nextLine();
```

---

## 4. `Math.random()` dhe `Math` Utility

### 4.1 `Math.random()`

```java
double r = Math.random(); // 0.0 <= r < 1.0
System.out.println("Random: " + r);
```

### 4.2 Funksion random në interval [x, y]

```java
static int random(int x, int y) {
    double rand = x + Math.random() * (y - x);
    return (int) Math.round(rand);
}
```

- `Math.random() * (y - x)` → [0, y-x)
    
- `+ x` → [x, y)
    
- `Math.round()` → e afron në numër të plotë
    

### 4.3 Disa metoda të `Math`

```java
System.out.println("Min: " + Math.min(10, 5));   // 5
System.out.println("Max: " + Math.max(12, 15));  // 15
System.out.println("Round: " + Math.round(10.8)); // 11
System.out.println("Random: " + Math.random());
```

---

## 5. Strings

### 5.1 Literal vs objekt i ri

```java
String emri1 = "Filan";             // literal
String emri2 = new String("Filan"); // objekt i ri
String emri3 = "Filan";             // i njëjti literal si emri1
```

```java
System.out.println("Emri1 == Emri2: " + (emri1 == emri2));
System.out.println("Emri2 == Emri3: " + (emri2 == emri3));
System.out.println("Emri3 == Emri1: " + (emri3 == emri1));
```

- `==` krahas(in **referencat**)
    
- Strings duhen krahasuar me `.equals()`
    

### 5.2 `.equals()` vs `==`

```java
if (emri1.equals(emri2)) {
    // krahason përmbajtjen
}

if (emri1.equalsIgnoreCase(emri2)) {
    // krahason pa dallim shkronja të mëdha/vogla
}
```

### 5.3 Metodat kryesore të `String`

```java
emri1.charAt(0);
emri1.length();
char[] chars = emri1.toCharArray();
String emri4 = new String(chars);

emri1 = emri1.toLowerCase();
emri1 = emri1.toUpperCase();

emri1 = emri1.replace("Fil", "Nal");

String[] fjalet = "filan fisteku".split(" ");

"    filan    ".trim();

emri1.isEmpty();
emri1.isBlank();
```

---

## 6. `StringBuilder` dhe `StringBuffer`

### 6.1 `StringBuilder`

```java
StringBuilder sb = new StringBuilder("Filan");
sb.append(" Fisteku");
sb.insert(0, "FIEK - ");
sb.reverse();
sb.deleteCharAt(10);

System.out.println("SB: " + sb.toString());
```

### 6.2 Pse `StringBuilder` është më i shpejtë se `String`

```java
String numbers = "";
StringBuilder sbNumbers = new StringBuilder("");

long start = System.currentTimeMillis();
for (int i = 0; i < 1000000; i++) {
    numbers += i;
}
long end = System.currentTimeMillis();
System.out.println("String time: " + (end - start));

start = System.currentTimeMillis();
for (int i = 0; i < 1000000; i++) {
    sbNumbers.append(i);
}
end = System.currentTimeMillis();
System.out.println("StringBuilder time: " + (end - start));
```

### 6.3 `StringBuffer`

- E ngjashme me `StringBuilder`, por **thread-safe**
    
- Më e ngadaltë
    

---

## 7. Koleksionet – `ArrayList`, `HashSet`, `HashMap`

### 7.1 `ArrayList`

````java
import java.util.ArrayList;

ArrayList<Integer> numrat = new ArrayList<>();

num


---

### (Vazhdim) 7.1 `ArrayList`

```java
numrat.add(10);
numrat.add(5);
numrat.add(8);

Integer numberToRemove = 10;
numrat.remove(numberToRemove); // fshin me vlerë
numrat.remove(0);              // fshin me indeks
numrat.add(0, 10);             // shton 10 në pozicionin 0
````

#### Metoda të tjera të dobishme

```java
numrat.removeAll(numrat2);
numrat.indexOf(55);

numrat.get(numrat.size() - 1); // last
numrat.get(0);                 // first
numrat.get(1);                 // numrat[i]
numrat.contains(10);
numrat.containsAll(numrat2);
numrat.size();
```

> **Shënim:** `ArrayList` NUK ka `getFirst()` ose `getLast()` (janë në `LinkedList`).

---

### 7.2 `HashSet`

```java
import java.util.HashSet;

HashSet<String> emrat = new HashSet<>();

emrat.add("Filan");
emrat.add("Fisteku");
emrat.add("Filan"); // injorohet

System.out.println(emrat.contains("Filan"));

emrat.remove("Filan");
System.out.println(emrat.size());
```

- Nuk lejon duplikate
    
- Shumë i shpejtë për kërkime
    
- S’ruan rendin
    

---

### 7.3 `HashMap`

```java
import java.util.HashMap;

HashMap<String, Integer> notat = new HashMap<>();

notat.put("Filan", 10);
notat.put("Fisteku", 9);

System.out.println(notat.get("Filan"));

if (notat.containsKey("Fisteku")) {
    System.out.println("E gjetëm Fistekun");
}

notat.remove("Filan");
```

### Iterimi

```java
for (String key : notat.keySet()) {
    System.out.println(key + " → " + notat.get(key));
}

for (var entry : notat.entrySet()) {
    System.out.println(entry.getKey() + " → " + entry.getValue());
}
```

---

## 8. `static`, `final`, `abstract` në klasa

### 8.1 `static`

- I përket klasës, jo objektit.
    
- Shpërndahet mes të gjitha objekteve.
    

```java
class Student {
    static String uuid = "UUID001";

    String id;
    String fakulteti;

    Student(String id, String fakulteti) {
        this.id = id;
        this.fakulteti = fakulteti;
    }

    void shtypDetajet() {
        System.out.println("UUID: " + Student.uuid);
        System.out.println("Id: " + this.id);
        System.out.println("Fakulteti: " + this.fakulteti);
    }
}
```

Ndryshimi i static prek të gjitha instancat:

```java
Student.uuid = "UUID6";
```

---

### 8.2 `final`

- **final field** → nuk ndryshohet pasi caktohet
    
- **final method** → nuk mund të override-het
    
- **final class** → nuk mund të trashëgohet
    

```java
final class Student {}
class Teacher {} // OK

class A {
    final void metoda() {}
}

class B extends A {
    // metoda() nuk mund të override-het
}
```

---

### 8.3 `abstract`

- Klasa abstrakte nuk krijon objekte
    
- Mund të ketë metoda normale + metoda abstrakte
    

```java
abstract class Punetor {
    abstract void puno();

    void info() {
        System.out.println("Info për punëtorin");
    }
}

class Profesor extends Punetor {
    @Override
    void puno() {
        System.out.println("Profesor duke ligjëruar...");
    }
}
```

---

## 9. `@Override`

```java
class Kafsha {
    void benZhurme() { System.out.println("Kafsha bën zhurmë"); }
}

class Qeni extends Kafsha {
    @Override
    void benZhurme() { System.out.println("Ham ham!"); }
}
```

- Kontrollon që metoda e prindit ekziston
    
- Parandalon gabime në emër (p.sh. `benZhurmee`)
    
- Nuk është vetëm dekorativ – bën kontroll real
    

---

## 10. `return` brenda metodave

Përdoret për të ndalur ekzekutimin e metodës:

```java
public void setName(String name) {
    if (name.length() < 7 || name.split(" ").length != 2) {
        System.out.printf("New name '%s' is not valid!
", name);
        return;
    }
    this.name = name;
}
```

---

## 11. Përmbledhje e Shpejtë

- **Loops** → `for`, `while`, `do-while`
    
- **Arrays/Matrices** → `int[]`, `int[][]`
    
- **Scanner** → input dhe problemi i `nextLine()`
    
- **Math** → random, round, min/max
    
- **Strings** → equals, replace, split, trim
    
- **StringBuilder** → concatenim efikas
    
- **ArrayList** → lista dinamike
    
- **HashSet** → vlera unike
    
- **HashMap** → key-value
    
- **static** → veti e klasës
    
- **final** → nuk ndryshohet / nuk trashëgohet
    
- **abstract** → modele të përgjithshme për klasat
    
- **@Override** → siguron override korrekt
    

---