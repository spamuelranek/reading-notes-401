# Hash tables
## What are they and what do they do?

## Today we find out on the wild world of coding!

### Here's Your host Zaratalax

## [Intro to Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
- Hashtable
  - `hash`
    - the result of an algorithm coverting a string into a value
    - hashtable: is used to determine the index of an array
  - `buckets`
    - is what is contained at each index of the array
  - `collisiions`
    - one keygets hased to the same location of the hashtable

- What are they
  - Use Key-Value pairs
    - implemented with `Bucket` or `Node` 

  - hashing
    - it creates a integer value associated with a key
    - this allows for O(1) look up times because we will be able to give the key and the function will know what the index is.
    - need to manipulate the string to generate an integer. 
      - this should not be random

- Collisions
  - if a collision does occur
    - we can connect a node to the previously existing node and create a linked list

- Bucket Size
  - more buckets decrease the likelyhood of collisions but take up space with nothing

### Internal Methods
  - `add()`
    - send the key to `getHash` method
    - go to the generated index
      - if nothing exists there, add the key value pair
      - if something is there, add it to the existing data structure

  - `find()`
    - takes a key
    - sends the key to `getHash` method
    - iterate over the items at the index returned from `getHash`
  
  - `contains()`
    - takes a key
    - sends the key to `getHash`
    - go to the generated index. Iterate over the bucket contents to check if the key exists

  - `gethash`
    - will accept a key
    - will perform some operation on it
    - will return an index

### [Basics of Hash Tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)

### [What is a HashTable Data Structure](https://www.youtube.com/watch?v=MfhjkfocRR0)

### [Hash Table](https://en.wikipedia.org/wiki/Hash_table)