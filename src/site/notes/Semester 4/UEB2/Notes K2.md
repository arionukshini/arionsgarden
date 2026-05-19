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
