
# Flattening a Nested List

This snippet recursively flattens a nested list, turning it into a single list of values, regardless of the depth of nesting.

## Code
```python
def flatten_list(nested_list):
    flat_list = []
    
    for item in nested_list:
        if isinstance(item, list):
            flat_list.extend(flatten_list(item))  # Recursive call for nested lists
        else:
            flat_list.append(item)
    
    return flat_list
```

## Usage
```python
nested_list = [1, [2, [3, 4], 5], 6]
print(flatten_list(nested_list))  # Output: [1, 2, 3, 4, 5, 6]
```
