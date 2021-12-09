# Dunderhead you statistically can not be this wrong
# I just guessed
# Thats what I mean, a bouncy ball has better odds in getting something right 

## [Dunder Methods](https://dbader.org/blog/python-dunder-methods)
- Dunder refers to `__`
  - these are existing methods that can be rewritten to meet a desired behavior

```python

class One_fast_car:

  def __init__(self,name):
    self.name = name

  def __str__(self):
    return f"That {self.name} is so fast"

fast_car = One_fast_car("speedy")
which_is_so_fast = str(fast_car)
print(which_is_so_fast) ==> "That speedy is so fast"
```
``` python

class This_has_a_value:
  def __init__(self, value):
    self.value = value

  def __lt__(self,other):
    return self.value < other.value

first = This_has_a_value(5)
second = This_has_a_value(8)

first < second  ==> True
```
## [Probability](https://www.dataquest.io/blog/basic-statistics-in-python-probability/)
- The chance of an event happening
- example given that is very poorly formatted
```python
import random
def coin_trail():
  heads = 0
  for i in range(100):
    if random.random() <= 0.5:
      heads += 1
  return heads

def simulate(n):
  traials = [] 
  for i in range(n):
    trails.append(coin_trial())
  return(sum(trials)/n)

simulate(10) ==> 5.4

```

- Central Limit Theorem
  - with a greater n value of trails we get closer to the ideal probability

- Three Sigma Rule
  - describes the amount of data one standard deviation (sigma) away from the mean.

- Z score
  - `z = (data_point_in_question - the_mean)/the_standard_deviation`

   


