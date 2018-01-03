# Data Science Math NOTES

## Functions

**Function**: A rule for a relationship between an input, or independent, quantity and an output, or dependent, quantity in which **each input value uniquely determines one output value**. We say “the output is a function of the input.”

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

![Graphs of basic functions that you should know on sight.](https://math.libretexts.org/@api/deki/files/925/CNX_Precalc_Figure_01_03_012.jpg?revision=1)

### Composition of Functions
When the output of one function is used as the input of another, we call the entire operation a composition of functions. We write f(g(x)), and read this as “f of g of x” or “f composed with g at x”.
An alternate notation for composition uses the composition operator: o

(f o g)(x) is read “f of g of x” or “f composed with g at x”, just like f(g(x)).

### Vertical Shift
Given a function f(x), if we define a new function g(x) as g(x) = **f(x)+k**, where k is a constant
then g(x) is a vertical shift of the function f(x), where all the output values have been increased by k.

- If **k is positive**, then the graph will **shift up**
- If **k is negative**, then the graph will **shift down**

### Horizontal Shift
Given a function f(x), if we define a new function g(x) as g(x) = **f(x+k)**, where k is a constant
then g(x) is a horizontal shift of the function f(x)

- If **k is positive**, then the graph will **shift left**
- If **k is negative**, then the graph will **shift right**

### Reflections
Given a function f(x), if we define a new function g(x) as g(x) = **-f(x)**,
then g(x) is a **vertical reflection** of the function f(x), sometimes called a reflection about the x-axis

If we define a new function g(x) as **f(-x)**,
then g(x) is a **horizontal reflection** of the function f(x), sometimes called a reflection about the y-axis

### Vertical Stretch/Compression
Given a function f(x), if we define a new function g(x) as g(x) = **kf(x)**, where k is a constant
then g(x) is a **vertical stretch or compression** of the function f(x).

- If k > 1, then the graph will be stretched
- If 0 < k < 1, then the graph will be compressed
- If k < 0, then there will be combination of a vertical stretch or compression with a vertical reflection

### Combining Transformations
When combining vertical transformations, it is very important to consider the order of the transformations. For example, vertically shifting by 3 and then vertically stretching by 2 does not create the same graph as vertically stretching by 2 and then vertically shifting by 3. The order follows nicely from order of operations.

#### Combining Vertical Transformations
When combining vertical transformations written in the form af(x) + k,
first vertically stretch by a, then vertically shift by k.

## Linear FunctionsA linear function is a function whose graph produces a line. Linear functions can always be written in the form **f(x) = b+mx** or **f(x) = mx+b**; they’re equivalent where b is the initial or starting value of the function (when input, x = 0), and m is the constant rate of change of the function This form of a line is called **slope-intercept form** of a line.

#### Slope and Increasing/Decreasing**m is the constant rate of change** of the function (also called **slope**). The slope determines if the function is an increasing function or a decreasing function.f(x) = b + mx is an **increasing function if m > 0**f(x) = b + mx is a **decreasing function if m<0**If m = 0 , the rate of change zero, and the function f(x) = b+0x = b is just a horizontal line passing through the point (0, b), neither increasing nor decreasing.

m = change in y over the change in x = (y2 - y1) / (x2 - x1)

#### Point-Slope Equation of a LineAn equation for the line passing through the point (x1, y1) with slope m can be written as y − y1 = m(x − x1)This is called the **point-slope form** of a line.

Point-slope is a specific form of linear equations in two variables:
y - b = m(x - a) 

When an equation is written in this form, m gives the slope of the line and (a,b) is a point the line passes through.

#### Graphical Interpretation of a Linear EquationGraphically, in the equation **f(x) = b + mx**- **b** is the **vertical intercept** of the graph and tells us we can start our graph at (0, b)- **m** is the **slope** of the line and tells us how far to rise & run to get to the next point

#### Finding **Horizontal Intercept**The horizontal intercept of the function is where the graph crosses the horizontal axis. If a function has a horizontal intercept, you can always find it by solving f(x) = 0.#### Intersections of LinesThe graphs of two lines will intersect if they are not parallel. They will intersect at the point that satisfies both equations. To find this point when the equations are given as functions, we can solve for an input value so that f(x) = g(x) . In other words, we can set the formulas for the lines equal, and solve for the input that satisfies the equation.

## Exponents

### Laws of Exponents:All variables here represent real numbers and all variables in denominators are nonzero.1. x^a⋅x^b = x^(a+b)  
2. x^a / x^b = x^(a-b)  
3. (x^a)^b = x^ab  
4. (xy)^a = x^a⋅y^a  
5. (x/y)^b = x^b / y^b  
6. x^0 = 1, provided x != 0  
7. x^-n = 1/x^n, provided x != 0    
8. x^1/n = the nth root of x, provided x != 0  

## QuadraticsQuadratics are transformations of the f(x) = x2 function. Quadratics commonly arise from problems involving area and projectile motion

### Forms of Quadratic FunctionsThe **standard form** of a quadratic function is **f(x) = ax^2 + bx + c** 

The **transformation form** of a quadratic function is **f(x) = a(x−h)^2 + k**
 
The **vertex** *(the lowest point or turnaround point of the graphed curve)* of the quadratic function is located at (h, k), where h and k are the numbers in the transformation form of the function. Because the vertex appears in the transformation form, it is often called the **vertex form**.

#### InterceptsAs with any function, we can find the **vertical intercepts** of a quadratic by evaluating the function at an input of zero.  In the standard form of a quadratic, the constant term c reveals the vertical intercept of the graph, since f(0) = a(0)^2 + b(0) + c = c

We can find the **horizontal intercepts** by solving for when the output will be zero. Depending upon the location of the graph, we might have zero, one, or two horizontal intercepts.

#### Quadratic FormulaFor a quadratic function given in standard form f(x) = ax^2 + bx + c, the ***quadratic formula gives the horizontal intercepts*** of the graph of this function.
x = (−b ± sqrt(b^2 − 4ac)) / 2a

![Quadratic Formula.](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c4/Quadratic_formula.svg/200px-Quadratic_formula.svg.png)

## Polynomials and Rational Functions 

### Polynomial Functions#### Terminology of Polynomial FunctionsA **polynomial** is function that can be written as f(x) = a0 + a1x + a2x^2 + ... + anx^n  
Each of the ai constants are called **coefficients** and can be positive, negative, or zero, and be whole numbers, decimals, or fractions.  
A **term** of the polynomial is any one piece of the sum, that is any ai xi . Each individual term is a transformed power function.
The **degree** of the polynomial is the highest power of the variable that occurs in the polynomial.
The **leading term** is the term containing the highest power of the variable: the term with the highest degree.
The **leading coefficient** is the coefficient of the leading term.
Because of the definition of the “leading” term we often rearrange polynomials so that the powers are descending. f(x)=anx^n + .....+ a2x^2 + a1x + a0

#### Intercepts

Find **vertical intercepts** by solving for f(0)

Finding **horizontal intercepts** can be challenging, so technology is often used.

### Rational FunctionsRational functions are the ratios, or fractions, of polynomials. A rational function is a function that can be written as the ratio of two polynomials, P(x) / Q(x)

#### Vertical and Horizontal AsymptotesA **vertical asymptote** of a graph is a vertical line x = a where the graph tends towards positive or negative infinity as the inputs approach a. **As x → a , f(x) → ± ∞**

The vertical asymptotes of a rational function will occur where the denominator of the function is equal to zero and the numerator is not zero.
A **horizontal asymptote** of a graph is a horizontal line y = b where the graph approaches the line as the inputs get large. **As x → ± ∞ , f(x) → b**

The horizontal asymptote of a rational function can be determined by looking at the degrees of the numerator and denominator.- Degree of denominator > degree of numerator: Horizontal asymptote at y = 0 
- Degree of denominator < degree of numerator: No horizontal asymptote- Degree of denominator = degree of numerator: Horizontal asymptote at ratio of leading coefficients.

#### Intercepts
As with all functions, a rational function will have a **vertical intercept when the input is zero**, if the function is defined at zero. It is possible for a rational function to not have a vertical intercept if the function is undefined at zero.
Likewise, a rational function will have **horizontal intercepts at the inputs that cause the output to be zero** (unless that input corresponds to a hole). It is possible there are no horizontal intercepts. Since a fraction is only equal to zero when the numerator is zero, horizontal intercepts will occur when the numerator of the rational function is equal to zero.

## Exponential FunctionsAn **exponential growth or decay function** is a function that grows or shrinks at a constant percent growth rate. The equation can be written in the form **f(x) = a(1+ r)^x or f(x) = ab^x where b = 1 + r**

Where:
- a is the initial or starting value of the function- r is the percent growth or decay rate, written as a decimal- b is the growth factor or growth multiplier. Since powers of negative numbers behave strangely, we limit b to positive values.

### Euler’s Number: e ≈ 2.718282
See textbook page 62 for explanation

### Graphical Features of Exponential FunctionsGraphically, in the function f(x) = ab^x
- a is the vertical intercept of the graph- b determines the rate at which the graph grows    - the function will increase if b > 1    - the function will decrease if 0 < b < 1
The graph will have a horizontal asymptote at y = 0  The graph will be concave up if a > 0; concave down if a < 0.  The domain of the function is all real numbers  
The range of the function is (0,∞)

When sketching the graph of an exponential function, it can be helpful to remember that the graph will pass through the points (0, a) and (1, ab).
The value b will determine the function’s long run behavior: 

- If b > 1, as x → ∞, f(x) → ∞ and as x → −∞ , f(x) → 0
- If 0 < b < 1, as x→∞, f(x) → 0 and as x → −∞, f(x) → ∞

## Logarithmic FunctionsLogarithms are the inverse of exponential functions -- they allow us to undo exponential functions and solve for the exponent. They are also commonly used to express quantities that vary widely in size.

### Common and Natural LogarithmsThe common log is the logarithm with base 10, and is typically written log(x) . 

The natural log is the logarithm with base e, and is typically written ln(x) .