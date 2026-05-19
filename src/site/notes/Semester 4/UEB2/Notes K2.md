---
{"dg-publish":true,"permalink":"/semester-4/ueb-2/notes-k2/"}
---

# Komunikimi me bazat e të dhënave PHP & MySQL

Programi (PHP) përcakton cilat të dhëna duhet të shfaqen, zakonisht duke përdorur informacionin nga kërkesat GET ose POST. 
Më pas, përdor një API të bazës së të dhënave për të bashkëvepruar me bazën e të dhënave. 
Megjithëse e njëjta ndarje mund të arrihet edhe duke ruajtur përmbajtjen në fajlla në server.

## API-ja e BAZËS SË TË DHËNAVE

API qëndron për ndërfaqen e programimit të aplikacionit dhe në përgjithësi i referohet klasave, metodave, funksioneve dhe variablave që aplikacioni juaj përdor për të kryer disa detyra.
Disa API të bazës së të dhënave funksionojnë vetëm me një lloj specifik të bazës së të dhënave; të tjerat janë cross-platform dhe mund të funksionojnë me baza të të dhënave të shumta

### Si te qasemi në DBMS
Megjithëse përfundimisht do të jeni në gjendje të manipuloni bazën e të dhënave nga kodi juaj PHP, ka disa operacione rutinë të mirëmbajtjes që nuk garantojnë kodin e personalizuar.
Mjetet përfshijnë: 
- Command Line Interface 
- phpMyAdmin 
- MySQLWorkbench

Për të nisur një sesion interaktiv të linjës së komandës MySQL, duhet të specifikoni hostin, emrin e përdoruesit dhe emrin e bazës së të dhënave për t'u lidhur siç tregohet më poshtë: 
**mysql -h 192.168.1.14 -u bookUser -p**

### AKSESIMI I MYSQL-së në PHP
Pavarësisht se çfarë API përdorni, algoritmi bazë i lidhjes së bazës së të dhënave është i njëjtë:
1. Lidhja me bazën e të dhënave. 
2. Trajtimi gabimeve. 
3. Ekzekutimi query te SQL. 
4. Rezultatet. 
5. Burime dhe lidhjet.

Të dy mysqli dhe PDO janë PHP extensions të përdorura për të hyrë dhe manipuluar bazat e të dhënave. 

Mysqli- MySQL Improved Extension (It is an object-oriented extension that provides both procedural and object-oriented APIs).

PDO (PHP Data Objects)-është një shtresë abstraksioni i bazës së të dhënave që ofron një API të unifikuar për të punuar me lloje të ndryshme të bazave të të dhënave, duke përfshirë MySQL, SQLite, Oracle, PostgreSQL dhe të tjera.

Lidhja me një bazë të dhënash me mysqli:
```php
$host = "localhost";
$database = "dbtest";
$user = "dhurata";
$pass = "123456";
$connection = mysqli_connect($host, $user, $pass, $database);
```
Lidhja me një bazë të dhënash me PDO:
```php
$connectionString = "mysql:host=localhost;dbname=dbtest";
$user = "dhurata";
$pass = "123456";
$pdo = new PDO($connectionString, $user, $pass);
```

### Ruajtja e te dhenave te lidhjes

```php
<?php
define('DBHOST', 'localhost');
define('DBNAME', 'dbtest');
define('DBUSER', 'dhurata');
define('DBPASS', '123456');

//perdorimi konstanteve 
require_once('protected/config.php');
$connection = mysqli_connect(DBHOST, DBUSER, DBPASS, DBNAME);
?>
```

### Trajtimi i gabimeve

Teknikat procedurale të mysqli përdorin deklarata të kushtëzuara (if...else).
Teknika PDO përdor try-catch e cila mbështetet në thrown exceptions kur ndodh një gabim.

#### Qasja Procedurale

Trajtimi i gabimeve të lidhjes me mysqli (versioni 1)
```php
$connection = mysqli_connect(DBHOST, DBUSER, DBPASS, DBNAME);
$error = mysqli_connect_error();
if ($error != null) {
	$output = "E pa mundur te qasemi n DB_Test" . $error;
	exit($output);
}
```

Trajtimi i gabimeve të lidhjes me mysqli (versioni 2)
```php
$connection = mysqli_connect(DBHOST, DBUSER, DBPASS, DBNAME);
if ( mysqli_connect_errno() ) {
	die( mysqli_connect_error() ); // die() e njejt me exit() 
}
```

#### Object-Oriented PDO me try-catch

```php
try { 
	$connectionString = "mysql:host=localhost;dbname=dbtest";
	$user = "root";
	$pass = "";
	$pdo = new PDO($connectionString, $user, $pass);
}
catch (PDOException $e) {
	die( $e->getMessage() ); 
}
```

##### Mënyrat e menaxhimit të gabimeve në PDO

- **PDO::ERRMODE_SILENT** 
	- Modaliteti i paracaktuar. 
	- PDO vetëm vendos kodin e gabimit pa shfaqur mesazh. 
	- Përdoret zakonisht kur aplikacioni është në përdorim normal. 
- **PDO::ERRMODE_WARNING**
	- Përveç kodit të gabimit, PDO shfaq edhe një mesazh paralajmërues. 
	- Është i dobishëm gjatë testimit dhe korrigjimit, sepse tregon problemet pa ndalur ekzekutimin e aplikacionit. 
- **PDO::ERRMODE_EXCEPTION** 
- *Përveç kodit të gabimit, PDO vendos një PDOException. Ky modalitet:* 
	- Jep informacion të detajuar për gabimin 
	- Ndërpret ekzekutimin në pikën ku ndodh gabimi 
	- Është shumë i dobishëm gjatë korrigjimit dhe zhvillimit

```php
try { 
	$connectionString = "mysql:host=localhost;dbname=dbtest";
	$user = "root";
	$pass = "";
	$pdo = new PDO($connectionString, $user, $pass); 
	// useful during initial development and debugging 
	$pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_WARNING , PDO::ERRMODE_EXCEPTION);
	.... 
}
```

## Ekzekutimi i Query

Ekzekutimi i një query SELECT (mysqli)
```php
$connection = mysqli_connect(DBHOST, DBUSER, DBPASS, DBNAME);
$sql = "SELECT * FROM tbl_llogin ORDER BY Emri";
$result = mysqli_query($connection, $sql);
```

Ekzekutimi i nje query SELECT (PDO)
```php
$sql = "SELECT * FROM tbl_llogin ORDER BY Emri";
$result = $pdo->query($sql);
```

### Përpunimi i Rezultateve për query

```php
$connectionString = "mysql:host=localhost;dbname=dbtest";
$user = "dhurata";
$pass = "123456"; $pdo = new PDO($connectionString, $user, $pass); $sql1 = "SELECT * FROM tbl_llogin ORDER BY Emri";
$result1 = $pdo->query($sql1);
while ($row = $result1->fetch()) {
	echo $row['id'] . "-" . $row['Emri'] ."-". $row['Mbiemri'];
	echo "<br/>";
}
```
![Pasted image 20260519093218.png](/img/user/Pasted%20image%2020260519093218.png)

### Funksionet e marrjes 👀

![Pasted image 20260519103402.png](/img/user/Pasted%20image%2020260519103402.png)

```php
$row = $result->fetch(); 
$rows = $result->fetchAll(); 
$obj = $result->fetchObject(); 
$row = mysqli_fetch_assoc($result);
```

```php
class login { 
	public $ID;
	public $Emri;
	public $Mbiemri;
	public $Adresa;
	public $Vendbanimi; 
} 
$connectionString = "mysql:host=localhost;dbname=dbtest";
$user = "dhurata"; 
$pass = "123456"; 
$pdo = new PDO($connectionString, $user, $pass); 
$sql1 = "SELECT * FROM tbl_llogin ORDER BY Emri"; 
$result1 = $pdo->query($sql1); 

while ($r=$result1->fetchObject("llogin")) { 
	echo 'ID: '.$r->id."<br/>"; 
	echo 'Emri: '.$r->Emri."<br/>"; 
	echo 'Mbiemri: '.$r->Mbiemri."<br/>"; 
	echo 'Adresa: '.$r->Adresa."<br/>"; 
	echo 'Vendbanimi: '.$r->Vendbanimi."<br/>"; 
}
```

![Pasted image 20260519103738.png](/img/user/Pasted%20image%2020260519103738.png)

```php
class login { 
	public $ID;
	public $Emri;
	public $Mbiemri;
	public $Adresa;
	public $Vendbanimi;
	function __construct($record) {
		$this->ID=$record["id"]; 
		$this->Emri=$record["Emri"];
		$this->Mbiemri=$record["Mbiemri"];
		$this->Adresa=$record["Adresa"];
		$this->Vendbanimi=$record["Vendbanimi"]; 
	} 
} 

$sql1 = "SELECT * FROM tbl_llogin ORDER BY Emri";
$result1 = $pdo->query($sql1);

while ($row=$result1->fetch()) {
	$p = new login($row);
	echo 'ID: '.$p->ID."<br>";
	echo 'Emri: '.$p->Emri."<br>";
	echo 'Mbiemri: '.$p- >Mbiemri."<br>";
	echo 'Adresa: '.$p- >Adresa."<br>";
	echo 'Vendbanimi: '.$p- >Vendbanimi."<br>";
	echo '<hr>'; 
}
```

### Mbyllja e lidhjes

```php
$host = "localhost";
$database = "dbtest";
$user = "dhurata";
$pass = "123456";
$connection = mysqli_connect($host, $user, $pass, $database);
$result = mysqli_query($connection, "SELECT * FROM tbl_llogin ORDER BY Emri");
// lironi kujtesën e përdorur nga grupi i rezultateve.
//Kjo është e nevojshme nëse do të ekzekutoni një query tjetër në këtë lidhje 
mysqli_free_result($result);
mysqli_close($connection);


$connectionString = "mysql:host=localhost;dbname=dbtest";
$user = "dhurata";
$pass = "123456";
$pdo = new PDO($connectionString, $user, $pass);
$pdo = null;
```

## Shembull i pasigurt

```php
$username = $_POST['username']; 
$sql = "SELECT * FROM users WHERE username = '$username'"; 
$result = $pdo->query($sql);
```

## Shembull i sigurt

```php
$username = $_POST['username']; 
$sql = "SELECT * FROM users WHERE username = ?"; 
$stmt = $pdo->prepare($sql); 
$stmt->execute([$username]);
```

**prepare()** krijon query-n me placeholder. 
**execute()** vendos vlerat reale në mënyrë të sigurt. 
Kjo e mbron aplikacionin nga SQL Injection.

## Puna me parametrat

```php
<?php
include_once 'db.php';
//duke shfrytezuar PDO 
$sql = "UPDATE tbl_Kategoria SET Pershkrimi='Biznes' WHERE Pershkrimi='Web'";
$count = $pdo->exec($sql);
echo "<p>U modifikua me suksese " . $count . " rreshti</p>";

//duke shfrytezuar mysqli()
$sql = "UPDATE tbl_Kategoria SET Pershkrimi='Web' WHERE Pershkrimi='Biznes'";
if ( mysqli_query($con1, $sql) ) { 
	$count = mysqli_affected_rows($con1); 
	echo "<p>U modifikua me suksese " . $count . " rreshti</p>"; 
} 
?>
```


```php
$from = $_POST['old']; 
$to = $_POST['new']; 
$sql = "UPDATE tbl_Kategoria SET Pershkrimi= '$to' WHERE Pershkrimi= '$from'"; 
$count = $pdo->exec($sql);
```
Ndërsa kjo funksionon, ajo hap faqen tonë në një nga sulmet më të zakonshme të sigurisë në ueb, “SQL injection attack”.

## Ilustrim i SQL injection

![Pasted image 20260519123123.png](/img/user/Pasted%20image%2020260519123123.png)

### Pastrimi i të dhënave të përdoruesve

Në MySQL, hyrjet e përdoruesit mund të pastrohet në PHP duke përdorur metodën **mysqli_real_escape_string()** ose, nëse përdorni PDO, metodën **quote()**
```php
$from = $pdo->quote($_POST['old']);
$to = $pdo-> quote($_POST['new']);
$sql = "UPDATE tbl_Kategoria SET Pershkrimi=$to WHERE Pershkrimi=$from";
$count = $pdo->exec($sql);
```

### Deklarata të përgatitura

```php
$stmt = $conn->prepare("INSERT INTO tbl_Profesori (emri, mbiemri, email) VALUES (?, ?, ?)"); 
$stmt->bind_param($firstname, $lastname, $email); 

// set parameters and execute
$firstname = "John"; 
$lastname = "Doe"; 
$email = "john@example.com"; 
$stmt->execute(); 

$firstname = "Julie"; 
$lastname = "Dooley"; 
$email = "julie@example.com"; 
$stmt->execute(); 

echo “Rekordi ri eshte ruajtur me sukses!"; 
$stmt->close(); 
$conn->close();
```
```php
$id = $_GET['id'];
$sql = "SELECT Title, CopyrightYear FROM Books WHERE ID=?"; 
// krijoni një deklaratë të përgatitur
if ($statement = mysqli_prepare($connection, $sql)) { 
	// lidhja e parametrave s - string, b - blob, i - int, etc 
	mysqli_stmt_bindm($statement, 'i' , $id); 
	// ekzekutimi 
	mysqli_stmt_execute($statement);
	...
```

#### PDO

```php
$id = $_GET['id']; 

/* metoda 1: ?- parameter */ 
$sql = "SELECT Title, CopyrightYear FROM Books WHERE ID = ?";
$statement = $pdo->prepare($sql); 
$statement->bindValue(1, $id);
$statement->execute(); 

/* metoda 2 */ 
$sql = "SELECT Title, CopyrightYear FROM Books WHERE ID = :id"; 
$statement = $pdo->prepare($sql); 
$statement->bindValue(':id', $id); 
$statement->execute();
```

### Përdorimi i transaksioneve

#### MySQLi
```php
$result1 = mysqli_query($conn1, "INSERT INTO tbl_Kategori (Pershkrimi) VALUES ('Histori')"); 
$result2 = mysqli_query($conn1, "INSERT INTO tbl_Kategori (Pershkrimi) VALUES ('Art')"); 
if ($result1 && $result2) { 
	/* commit transaction */ 
	mysqli_commit($conn1); 
} else {
	/* rollback transaction */ 
	mysqli_rollback($conn1);
}
```

#### PDO
```php
$pdo = new PDO($connString,$user,$pass); 
$pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
 
try { 
	// begin a transaction 
	$pdo->beginTransaction(); 
	$pdo->query("INSERT INTO Categories (CategoryName) VALUES('Philosophy')"); 
	$pdo->query("INSERT INTO Categories (CategoryName) VALUES ('Art')"); 
	$pdo->commit(); 
} catch (Exception $e) { 
	$pdo->rollback(); 
}
```

### Lista me lidhje

![Pasted image 20260519125421.png](/img/user/Pasted%20image%2020260519125421.png)

```php
$sql = "SELECT * FROM Categories ORDER BY CategoryName"; 
$result = $pdo->query($sql); 
while ($row = $result->fetch()) { 
	echo '<li>'; 
	echo '<a href="list.php?category='. $row['ID']. '">';
	echo $row['CategoryName'];
	echo '</a>';
	echo '</li>'; 
}
```

## Fajlli për konektim, db.php

```php
<?php
//Menyra I
$host="localhost";
$database="dbtest";
$user="root";
$pass="123456";
$con1=mysqli_connect($host, $user,$pass,
$database);
if(!$con1) {
	die('Gabim:' .mysqli_connect_error());
}

//Menyra II 
try { 
	$con2="mysql:host=localhost;dbname=dbtest";
	$user1="root"; 
	$pass1="123456"; 
	$pdo=new PDO($con2,$user1,$pass1);
} catch (PDOExeption $th) {
	die( $th->getMessage()); 
} 
?>
```

# Menaxhimi Applikacionit (Përdorimi i kontrollit të Sesioneve dhe Cookies në PHP)

Një faqe ueb mund të kalojë informacionin e vargut të query nga shfletuesi te serveri duke përdorur njërën nga dy metodat: 
- një varg pyetjesh brenda URL-së (GET) dhe 
- një varg pyetjesh brenda header së HTTP (POST)

Fillimisht, modeli Request / Response ishte pa gjendje (stateless) – të gjithë shfletuesit dukeshin njësoj. Kjo ishte shumë problematike dhe zgjati shumë pak, pasi nuk lejonte personalizim apo ruajtje të gjendjes së përdoruesit.

# Cookies

**Cookies** - nga ana e klientit për gjendjen e vazhdueshme të informacionit. 
Janë emër=vlerë që ruhen brenda një ose më shumë fajlla teksti që menaxhohen nga shfletuesi. 
Cookies janë një zgjidhje e ndryshme për problemin e ruajtjes së gjendjes në një numër transaksionesh, ndërkohë që kanë ende një URL të pastër. 
Një cookies është një pjesë e vogël e informacionit

### Pse Cookies?

Ndërsa informacioni i cookie-ve ruhet dhe merret nga shfletuesi, informacioni në një cookie udhëton brenda /heder së HTTP. 
- Faqet që përdorin cookie nuk duhet të varen nga disponueshmëria e tyre për veçori kritike.
- Përdoruesi mund të fshijë cookie-t ose t’i ndryshoj ato. 

Mund të vendosni një cookie në makinën e një përdoruesi duke dërguar një hedera HTTP që përmban të dhëna në formatin e mëposhtëm:
**Set-Cookie: name=value; \[expires=date;\] \[path=path;\] \[domain=domain_name;\] \[secure;\] [HttpOnly]**

Një sesion nuk ka deklarat skadence dhe kështu do të fshihet në fund të sesionit të shfletimit të përdoruesit. 
Cookie-t e vazhdueshme kanë një datë skadimi të specifikuar;

```php
$name = "perdoruesi"; 
$value = "test"; 
setcookie($name, $value);
```

```php
<?php
$e = time()+60*60*24;
$name = "perdoruesi";
$value = "test";
setcookie($name, $value, $e);

//Ose

setcookie("TestCookie", $value, strtotime( '+30 days' ) );
?>
```

```php
<?php
$expiryTime = time()+60*60*24;
$name = "perdoruesi";
$value = "test";
setcookie($name, $value, $expiryTime);
if( !isset($_COOKIE['perdoruesi']) ) {
	//nuk eshte valid
}
else {
	echo "Emri i përdoruesit i marrë nga cookie është: ";
	echo $_COOKIE['perdoruesi'];
}
?>
```

```php
setcookie($cookie_name, $cookie_value, time() + (86400 * 30)); 

setcookie($cookie_name, $cookie_value, time() + (86400 * 30), "https://fiek.uni-pr.edu/"); 

setcookie("user", "", time() - 3600); //fshirja e cookies
```

## Sessionet

Çdo sesion i shfletuesit ka gjendjen e vet të sesionit, e cila: 
- Ruhet në server si një file i serializuar 
- Deserializohet dhe ngarkohet në memorie sa herë që bëhet një kërkesë nga përdoruesi
Kjo lejon që aplikacioni të rivendosë gjendjen e përdoruesit pa ruajtur informacion në anën e klientit.

Të gjitha mjediset moderne të zhvillimit ofrojnë mekanizma për gjendjen e sesionit. 
Gjendja e sesionit është një mekanizëm i bazuar në server, që mundëson: 
- Ruajtjen dhe marrjen e objekteve të çdo lloji për çdo përdorues individual. 
- Menaxhimin e të dhënave komplekse të lidhura me një sesion specifik. 
Shembull në PHP: 
- Variablat e sesionit ruhen në **$\_SESSION** 
- Aktivizimi i sesionit bëhet me funksionin **session_start()**

```php
session_start();
$_SESSION['session_var'] = "PHP!";
echo 'Permbajtja e '.$_SESSION['session_var'].' eshte ' .$_SESSION['session_var'].'<br>';
```

Sesionet në PHP identifikohen me një ID unike të sesionit 32 bajt. Kjo transmetohet mbrapa dhe me radhë midis përdoruesit dhe serverit nëpërmjet një cookies sesioni.

Një server kryesor përpunon të gjitha kërkesat. 
Ruajtja e sesionit është më e thjeshtë (në memorie ose në fajlla). 
Nuk ka problem me konsistencën, sepse të gjitha kërkesat kalojnë përmes të njëjtit server.

```php
<?php
// Tell PHP we won't be using cookies for the session
ini_set('session.use_cookies', '0');
ini_set('session.use_only_cookies',0);
ini_set('session.use_trans_sid',1);
session_start();
// Start the view
?>

<p><b>No Cookies for You!</b>/p>
```

# AJAX