# Game of Greed

## [Random Module](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)
- the random number module for pyton
- `randint`
  - accepts two parameters (lowest, highest)
``` python
import random
print.random.randint(1,10)  ==> 2-10
```
- `random`
  - takes no argument and generates a random number between 0 -1
``` python
import random
random.random() * 10  ==> 0 - 10
```
- `choice`
  - takes a list as an argument
``` python
import random
the_list = ["marco", "polo", "travler"]
random.choice(the_list)  ==> "marco"|"polo"|"travler"
```
- `shuffle`
  - takes a list as an argument
``` python
import random
to_be_modified = [1,2,3,4]
shuffled_list = random.shuffle(to_be_modified)
print(shuffled_list) ==> [2,4,3,1]
```
- `randrange`
  - takes 2 or three
  - a start, a stop, and a step if wanted
``` python
import random
range = random.range(5,10, 2)
```

## [Risk Analysis](https://www.edureka.co/blog/risk-analysis-in-software-testing/)
- Risk
  - probability of an unwanted incident
- Risk Analysis
  - identifing potential or problematic area
  - creating a test plan
  - create tests
  - Preform Risk Analysis
    - searching the risk
    - analyzing the impact of each individual risk
    - measures for the risk identified
- Risk Identification
  - Business Risk
    - risk that come from company or customer
  - Testing Risk
    - problems with testing
  - Premature Release Risk
    - the effects of releasing an unsatisfactory product
  - Software Risks
    - associated with the software development process

## [Test Coverage](https://martinfowler.com/bliki/TestCoverage.html)
- it is about testing quality not quantity
- good coverage:
  - rarely get bugs that escape into production
  - rarely hesitant to change some code for fear it will cause production bugs
- Test Coverage tools:
  - good for finding untested code
  - not for making sure code is good

## [Big 0](https://www.youtube.com/watch?v=v4cd1O4zkGw)
- constant time beats linear time
- adding up the steps of a function
  - O(a) + O(b) = O(a+b)
- drop constants
  - O(2a) => O(n)
- different inputs  => different variagles
- Drop non-dominate terms
  - the parts that will most commonly running

