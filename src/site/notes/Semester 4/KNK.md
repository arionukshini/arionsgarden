---
{"dg-publish":true,"permalink":"/semester-4/knk/"}
---

E kishim bo edhe per admin edhe per user, sikur a di qka na bojke arbena sot, o po e poshter.

Qe keni naj ide a diqka qe ju bje nmen qe shkon me programin shtone ose shkruni.

# Tina:

1. kur ben login si user shfaq keto (vetem krijoj njehere dhe me pas placeholder diqka jo krejt te perfundume): 
	- Dashboard (duhet me ndryshu normal se qato info jan veq per admin)
	- My Contract (shfaq info per kontraten te ati useri pra jo tabela)
	- My Salary
	- My Department (shfaq koleget ne te njejtin department)
	- Settings
2. mos i shfaq kto te admini dhe ato te adminit tek useri
3. dashboard shfaq summary te userit, munesh me shtu edhe najsen qe ki ide, po tregon, qfare kontrate ki, pagen normale, diten e punesimit, poziten etj

# Arion:


1. ErrorHandling (ne fund)

# Arijola

1. tek my salary shfaq pagen neto/ bruto e te gjitha pjeset e tjera, jo si tebele por e ndame me sections dhe cards. mos e bej pjesen e kalkulimit te pages pra leje hapsire per ditet e punes dhe qe e llogarit pagen e userit
2. historiku i pagave, bone qaty poshte atynve pjeseve, ose anash tankohen ose me button me bo slide prej te djathtes ne te majte pra si sidebar
3. bone fix pjesen e kalkulo pagen tek pjesa e pages tek admin se nuk shfaq sen

# Arjanite punetorja 


1. Navigimim me tab ne welcome screen edhe ku ka met, po ashtu me enter me mujt mu kyq etj. (ne fund) 
2. popup qe kontrata juaj do te skadoj nese ben login si user dhe kontrata mbraon brenda 2 jave, ndryshoje nsql qe don kontratat qe mos me shtu tan kohen new info
3. shto icona per taskbar dhe windows, krijon folder tek recourses/icons
4. opsion i export i databazave ne format pdf/excel per admin part


# Alketa

1. Llogaritje e pages mujore ne program, pra permes kodit e jo databaze, merr pagat, ditet pushim, ditet e punes dhe krejt info te tjera dhe kur ben input ditet e punesh paga e kalkuluar ndryshon, pra paga bruto/neto eshte veq e kjo e kalkuluar eshte veq, pra e shkrun 20 dite pune vet bohet update ajo seamless.
2. pjesen e my contract, shfaq kur ja ke fillu punes, kur mbaron kontrata, llojin e kontrata, statusin e saj
3. pjesen e departments, shfaq departamentin qe je ti, koleget e te atij departamenti, pra merr puntoret e tjere me department_id te njejt

# Edison:


1. readme



# Add User prej admin

first things first, please perdorni codex ose claude code, pra qe e bon kodin vet se hekni kshtu me chat

add user option tek users ne pamje te admin, hap nje popup ose ben me mire krejt window mu ndryshu, ne nje step by step wizard per me shtu ni user te ri qe ne te njejten kohe e shton tek te gjitha tabelat, si foto poshte diqka

![Pasted image 20260529233746.png](/img/user/Pasted%20image%2020260529233746.png)

ne fund pas insertimit ne tabela ben insert te users, ku prej name dhe surname e ben generate ni username, pra arion ukshini ne arion.ukshini, por nese ekzison nje entry me emrin arion ukshini atehere username eshte arion.ukshini2, dhe per password jep nje temp password dhe te tabel fusha, must reset password eshte true.
e lidh emplyee_id qe krijohet me users table, table kto krejt jan te krijume, mos harro me bo hash passwordin

prej chatgpt: 
## STEP 1 — Personal Information

Basic employee info:

- First Name
- Last Name
- Email
- Phone
- Position
- Department
- Status

---

## STEP 2 — Contract Information

- Contract Type
- Start Date
- End Date
- Contract Status

---

## STEP 3 — Salary Information

- Gross Salary
- Bonus
- Deductions
- Work Hours
- Vacation Days
- Overtime

Then auto-calculate:

- Daily Rate
- Overtime Pay
- Net Salary

---

## STEP 4 — Account Information

THIS PART SHOULD BE MOSTLY AUTOMATIC.

Show:

```
Generated Username: arion.ukshini
Temporary Password: H7kP2s9Q
Role: USER
```

Maybe allow admin to edit username manually if needed.

Jep opsionin ne top me shku back ose exit, pra shfaq ikonat arrow back dhe X per exit, ku pra behet delete ai insert qe eshte bo, edhe pse nese id eshte auto_increment dhe kjo bahet shpesh mujn shume id me hup po e bojm ni zgjidhje

per edit user, ska nevoj mu kan kaq e detajume, vetem me mujt me bo edit info te userit, pra emplyee_id, username, pass, amo emplyee_id duhet mu kon unik

munesh edhe mo bo qe nese e shkrun emrin mu bo fill edhe email automatikisht, normal e ndryshushme amo si username mu bo arion.ukshini2@company.net, normal vetem kjo lloj email lejohet, perdor exceptions qe ekzistojne (invalidemail)

# Ide tjera:

check in function, pra tabele per check in, ne dashbord te userit, eshte nje section i vogel me buttonat check in dhe check out, ku e shton tek tabela entry check in dhe check out, pra ne fillim bon insert tani update, kjo pra per me llogarite ditet e punes qe ke punu etj.

bashk me kto shkon edhe ni kalendar qe tregon mujin e tani me filled color ditete qe ke punu pra check in

nuk lejon me bo check out pa bo check in dhe check in pa check out


### WIP:

**Bonus:**
- heqja nga paga nese useri nuk kyqet pra nuk ben check in ne pune

Design:
- hover effect


# Per fund

- Translate krejt senet
- Fshirja e kodit te pa perdorur
- Navigimi i krejt programit me tab edhe me shortcuts
- Testimi per bugs
- ErrorHandling