# Basics of the R language 

## Variables

Variables are the identifier or the named space in the memory, which are stored and can be referenced and manipulated later in the program. 

### Rule variable in R {-}

It is recommended that you use nouns to name a variable. Use underscores (e.g. donnees_menages) rather than CamelCase (e.g. donneesMenages). If you prefer camelCase, use it systematically throughout the script to standardise the code.

Notes:

+ Do not use T or F to name variables (as these are abbreviations for the Booleans TRUE and FALSE);
+ Do not use names that are already basic R functions(mean for example). This doesn't always generate errors, but it does prevent errors that are difficult to detect!
+ The variable name must start with letter and can contain number,letter,underscore('_') and period('.').
+ Special characters such as '#', '&', etc., along with White space (tabs, space) are not allowed in a variable name.
+ Underscore('_') at the beginning of the variable name are not allowed

### Variable assignment {-}

Variables in R can be assigned in one of three ways.

- Assignment Operator: **=** used to assign the value.The following example contains 20 as value which is stored in the variable 'first.variable' Example: first.variable = 20

- **<-** Operator: The following example contains the New Program as the character which gets assigned to 'second_variable'.
Example: second_variable <- "New Program"

- **->** Operator: The following example contains 565 as the integer which gets assigned to 'third.variable'.
Example: 565 -> third.variable

## Types

In programming, data type is an important concept. Variables can store data of different types, and different types can do different things.In R, variables do not need to be declared with any particular type, and can even change type after they have been set:

```r
val <- 3 #val is type of numeric
val <- "Hello" #val is now a type of character
```

There are several types of variable in R, but the most common are:

+ integer: for all whole numbers

```r
class(1L)
#> [1] "integer"
```

+ numeric: for decimals

```r
class(1.0)
#> [1] "numeric"
```

+ character: for text

```r
class("This is an R course")
#> [1] "character"
```

+ logical: for booleans (**TRUE** or **FALSE**)

```r
class(TRUE)
#> [1] "logical"
```

+ factor : for categories

```r
factor.1 <- as.factor(c("green","blue","red"))
class(factor.1)
#> [1] "factor"
```
In addition to variable types in R, we also have data types, including:

+ vectors: A vector is simply a list of items that are of the same type.

```r
vector_1 <- c(1,8)
print(vector_1)
#> [1] 1 8
```


```r
vector_2 <- c(1,"diamond") #1 will become a character because all the elements 
                           #in the vector are supposed to have the same type
print(vector_2)
#> [1] "1"       "diamond"
```
+ list:\
Lists are the R objects which contain elements of different types like − numbers, strings, vectors and another list inside it. A list can also contain a matrix or a function as its elements. List is created using list() function.

```r
# Create a list containing strings, numbers, vectors and a logical values.
list_data <- list("Red", c(21,32,11), TRUE)
print(list_data)
#> [[1]]
#> [1] "Red"
#> 
#> [[2]]
#> [1] 21 32 11
#> 
#> [[3]]
#> [1] TRUE
```


+ matrix :\
A matrix is a two dimensional data structure with variables of the same type

```r
matrix(1:9, nrow = 3, ncol = 3)
#>      [,1] [,2] [,3]
#> [1,]    1    4    7
#> [2,]    2    5    8
#> [3,]    3    6    9
```
+ dataframe :\
A dataframe is a two dimensional data structure with variables of differents types.

```r
data <- data.frame(id = c(1, 2), Age = c(21, 15), Name = c("John", "Dora"))
print(data)
#>   id Age Name
#> 1  1  21 John
#> 2  2  15 Dora
```
## Operators

Operators in R can mainly be classified into the following categories: arithmetic Operators,relational Operators, logical Operators,assignment Operators

1. R arithmetics operators:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- addition (+)
    

```r
print(5+2)
#> [1] 7
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- subtraction(-)
     

```r
print(1-9)
#> [1] -8
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- multiplication (*)
  

```r
print(6*500)
#> [1] 3000
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- division (/)
  

```r
print(5/2)
#> [1] 2.5
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- exponent (^)
  

```r
print(2^3)
#> [1] 8
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- modulus (%%)
    

```r
print(9%%2)
#> [1] 1
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- integer division(%/%)
 

```r
print(9%/%2)
#> [1] 4
```
2. Relational operators:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- less than (<)


```r
print(5<10)
#> [1] TRUE
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- greater than (>)
    

```r
print(2>8)
#> [1] FALSE
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- less than or equal to (<=)
  

```r
print(5<=5)
#> [1] TRUE
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- greater than or equal to (>=)
    

```r
print(5>=4)
#> [1] TRUE
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- equal to (==)
   

```r
x <- 7
print(x == 7)
#> [1] TRUE
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- not equal to(!=)
    

```r
y = 6
print(y!=4)
#> [1] TRUE
```
3. Logical operators:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- logical NOT (!)


```r
x <- c(TRUE, FALSE, 0, 6)
y <- c(FALSE, TRUE, FALSE, TRUE)
!x
#> [1] FALSE  TRUE  TRUE FALSE
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Logical AND (&)
  

```r
x & y
#> [1] FALSE FALSE FALSE  TRUE
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Logical OR (|)
 

```r
x | y
#> [1]  TRUE  TRUE FALSE  TRUE
```
4. Assignment operators:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Leftwards assignment (<-,<<-)


```r
x <- 5
x <<- 6
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Rightwards assignment (->, ->>)
    

```r
5 -> x
6 ->>x
```
