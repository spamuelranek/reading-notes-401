# Graphs
## Yeah pictures
# No. They are data structures
## Yeah all graphs are
# But these you don't see
## what?

## [Graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)

- Keywords
  - vertex
    - a node with xero to more adjacent vertices
  - edge
    - An edge is a connection between two vertices
  - neighbor
    - neighbors are vertices connected by an edge
  - degree
    - number of edges connected to a vertex

### Directed vd Undirected
  - Undirected Graph
    - each edge is undirected or bi-directional
    - there is no specified direction of relationship between nodes

  - Directed Graphs(Digraph)
    - each edge has a direction
    - a specific relationship between vertexs

  - Different types of graphs
    - complete
      - all nodes have connections to all others
    - connected
      - all vertices has at least one edge
    -disconnected
      - not all vertices has at least one edge
    
### Acyclic vs Cyclic
  - Cycle
    - an ability to potentially end up at the vertex you started at when traversing the graph

  - Acyclic
    - directed graph with out cycles
    - undirected non-complete

  - Cyclic
    - a graph that has cycles

### How to "draw" a graph
- Adjacency Matrix
  - it is boolen table
  - dimensions of n * n (n is number of vertices)
``` python
adjacency_matrix = [[0,1,0],[1,0,0][0,0,0]]
```
  - this describes vertex a is connected to b but not c
  - c is an island
  - it is a disconnected graph

- Adjacency list
  - a list that has a linked list to describe all of the vertices that connect to each vertex(ie the element in a list)

```python
adjavency_list = [
  [{a}->{b}],
  [{b}->{a}],
  [{c}]
]
```

### Weighted Graphs
- Edges are assigned values
- Weight Matrix
  - adjacency matrix but instead of a boolean it is the weight associated with that edge
  - adjacency list with wieghts stores the node and the value associated with that edge

### Traversal
- Breadthe first
  - tips:
    - if graph has cycles possible to create infinit loops
    - need to create a `visited` collection to  checkif the node has been checked
``` python
def breath_first(vertex):
  nodes = []
  breadth = Queue()
  visited = set()

  breadth.enq(vertex)
  visited.add(vertex)

  while breadth is not None:
    front = breadth.deq()
    nodes.append(front)

    for child in front.Children:
      if child not in visited:
        visited.add(child)
        breadth.enq(child)

  return nodes
```
```python
def depth_first(vertex):
  nodes = []
  breadth = Stack()
  visited = set()
  
  breadth.push(vertex)

  while breadth is not is_empty():
    if breadth
    for child in vertex.children:
      if child not in visited:
        visited.add(vertex)

        breadth.push(child)
```
