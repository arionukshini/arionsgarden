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

Idk bro i think its time to wrap ts up