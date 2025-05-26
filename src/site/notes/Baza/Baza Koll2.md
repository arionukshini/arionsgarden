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
$\underline{I}_{k} = I_{k}e^{j\psi_{k}}$ , pra shprehja merr formen => 
$$\Im m \{[\underline{I}_{1}+\underline{I}_{2}+\dots+\underline{I}_{n}]e^{jwt}\}=0$$
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
$\underline{U}_{k} = U_{k}e^{j\vartheta_{k}}$ , pra shprehja merr formen => 
$$\Im m \{[\underline{U}_{1}+\underline{U}_{2}+\dots+\underline{U}_{n}]e^{jwt}\}=0$$
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
eshte i kyqur ne skajet e lidhjes serike te qarkut serike R,L.
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
Shuma do te jete: 
$$\overline{I} = \overline{I}_{1} + \overline{I}_{2} = I|\underline{\psi}$$
ku
![Pasted image 20250525194247.png](/img/user/Pasted%20image%2020250525194247.png)
![Pasted image 20250525194253.png](/img/user/Pasted%20image%2020250525194253.png)
![Pasted image 20250525194301.png](/img/user/Pasted%20image%2020250525194301.png)
Vlen ligji komutativ: $\overline{I}_{1} + \overline{I}_{2} = \overline{I}_{2} + \overline{I}_{1}$ .

# Trajta komplekse e relacioneve te elementeve te qarkut elektrik #card 

Madhesite e burimeve te tensionit dhe rrymes jepen ne domenin kohor, andaj qarku elektrik i rrymave alternative paraqet nje qark elektrik ne domenin e kohes.
Nese burmiet e tensionit paraqiten ne trajten e tyre komplekse, atehere qarku i tille konsiderohet si qark ne domenin e frekuences.
Analiza e qarqeve ne domoenin frekuences eshte me e lehte se ne domenin e kohes. Ne menyre qe ta kthejne ne domen te frekuences (trajten komplekse) duhet qe perveq burimeve edhe elementet e qarkut te transformohen.
Analizojme elementet pasive te qarkut:
Rryma ne degen me rezistence: $i=I_{m}Sin(wt+\psi)=\sqrt{2}ISin(wt+\psi)$, andaj tensioni ne kete element do te percaktohet nga shprehja $u=R*i=R\sqrt{2}ISin(wt+\psi)$.
Trajta komplekse e tensionit te dhene eshte: $\underline{U}=RIe^{j\psi}$ dhe rryma: $\underline{I}=Ie^{j\psi}$ atehere $\underline{U}=R\underline{I}$.
![Pasted image 20250525210043.png](/img/user/Pasted%20image%2020250525210043.png)
Ne vazhdim le te supozohet se rryma neper nje bobine me induktivitet L. Tensioni do te jete:
![Pasted image 20250525210215.png](/img/user/Pasted%20image%2020250525210215.png)
Ndersa ne trajten komplekse:
![Pasted image 20250525210244.png](/img/user/Pasted%20image%2020250525210244.png)
![Pasted image 20250525210255.png](/img/user/Pasted%20image%2020250525210255.png)
![Pasted image 20250525210303.png](/img/user/Pasted%20image%2020250525210303.png)
Pra tensioni dhe rryma jane te shfazuar per $\pi$/2 perkatesisht rryma mbetet pas tensionit per $\pi$/2.
Nese marrim kondensator, ne vend te bobines:
![Pasted image 20250525210437.png](/img/user/Pasted%20image%2020250525210437.png)
![Pasted image 20250525210441.png](/img/user/Pasted%20image%2020250525210441.png)
![Pasted image 20250525210445.png](/img/user/Pasted%20image%2020250525210445.png)
![Pasted image 20250525210454.png](/img/user/Pasted%20image%2020250525210454.png)
ose
![Pasted image 20250525210501.png](/img/user/Pasted%20image%2020250525210501.png)![Pasted image 20250525210504.png](/img/user/Pasted%20image%2020250525210504.png)
![Pasted image 20250525210517.png](/img/user/Pasted%20image%2020250525210517.png)
Kondensatori ngel pas rrymes per $\pi$/2.

# Impedanca dhe admitanca #card 

Jane percaktuar marredheniet e tensionit dhe rrymes per rezistor, bobine dhe kondensator, ne trajten:
$$\underline{U}=R \underline{I};\space\space\space\space\space\space\space\space\space\space \underline{U}=jwL \underline{I};\space\space\space\space\space\space\space\space\space\space \underline{U}=-j \frac{\underline{I}}{wC}$$
Ana e majte e shprehjeve larte, varet nga frekuenca dhe quhet impedance.
Kjo madhesi percaktohet si raport i tensionit dhe rrymes ne domenin e frekuences. Andaj impedanca e elementeve te qarkut, rezistorit, bobines dhe kondensatorit eshte:
$$\underline{Z}_{R}=R;\space\space\space\space\space\space\space\space\space\space \underline{Z}_{L}=jwL;\space\space\space\space\space\space\space\space\space\space \underline{Z}_{C}=\frac{-j}{wC}$$
Shihet se kur w=0, impedanca e bobines eshte e barabart me zero, kurse ajo e kondensatorit tenton ne vlere te pakufizuar.
$$\underline{Z}=R+jX$$
$$R=\Re e \{\underline{Z}\} \to rezistence\space aktive \space\space\space\space\space\space\space\space\space\space X=\Im m \{\underline{Z}\} \to rezistence\space reaktive$$
Impedanca mund te paraqitet edhe ne trajte eksponenciale:
![Pasted image 20250525211628.png](/img/user/Pasted%20image%2020250525211628.png)
![Pasted image 20250525211632.png](/img/user/Pasted%20image%2020250525211632.png)
![Pasted image 20250525211641.png](/img/user/Pasted%20image%2020250525211641.png)
Shpesh ehste me e pershtatshme te perdorim me vleren reciproke te impedances, e cila quhet admitance.
$$\underline{Y}=\frac{1}{\underline{Z}}=\frac{\underline{I}}{\underline{V}}\space\space\space\space\space\space\space\space\space\space\underline{Y}=G+jB$$
$$G=\Re e \{\underline{Y}\} \to percueshmeria\space aktive \space\space\space\space\space\space\space\space\space\space B=\Im m \{\underline{Y}\} \to percueshmeria\space reaktive$$
![Pasted image 20250525212015.png](/img/user/Pasted%20image%2020250525212015.png)
prej nga
![Pasted image 20250525212022.png](/img/user/Pasted%20image%2020250525212022.png)

# Teorema e transmetimit maksimal te fuqise aktive te shpenzuesit (konsumatorit) #card 

Ka shume rendesi te percaktohen kushtet e qarkut per te realizuar ne te transmetimin maksimal te fuqise qe perdoret ne konsumator. Me fjale tjera: Impedanca e konsumatorit te jete e tille qe fuqia aktive e saj te jete maksimale.
Le te veshtrohet konsumatori me impedance $\underline{Z}_{k}=R_{k}+jX_{k}$ , i cili ehste i lidhur ne burimin e tensionit alternativ i cili e ka impedancen e brendshme $\underline{Z}_{g}=R_{g}+jX_{g}$.
Rryma ne qark e ka trajten:
![Pasted image 20250526153327.png](/img/user/Pasted%20image%2020250526153327.png)
![Pasted image 20250526153334.png](/img/user/Pasted%20image%2020250526153334.png)
ndersa fuqia e dukshme e konsumatorit eshte: 
$$\underline{S}_{k}=\underline{Z}_{k}I^2=R_{k}I^2+jX_{k}I^2$$
prej nga 
![Pasted image 20250526153545.png](/img/user/Pasted%20image%2020250526153545.png)
![Pasted image 20250526153641.png](/img/user/Pasted%20image%2020250526153641.png)
Pas derivimit te pare sipas $X_{k}$, dhe barazimit me zero:
![Pasted image 20250526153718.png](/img/user/Pasted%20image%2020250526153718.png)
![Pasted image 20250526153723.png](/img/user/Pasted%20image%2020250526153723.png)
Pas derivimit sipas $R_{k}$:
![Pasted image 20250526153808.png](/img/user/Pasted%20image%2020250526153808.png)
ose
![Pasted image 20250526153815.png](/img/user/Pasted%20image%2020250526153815.png)
kur perdoret kushti 4.135, fitohet:
![Pasted image 20250526154014.png](/img/user/Pasted%20image%2020250526154014.png)
Krahasuar me shprehjen per fuqine e konsumatorit, shihet se fuqia aktive e gjeneratorit eshte dy here me e madhe se fuqia aktive e konsumatorit. Kjo dmth se ne rastin e pershtatjes gjysma e energjise se gjeneratorit shpenzohet ne vet gjeneratorin.

# Paraqitja e rrymes konstante ne qarkun elektrik #card 

Zgjidhja e problemeve ne qarqet elektrike ku vjen ne shprehje dukuria e induksionit elektromagnetik nuk eshte aq e thjeshte.
Andaj, se pari do te fillohet me shqyrtimin e rasteve me te thjeshta per zgjidhje. Nje prej tyre eshte ai i paraqitjes se rrymes konstante ne qarkun e thjeshte.
![Pasted image 20250526154703.png](/img/user/Pasted%20image%2020250526154703.png)
Ky problem deri tash ka qene i thjeshte, se posa u kyq nje burim tensioni me fel. konstante, E, ndermjet skajeve te rezistorit R, pernjehere paraqitet rryma konstante $I=E/R$. Eshte pak e quditshme qe intensiteti i rrymes elektrike nga vlera I=0 kercen ne vleren konstante E/R, qe nuk eshte e natyrshme, sepse: madhesite fizike makroskopike nuk ndryshojne gjate kohes me kercime, por patjeter ne menyre te vazhdueshme (kontinuale).
![Pasted image 20250526155102.png](/img/user/Pasted%20image%2020250526155102.png)
Ekuacioni i baraspeshes ne kete qark do te jete:
![Pasted image 20250526155137.png](/img/user/Pasted%20image%2020250526155137.png)
ku $e_{j}$ eshte forca elektrorezistore per shkak te efektit te Xhaulit, ndersa $e'$ eshte fel. e autoinduksionit.
Pasi te zevendesohen vlerat per keto dy forca elektrike, fitohet:
![Pasted image 20250526155327.png](/img/user/Pasted%20image%2020250526155327.png)
![Pasted image 20250526155353.png](/img/user/Pasted%20image%2020250526155353.png)
Dukuria e rrymes elektrike ne qark ^. Paraqet ekuacionin diferencial te rendit te pare dhe homogjen.
$i=i_{p}+i_{h}$, ku per $i_{p}$
![Pasted image 20250526155647.png](/img/user/Pasted%20image%2020250526155647.png)
kurse per $i_{h}$
![Pasted image 20250526155714.png](/img/user/Pasted%20image%2020250526155714.png)
![Pasted image 20250526155755.png](/img/user/Pasted%20image%2020250526155755.png)
![Pasted image 20250526155812.png](/img/user/Pasted%20image%2020250526155812.png)
![Pasted image 20250526155904.png](/img/user/Pasted%20image%2020250526155904.png)
![Pasted image 20250526155927.png](/img/user/Pasted%20image%2020250526155927.png)
![Pasted image 20250526155937.png](/img/user/Pasted%20image%2020250526155937.png)
Para se te veproj burimi, rryma eshte zero: $i(0)=0$, ndersa 12.5
$$i(0)=\frac{E}{R}+A \space \space pas\space \space barazimit\space \space te\space \space dy\space \space shprehjeve\space \space vlera\space \space e \space \space konstantes \space \space A=-\frac{E}{R}$$
Shpejtësia e ndryshimit të rrymës varet nga herësi  $\tau=L/R$ , që quhet konstantja kohore e qarkut.