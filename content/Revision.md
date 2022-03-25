# Revision om ML

## Python


` // ` rounds off the number to nearest integer. 5//2 = 2.5 -> 2; 6/2 = 3 ->  3

Useful functions: 
```
min()
max()
float()
int()
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
