---
{"dg-publish":true,"permalink":"/semester-4/knk/"}
---

E kishim bo edhe per admin edhe per user, sikur a di qka na bojke arbena sot, o po e poshter.

# Tina:

1. Kur behet register, hash passwordin me salt, dmth salted hash.
2. Ne reset password dhe confirm password, te krahasohet me salt.
3. Nese munesh me shfaq passwordin te account, normal kur eshte hash nuk munesh kshtuqe ska problem qe jo
4. Qasja si user dhe admin, qita duhet me fol edhe niher se **shm.** nese jan dy persona me emer te njejt qysh mi marr prej databazes, nashta duhet mja bo secilit puntor nje username special.

# Arion:

1. Permisimi i departamentit, nuk shfaq lokacionin por lloj departamenti ✅
2. **Kontrata:** sa kontrata jan aktive, te skaduara, ne pritje
3. ErrorHandling

# Arijola

1. Krijon view per tabelat e tjera te databazes, pra si punetoret, por tash per pagat, kontratat etj.
2. Shton opsionin per me shtu, fshi, perditesu databazen prej programit (si punetoret)
3. Lidh tabelat me keys (primary/foreign), qe **shm.** tek kontratat permes emplyeeid mu shfaq emri mbiemri i punetorit

# Arjanite punetorja

1. Opsionin per logout ne hamburger menu
2. Propmpt per exit te programit **sh.** (exit to desktop, exit to main menu, cancel)
3. Validim i pjeses se kontrates tek puntoret, pra kur shtohet nje ose perditesohet, pjesa e kontrates te ket validim qe te jet "Active/Expired/Pending" e jo najsen pa sense, ose munesh me bo me dropdown menu, me zgjedh

# Alketa

1. Perditesim i tabeles salaries (pagave), me shtu bonus, paga neto/bruto, oret pune/mas orarit, historiku i pagave deri ne 3 muj, ditet pushimi (qe don qita)
2. Llogaritje e pages mujore ne program, pra permes kodit e jo databaze

# Edison:

1. Export i databazave ne format pdf/excel
2. Shfaqja e te dhenave te sakta ne dashboard, average pay etj.


### WIP:

**Bonus:**
- heqja nga paga nese useri nuk kyqet pra nuk ben check in ne pune

Design:
- iconat per taskbar, window etj.
- logo ne program dhe dizajnim me te mire jo bland
- window size me e pershtatshme

User: 
- pagen e vet
- kontraten, kur i skadon e sene
- depratamentin
- nese nuk eshte emri ne databaze, te qet qe nuk je i punesuar
- pas kyqjes, nese kontrata skadon ne 2 jave, jep prompt per qe eshte duke u skadu kontrata