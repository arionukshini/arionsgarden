---
{"dg-publish":true,"permalink":"/semester-4/rrjeta/notes/"}
---

## Çka përmban fusha `Value` te DNS Resource Records?
Një DNS **Resource Record** përbëhet nga fushat: `Name`, `Value`, `Type` dhe `TTL`. Përmbajtja e fushës `Value` varet nga lloji i record-it.

| Type      | Çka përmban fusha **Value**?                               | Shembull i përgjithshëm          | Shembull me Google              |
| --------- | ---------------------------------------------------------- | -------------------------------- | ------------------------------- |
| **A**     | Adresën **IPv4** të hostit                                 | `example.com → 93.184.216.34`    | `google.com → 142.250.185.78`   |
| **NS**    | Emrin e serverit autoritativ DNS për domenin               | `example.com → ns1.example.com`  | `google.com → ns1.google.com`   |
| **CNAME** | Emrin kanonik të hostit drejt të cilit drejtohet një alias | `www.example.com → example.com`  | `alias.google.com → google.com` |
| **MX**    | Emrin e serverit që pranon email-et për domenin            | `example.com → mail.example.com` | `google.com → smtp.google.com`  |
Pra:
- **A → adresë IPv4**
- **NS → emri i DNS serverit autoritativ**
- **CNAME → emri kanonik i hostit**
- **MX → emri i mail serverit**
## Përshkruani se si punon “Trace route” programi?

Programi trace route dergon shume paketa te vecanta nga hosti burimor drejt nje hostname  
destinues. Duke kaluar rruges drejte destinacionit, paketat kalojn neper nje numer te router-ve.  
Kur nje router pranon nje nga keto paketa te vecanta, ai dergon tek burimi nje mesazh te shkurte  
qe permban emrin dhe adresen e routerit. Hosti i burimit te paketave regjistron kohen qe kalon  
nga fillimi i dergimit te paketave e deri te pranimi i mesazheve perkatese si dhe regjistron emrin  
dhe adresen e routerit qe kthen mesazhin. Ne kete form hosti burimor mund te konstruktoj rrugen e paketave nga burimi tek destinacioni, dhe vonesat e tyre.
![Pasted image 20260630141322.png](/img/user/Semester%204/Images/Pasted%20image%2020260630141322.png)