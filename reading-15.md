# TREE

## [Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

### Common Terminology
- Node - value and reference to node/ or other nodes
- Root - not at the beginning
- K - max number of children a node can have
- Left - referece to the "left" child
- Right - same as Left but for "right"
- Edge - link between parent node and child node
- Leaf - Node that has no children
- Height - the amount of edges between the root and the furthest leaf

### Traversal
- Three common ways
- Pre-order
- In-order
- Post-order

- Pre-order
``` python
def pre_order(self, pre_order_list = []):

  pre_order_list.append(self.root.value)
  

  if self.root.left:
    pre_order(self.root.left, pre_order_list)

  if self.root.rigt:
    pre_order(self.root.right,pre_order_list)

  return pre_order_list
```

- In-order
``` python

def in_order(self, in_order_list = [])

  if self.root.left:
    in_order(self.root.left, in_order_list)

  in_order_list.append(self.root.value)

  if self.root.right:
    in_order(self.root.right,in_order_list)

  return in_order_list

```
- Post-order
```python
def post_order(self, post_order_list = [])

  if self.root.left:
    in_order(self.root.left, post_order_list)


  if self.root.right:
    in_order(self.root.right,post_order_list)

  post_order_list.append(self.root.value)

  return post_order_list

```

### Breadth First
- Integrates a queue into the traversal process

- breadthFirst

``` python
def breadth_first(self, root)

queue.enqueue(root)
breadth_list = []

while not queue.is_empty():

  next_node = queue.dequeue()

  breadth_list.append[next_node.value]

  if next_node.left:
    queue.enqueue(next_node.left)

  if next_node.right:
    queue.enqueue(next_node.right)
```

### K trees
- Can have max value of children
- Traversal is similar
