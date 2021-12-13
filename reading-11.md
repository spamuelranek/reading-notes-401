# DATA ANALYSIS

## [What is Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html)

- JupyterLab is a workspace
  - It allows for the use of several different formats of files at text.
  - Allows for making interactive pieces of code while also leaving text structure on the page as well.
  - Creating cells is the way to add and subtract content to the "notebook"
  - Common keyboard shortcuts:
    - `c` - copy
    - `v` - paste
    - `x` - cut
    - `z` - undo
    - `shift +` - redo
    - `a` add a cell above
    - `b` add a cell below
    - `dd` to delete a cell
    - `y` to change a cell format to code
    - `m` to change a cell format to markdown
    - `shift+enter` to run code/ display markdown
  - Kernel will be the interpreter you choose to use in your code

## [NumPy](https://www.dataquest.io/blog/numpy-tutorial-python/)

### NumPy: Data Analysis with Python
- csv: older tradiontional format
  - delimiter separated value more generic type now
  - to be able to read these values

``` python
import csv
with open("kickpower-sam.csv","r") as kicker:
  kicks = list[csv.reader(f, delimiter= ";")]

print(kicker) ==> [Listof[Lists][Lists]]
```

|kick #|Power of Kick|How much concrete it could damage|
|---|---|---|
|1|1100 k/js|2 in|
|2|4500 k/js|4.5 in|
|3|9500 k/js|8.8 in|
|4|11000 k/js|No Concrete remained|

- To build in NumPy
```python
import csv
with open("kickpower-sam.csv","r") as kicker:
  kicks = list[csv.reader(f, delimiter= ";")]
import numpy as numpy
kicks_reformatted = numpy.array(kicks[1:], dtype = numpy.float)
```
- After that `kicks_reformatted` will be a two demesional array
- NumPy does it fast than python
- Numpy lists act similiarly to regular python lists
  - targeting specific cells
  - slices
  - additional using `:` to gather an entire column
    - `kicks_reformatted[:,2]` would return the concrete damage column
  - can do the opposite to gather an entire row
    - `kicks_reformtatted[3,:]` would return the third kick

- Data Types
  - float - numeric floating point data
  - int - interger data
  - string - character data
  - object - Python objects

- Array Math Operations
  - Array * some_integer of float
    - returns an new array with that operation applied to each element
  - Array += some_integer of float
    - changes array in place
  - can only run these operations if the dimensions of the array are compatiable
    - either the trailing dimensions are equivalent
    - one of them is one

- Other NumPy Array Functions
  - `sum` NumPyArray.sum
  - `mean` NumPyArray.mead
  - `standard deviation` NumPyArray.std
  - `min/max` NumPyArray.min/max separate methods

- Comparisons
  - able to use operators `<, >, <=, >=, ==` on each element and return a boolean

[Return to Home](README.md)


