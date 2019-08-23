# Case
Find common keys, values, etc for two dictionaries.

# Solution
Use base operators and constructions.

# Simple example
```python
dc1 = {
    'a': 1,
    'b': 2,
    'c': 3,
}

dc2 = {
    'd': 4,
    'a': 5,
    'b': 2,
}

# Keys in common, return {'b', 'a'}
dc1.keys() & dc2.keys()

# Keys in dc1 that are not in dc2, return {'c'}
dc1.keys() - dc2.keys()

# Key, value pairs in common, return {('b', 2)}
dc1.items() & dc2.items()
```
