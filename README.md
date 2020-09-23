<div align="center">

## Learn MySQL thru PHP\! Easily and Quickly\! \(updated\!\)


</div>

### Description

This code teaches you how to connect and use a MySQL database thru PHP 3/4. Great for beginners! I update it, so the version on this page has no comments because the PSC butchers it alot, so if you would like an explanation of the code go here http://www.moddingcentral.com/~oblivion/ I dont think this is allowed but its for the better. If you want to copy and paste the code then do it thru this the PSC page.
 
### More Info
 
Learn to use MySQL thru PHP, explains basic PHP functions and introduces you to MySQL statments like INSERT, SELECT, UPDATE, DROP and DELETE and includes error checking

A php 3 or 4 server is required as well as a MySQL database that is accessible to you.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Piotr Sienkiewicz](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/piotr-sienkiewicz.md)
**Level**          |Beginner
**User Rating**    |4.6 (37 globes from 8 users)
**Compatibility**  |PHP 3\.0, PHP 4\.0
**Category**       |[Databases](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/databases__8-5.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/piotr-sienkiewicz-learn-mysql-thru-php-easily-and-quickly-updated__8-355/archive/master.zip)

### API Declarations

```
You can do whatever you want with this,
but if you believe it has helped you I
would appreciate a vote here at PSC
```


### Source Code

```
<?php
$connect = mysql_connect('localhost','username','password');
mysql_query("CREATE TABLE table1 (id INT (5) not null , name VARCHAR (32) not null )");
mysql_query("DROP TABLE table1");
mysql_query("CREATE TABLE table1 (id INT (5) not null , name VARCHAR (32) not null )") or die(mysql_error());
mysql_query("INSERT INTO table1 (id, name) VALUES ('1', 'name1')") or die(mysql_error());
mysql_query("INSERT INTO table1 (id, name) VALUES ('2', 'name2')") or die(mysql_error());
mysql_query("INSERT INTO table1 (id, name) VALUES ('3', 'name3')") or die(mysql_error());
mysql_query("INSERT INTO table1 (id, name) VALUES ('4', 'name4')") or die(mysql_error());
mysql_query("INSERT INTO table1 (id, name) VALUES ('5', 'name5')") or die(mysql_error());
$query = mysql_query("SELECT * FROM table1");
$query = mysql_query("SELECT id, name FROM table1");
while($rst = mysql_fetch_array($query)){
	print("$rst[id]<br>$rst[name]<br><br>");
}
$rst = mysql_fetch_array($query);
print("$rst[id]<br>$rst[name]<br><br>");
mysql_query("UPDATE table1 SET name = 'new_name1' WHERE id = '1'") or die(mysql_error());
mysql_query("DELETE FROM table1 WHERE id = '1' AND name = 'name1'") or die(mysql_error());
mysql_query("DELETE FROM table1") or die(mysql_error());
mysql_close();
?>
```

