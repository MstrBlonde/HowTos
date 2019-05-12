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
$stmt = $pdo->query('SELECT * FROM members');
```

## Fetch data

```php
while($row = $stmt->fetch(PDO::FETCH_ASSOC)) {
  echo $row['email'];
}
```

or fetch as an object:

```php
while($row = $stmt->fetch(PDO::FETCH_OBJ)) {
  echo $row->email;
}
```

## Set a default fetch attribute

```php
$pdo->setAttribute(PDO::ATTR_DEFAULT_FETCH_MODE, PDO::FETCH_OBJ);
```

## Fetch data with prepared statements

### Positional

```php
$email = 'mstrblonde@gmail.com';
$sql = 'SELECT * FROM members WHERE email = ?';
$stmt = $pdo->prepare($sql);
$stmt->execute([$email]);
$users = $stmt->fetchAll();
```
