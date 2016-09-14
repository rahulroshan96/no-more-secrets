## db init scripts

mysql to mongo migration

## setup data migration automation script
configure **run_once_auto.js** and **cfg/index.js** \n
execute command:
```
mongo < run_once_auto.js
```
configure the new object id to **cfg/index.js**
@line: 92, **executed** must be name of document
```
collection.find({
    "executed": {
        "$exists": 1
    }
```
@line: 103, **executed** must be name of document
```
opts['last_executed_number'] = result[0].executed;
```
