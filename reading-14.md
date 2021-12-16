# Matplotlib

## [Matplotlib](https://github.com/rougier/matplotlib-tutorial)
- Matplotlib
  - most common way of visualizing 2D data in python
- IPython
  - a Python Shell that has additional functionality and interactive matplotlib sessions
- pyplot
  - is an object-oriented plotting library
  - modeled closely after Matlab

### Simple Plot
- Create a plot with a sine and cosine function on the same plot
``` python
import numpy as np

X = np.linspace(-np.pi, np.pi, 256, endpoint = True)
C, S = np.cos(X), np.sin(X)

# change colors of the lines / adding labels to lines for legend
plt.plot(X,C, color="blue", label = "cosine)
plt.plot(X,S, color="red", label = "sine")

#change the limits on the plot
plt.xlim(X.min()*1.1, X.max()*1.1)
plt.ylim(X.min()1.1, X.max()*1.1)

#change tick marks on plot
plt.xtick( [-np.pi, -np.pi/2, 0, np.pi/2, np.pi])
plt.yticks([-1,0,1])

#add a legend
plt.legend(loc= 'upper left', frameon= False)

```

- Even more to do:
- Animation
  - more easily done now
  - key is: `FuncAnimation` as an update function
- Other plots
  - regular
  - scatter plots
  - Bar Plot
  - contour plot
  - imshow (show an image to current axes)
  - Quiver plot (plot a 2-D field of arrows)
  - Pie Chart
  - Polar Axis
  - 3D Plots
