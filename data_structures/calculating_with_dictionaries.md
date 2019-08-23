# Case
Calculations on a dictionary of data.

# Solution
Use *zip* function.

### Simple example
```python
prices = {
    'foo': 11.11,
    'foo1': 12.12,
    'foo2': 13.13,
    'foo3': 14.14,
}

# Return (11.11, 'foo')
min_price = min(zip(prices.values(), prices.keys()))

# Return (14.14, 'foo3')
max_price = max(zip(prices.values(), prices.keys()))

# Return [(11.11, 'foo'), (12.12, 'foo1'), (13.13, 'foo2'), (14.14, 'foo3')]
sorted_prices = sorted(zip(prices.values(), prices.keys()))
```

### Advances example
```python
prices = {
    'foo': 11.11,
    'foo1': 12.12,
    'foo2': 13.13,
    'foo3': 14.14,
}

# Return 11.11
min_value = prices[min(prices, key=lambda k: prices[k])]
```
