# Generate a 2d graph object for displaying (x,y) data as text

## Args

1. ```height``` (int): Number of vertical positions
1. ```width``` (int): Number of horizontal positions
1. ```init_x``` (int): 0 reference offset from left edge 
1. ```init_y``` (int): 0 reference offset from bottom edge
1. ```fill``` (str): Character to fill each position in grid. Default is "." 

## Functions

### ```generate(self)```
Generate a graph sized from init arguments.

Returns:
list[list[str]]: List of rows of positions

### ```set(self, _x, _y, item)```
Set value at a specified position to item, usually str or int.

Args:

```_x``` (int): x coordinate to set

```_y``` (int): y coordinate to set

```item``` (str or int): Value, usually str or int, to set at position

### ```get(self, _x, _y)```
Get value at position.

Args:

```_x``` (int): x coordinate to get

```_y``` (int): y coordinate to get

Returns:
str or int: Value of object from specified position

### ```transpose(self, _x, _y)```
Converts x,y coordinates to i,j type tuple for use in a subscriptable
nested loop. (list of lists) 

x values increase to the right like nested j values do. 
y values increase upwards which is opposite to i in general.
x,y starting position is lower-left by default. i,j is upper-left.

Args:

```_x``` (int): x coordinate

```_y``` (int): y coordinate

Returns:
tuple: (i,j) Position reference for use in a subscriptable nested loop. 

### ```display(self)```
Converts graph list to printable string.

Returns:
str: Easily printable block string