## db init scripts

mysql to mongo migration

## setup data migration automation script
configure **run_once_auto.js** and **cfg/index.js**, then
execute command:
```
mongo < run_once_auto.js
```
configure the new object id in **cfg/index.js** file

In **run_migration_auto.js** @line: 92, **executed** must be replaced with document name
```
collection.find({
    "<executed>": {
        "$exists": 1
    }
```
In **run_migration_auto.js**@line: 103, **executed** must be replaced with the document name
```
opts['last_executed_number'] = result[0].<executed>;
```
