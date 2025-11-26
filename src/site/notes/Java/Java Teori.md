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