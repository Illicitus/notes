# Case
Sort the entries according to one or more of the dictionary values.

# Solution
Use *itemgetter* from *operator*.

### Simple example
```python
from operator import itemgetter

data = [
    {'fname': 'ffoo', 'lname': 'lfoo', 'id': 1},
    {'fname': 'ffoo3', 'lname': 'lfoo3', 'id': 4},
    {'fname': 'ffoo1', 'lname': 'lfoo1', 'id': 2},
    {'fname': 'ffoo4', 'lname': 'lfoo4', 'id': 5},
    {'fname': 'ffoo2', 'lname': 'lfoo2', 'id': 3},
]

"""
Return [
    {'fname': 'ffoo', 'lname': 'lfoo', 'id': 1},
    {'fname': 'ffoo1', 'lname': 'lfoo1', 'id': 2},
    {'fname': 'ffoo2', 'lname': 'lfoo2', 'id': 3},
    {'fname': 'ffoo3', 'lname': 'lfoo3', 'id': 4},
    {'fname': 'ffoo4', 'lname': 'lfoo4', 'id': 5},
]
"""
by_fname = sorted(data, key=itemgetter('fname'))

"""
Retrun [
    {'fname': 'ffoo', 'lname': 'lfoo', 'id': 1},
    {'fname': 'ffoo1', 'lname': 'lfoo1', 'id': 2},
    {'fname': 'ffoo2', 'lname': 'lfoo2', 'id': 3},
    {'fname': 'ffoo3', 'lname': 'lfoo3', 'id': 4},
    {'fname': 'ffoo4', 'lname': 'lfoo4', 'id': 5},
    ]
"""
by_id = sorted(data, key=itemgetter('id'))
```
