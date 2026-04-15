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

![Pasted image 20260414210252.png](/img/user/Pasted%20image%2020260414210252.png)

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

![Pasted image 20260414211301.png](/img/user/Pasted%20image%2020260414211301.png)

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

![Pasted image 20260414220337.png](/img/user/Pasted%20image%2020260414220337.png)

**trim()** largon hapësirat nga të dy anët e një string

![Pasted image 20260414220516.png](/img/user/Pasted%20image%2020260414220516.png)

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
![Pasted image 20260414221011.png](/img/user/Pasted%20image%2020260414221011.png)
![Pasted image 20260414221039.png](/img/user/Pasted%20image%2020260414221039.png)

### Përdorimi variablave superglobale
- PHP përfshin vargje të ndryshme globale të paracaktuara, të quajtura superglobale 
- Superglobalë përmbajnë informacione për klientin, serverin dhe mjedisin që mund t'i përdorni në skriptet tuaja 
- Superglobalë janë vargje shoqëruese –elementet e të cilëve referohen me një çelës alfanumerik në vend të një numri indeksi
![Pasted image 20260414221258.png](/img/user/Pasted%20image%2020260414221258.png)

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
![Pasted image 20260414230906.png](/img/user/Pasted%20image%2020260414230906.png)

Pasi të kemi mbaruar përdorimin e një fajlli, duhet të mbyllim atë, duke përdorur fclose() funksionon si më poshtë: `fclose($fp)`.

Funksioni flock() bllokon dhe liron një fajll:
![Pasted image 20260414233446.png](/img/user/Pasted%20image%2020260414233446.png)

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

![Pasted image 20260415132236.png](/img/user/Pasted%20image%2020260415132236.png)
![Pasted image 20260415133918.png](/img/user/Pasted%20image%2020260415133918.png)

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


