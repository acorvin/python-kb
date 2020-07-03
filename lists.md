# Python: Lists

```python
colors = ['red', 'blue', 'yellow']

def is_long(colors):
    if len(colors) > 2:
      return 'Yes'

print(is_long(colors))
```

## "in" and "not" operators

```
print("fast" in "breakfast)")
# True
```

```
courses = ["python", "javascript", "deno", "vue"]

print("react" in courses)

if "react" not in courses:
print("That course is not here.")
```

## Indexing

```
print("alphabet"[5]) # b

fruits = ["apples", "oranges", "bananas", "peaches"]
```

### An index value of -1 will always print the last value no matter how long the list is.

```
print(fruits[-1]) # peaches
```

## Slicing Elements

### List elements are inclusive. If you want to output "oranges" AND "bananas", you would think you would select an index range of [1:2] however, since they are inclusive, it will print up to index 2 but not include it. You need to select one element highter, [1:3] in order to include the following index element.

```
print(fruits[1:3]) # ['oranges', 'bananas']
```

### Excluding 0 will yeild the same results. It is the start of the array. When there is no number, it means start at index 0.

```
print(fruits[0:3]) # ['bananas', 'peaches']

print(fruits[:3]) # ['bananas', 'peaches']
```

### Start at index 0 and go up to, but not including, the last value.

```
print(fruits[:-1]) # ['apples', 'oranges', 'bananas']
```

### If you end with a highter range than exists, Python will just go up to the last existing position.

### The program will only yeild an exception if you attempt to extract from a value that is out of range.

```
print(fruits[2:500]) # ['bananas', 'peaches']
```

### Go all the way to the end.

```
print(fruits[2:]) # ['bananas', 'peaches']
```

### Start at -4 from the end of the list and go up to but not include positon 2.

```
print(fruits[-4:-2]) # ['bananas', 'peaches']
```

### Start 2 from the end then go all the way to the end.

```
print(fruits[-2:]) # ['bananas', 'peaches']
```

### Skip forward by 2 in a list.

```
print(fruits[::2]) # ['apples', 'bananas']
```

### Skip backward by 2 in a list.

```
print(fruits[::-2]) # ['muffins', 'oranges']
```
