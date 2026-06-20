---
{"dg-publish":true,"permalink":"/semester-4/ueb-2/notes/"}
---

# Hyrja

Skriptat mund te jene client side ose server side.
Client side ekzakutohen te klienti dhe klienti e sheh kodin.
Server side qendron ne server dhe eshte i fshehur perveq daljes HTML.

### Avantazhet/Disavantazhet e programimit Server Side 

Avantazhet: 
- Transportueshmëria: Çdo gjë që bëjmë do të funksionojë në çdo shfletues 
- Përshtatshmëria: Mund të përshtatim daljen me cilindo shfletues që përdor përdoruesi! 
- Fleksibiliteti: Mund të ndryshojmë serverë pa modifikuar asnjë skript!
Disavantazhet: 
- Joefikasiteti: duhet kohë për t'u ekzekutuar 
- Gjerësia e brezit: kërkon kohë për të dërguar të dhëna nga një program te një klient 
- Shkallueshmëria: programet komplekse janë të pazbatueshme nëse nuk keni një server të madh ose dhomë serverësh 
- Konkurrenca: është e vështirë të shkruash skripta nga ana e serverit në mënyrë që disa kopje të një skripti të mund të ekzekutohen njëkohësisht 
- Siguria: Shumë e lehtë për të shkruar programe të pasigurta

## Çfarë është PHP? 
Gjuhë skriptimi nga ana e serverit 
- Mund të vendoset direkt në HTML 
- Mbështet veçoritë më të zakonshme POO: klasa, trashëgimi
Përdoret për të bërë faqet e internetit dinamike

E konceptuar në vitin 1994-95 nga Rasmus Lerdorf 
Fillimisht qëndronte për "Personal Home Page", por ndryshoi në PHP Hypertext Preprocessor.

Prapashtesa e fajllit: .php (jo HTML) megjithëse kodi PHP është i vendosur brenda kodit HTML.
Serveri e ekzakuton kodin PHP, klienti interpreton HTML e file-it, pra kodi PHP nuk shihet nga klienti.

Komentet shkruhen me: "#", "//", "/* \*/".

### Interprentimi 
Teksti brenda " " interpretohen, zëvendësohen me kuptimin e tyre. Teksti brenda ‘ ’ janë shkronja.

```php
$f=200;
echo "Vlera është $f"; // Vlera është 200
echo 'Vlera është $f'; // Vlera është $f
```

"." perdoret per lidhje

```php
$p="P";
$h="H";

echo $p.$h.$p;
$x=$p.$h.$pp;
echo "<br\>".$x[1];
```

```php
<?php

// Emrat e variablave të specifikuar në kohën e ekzekutimit
$work_day1="E hane";
$work_day2="E marte";
$work_day3="E merkure"; 
$work_day4="E enjete"; 
$work_day5="E premte"; 

for($i=1; $i<=5;$i++) { 
	echo ${"work_day".$i}; 
}

?>
```

![Pasted image 20260414210252.png](/img/user/Semester%204/Images/Pasted%20image%2020260414210252.png)

Deklarimi i konstanteve:
```php
<?php
define('Const_1', 100); 
define('PI', 3.14);
const Const_2=4; 
echo Const_1; 
echo PI; 
echo Const_2;
?>
```

### Deklarata PHP

**phpinfo()** - shfaq informacionin e sistemit (d.m.th., konfigurimin aktual të php) 
**$\_SERVER ['HTTP_USER_AGENT’];** - informata per shfletuesin

![Pasted image 20260414211301.png](/img/user/Semester%204/Images/Pasted%20image%2020260414211301.png)

## Funksionet:

Funksionet janë grupe deklaratash që mund t'i ekzekutoni si një njësi e vetme.
Përkufizimet e funksionit janë linjat e kodit që përbëjnë një funksion.
Sintaksa për përcaktimin e një funksioni është:

```php
<?php
function name_of_function(parameters) { statements; }
?>
```

### Funksione me/pa definimin e tipeve te parametrave

Rasti 1:
```php
<?php
function shuma_numrave($a, $b) {
    echo "</br> Shuma e numrave eshte: ".$a+$b;
}
shuma_numrave(2,4);
?>
```
Rasti 2:
```php
<?php
declare(strict_types=1);

function shuma_numrave(int $a, int $b){
    echo "</br> Shuma e numrave eshte: ".$a+$b;
}
shuma_numrave(2,3.3);
// gabim sepse kemi vendos 3.3 ne int

function HI($rol="Student"){
    echo "Mireserdhe $rol ";
}
HI("Profesor");
HI();
?>
```

### Funksione me vlera kthimi

```php
<?php
function mesatarja_numrave( int $a, int $b, int $c) {
    $shuma=$a+$b+$c;
    return $shuma/3;
}

echo "</br> Mesatarja e numrave:".mesatarja_numrave(2,4,5);
?>
```

### Funksione: Parametri me referencë (**&**)

```php
<?php
$a=5;
$b=&$a;
$a=6;

echo $a;
echo "<br/>".$b;
// Rezultati: 6, 6


function test($x) {
    $x = 100;
}

$a = 5;
test($a);
echo $a; // 5

function test(&$x) {
    $x = 100;
}

$a = 5;
test($a);
echo $a; // 100
?>
```

### Funksionet e integruara

![Pasted image 20260414220337.png](/img/user/Semester%204/Images/Pasted%20image%2020260414220337.png)

**trim()** largon hapësirat nga të dy anët e një string

![Pasted image 20260414220516.png](/img/user/Semester%204/Images/Pasted%20image%2020260414220516.png)

**func_get_args()** është një funksion i PHP që përdoret brenda një funksioni tjetër dhe kthen të gjithë argumentet e dërguara në atë funksion si një array 
- funksione me numër të ndryshueshëm parametrash 
- func_get_args() Kthen të gjithë argumentet si array 
- func_get_arg($n) Kthen argumentin me indeks të caktuar 
- func_num_args() Kthen numrin e argumenteve

Fushëveprimi i Variablave: 
- Local 
- Static 
- Global 
- Function parameters
- 
![Pasted image 20260414221011.png](/img/user/Semester%204/Images/Pasted%20image%2020260414221011.png)
![Pasted image 20260414221039.png](/img/user/Semester%204/Images/Pasted%20image%2020260414221039.png)

### Përdorimi variablave superglobale
- PHP përfshin vargje të ndryshme globale të paracaktuara, të quajtura superglobale 
- Superglobalë përmbajnë informacione për klientin, serverin dhe mjedisin që mund t'i përdorni në skriptet tuaja 
- Superglobalë janë vargje shoqëruese –elementet e të cilëve referohen me një çelës alfanumerik në vend të një numri indeksi
![Pasted image 20260414221258.png](/img/user/Semester%204/Images/Pasted%20image%2020260414221258.png)

for: inicializimi, kushti dhe operacionet post-loop si në JavaScript
foreach: veçanërisht i dobishëm për përsëritjen nëpër vargje

```php
$FastFoods = array("pizza", "burgers", "french fries", "tacos", "fried chicken");
for ($Count = 0; $Count < 5; ++$Count) {
echo $FastFoods[$Count], "<br>";
}
foreach ($FastFoods as $MenuItem) { echo "$MenuItem";}
```

Shenja në (**@**) përdoret si operator i kontrollit të gabimeve në PHP: 

```php
$file_name = @file(‘nuk eshte I lexueshem’);
$conn = @mysqli_connect("localhost", "user", "pass");
```
### Magic Constants në PHP

Magic constants në PHP janë konstanta të paracaktuara që ndryshojnë vlerën e tyre në varësi të kontekstit ku përdoren. 
Quhen “magic” sepse PHP i zëvendëson automatikisht me një vlerë specifike gjatë ekzekutimit të kodit. 
- Fillojnë me dy underscore: __ 
- Përfundojnë me dy underscore: __ 
- Vlera e tyre varet nga vendndodhja (file, klasë, funksion, metodë, etj.) 
- Nuk mund të ndryshohen nga programuesi

# Ruajtja dhe marrja e të dhënave nga fajllat në PHP

Dy teknika bazë për të lexuar/shkruar fajllat në PHP:
**Qasja stream:** 
- Lexon vetëm një pjesë të vogël të fajllit në të njëjtën kohë 
- Kërkon programim më të kujdesshëm 
- Është qasja më efikase për kujtesën kur lexoni fajlla shumë të mëdhenj
**Qasje All-In-Memory:** 
- Mund të lexojë të gjithë fajllin në memorie (d.m.th., në një variabël PHP) 
- Jo i përshtatshëm për fajlla të mëdhenj 
- E bën përpunimin e fajllit jashtëzakonisht të lehtë

Per te hapur nje file perdorim
`$fp = fopen("$document_root/../orders/orders.txt", 'w’);`

File Modes per fopen()
![Pasted image 20260414230906.png](/img/user/Semester%204/Images/Pasted%20image%2020260414230906.png)

Pasi të kemi mbaruar përdorimin e një fajlli, duhet të mbyllim atë, duke përdorur fclose() funksionon si më poshtë: `fclose($fp)`.

Funksioni flock() bllokon dhe liron një fajll:
![Pasted image 20260414233446.png](/img/user/Semester%204/Images/Pasted%20image%2020260414233446.png)

```php
$file = fopen("order1.txt","a");
flock($file,LOCK_EX);
if (flock($file,LOCK_EX)) {
	fwrite($file,"Fajlli eshte mbishkkruar nga @...");
} else { echo "Gabim gjate...!"; }
```

`feof()` kontrollon nëse " end-of-file " (EOF) është arritur për një fajll të hapur. 
`fgets()` lexon një rresht, derisa të ndeshet me një karakter p.sh. \n. 
- fgetss () ose fgetcsv() 
- P.sh $p = fgetcsv($fp, 0, "\t");

Ky kod lexon një karakter të vetëm në të njëjtën kohë nga fajll duke përdorur `fgetc()` dhe e ruan atë në $char, derisa të arrihet fundi i fajllit.
Më pas bën një përpunim të vogël për të zëvendësuar karakteret e tekstit në fund të rreshtit (\n) me ndërprerje të rreshtave HTML ( \<br> ).

```php
$fp = fopen("porosia.txt", 'a');
while (!feof($fp)) { 
	$char = fgetc($fp); 
	if (!feof($fp)) 
		echo ($char== "\n" ? "<br>": $char); 
}
```

Mund të lexoni të gjithë fajllin me një komand. Janë disa mënyra të ndryshme se si mund të realizohet: `readfile("porosia.txt");`.

Mënyra tjeter që mund të lexoni nga një fajll është të përdorni funksionin fread() për të lexuar te dhenat nga fajlli: 
```php
$file = fopen("porosia.txt","r");
echo fread($file,filesize("porosia.txt"));
fclose($file);
```

`File()` - për të lexuar fajllin në një grup rreshtash

```php
$line=file("porosia.txt");
foreach ($line as $l) {
	echo $l."<br>";
}
```

`File_get_contents()` - për të lexuar fajllin në një variabël vargu

```php
$page=file_get_contents("https://fiek.uni-pr.edu/");
$page=preg_split("/\n/",$page );

foreach ($page as $p) {
	echo "<br>".$p."<br>";
}
```

`File_put_contents()` - për të shkruar përmbajtjen e një vargu në një fajll 

```php
$shto_x="PhD.Dhurate Hyseni \n";
file_put_contents("porosia.txt", $shto_x, FILE_APPEND);
$f=file("profesoret.txt");
foreach ($f as $l) { echo $l."<br>"; }
```

`opendir(), readdir(), closedir()` per direktorite.

Nëse dëshironi të kontrolloni nëse një fajlle ekziston pa e hapur atë, mund të përdorni `file_exists()`, si: 
```php
if (file_exists("porosia.txt")) {
	echo 'Jane disa porosi duke pritur per procesim...';
} else {
	echo 'Nuk ka porosi ne fajll.';
}
``` 
Mund të kontrollohet madhësinë e një fajlli duke përdorur funksionin filesize(): 
`echo filesize("porosia.txt");`

Nëse dëshirojmë të fshim fajllin e porosisë pasi të jenë përpunuar porositë, mund ta përdorim unlink().
Mund të manipuloni dhe zbuloni pozicionin e pointerit të fajllit me funksionin ftell().

![Pasted image 20260415132236.png](/img/user/Semester%204/Images/Pasted%20image%2020260415132236.png)
![Pasted image 20260415133918.png](/img/user/Semester%204/Images/Pasted%20image%2020260415133918.png)

rewind() – Kthehu në fillim të file-it
```php
$file = fopen("example.txt", "r");
echo fgets($file);
rewind($file);
```
fseek() – Lëviz në një pozicion specific 
```php
fseek($fp, 10, SEEK_SET); // shkon te byte 10
fseek($fp, 5, SEEK_CUR); // lëviz 5 byte përpara
fseek($fp, -10, SEEK_END); // 10 byte para fundit 
```
SEEK_SET nga fillimi
SEEK_CUR nga pozicioni aktual
SEEK_END nga fundi

# Arrays

Deklarimi me konstruktor `array();`

```php
$v_Zbrast= array();

$v_MeElemente_1= array("com","edu", "net", "org", "gov");

$v_MeElemente_2=["com","edu", "net", "org", "gov"];

$v_Zbrast[0]="elementi1"; $v_Zbrast[1]="elementi2"; $v_Zbrast[2]="elementi3";

$v_Zbrast[]="elementi4";
$v_Zbrast[]="elementi5";
$v_Zbrast[]="elementi6";
  
for($i=0; $i<count($v_MeElemente_1); $i++)
    echo "Elementi: ".$i." eshte <b> ".$v_MeElemente_1[$i]."</b></br>";
    
    
$cmimet = array('Molla'=>100, 'Buka'=>10, 'Uji'=>1);
echo " ".$cmimet["Molla"];


$v_MeElemente_3=array(0=>"edu", 1=>"com", 2=>"net", 3=>"org",4=>"gov", 5=>"net");

$v_MeElemente_4=array("edu"=>"education","com"=>"commercial","net"=>"network","gov"=>"government", "org"=>"organization" );

for($i=0; $i< count($v_MeElemente_4);$i++)
    echo "Elementi: ".$v_MeElemente_3[$i]." eshte <br>".$v_MeElemente_4[$v_MeElemente_3[$i]]."</b></br>";
```

`rang()` për të krijuar një sekuencë në rritje të numrave në një varg

```php
$v_MeElemente_5= range(1,10,2);
for($i=0; $i<count($v_MeElemente_5); $i++)
    echo "Elementi: ".$i." eshte <b> ".$v_MeElemente_5[$i]."</b></br>";

$v_MeElemente_6=range("A", "B");
echo "Elementi ".$v_MeElemente_6[0]; // Elementi A
```

### Exploding Arrays

E merr nje fjali si "Studentet e dalluar ne Web Programim" dhe e ndan pjese pjese dhe e shendrron ne array. 

```php
$inp = "Studentet e dalluar ne Web Programim";

$temp = explode(' ', $inp);
print_r($temp);

$tekst = implode(",", $temp);
print_r($tekst);
```
`count($v_MeElemente_1)`

![Pasted image 20260415141042.png](/img/user/Semester%204/Images/Pasted%20image%2020260415141042.png)

`urlencode()` Karakteret speciale si : dhe / në URL-në "ridrejtim" janë koduar si %3A dhe %2F për të shmangur ndërhyrjen në strukturën e URL-së së përgjithshme.
`rawurlencode()` Zëvendëson të gjitha karakteret e tjera jo-alfanumerike përveç -, \_, ., dhe ~ me një shenjë përqindjeje të ndjekur nga dy shifra heksadecilam. Ky funksion zëvendëson gjithashtu hapësirat me një përqindje të ndjekur nga dy shifra heks: %20
![Pasted image 20260415143656.png](/img/user/Semester%204/Images/Pasted%20image%2020260415143656.png)

```php
<html>
<body>
    <form method="POST" >
        <label>Username</label> <br/>
        <input type="textbox" name="username"/ > <br/>
        <label>Pass</label> <br/>
    <input type="password" name="pass"/ > <br/>
    <input type="submit" value="Dergo"/>
    </form>
</body>
</html>

<?php

if(!empty($_POST["username"])&&!empty($_POST["pass"]) )
{
	$v=$_POST["username"] ." ".$_POST["pass"];
	$a= rawurlencode($v);
	echo ' <br>Te dhenat: '.$v;
	echo ' <br>Te dhenat rawurlencode: '.$a;
}

?>
```

![Pasted image 20260415220553.png](/img/user/Semester%204/Images/Pasted%20image%2020260415220553.png)
![Pasted image 20260415220609.png](/img/user/Semester%204/Images/Pasted%20image%2020260415220609.png)
![Pasted image 20260415220922.png](/img/user/Semester%204/Images/Pasted%20image%2020260415220922.png)

## $\_GET dhe $\_POST Superglobals
Aksesoni të dhënat në një varg pyetjesh të dërguar nga klienti: 
- Nëse të dhënat dërgohen përmes kërkesës HTTP GET: të dhënat e aksesueshme nga PHP brenda URL-së dhe të ruajtura në: $\_Get vargun, $\_Get[“var_1”] dhe $\_Get[“var_2”] 
- Nëse të dhënat dërgohen përmes kërkesës HTTP POST: të dhënat nuk janë të dukshme nga PHP në URL, por të aksesuesh me brenda kërkesës HTTP POST: $\_Post vargu, $\_Pos[“var_1”] dhe $\_Post[“var_2”]

# Errors

include() dhe require(), ngarkon një fajll në një skript PHP.

Po kur fajlli nuk mund të përfshihet (ai nuk ekziston, ose serveri nuk e lejon aksesin në të)? 
- Include- shfaqet vetëm një paralajmërim (E_WARNING) dhe ekzekutimi vazhdon 
- Require- shfaqet një gabim (E_ERROR) dhe ekzekutimi ndalon

include_once() dhe require_once(), i njëjtë me include dhe require përveç, nëse fajlli tashmë është përfshirë, nuk do të kërkohet prap

## Llojet e gabimeve

**Gabimet e pritshme (Expected Errors):**
Janë gabime që parashikohen të ndodhin gjatë ekzekutimit.
Shembuj: 
- Qasja e përdoruesit (input i gabuar) 
- Problemet me lidhjen e bazës së të dhënave
Duhet të trajtohen me kontroll (p.sh. validim, try-catch) 

**Paralajmërimet (Warnings):**
Janë probleme që gjenerojnë një mesazh paralajmërues nga PHP
Nuk e ndalojnë ekzekutimin e faqes
Mund të ndikojnë në funksionalitet, por skripti vazhdon 

**Gabime fatale (Fatal Errors):** 
Janë gabime serioze 
Ndërpresin menjëherë ekzekutimin e faqes nëse nuk trajtohen 
Shembuj: 
- Thirrje e funksioneve që nuk ekzistojnë 
- Probleme kritike në kod

### Kontrollimi i vlerave

![Pasted image 20260415163058.png](/img/user/Semester%204/Images/Pasted%20image%2020260415163058.png)

### Kontrolloni për një numër

![Pasted image 20260415163130.png](/img/user/Semester%204/Images/Pasted%20image%2020260415163130.png)

## Raportimi i gabimeve në PHP

Ekzistojnë tre menyra kryesore të raportimit të gabimeve:
- error_reporting 
- display_errors 
- log_errors

### Vendosja e error_reporting

**Sintaksa error_reporting**, tregon cilin lloj të gabimit të raportoni.
Mund të vendoset në mënyrë programore brenda çdo fajlli PHP: `error_reporting(E_ALL);`
Mund të vendoset gjithashtu brenda fajllit php.ini: **error_reporting = E_ALL**

```php
<?php
// Çaktivizoni raportimin e gabimit
error_reporting(0);
// Raportoni gabimet e kohës së ekzekutimit
error_reporting(E_ERROR | E_WARNING | E_PARSE);
// Raportoni të gjitha gabimet
error_reporting(E_ALL);
// Njësoj si raportimi i gabimit (E_ALL);
ini_set("error_reporting", E_ALL);
// Raportoni të gjitha gabimet përveç E_NOTICE
error_reporting(E_ALL & ~E_NOTICE);
?>
```

### Vendsja e display_errors

**Cilësimi display_error** specifikon nëse mesazhet e gabimit duhet ose jo të shfaqen në shfletues. 
Mund të vendoset nëpërmjet funksionit **ini_set()**: `ini_set(' display_error ','0’);`
Mund të vendoset gjithashtu brenda fajllit php.ini: **display_error = Off**
### Vendosja e log_error

Vendndodhja për të ruajtur logs mund të caktohetnë mënyrë programore: 
`ini_set('error_log', '/restricted/my-errors.log’); `
Mund të vendoset gjithashtu brenda fajllit **php.ini**: **error_log = /restricted/my-errors.log**

Gjithashtu mund të dërgoni mesazhe në logs e gabimeve në çdo kohë nëpërmjet funksionit **error_log()**:
![Pasted image 20260415164527.png](/img/user/Semester%204/Images/Pasted%20image%2020260415164527.png)

## Trajtimi i gabimeve procedurale

Lidhja me një bazë të dhënash, mund të ketë një gabim...

![Pasted image 20260415164645.png](/img/user/Semester%204/Images/Pasted%20image%2020260415164645.png)

### Try, catch, finally

![Pasted image 20260415164745.png](/img/user/Semester%204/Images/Pasted%20image%2020260415164745.png)
### Metodat e objektit Exception

![Pasted image 20260415164815.png](/img/user/Semester%204/Images/Pasted%20image%2020260415164815.png)
![Pasted image 20260415165017.png](/img/user/Semester%204/Images/Pasted%20image%2020260415165017.png)

## Trajtuesit e personalizuar

`set_exception_handler('my_exception_handler');`

![Pasted image 20260415165126.png](/img/user/Semester%204/Images/Pasted%20image%2020260415165126.png)

## Regular Expressions- RegEx

![Pasted image 20260415165834.png](/img/user/Semester%204/Images/Pasted%20image%2020260415165834.png)

Sh. **308-9932** => `^\d{3}–\d{4}$`

Viza është një karakter i mirëfilltë; pjesa tjetër janë të gjitha metakaraktere
Simboli ^ dhe $ tregojnë fillimin dhe fundin e vargut,
Metakarakteri \d tregon një shifër, ndërsa metakarakteret {3} dhe {4} tregojnë respektivisht tre dhe katër përsëritje të ndeshjes së mëparshme (d.m.th., një shifër).

`^\d{3}–\d{4}$`
Një shprehje e rregullt më e sofistikuar për një numër telefoni nuk do të lejonte që shifra e parë në numrin e telefonit të ishte zero ("0") ose një ("1").Shprehja e rregullt e modifikuar për këtë do të ishte: 
`^[2-9]\d{2}–\d{4}$` 
Mund ta bëjmë shprehjen tonë të rregullt pak më fleksibël duke lejuar ose një hapësirë të vetme (440 6061), një pikë (440.6061) ose një vizë (440-6061) midis dy grupeve të numrave.Këtë mund ta bëjmë nëpërmjet metakarakterit \[ ]:
`^[2-9]\d{2}[–\s\.]\d{4}$`

```php
<?php
$email = "arion@gmail.com";

if (preg_match('/^[a-zA-Z0-9_\-\.]+@[a-zA-Z0-9\-]+\.[a-zA-Z0-9\-\.]+$/', $email)) { 
	echo "Email $email eshte valide.";
	echo "<br>";
} else {
	echo "Email $email nuk eshte valide.";
	echo "<br>";
}
?>
```

### Validimi PHP

![Pasted image 20260415170800.png](/img/user/Semester%204/Images/Pasted%20image%2020260415170800.png)
![Pasted image 20260415170821.png](/img/user/Semester%204/Images/Pasted%20image%2020260415170821.png)

# Klasat dhe objektet në PHP


```php
$now = new DateTime();
$nextWeek = new DateTime('today +1 week');

echo 'Now: '. $now->format('Y-m-d') ."\n";
echo 'Next Week: '. $nextWeek->format('Y-m-d') ."\n";
```

### Objektet e serverit dhe desktopit

Desktop app. mund të ngarkojë një objekt në memorie dhe ta përdorë atë për disa ndërveprime të përdoruesve, një objekt PHP ngarkohet në memorie vetëm për jetëgjatësinë e asaj kërkese HTTP. 

Ne duhet t'i përdorim klasat ndryshe sesa në botën e desktopit, pasi objekti duhet të rikrijohet dhe të ngarkohet në memorie 
- Ndryshe nga një desktop, ka potencialisht mijëra përdorues që bëjnë kërkesa menjëherë, kështu që jo vetëm që objektet shkatërrohen me përgjigjen ndaj çdo kërkese, por memoria duhet të ndahet midis shumë kërkesave të njëkohshme, secila prej të cilave mund të ngarkojë objekte në memorie ose per çdo kërkesë që e kërkon atë.

### Definimi i klasave

```php
class Artist { 
	public $firstName; 
	public $lastName; 
	public $birthDate; 
	public $birthCity; 
	public $deathDate; 
}
```

### Instanca e objekteve

```php
$dali = new Artist();
$picasso = new Artist();
```

Pasi të keni instancen e një objekti, mund të përdorni dhe modifikoni vetitë e secilit veçmas duke përdorur emrin e variables dhe një shigjetë (**->**).
```php
$picasso = new Artist(); 
echo $picasso->firstName= "Pabblo";
echo $picasso->lastName="Picasso"; 
echo $picasso->birthDate="Malaga";
echo $picasso->birthCity= "Octamber 25 1881";
echo $picasso->deathDate="April 8 1973";
```

### Konstruktorët

Në PHP, konstruktorët përcaktohen si funksione (siç do ta shihni, të gjitha metodat përdorin fjalën function) me emrin \_\_construct().
Në konstruktor çdo parametër i caktohet një variabli të brendshëm të klasës duke përdorur sintaksën $this->.

```php
function __construct($firstName,$lastName, $birthDate,$birthCity, $deathDate=null) { 
$this->firstName=$firstName; 
$this->lastName=$lastName; 
$this->birthDate=$birthDate; 
$this->birthCity=$birthCityl; 
$this->deathDate=$deathDate; 
}}

$picasso=new Artist("Pabblo" ,"Picasso","Malaga", "Octamber 25 1881","April 8 1973"); 
$dali= new Artist("Salvador","Dali","Figures","May 11 1904", "Jan 23 1989");
```

### Dekonstruktoret

\_\_destruct() është një metodë në PHP, e cila ekzekutohet automatikisht kur një objekt shkatërrohet ose kur nuk ka më referenca ndaj tij.

```php
class Example { 
public function __construct() {
	echo "Objekti u krijua! \n";
} 
public function __destruct() {
	echo "Objekti eshte fshi! \n";
} } 

// Krijojmë një objekt
$obj = new Example();
echo "Duke ekzekutuar kodin...\n"; 
// Kur skripta përfundon ose objekti nuk është më i nevojshëm, `__destruct()` ekzekutohet automatikisht.


public function __destruct() {
	$this->conn->close();
	echo "Lidhja me databazën u mbyll!\n";
}
```

## Metodat

Metodat janë si funksionet që I kemi mesuar, përveçse ato janë të lidhura me një klasë.
Ato përcaktojnë detyrat që çdo instancë e një klase mund të kryejë dhe janë të dobishme pasi lidhin sjelljen me objektet.

```php
class Artist
{
    public function outputAsTable() {
        $table= "<table>";
        $table .="<tr> <th colspan='2'>";
        $table .=$this->firstName." ".$this->lastName;
        $table .="</th></tr>";
        $table .="<tr><td>Birth: </td>";
        $table .="<td>".$this->birthDate."(".$this->birthCity.") </td></tr>";
        $table .="<tr><td> Death: </td>";
        $table .="<td>".$this->deathDate."</td></tr></table>";
        
        return $table;
    }
}


$picasso = new Artist( . . . )
echo $picasso->outputAsTable();
```

### Aksesueshmëria
Aksesueshmëria e një anëtari të klasës mund të vendoset si: 
- Publike prona ose metoda është e aksesueshme për cilindo që ka një referencë për objektin 
- Private vendos një metodë ose variabël që të jetë e aksesueshme vetëm brenda klasës 
- Protected lidhet me trashëgiminë…

![Pasted image 20260415202110.png](/img/user/Semester%204/Images/Pasted%20image%2020260415202110.png)

## Anëtarët statikë

- Një anëtar statik është një veti ose metodë që ndajnë të gjitha instancat e një klase. 
- Ndryshe nga një veti e zakonshme e instances, ku çdo objekt merr vlerën e vet për atë veti, për antëar statik ka vetëm një vlerë në një klase. 
- Anëtarët statikë përdorin sintaksën **self::** dhe nuk shoqërohen me një objekt 
- Ato mund të aksesohen pa ndonjë shembull të një objekti Artist duke përdorur emrin e klasës, domethënë nëpërmjet.
**Artist::$artistCount**

```php
class Artist {
    public $firstName;
    public $lastName;
    public $birthDate;
    public $birthCity;
    public $deathDate;
    public static $artistCount=0;
    function __construct($firstName,$lastName, $birthDate,$birthCity, $deathDate) {
        $this->firstName=$firstName;
        $this->lastName=$lastName;
        $this->birthDate=$birthDate;
        $this->birthCity=$birthCity;
        $this->deathDate=$deathDate;
        self::$artistCount ++;
}}
```

### Metoda statike

Aplikohet në metoda për t'i lejuar ato të thirren pa instantimin e klasës.
Kjo është metoda ekuivalente me konstante për klasë.
```php
class Math {
static function katroti($input) {
	return $input*$input; 
}}
echo Math::katroti(8);
```

#### Konstantet e klasës

`const EARLIEST_DATE = '1 janar 1200’;`
Qasja brenda dhe jashtë klasës duke përdorur 
- self::EARLIEST_DATE në klasë dhe 
- classReference::EARLIEST_DATE jashtë klase

```php
class Math { const pi = 3.14159; }
echo "Math::pi = ".Math::pi;
```

## Kapsulimi

Një mënyrë tjetër për të kuptuar kapsulimin: është fshehja e detajeve të implementimit të një objekti.
Nëse një klasë e kapsuluar siç duhet i bën vetitë e saj private, atëherë si t'i aksesoni ato? 
- getters 
- setters

```php
public function getFirstName() { 
	return $this->firstName; 
}
```

## Trashëgimia

Trashëgimia ju mundëson të krijoni klasa të reja PHP që ripërdorin, zgjerojnë dhe modifikojnë sjelljen që është përcaktuar në një klasë tjetër PHP. 
-  PHP ju lejon të trashëgoni vetëm nga një klasë në të njëjtën kohë 
- Një klasë që trashëgon nga një klasë tjetër thuhet se është një nënklasë ose një klasë e derivuar 
- Klasa nga e cila trashëgohet zakonisht quhet superklasë ose klasë bazë.

Një klasë PHP përcaktohet si një nënklasë duke përdorur fjalë “extends”.

`class Painting extends Art { . . . }`

```php
class A {
    public $attribute1;
    function operation1() { }
}

class B extends A {
    public $attribute2;
    function operation2() { }
}

$b = new B();
$b->operation1();
$b->attribute1 = 10;
$b->operation2();
$b->attribute2 = 10;

$a = new A();
$a->operation1();
$a->attribute1 = 10;
$a->operation2(); // Gabim
$a->attribute2 = 10; // Gabim
```

self:: referon gjithmonë klasën ku është shkruar metoda. 
static:: ndjek trashëgiminë dhe përdor metodën nga klasa që e thërret. 
Në këtë kod, B::test(); thërret versionin e whichclass() nga A për shkak të self::. 
Për të marrë whichclass() e B, duhet të përdorim static:: në test().

### Kopjimi objekteve
Fjala CLONE e cila ju lejon të kopjoni një objekt ekzistues
```php
$t = new B();
$a = clone $t;
```
Krijohet një kopje të objektit $t të së njëjtës klasë, me të njëjtat vlera per attribute.

```php
class Book {
    private $title;
    public function __construct($title) {
        $this->title = $title;
    }
}

$book = new Book("PHP Programming");
echo $book; // Gabim: Object of class Book could not be converted to string
  
  
class Book {
    private $title;
    public function __construct($title) {
        $this->title = $title;
    }
  
    // Metoda __toString() për të shfaqur objektin si tekst
    public function __toString() {
        return "Book Title: " . $this->title;
    }
}

$book = new Book("PHP Programming");
echo $book; // Do të printojë: Book Title: PHP Programming
```

## Krijimi i nje objekti

- **stdClass** është një klasë e paracaktuar dhe e thjeshtë në PHP që mund të përdoret për të krijuar objekte që mund të shtohen në mënyrë dinamike atributet. 
- Nuk ka metoda; është thjesht një objekt ku mund të shtoni vetë variabla. 
- Është e dobishme kur nuk nevojiten metoda të komplikuara, dhe kur duam të përdorim objekte të thjeshta. 
- Përdorimi i **stdClass** mund të jetë shumë i thjeshtë dhe fleksibël.

```php
// Krijohet një objekt i thjeshtë
$student = new stdClass();

// Shtohen variabla (atribute) në objekt
$student->name = "Ali";
$student->age = 21;
$student->course = "Computer Science";

// Printohet objektin
print_r($student);
```

### trait

```php
// Krijimi i një trait
trait Logger {
    public function log($message) {
        echo "[LOG]: " . $message . "<br>";
    }
}

// Krijimi i një trait tjetër
trait Notifier {
    public function notify($user) {
        echo "Notifying " . $user . "<br>";
    }
}

// Krijimi i një klase që përdor të dy trait-et
class User {
    use Logger, Notifier; // Përfshijmë të dy trait-et
    public function createUser($name) {
        echo "User $name created.<br>";
        $this->log("User $name was added to the system.");
        $this->notify($name);
    }
}

// Përdorimi
$user = new User();
$user->createUser("Dhuratë");
```

### Klasa abstakte

Nëse deklarojmë një klasë si abstrakte atëherë implementimi kryhet në nënklasën e cila trashigon mbiklasën.
Një klasë e cila përmban një metodë abstrakte është automatikisht një klasë abstrakte dhe duhet të deklarohet si abstrakte. 
Klasat abstrakte nuk mund të instancohen: 
- Vëtem nënklasat që kanë implementuar të gjitha metodat mund të instancohen.

```php
abstract class Art {
    private $name;
    private $artist;
    private $yearCreated;
    //… getters, setters

}
  
class Painting extends Art {
    private $medium;
    //…constructor, getters, setters
    public function __toString() {
        return parent::__toString() . ", Medium: ".$this->getMedium();
    }
}
```

## Polimorfizmi

Polimorfizmi është nocioni që një objekt mund të ofroj shumë gjëra në të njëjtën kohë.
![Pasted image 20260415210250.png](/img/user/Semester%204/Images/Pasted%20image%2020260415210250.png)

## Interfaces

Një ndërfaqe është një konstruksion klasik që përmban vetëm konstante dhe metoda abstrakte.
Në shumë mënyra, një ndërfaqe është e ngjashme me një klasë abstrakte, por qëllimi i një ndërfaqe është të specifikojë sjelljen për objektet.
```php
interface Viewable { 
	public function getSize();
	public function getPNG();
}
```

Në PHP, një klasë mund të thuhet se zbaton një ndërfaqe, duke përdorur fjalën implements: 
`class Painting extends Art implements Viewable { ... }`
![Pasted image 20260415211111.png](/img/user/Semester%204/Images/Pasted%20image%2020260415211111.png)
