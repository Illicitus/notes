# Case
Make a list of the largest or smallest N items in a collection.

# Solution
Use functions *nlargest* and *nsmallest* from *heapq* module.

### Simple example
```python
import heapq

col = [1, 3, 4, 5, -29]

# Return [5, 4, 3]
heapq.nlargest(3, col)

# Return [-29, 1, 3]
heapq.nsmallest(3, col) 
````

### Advanced example
```python
import heapq

data = [
  {'name': 'foo', 'value': 10, 'value1': 11},
  {'name': 'foo1', 'value': 100, 'value1': 110},
  {'name': 'foo2', 'value': 1000, 'value1': 1100},
]

expensive = heapq.nlargest(3, data, key=lambda s: s['value1'])
cheap = heapq.nsmallest(3, data, key=lambda s: s['value1'])
```
