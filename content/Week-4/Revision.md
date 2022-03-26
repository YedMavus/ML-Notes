---
title: "Revision"
date: 2022-03-26 00:00:00 +0000
katex: true
---
# Revision on ML

## Python


` // ` rounds off the number to nearest integer. 5//2 = 2.5 -> 2; 6/2 = 3 ->  3

Useful functions: 
```
min()
max()
float()
int()
round(num, <no of decimal places>)

```
How to declare custom functions? 
an example:
```
def mult_by_five(x):
    return 5 * x
```
etc

```
def mod_5(x):
    """Return the remainder of x after dividing by 5"""
    return x % 5

print(
    'Which number is biggest?',
    max(100, 51, 14),
    'Which number is the biggest modulo 5?',
    max(100, 51, 14, key=mod_5),
    sep='\n',
)
```
Here, max returns the largest of its arguments. But if we pass in a function using the optional key argument, it returns the argument x that maximizes key(x) (aka the 'argmax').



If else:

```
if x == 0:
        print(x, "is zero")
elif x > 0:
...
else
...
```


### Lists

AKA Array

Can consist of same or different types, and even of diff lists itself

`primes = [2, 3, 5, 7]`
indexing starts from 0.
Index -1 returns the last element, -2 the second last and so on.

Slicing:

In indexing, 
`0:3` or `:3` is a way of returning  index 0 and continuing up to but not including index 3.

List functions:

- `len()` gives length of list
- `sorted()` sorts list in alphabetical order
- `sum()`
- `max()` etc
- `list.append()` adds sth to list at the end
- `list.pop()` removes last element of list
- To declare an empty list A, `A = []`
- For n^x, use `n**x`
- `loud_short_planets = [planet.upper() + '!' for planet in planets if len(planet) < 6]`

Strings and Dictionary

- Useful string functions: `str.upper()`; `str.lower()`; `str.index("some string")`: Searches for the first index of substring in quotes; `str.startswith()` ; `str.endswith()`; `str.split()`: Breaks string by whitespaces into a list. When some character is given in quotes as attributes to the function, the breakage occurs at the occurence of that character; `"/".join([month,day,year])` outputs `'26/03/22'`; `"{}, you'll always be the {}th planet to me.".format(planet, position)` outputs `"Pluto, you'll always be the 9th planet to me."`;
- https://docs.python.org/3/library/string.html#formatstrings
- https://pyformat.info/
- **Dictionaries** are a built-in Python data structure for mapping keys to values.


