# Classes and Recursion

## [Classes and Objects](https://www.learnpython.org/en/Classes_and_Objects)
```python
class Bike():

  wheels = 2

  def __init__(self,description)
    self.description = descritpion

  def pedal(self)
    print(self.description)
    print("We ride!")
```
- defined by class
- `__init__` is a special case that is used for intializing the instance of an object
  - in this case we can initialize a instance of `class Bike()` with a description by passing it in

- Accessing a class variable
```python

my_bike = Bike("sweet bike")
print(my_bike.wheels)  ==> 2
my_bike.pedal() ==> "sweet bike" "We ride!"
``` 
## [Recursion](https://realpython.com/python-thinking-recursively/)
- Recursion
  - a function that directly or indirectly calls/invokes itself
  - a way to break down functions into smaller pieces
- Building a recursive function
  - Decompose the original problem into smaller pieces
  - Work it down to a base case
    - Base case is the point at the top/bottom of the recursive pyramid
    - the point in which the function does not need to call the function to return an answer
```python

def fibbi(n):
  if n == 0 or n == 1:
    return 1
  else:
    return (fibbi(n-1)) + (fibbi(n-2))
```
    - the base case in this "case" is our first `if` statement
    - Once one of those conditions is met the interpreter will be able to collapse the expressions that called the function

- Maintaining State
  - Threading
    - continuing to pass the variable through the function
  - Global
    - have it as a global counter

## [Pytest](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)
- @pytest.fixture
  - a predefined testing function
    - can be run when ever you call it
- pytest-cov
  - a module that will give a coverage report for every part of the python library
