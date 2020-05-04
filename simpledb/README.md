A very simple database using shell script. 

## Add record

Add record has pretty good performance because appending to a file is generally very efficient.

`./simpledb.sh db_set 123456 '{"name":"London","attractions":["Big Ben","London Eye"]}'`

## Get record

`./simpledb.sh db_get 42`

Get function has terrible performance for large number of records. Every time you want to look up a key, db_get has to scan the entire database file from beginning to end, looking for occurrences of the key. In algorithmic terms, the cost of a lookup is O(n): if you double the number of records n in your database, a lookup takes twice as long. That’s not good.

## View records

`cat database`
