# Case
Determine the most frequently occurring items in the sequence.

# Solution
User Counter from collections.

### Simple example
```python
from collections import Counter
data = [
    'foo',
    'foo1',
    'foo2',
    'foo3',
    'foo1',
    'foo1',
    'foo3',
]
    
data_counter = Counter(data)

# Return [('foo1', 3), ('foo3', 2), ('foo', 1)]
most_common = data_counter.most_common(3)
```
