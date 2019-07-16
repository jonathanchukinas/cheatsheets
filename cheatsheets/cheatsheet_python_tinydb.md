# TinyDB (Python ) Cheatsheet

```python
from tinydb import TinyDB, Query
db = TinyDB('db.json')
db.insert(<dict>)
db.all()
```

## Queries
```
Fruit = Query()
db.search(Fruit.type == 'peach')
db.search(Fruit.count > 5)

db.update(<dict>, <query>)
db.update({'count': 10}, Fruit.type == 'apple)

db.remove(Fruit.count > 6)

db.purge()
```
