# PDO Cheatsheet

## Create variables for sql

```php
$host="localhost";
$user="mhs_user";
$password="";
$dbname="users";
```

## Set the DSN

```php
$dsn = 'mysql:host=' . $host . ';dbname=' . $dbname;
```

## Create a PDO instance

```php
$pdo = new PDO($dsn, $user, $password);
```

## PDO QUERY

```php
$stmt = $pdo->query('SELECT * FROM users');
```
