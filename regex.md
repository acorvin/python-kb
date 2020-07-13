# Regular Expression operations
## https://docs.python.org/3/library/re.html

Python's built-in package "re" can be used to work with regular expressions.
```python
import re
```
Create a variable in which to store the data to be analyzed.
```
data = 'Call Max back. His number is 444-225-1111.'
```
Create a variable in which to store the regex sequences to be run. In this case, we will run a function which returns a match where the string contains digits. 
```
phone_num = re.compile(r'\d\d\d-\d\d\d-\d\d\d\d')
```
Create a variable which stores the search function which to be run on the data.
```
match_num = phone_num.search(data)
```
Output the results in a print statement.
```
print(match_num.group())
```