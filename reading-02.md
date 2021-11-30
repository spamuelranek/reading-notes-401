# TESTS, MAIN, RECURSION

## [TESTs](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)
- Tests are not the enemy
  - In fact they are the friend
- TEST DRIVEN DESIGN
  - Design the feature test
  - Run and fail test
  - Code the most basic feature
  - Pass the test
  - Refactor code to trully fulfill feature
- This design process requires making bite size pieces to work on
- Makes the design in the forfront and regular testing to fulfill the overall process

## [If __name__ equals __main__](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)
- A piece of code built for modulization
- It helps to define its functionality
  - If __name__ == "__main__":
  - things defined in side the code block of the if statement
    - will only be run if specifically invoked
    - otherwise other defined things will be run

## [Recursion](https://www.geeksforgeeks.org/recursion/)
- a function that calls itself directly or indirectly
- Base Case
  - The kernal of truth at the base of the recursion tower
  - It is the point where the recursion is not required to return a value
  - If no base case is set or if it is not reacable then
    - CREATE INFINITE LOOP and STACKOVER FLOW
  
[Return to Home](README.md)