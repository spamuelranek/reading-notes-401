# PAIN

## Big O

### [Pain and Suffering](https://codefellows.github.io/code-401-python-guide/curriculum/class-01/notes/pain_suffering)
- PAIN
  - This is one of the costs of the growth and learning
  - It has a purpose
  - This will be difficult
  - To learn you will be worse off in other areas of life temporarily
- SUFFERING
  - Not fun
  - Done without purpose
1. What’s your perspective?
  - The accepted norm which needs to be left in the past
2. Why are you doing this?
  - Because I needed something to do that was different
3. Do you want what comes at the end of this journey?
  - If it is jumping through very specific hoops for purposes that neither party cares about no, but if it involves a pretend amount of money then yes
4. Are you doing this for you?
  - It is only for me

### [Beginners Guide to Big 0](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation)
- O(1)
  - a task that will take the same amount of time/memory no matter the amount of inputs
  - e.g. adding to the front of a linked list
- O(N)
  - a task that will take an amount of time/memory that scales linearly in relation to the amount of inputs
  - e.g. moddifing each element in an array in a 1D array
- O(N^2)
  - a task that will take an amount of time/memory that will grow at the square in direct relation to the amount of inputs
  - e.g. moddifing each element in 2D or more array
- O(2^N)
  - a task that will take an amount of time/memory that will grow at an exponetial power of two in direct relation to the amount of inputs
  - e.g. the recursive calcuation of the fibonacci numbers (*Rob Bell- rob-bell.net*)
- O(log N)
  - a task that will take an amount of time/memory that will grow at a fractional rate in direct relation to the amount of inputs
  - e.g. a binary search that separates groupings in to halves repeatedly (*Rob Bell- rob-bell.net*)

### [A friendly intro to Big O Notation](https://www.codenewbie.org/basecs/8)
- Big O
  - a way of thinking about data structures and the ways to manipulate or traverse them
  - it is a classification system for understanding the resource management for a specific task
    - measures:
      - time
      - memory
    - both are finite and need to be treated as such... for now
  - As described in the Beginners Guide
    - Least cost of resources are 0(1)
    - Can be heaviest cose is 0(2^N)
  - Concept often comes tied in discussing linked lists
    - singely
      - contains data and reference to following data point in the list 
    - doublely
      - contains data and reference to both previous and following data point in the list
    - Because adding to the top of the stack of a linked list has a O of O(1)

### [Names and Values in Python](https://www.youtube.com/watch?v=_AEJHKGk9ns)
- Python
  - similar until different (duh)
  - dynamically typed
    - can store and value any time
- Names
  - refer to values
  - values live until no references
  - modification of values is present for all names
- Immutable values
  - strings, ints, floats, and tuples
    - can not be manipulated or mutated in place
- References
  - everything on the left side of the equal sign
  - obj attributes
  - list elements
  - Dict values and keys

[Return to Home](README.md)