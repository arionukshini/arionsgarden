---
{"dg-publish":true,"permalink":"/baza/baza-koll2/"}
---


# Ligji i pare i kirhofit #card

Le te jete i1, i2, i3 ... in, vlera momentale te rrymave ne nje nyje te qarkut te cilat dalin ose hyn ne te.
Ne baze te LIK, shuma e te gjitha ketyre rrymave, ne qdo moment, eshte e barabart me zero.
$$i_{1}+i_{2}+i_{3}+\dots+i_{n} = 0$$
Nese supozojme se rrymat jan ne forme sinusoidale:
$$i(t)=I_{m}Sin(wt+\psi)$$
atehere:
$$I_{m1}Sin(wt+\psi)+I_{m2}Sin(wt+\psi)+\dots+I_{mn}Sin(wt+\psi)=0$$
ose
$$\sqrt{2}\Im m \{I_{1}e^{j\psi_{1}}e^{jwt}\} + \Im m \{I_{2}e^{j\psi_{2}}e^{jwt}\} + \dots + \Im m \{I_{n}e^{j\psi_{n}}e^{jwt}\}=0$$
$$\sqrt{2}\Im m \{I_{1}e^{j\psi_{1}}e^{jwt} + I_{2}e^{j\psi_{2}}e^{jwt} + \dots + I_{n}e^{j\psi_{n}}e^{jwt}\}=0$$
$\underline{I}_{k} = I_{k}e^{j\psi_{k}}$ , pra shprehja merr formen => $$\Im m \{[\underline{I}_{1}+\underline{I}_{2}+\dots+\underline{I}_{n}]e^{jwt}\}=0$$
Pasiqe $e^{jwt} \neq 0$ atehere shprehja merr trajten perfundimatre:
$$\underline{I}_{1}+\underline{I}_{2}+\dots+\underline{I}_{n}=0$$
qe paraqet ligjin e pare te kirhofit ne domenin frekuencor (trajten komplekse) LIK shihet se eshte i njejte sikur tek qarqet e rrymave konstante, por tash me madhesi komplekse.

# Ligji i dyte i kirhofit #card

Le te jete u1, u2, u3 ... un, tensionet e n elementeve ne nje qark.
Bazuar ne LIIK, ne domenin kohor, do te jete:
$$u_{1}+u_{2}+u_{3}+\dots+u_{n} = 0$$
Nese supozojme se tensionet jan ne forme sinusoidale:
$$u(t)=U_{m}Sin(wt+\vartheta)$$
atehere:
$$U_{m1}Sin(wt+\vartheta)+U_{m2}Sin(wt+\vartheta)+\dots+U_{mn}Sin(wt+\vartheta)=0$$
ose
$$\sqrt{2}\Im m \{U_{1}e^{j\vartheta_{1}}e^{jwt}\} + \Im m \{U_{2}e^{j\vartheta_{2}}e^{jwt}\} + \dots + \Im m \{U_{n}e^{j\vartheta_{n}}e^{jwt}\}=0$$
$$\sqrt{2}\Im m \{U_{1}e^{j\vartheta_{1}}e^{jwt} + U_{2}e^{j\vartheta_{2}}e^{jwt} + \dots + U_{n}e^{j\vartheta_{n}}e^{jwt}\}=0$$
$\underline{U}_{k} = U_{k}e^{j\vartheta_{k}}$ , pra shprehja merr formen => $$\Im m \{[\underline{U}_{1}+\underline{U}_{2}+\dots+\underline{U}_{n}]e^{jwt}\}=0$$
Pasiqe $e^{jwt} \neq 0$ atehere shprehja merr trajten perfundimatre:
$$\underline{U}_{1}+\underline{U}_{2}+\dots+\underline{U}_{n}=0$$
qe paraqet ligjin e dyte te kirhofit ne domenin frekuencor ne trajten komplekse.

# Tensioni alternativ ne skajet e bobines #card 

Veshtrojme rastin kur bobina me induktivitet L kyqet ne tensionin alternativ, te trajtes:
$$u(t)=U_{m}Sin(wt+\vartheta)$$
Vlera momentale e intensitetit te rrymes neper bobine, do te jete:
![Pasted image 20250525184224.png](/img/user/Pasted%20image%2020250525184224.png)
![Pasted image 20250525184257.png](/img/user/Pasted%20image%2020250525184257.png)
Ne kete shprehje rryma $I_{0}$ paraqet vleren fillestare te rrymes ne bobine, e cila ne regjimin periodik te thjeshte eshte e barabarte me zero, keshtu qe ne vazhdim, mund te mosperfillet, ndersa $X_{L}=wL$ eshte rezistenca fiktive e bobines. Shprehjen me lart mund te paraqitet si: ![Pasted image 20250525184507.png](/img/user/Pasted%20image%2020250525184507.png)
pastaj $i(t)=I_{m}Sin(wt+\psi)$, shihet se:
$$I_{m}=\frac{U_{m}}{wL} \space dhe\space faza \space fillestare\space \psi=\vartheta - \frac{\pi}{2}$$
Pra, rryma neper bobine, e cila eshte e kyqur ne burimin e tensionit alternativ eshte poashtu alternative, me vlere maksimale te dhene me lart, ndersa faza fillestare e saj vonohet per $\pi$/2, ne krahasim me ate te tensionit.
![Pasted image 20250525185251.png](/img/user/Pasted%20image%2020250525185251.png)

# Tensioni alternativ ne skajet e kondensatorit #card 

Shqyrtojme rastin e kyqjes se kondensatorit te tensionit alternativ:
$$u(t)=U_{m}Sin(wt+\vartheta)$$
Vlera momentale e intensitetit te rrymes ne qark do te jete:
![Pasted image 20250525185606.png](/img/user/Pasted%20image%2020250525185606.png)
perkatesisht ![Pasted image 20250525185615.png](/img/user/Pasted%20image%2020250525185615.png)
shihet se vlera maksimale e rrymes eshte: $I_{m}=wCU_{m}$ dhe faza fillestare: $\psi=\vartheta+\pi/2$ nga shihet se faza fillestare e rrymes eshte per $\pi$/2 para asaj te tensionit. 
Rryma eshte alternative, njejt si tensioni.
Madhesia $X_{C}=\frac{1}{wC}$ quhet rezistenca fiktive e kondensatorit.
![Pasted image 20250525190005.png](/img/user/Pasted%20image%2020250525190005.png)

# Tensioni alternativ ne skajet e lidhjes serike te rezistorit dhe bobines #card 

$$u=U_{m}Sin(wt+\vartheta)$$
eshte i kyqurne skajet e lidhjes serike te qarkut serike R,L.
![Pasted image 20250525191430.png](/img/user/Pasted%20image%2020250525191430.png)
Ekuacioni i baraspeshes dinamike per kete qark ka trajten, ![Pasted image 20250525191800.png](/img/user/Pasted%20image%2020250525191800.png)
![Pasted image 20250525191808.png](/img/user/Pasted%20image%2020250525191808.png)
Meqe dhe intensiteit i rrymes elektrike eshte madhesi periodike e thjeshte, ajo mund te supozohet e trajtes,
![Pasted image 20250525191846.png](/img/user/Pasted%20image%2020250525191846.png)
![Pasted image 20250525191850.png](/img/user/Pasted%20image%2020250525191850.png)
ku amplituda Im dhe shfazimi i tensionit dhe rrymes duhet te percaktohen. Per me zevendesu kete shprehje ne baraspeshimin dinamik, nevojitet derivati i rrymes:
![Pasted image 20250525191958.png](/img/user/Pasted%20image%2020250525191958.png)
Pas zevendesimit:
![Pasted image 20250525192007.png](/img/user/Pasted%20image%2020250525192007.png)
Nga ky indetitet trigonometrik, fitohet:
![Pasted image 20250525192043.png](/img/user/Pasted%20image%2020250525192043.png)
Pas pjestimit te pjeses se majte (pa I-ne) me $\cos \varphi$
![Pasted image 20250525192123.png](/img/user/Pasted%20image%2020250525192123.png)
![Pasted image 20250525192129.png](/img/user/Pasted%20image%2020250525192129.png)
![Pasted image 20250525192138.png](/img/user/Pasted%20image%2020250525192138.png)
Pas zevendesimit ne 4.27: (munesh me zgjedh zevendesimin, pra sin dhe cos e zv deri sa te del qikjo poshte)
![Pasted image 20250525192157.png](/img/user/Pasted%20image%2020250525192157.png)
Kjo shprehje per nga natyra eshte rezistence elektrike dhe shenohet me Z, ndersa quhet impedance, por edhe rezistence fiktive.
Pra, impedanca e lidhjes serike te rezistorit dhe bobines eshte 
![Pasted image 20250525192419.png](/img/user/Pasted%20image%2020250525192419.png)
Vlera maksimale e rrymes dhe vlera efektive: $I_{m}=\frac{U_{m}}{Z}$ dhe $I=\frac{U}{Z}$ . $\varphi= \arctan\left( \frac{wL}{R} \right)$ 
![Pasted image 20250525192632.png](/img/user/Pasted%20image%2020250525192632.png)

# Tensioni alternativ ne skajet e lidhjes serike te rezistorit dhe kondensatorit #card 

Supozohet se ne skaje te lidhjes serike te rezistorit me rezistence R dhe kondensatorit me kapacitet C, vepron tensioni periodik i thjeshte $u=U_{m}Sin(wt+\vartheta)$.
Intensiteti i rrymes ne qark do te jtet poashtu madhesi periodike e thjeshte, dhe le te supozohet e trajtes $i=I_{m}Sin(wt+\vartheta-\varphi)=I_{m}Sin(wt+\psi)$, ku amplituda Im dhe kendi i shfazimit $\varphi$ jane te panjohura.
Ekuacioni i baraspeshes se qarkut ne fig. ka trajten: $u=u_{R}+u_{C}$.
![Pasted image 20250525193204.png](/img/user/Pasted%20image%2020250525193204.png)
Duke i pasur parasysh shprehjet e tensioneve ne rezistor dhe kondensator
![Pasted image 20250525193240.png](/img/user/Pasted%20image%2020250525193240.png)
![Pasted image 20250525193243.png](/img/user/Pasted%20image%2020250525193243.png)
![Pasted image 20250525193259.png](/img/user/Pasted%20image%2020250525193259.png)
atehere shprehja e baraspeshes shendrrohet ne:
![Pasted image 20250525193334.png](/img/user/Pasted%20image%2020250525193334.png)
![Pasted image 20250525193356.png](/img/user/Pasted%20image%2020250525193356.png)
![Pasted image 20250525193403.png](/img/user/Pasted%20image%2020250525193403.png)
![Pasted image 20250525193411.png](/img/user/Pasted%20image%2020250525193411.png)
![Pasted image 20250525193416.png](/img/user/Pasted%20image%2020250525193416.png)
Madhesia ne emruesin ne shprehjen me larte per nga natyra eshte rezistence elektrike dhe quhet impedance
![Pasted image 20250525193517.png](/img/user/Pasted%20image%2020250525193517.png)
ne kete rast kendi i shfazimit ndermjet tensionit dhe rrymes eshte negativ (4.45), qe do te thote se tensioni ngece pas rrymes elektrike.

# Operacioni i mbledhjes se fazoreve #card

Le te jene dhene fazoret e dy rrymave, te cilat duhet te mblidhen:
$$\overline{I}_{1}=I_{1} \space|\underline{\psi}_{1} \space\space\space\space\space  \overline{I}_{2}=I_{2} \space|\underline{\psi}_{2}$$
Shuma do te jete: $$\overline{I} = \overline{I}_{1} + \overline{I}_{2} = I|\underline{\psi}$$
ku
![Pasted image 20250525194247.png](/img/user/Pasted%20image%2020250525194247.png)
![Pasted image 20250525194253.png](/img/user/Pasted%20image%2020250525194253.png)
![Pasted image 20250525194301.png](/img/user/Pasted%20image%2020250525194301.png)
Vlen ligji komutativ: $\overline{I}_{1} + \overline{I}_{2} = \overline{I}_{2} + \overline{I}_{1}$ .

# Trajta komplekse e relacioneve te elementeve te qarkut elektrik #card 

Hala

# Impedanca dhe admitanca #card 

Hala