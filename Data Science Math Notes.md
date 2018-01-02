# Data Science Math NOTES

## Functions

**Function**: A rule for a relationship between an input, or independent, quantity and an output, or dependent, quantity in which each input value uniquely determines one output value. We say “the output is a function of the input.”

**Vertical Line Test**
The vertical line test is a handy way to think about whether a graph defines the vertical output as a function of the horizontal input. Imagine drawing vertical lines through the graph. If any vertical line would cross the graph more than once, then the graph does not define only one vertical output for each horizontal input.

#### Inequality                       

- 5 < h <= 10
- 5 <= h < 10
- 5 < h < 10
- h < 10
- h >= 10
- all real numbers

#### Interval notation

- (5, 10]
- [5, 10)
- (5, 10)
- (-∞,10)
- [10, ∞)
- (∞, ∞)

### Toolkit Functions

![Graphs of basic functions that you should know on sight.](https://github.com/betsyrosalen/datascienceNOTES/blob/master/Graphs%20of%20the%20Toolkit%20Functions.PNG "Toolkit Functions")

### Composition of Functions
When the output of one function is used as the input of another, we call the entire operation a composition of functions. We write f(g(x)), and read this as “f of g of x” or “f composed with g at x”.
An alternate notation for composition uses the composition operator: o
(f o g)(x) is read “f of g of x” or “f composed with g at x”, just like f(g(x)).

### Vertical Shift
Given a function f(x), if we define a new function g(x) as g(x) = f(x)+k, where k is a constant
then g(x) is a vertical shift of the function f(x), where all the output values have been increased by k.

- If k is positive, then the graph will shift up
- If k is negative, then the graph will shift down

### Horizontal Shift
Given a function f(x), if we define a new function g(x) as g(x) = f(x+k), where k is a constant
then g(x) is a horizontal shift of the function f(x)

- If k is positive, then the graph will shift left
- If k is negative, then the graph will shift right

### Reflections
Given a function f(x), if we define a new function g(x) as g(x) = -f(x),
then g(x) is a vertical reflection of the function f(x), sometimes called a reflection about the x-axis

If we define a new function g(x) as f(-x),
then g(x) is a horizontal reflection of the function f(x), sometimes called a reflection about the y-axis

### Vertical Stretch/Compression
Given a function f(x), if we define a new function g(x) as g(x) = kf(x), where k is a constant
then g(x) is a **vertical stretch or compression** of the function f(x).

- If k > 1, then the graph will be stretched
- If 0 < k < 1, then the graph will be compressed
- If k < 0, then there will be combination of a vertical stretch or compression with a vertical reflection

### Combining Transformations
When combining vertical transformations, it is very important to consider the order of the transformations. For example, vertically shifting by 3 and then vertically stretching by 2 does not create the same graph as vertically stretching by 2 and then vertically shifting by 3. The order follows nicely from order of operations.

#### Combining Vertical Transformations
When combining vertical transformations written in the form af(x) + k,
first vertically stretch by a, then vertically shift by k.
