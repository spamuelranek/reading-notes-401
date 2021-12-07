# Python Scope

## [Python Scope](https://realpython.com/python-scope-legb-rule/)
- LEGB
  - Local
  - Enclosing
  - Global
  - Built-in

- Global
  - Available to all code
- Local
  - only available to code within scope

- Pyton scope
  - implemented as dictionaries
  - stored in the special attribute `.__dict__`

- Global Scope
  - dir() will show all names available in the python scope
  - `__main__`
  - varaibles that are assigned in a fuction are seen to be locally scoped even if they have the same name as a globally scoped variable

- Global Statement
  - `global`
    - keyword that maps a local variable on to a global variable
```python
var = "I can not be tamed as a global variable"
def are_you_sure():
  global var
  var = "You have been tamed"

are_you_sure()
print(var) ==> "You have been tamed"
``` 

- Non-local Statement
  - `nonlocal`
    - keyword that allows access to modifing a var outside the functions scope
``` python
def the_first_function():
  var = "This is only scoped for this function"
  def the_second_function():
    nonlocal var
    var = "It is now also scoped to this function"
  the_second_function()
  print(var)

the_first_function() ==> "It is now also scope to this function
```

- Closures
  - structred nested functions
``` python
def outer(some_punctuation)
  def inner(string)
    return string + some_punctuation
  return inner

exclaim = outer("!")
question = outer("?")
exclaim("Look over there") ==> "Look over there!"
question("Look over there") ==> "Look over there?"
```

## [Big O notation](https://www.youtube.com/watch?v=5Uqawfl0VHQ)
- Big O
  - worst case scenario

[Return to Home](README.md)