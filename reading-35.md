# Pythonistas Assemble!

## Pythonisms

## [Dunder Methods](https://dbader.org/blog/python-dunder-methods)
- `dunder methods` are a special type of method that allows access to the way python as a whole looks at your new class
- the three most common:
  - `def __init__`
    - which helps set things up on the intial creation of an instance of a class
  - `def __str__`
    - which allows for a str() to be called on the object and to return a human readable string
  - `def __repr__`
    - which allows for repr()  to be called on the objext and to return an "offical" representation of the object

- Other interesting ones is:
  - `__getitem__` which allows for the object to be iterated over using a for loop and access via bracket notation

## [Iterators](https://dbader.org/blog/python-iterators)
- `iterators`
  - `__iter__` and `__next__` are the building blocks of iterables built from scratch
  - allows for better encapsulation
    - the ability to manipulate and read data with in an object
  - iterators will raise a StopIteration Error if a next() is called and there is no more things to iterate

## [Generators](https://dbader.org/blog/python-generators)
- "Generators look like regular functions but instead of using the return statement, they use yield to pass data back to the caller"
- generators
  - uses the yield operator
    - temporarialy passes control back to calling function
    - maintains individual state
    
[Return to Home](README.md)