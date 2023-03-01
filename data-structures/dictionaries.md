# Dictionaries

Python dictionaries are an unordered collection of key-value pairs, where each key is unique. They are sometimes referred to as associative arrays, hash tables, or maps in other programming languages.
Creating a Dictionary

A dictionary can be created using curly braces {} or by using the built-in dict() function. Each key-value pair is separated by a colon : and multiple pairs are separated by commas.

```
# Using curly braces
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Using the dict() function
my_dict = dict(apple=2.5, banana=1.5, orange=3.0)
```

## Accessing Values

Values in a dictionary can be accessed by their corresponding keys. If the key is not present in the dictionary, a KeyError is raised.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Accessing a value
print(my_dict['apple'])  # Output: 2.5

# Raising KeyError for non-existent key
print(my_dict['mango'])  # Raises: KeyError: 'mango'

```

## Updating and Adding Elements

You can add a new key-value pair to a dictionary or update an existing value using the assignment operator =.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Adding a new key-value pair
my_dict['mango'] = 4.0
print(my_dict)  # Output: {'apple': 2.5, 'banana': 1.5, 'orange': 3.0, 'mango': 4.0}

# Updating an existing value
my_dict['apple'] = 3.0
print(my_dict)  # Output: {'apple': 3.0, 'banana': 1.5, 'orange': 3.0, 'mango': 4.0}

```

## Removing Elements

You can remove an element from a dictionary using the del keyword or the pop() method. The pop() method returns the value of the removed element.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Removing a key-value pair using del
del my_dict['orange']
print(my_dict)  # Output: {'apple': 2.5, 'banana': 1.5}

# Removing a key-value pair using pop
value = my_dict.pop('banana')
print(value)  # Output: 1.5
print(my_dict)  # Output: {'apple': 2.5}

```

## Iterating over a Dictionary

You can iterate over a dictionary using a for loop. By default, the loop iterates over the keys of the dictionary. To iterate over both keys and values, use the items() method.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Iterating over keys
for key in my_dict:
    print(key)

# Output:
# apple
# banana
# orange

# Iterating over keys and values
for key, value in my_dict.items():
    print(key, value)

# Output:
# apple 2.5
# banana 1.5
# orange 3.0

```

## Dictionary Methods

Python dictionaries have several built-in methods that can be used to manipulate and retrieve information from a dictionary. Some of the commonly used methods are:
keys()

The keys() method returns a view object that contains the keys of the dictionary.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Retrieving keys
keys = my_dict.keys()
print(keys)  # Output: dict_keys(['apple', 'banana', 'orange'])
```

values()

The values() method returns a view object that contains the values of the dictionary.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Retrieving values
values = my_dict.values()
print(values)  # Output: dict_values([2.5, 1.5, 3.0])
```

items()

The items() method returns a view object that contains the key-value pairs of the dictionary as tuples.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Retrieving items
items = my_dict.items()
print(items)  # Output: dict_items([('apple', 2.5), ('banana', 1.5), ('orange', 3.0)])

```

get()

The get() method returns the value of the specified key. If the key is not found, it returns the specified default value or None if no default value is provided.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Retrieving a value using get
value = my_dict.get('apple')
print(value)  # Output: 2.5

# Retrieving a non-existent key using get with default value
value = my_dict.get('mango', 0)
print(value)  # Output: 0

# Retrieving a non-existent key using get with no default value
value = my_dict.get('mango')
print(value)  # Output: None

```

clear()

The clear() method removes all the key-value pairs from the dictionary.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Clearing the dictionary
my_dict.clear()
print(my_dict)  # Output: {}

```

copy()

The copy() method returns a shallow copy of the dictionary.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Creating a copy of the dictionary
new_dict = my_dict.copy()
print(new_dict)  # Output: {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}
```

update()

The update() method updates the dictionary with the key-value pairs from another dictionary or iterable.

```
my_dict = {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}

# Updating the dictionary with another dictionary
my_dict.update({'mango': 4.0, 'grape': 2.0})
print(my_dict)  # Output: {'apple': 2.5, 'banana': 1.5, 'orange': 3.0, 'mango': 4.0, 'grape': 2.0}

```

## Dictionary Comprehension

Dictionary comprehension is a concise way to create dictionaries using an iterable. It is similar to list comprehension but instead of creating a list, it creates a dictionary.

```
# Creating a dictionary using dictionary comprehension
fruits = ['apple', 'banana', 'orange']
prices = [2.5, 1.5, 3.0]

my_dict = {fruits[i]: prices[i] for i in range(len(fruits))}
print(my_dict)  # Output: {'apple': 2.5, 'banana': 1.5, 'orange': 3.0}
```

Nested Dictionaries

Dictionaries can also contain other dictionaries as values, creating a nested dictionary.

```
# Creating a nested dictionary
person = {'name': 'John', 'age': 25, 'address': {'street': '123 Main St', 'city': 'New York', 'zip': '10001'}}
print(person)  # Output: {'name': 'John', 'age': 25, 'address': {'street': '123 Main St', 'city': 'New York', 'zip': '10001'}}

# Accessing values in a nested dictionary
print(person['address']['city'])  # Output: New York

```

Dictionaries are a powerful and flexible data structure in Python that allow you to store and retrieve data using key-value pairs. They are commonly used in many applications and can be manipulated and transformed using a variety of methods and techniques.
