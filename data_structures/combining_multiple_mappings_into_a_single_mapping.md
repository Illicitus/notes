# Case
Combine into a single mapping to perform certain operations, such as looking up values or checking for the existence of keys.

# Solution
Use *ChainMap* from *collections*.

### Simple example
```python
from collections import ChainMap

dict1 = {'x': 1, 'z': 3}
dict2 = {'y': 2, 'z': 4}

com = ChainMap(dict1, dict2)

"""
First check in dict1, then in dict2.
"""

# Return 1
com['x']

# Return 2
com['y']

# Return 3
com['z']
```
