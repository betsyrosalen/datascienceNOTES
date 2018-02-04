# R Notes

## Data Types in R (vs. Python)

### Primitives

R | Python | Notes
----- | ----- | -----
character | Str | 
complex | ??? | includes imaginary numbers
numeric | Float | 
integer | Int | 
logical | Bool | 

`is.datatyppe` will return TRUE or FALSE

`as.datatype` will convert from the original datatype to the one specified

Can coerce data from lower end without loss of precision to uppper end but not the other way around.

### Non-Primitives

R | Python | Notes
----- | ----- | -----
factor |  | Like Python dictionaries but has levels as well, can be ordered
date |  | 
vector  |  | all R primitives are technically vectors and can have length
list |  | 
data.frame |  | 

There is no `is.date` function.


## Built-in Functions

This section taken from <https://www.statmethods.net/management/functions.html> with some additions by me.

Almost everything in R is done through functions. Here I'm only refering to numeric and character functions that are commonly used in creating or recoding variables.

(To practice working with functions, try the functions sections of this this interactive course.)

### Numeric Functions

Function | Description
----- | -----
`+`, `-`, `*`, `/` | addition, subtraction, multiplication, division
`x %% y` | modulo or remainder of division of x by y
`x %/% y` | integer division - number of times y goes into x without remainder
`x ^ y` (or `x ** y`) | exponentiation - x raised to the power y
`abs(x)` | absolute value
`sqrt(x)` | square root
`ceiling(x)` | ceiling(3.475) is 4
`floor(x)` | floor(3.475) is 3
`trunc(x)` | trunc(5.99) is 5
`round(x, digits=n)` | round(3.475, digits=2) is 3.48
`signif(x, digits=n)` | signif(3.475, digits=2) is 3.5
`cos(x)`, sin(x), tan(x) | also acos(x), cosh(x), acosh(x), etc.
`log(x)` | natural logarithm
`log10(x)` | common logarithm
`exp(x)` | e^x

### Logical Operators

Operator | Description
----- | -----
`<` | less than
`<=` | less than or equal to
`>` | greater than
`>=` | greater than or equal to
`==` | exactly equal to
`!=` | not equal to
`!x` | Not x
`x` | y | x OR y
`x & y` | x AND y
`isTRUE(x)` | test if X is TRUE

### Character Functions

Function | Description
----- | -----
`substr(x, start=n1, stop=n2)` | Extract or replace substrings in a character vector.<br>x <- "abcdef" <br>substr(x, 2, 4) is "bcd" <br>substr(x, 2, 4) <- "22222" is "a222ef"
`grep(pattern, x , ignore.case=FALSE, fixed=FALSE)` | Search for pattern in x. If fixed =FALSE then pattern is a regular expression. If fixed=TRUE then pattern is a text string. Returns matching indices.<br>grep("A", c("b","A","c"), fixed=TRUE) returns 2
`sub(pattern, replacement, x, ignore.case =FALSE, fixed=FALSE)` | Find pattern in x and replace with replacement text. If fixed=FALSE then pattern is a regular expression.<br>If fixed = T then pattern is a text string. <br>sub("\\s",".","Hello There") returns "Hello.There"
`strsplit(x, split)` | Split the elements of character vector x at split. 
`strsplit("abc", "")` | returns 3 element vector "a","b","c"<br>paste(..., sep="") | Concatenate strings after using sep string to seperate them.<br>paste("x",1:3,sep="") returns c("x1","x2" "x3")<br>paste("x",1:3,sep="M") returns c("xM1","xM2" "xM3")<br>paste("Today is", date())
`toupper(x)` | Uppercase
`tolower(x)` | Lowercase

### Basic Statistical Functions

Basic statistical functions are provided in the following table. Each has the option na.rm to strip missing values before calculations. Otherwise the presence of missing values will lead to a missing result. Object can be a numeric vector or data frame.

Function | Description
----- | -----
`min(x)` | minimum
`max(x)` | maximum
`sum(x)` | sum
`range(x)` | range
`mean(x, trim=0,<br>na.rm=FALSE)` | mean of object x<br># trimmed mean, removing any missing values and <br># 5 percent of highest and lowest scores <br>mx <- mean(x,trim=.05,na.rm=TRUE)
`median(x)` | median
`var(x)` | variance
`sd(x)` | standard deviation of object(x). <br>also look at var(x) for variance and mad(x) for median absolute deviation.
`summary(x)` | Returns Min, Max, 1st Qtr, 3rd Qtr, Median, Mean and num of missing values - N0 SD
`quantile(x, probs)` | quantiles where x is the numeric vector whose quantiles are desired <br>and probs is a numeric vector with probabilities in [0,1].<br># 30th and 84th percentiles of x<br>y <- quantile(x, c(.3,.84))
`fivenum(x)` | min, 1st, 2nd, 3rd Quartiles, and Max
`IQR(x)` | Spread between 25th and 75th percentile
`diff(x, lag=1)` | lagged differences, with lag indicating which lag to use
`scale(x, center=TRUE, scale=TRUE)` | 	column center or standardize a matrix.

**NOTE:** adding `na.rm=TRUE` will ignore missing values in most functions above

### Statistical Probability Functions

The following table describes functions related to probaility distributions. For random number generators below, you can use set.seed(1234) or some other integer to create reproducible pseudo-random numbers.

Function | Description
----- | -----
`dnorm(x)` | normal density function (by default m=0 sd=1)<br># plot standard normal curve<br>x <- pretty(c(-3,3), 30)<br>y <- dnorm(x)<br>plot(x, y, type='l', xlab="Normal Deviate", ylab="Density", yaxs="i")
`pnorm(q)` | cumulative normal probability for q <br>(area under the normal curve to the left of q)<br>pnorm(1.96) is 0.975
`qnorm(p)` | normal quantile. <br>value at the p percentile of normal distribution <br>qnorm(.9) is 1.28 # 90th percentile 
`rnorm(n, m=0,sd=1)` | n random normal deviates with mean m and standard deviation sd. <br># 50 random normal variates with mean=50, sd=10<br>x <- rnorm(50, m=50, sd=10)
`dbinom(x, size, prob)`<br>`pbinom(q, size, prob)`<br>`qbinom(p, size, prob)`<br>`rbinom(n, size, prob)` | binomial distribution where size is the sample size and prob is the probability of a heads (pi) <br># prob of 0 to 5 heads of fair coin out of 10 flips<br>dbinom(0:5, 10, .5)<br># prob of 5 or less heads of fair coin out of 10 flips
`pbinom(5, 10, .5)`<br>`dpois(x, lamda)`<br>`ppois(q, lamda)`<br>`qpois(p, lamda)<br>rpois(n, lamda)` | poisson distribution with m=std=lamda<br># probability of 0,1, or 2 events with lamda=4<br>dpois(0:2, 4)<br># probability of at least 3 events with lamda=4 <br>1- ppois(2,4)
`dunif(x, min=0, max=1)`<br>`punif(q, min=0, max=1)`<br>`qunif(p, min=0, max=1)`<br>`runif(n, min=0, max=1)` | uniform distribution, follows the same pattern as the normal distribution above. <br># 10 uniform random variates<br>x <- runif(10)

### Other Useful Functions

Function | Description
----- | -----
`seq(from , to, by)` | generate a sequence<br>indices <- seq(1, 10, 2) <br># indices is c(1, 3, 5, 7, 9)
`rep(x, ntimes)` | repeat x n times<br>y <- rep(1:3, 2) <br># y is c(1, 2, 3, 1, 2, 3)
`cut(x, n)` | divide continuous variable in factor with n levels y <- cut(x, 5)

Note that while the examples on this page apply functions to individual variables, many can be applied to vectors and matrices as well.

## More R Shortcuts and Functions

**Tip:** If you use the up and down arrow keys, you can scroll through your previous commands, your so-called command history. You can also access it by clicking on the history tab in the upper right panel. This will save you a lot of typing in the future.

R Comand | Description
----- | -----
`ctrl + L` | to clear console
`?function_name` | Displays the documentation for the function in the viewer window in RStudio
`getwd()` | get the working directory
`setwd("file\path")` | set the working directory
`str(dataframe)` | returns the structure of the dataframe
`dim(dataframe)` | Returns the dimensions of the dataframe
`names(dataframe)` | Returns the names of the columns or variabes in the dataframe
`dataframe$variable` | Returns all of the values in the specified variableas a ***vector***
`table(df$var1, useNA='ifany')` | Creates a table of sums of each value for the variable
`table(df$var1, df$var2, useNA='ifany')` | Creates a table of sums of the inersection of the two variables
`prop.table(table(df$var))` | Creates a table of the proportion of each value for the variable
`barplot(table(df$var), las=3)` | Creates a bargraph of the values of the variable
`plot(x = df$var1, y = df$var2)` | Creates a scatterplot of the two variables<br> Technically you don't need the x= and y= as long as you put them first and in that order because by default the first 2 arguments are for the x and y variables
`plot(df$var1, df$var2, type = "l")` | Creates a linegraph of the two variables
`df$totals <- df$var1 + df$var2` | Creates a new column and puts the total of var1 and var2 in that column
`df[which.max(df$var),]` | Finds the row with max in specified variable column

## Reading R data from GitHub

Here is some sample code for reading R from a dataset that has been posted in a GitHub repository:

```
library(RCurl) 
x <- getURL("https://raw.github.com/aronlindberg/latent_growth_classes/master/LGC_data.csv") 
y <- read.csv(text = x)
```

source: <http://stackoverflow.com/questions/14441729/read-a-csv-from-github-into-r>
