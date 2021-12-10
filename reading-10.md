# Stacks and Queues

## [Stacks and Queues](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

- ### Stack
  - built of nodes
    - value
    - and reference to next

- Terminology
  - Push - nodes going into a stack
  - Pop - nodes are being removed from a stack
  - Top - the node at the top of a stack
  - Peek - view the value of the top
  - isEmpty - returns true when a stack is empty

- Stack concepts
  - FILO
    - First In Last Out
    - Bottom of the stack has to wait to be the top to pop
  - LIFO
    - If the node is pushed and is the top it will be the next pop

- Push
  - same as adding to the end of a linked list at the moment except the top "head" is at the end as well

- Pop
  - similar to removimg the first node of a linked list but we want to return the value of the node as well
  - thus we need a temp variable in order to keep a reference to it
```python
def pop(self)
  temp_top = self.top
  self.top = self.top.next
  self.top.next = None
  return temp_top.value
```
- Peek
  - checking the top.value

- IsEmpty
  - return top = None

- ### Queue
- Common Terminology
  - Enqueue - Nodes to be add to queue
  - Dequeue - Nodes to be removed from the queue
  - Front - Front Node of queue
  - Rear - Last Node of queue (has a next of None)
  - Peek - view the value of the Front Node
  - IsEmpty - returns true if queue is empty

- Q Concepts
  - FIFO
    - First In First Out
    - The first person in line is the first person to enter the event
  - LILO
    - Last In Last Out
    - The last person in line is the last person to enter the event
- En q
  - adding a node to the end of the list
```python
def enqing(self)
  new_node = Node(value)
  self.rear.next = new_node
  self.rear = new_node
  return None
```

- De q
  - removing the front node and returning the value
```python
def de_q(self)
  temp_front = self.front
  self.front = self.front.next
  temp_front = None #Done to clear any reference to allow for clean up
  return temp_front.value
```

- Peek
  - look at the value of Front

- IsEmpty
  - check to see if there is a front