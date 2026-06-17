---
{"dg-publish":true,"permalink":"/semester-4/siguri/notes/"}
---

# RSA

![Pasted image 20260617201122.png](/img/user/Pasted%20image%2020260617201122.png)

# C# RSA

|Sintaksa|Çfarë eksporton/importon?|A përmban çelës privat?|Përdorimi|
|---|---|--:|---|
|`rsa.ExportParameters(false)`|Vetëm çelësin publik|❌ Jo|Për t’ia dërguar dikujt tjetër|
|`rsa.ExportParameters(true)`|Çelësin publik + privat|✅ Po|Backup ose bartje e krejt çelësit|
|`rsa.ImportParameters(key)`|Importon parametrat e çelësit|Varet nga `key`|Fut çelësin në një objekt RSA|

# Smart Card

| Kodi hexadecimal | Kuptimi                                               |
| ---------------- | ----------------------------------------------------- |
| **`90 00`**      | ✅ Komanda u krye me sukses                            |
| **`61 XX`**      | Ka edhe `XX` byte të dhëna për t’u marrë              |
| **`62 00`**      | ⚠️ Paralajmërim; gjendja e kartës nuk ka ndryshuar    |
| **`67 00`**      | Gjatësia e të dhënave është gabim                     |
| **`69 82`**      | Kushti i sigurisë nuk është plotësuar                 |
| **`69 83`**      | Metoda e autentikimit është bllokuar                  |
| **`69 85`**      | Kushtet për ekzekutimin e komandës nuk janë plotësuar |
| **`69 86`**      | Komanda nuk lejohet                                   |
| **`6A 80`**      | Të dhënat janë gabim                                  |
| **`6A 81`**      | Funksioni nuk mbështetet                              |
| **`6A 82`**      | File nuk u gjet                                       |
| **`6A 83`**      | Record nuk u gjet                                     |
| **`6A 84`**      | Nuk ka hapësirë të mjaftueshme                        |
| **`6A 86`**      | Parametrat `P1` dhe `P2` janë gabim                   |
| **`6B 00`**      | Parametrat `P1/P2` janë gabim                         |
| **`6C XX`**      | Gjatësia e saktë që duhet përdorur është `XX`         |
| **`6D 00`**      | Instruksioni `INS` nuk mbështetet                     |
| **`6E 00`**      | Klasa `CLA` nuk mbështetet                            |
| **`6F 00`**      | Gabim i panjohur / pa diagnozë të saktë               |

**90 00 = SUCCESS**
**67 00 = WRONG LENGTH**
**69 82 = SECURITY ERROR**
**6A 82 = FILE NOT FOUND**
**6A 86 = WRONG P1/P2**
**6D 00 = INS NOT SUPPORTED**
**6E 00 = CLA NOT SUPPORTED**
**6F 00 = UNKNOWN ERROR**

