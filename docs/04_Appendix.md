---
editor_options: 
  markdown: 
    wrap: 72
---




# (APPENDIX) Appendix {.unnumbered}

# Recaps in 1 minutes or less

## Possibilities of using R

-   Console: type a command and hit <kbd>Enter</kbd>

    -   *Base R* Console
    -   *RGui* Console on Windows
    -   *RStudio* Console

-   Script: edit a text files and hit <kbd>Ctrl+R</kbd> or <kbd>Ctrl+Enter</kbd>

    -   *RGui* Script Window (<kbd>Ctrl+R</kbd>)
    -   *RStudio* Source Pane (<kbd>Ctrl+Enter</kbd>)

-   Point and Click

    -   *R Commander*
    -   *jamovi*, *JASP* etc.

## Console features

-   history of command: <kbd>Up/Down arrows</kbd>
-   autocompletion: <kbd>TAB</kbd>
-   continuation prompt: <kbd>Esc</kbd>

## Advantages of Script editor in RStudio

-   multi-line editor
-   full-featured text editor: e.g. row numbering, syntax highlighting
-   autocompletion of filenames, function names, arguments and objects
-   cross-platform interface to R
-   surrounded by integrated graphical environment (workspace, files, plots, help, etc.)

## Useful keyboard shortcuts in RStudio

-   <kbd>Ctrl+Enter</kbd>: Run commands
-   Clipboard Operations (Cut, Copy, Paste Operations): <kbd>Ctrl+X</kbd>, <kbd>Ctrl+C</kbd>, <kbd>Ctrl+V</kbd>
-   <kbd>Ctrl++</kbd>, <kbd>Ctrl+-</kbd>: Zoom in/out
-   <kbd>Ctrl+Shift+C</kbd>: Comment lines/uncomment lines
-   <kbd>Ctrl+F</kbd>: Find and replace text within script editor
-   <kbd>Ctrl+S</kbd>: Save the script file
-   <kbd>Alt+-</kbd>: Write assignment operator
-   <kbd>Ctrl+Shift+F10</kbd>: Restart R session

## Base types in R

-   character (or string): `"apple juice"`
-   integer (whole numbers): `12L`
-   double (real numbers, decimal numbers): `12`, `12.4`
-   logical (true false type things): `TRUE`, `FALSE`

## Data structures

-   *Vector*: one-dimensional, homogeneous
-   *Matrix*: two-dimensional, homogeneous
-   *Array*: two or more dimensional, homogeneous
-   *List*: one-dimensional, heterogeneous
-   *Factor*: integer vector with levels, which is a character vector
-   *Data frame*: two-dimensional, heterogeneous

| Dimension |   Homogenous   | Heterogeneous |
|:---------:|:--------------:|:-------------:|
|    1D     | Vector, Factor |     List      |
|    2D     |     Matrix     |  Data frame   |
|    nD     |     Array      |               |

: Data structures

## Operators

| Operator                       | Description               | Example                 |
|--------------------------------|--------------------------|-------------------------|
| `::`                           | access                   | `MASS::survey`          |
| `$`                            | component                | `my.s$Sex`              |
| `[` `[[`                       | indexing                 | `my.s$Height[c(2, 45)]` |
| `^` `**`                       | exponentiation           | `2^3`                   |
| `-` `+`                        | unary minus, unary plus  | `-2`                    |
| `:`                            | sequence operator        | `1:10`                  |
| `%any%` e.g. `%%` `%/%` `%in%` | special operators        | `12%%3`                 |
| `*` `/`                        | multiplication, division | `12*3`                  |
| `+` `-`                        | addition, subtraction    | `2.3 + 2`               |
| `<` `>` `<=` `>=` `==` `!=`    | comparisions             | `2<=3`                  |
| `!`                            | logical NOT              | `!TRUE`                 |
| `&`                            | logical AND              | `TRUE & FALSE`          |
| `|`                            | logical OR               | `TRUE | FALSE`          |
| `<-`                           | assignment               | `col <- 12`             |

: R operators in order of precedence from highest to lowest

R language provides following types of operators:

-   Arithmetic Operators: `^` `**`, `-` (unary), `+` (unary), `%%`, `%/%`, `*`, `/`, `-` (binary), `+` (binary)
-   Relational Operators: `<`, `>`, `<=`, `>=`, `==`, `!=`, `%in%`
-   Logical Operators: `!`, `&`, `|`
-   Assignment Operators: `<-`
-   Miscellaneous Operators: `::`, `$`, `[`, `[[`, `:`, `?`

## Maths functions


Table: (\#tab:matfuggvenyek)Mathematical functions

Function                                                                  Description                                                                                     Example                                                                  
------------------------------------------------------------------------  ----------------------------------------------------------------------------------------------  -------------------------------------------------------------------------
<span style="   font-family: monospace;  " >abs(x)</span>                 Takes the absolute value of x                                                                   <span style="   font-family: monospace;  " >abs(-1)</span>               
<span style="   font-family: monospace;  " >sign(x)</span>                The signs of `x`                                                                                <span style="   font-family: monospace;  " >sign(pi)</span>              
<span style="   font-family: monospace;  " >sqrt(x)</span>                Returns the square root of x                                                                    <span style="   font-family: monospace;  " >sqrt(9+16)</span>            
<span style="   font-family: monospace;  " >exp(x)</span>                 Returns the exponential of x                                                                    <span style="   font-family: monospace;  " >exp(1)</span>                
<span style="   font-family: monospace;  " >log(x,base=exp(1))</span>     Takes the logarithm of x with base y; if base is not specified, returns the natural logarithm   <span style="   font-family: monospace;  " >log(exp(3));log(8,10)</span> 
<span style="   font-family: monospace;  " >log10(x);log2(x)</span>       Takes the logarithm of x with base 10 or 2                                                      <span style="   font-family: monospace;  " >log10(1000);log2(256)</span> 
<span style="   font-family: monospace;  " >cos(x);sin(x);tan(x)</span>   Trigonometric functions                                                                         <span style="   font-family: monospace;  " >cos(pi);sin(0);tan(0)</span> 
<span style="   font-family: monospace;  " >round(x,digits=0)</span>      Rounds a numeric input to a specified number of decimal places                                  <span style="   font-family: monospace;  " >round(c(1.5,-1.5))</span>    
<span style="   font-family: monospace;  " >floor(x)</span>               Rounds a numeric input down to the next lower integer                                           <span style="   font-family: monospace;  " >floor(c(1.5,-1.5))</span>    
<span style="   font-family: monospace;  " >ceiling(x)</span>             Rounds a numeric input up to the next higher integer                                            <span style="   font-family: monospace;  " >ceiling(c(1.5,-1.5))</span>  
<span style="   font-family: monospace;  " >trunc(x)</span>               Truncates (i.e. cuts off) the decimal places of a numeric input                                 <span style="   font-family: monospace;  " >trunc(c(1.5,-1.5))</span>    

## String functions



Function                  |  Description                     | Example
--------------------------|----------------------------------|----------------------
`paste();paste0(sep="")`  | Concatenate strings              | `paste('a','b',sep='=')`
`nchar(x)`                | Count the number of characters   | `nchar('alma')`
`substr(x,start,stop)`    | Substrings of a character vector | `substr('alma', 3, 5)`
`tolower(x)`              | Convert to lower-case            | `tolower('Kiss Géza')`
`toupper(x)`              | Convert to upper-case            | `toupper('Kiss Géza')`
`chartr(old,new,x)`       | Translates characters            | `chartr('it','ál','titik')`
`cat(sep=" ")`            | Concatenate and print            | `cat('alma','fa\n',sep='')`
`grep();grepl();regexpr()`| Pattern matching                 | `grepl(pattern='lm',x='alma')`
`sub();gsub()`            | Pattern matching and replacement | `gsub('lm',repl='nyj',x='alma')`

## Base R Statistical Functions


Table: (\#tab:statfuggvenyek2)Base R Statistical Functions

Function                                                       Description                            Example                                                              Value of Example                                        
-------------------------------------------------------------  -------------------------------------  -------------------------------------------------------------------  --------------------------------------------------------
<span style="   font-family: monospace;  " >max(x)</span>      The largest value of `x`               <span style="   font-family: monospace;  " >max(1:10)</span>         <span style="   font-family: monospace;  " >10</span>   
<span style="   font-family: monospace;  " >min(x)</span>      The smallest value of `x`              <span style="   font-family: monospace;  " >min(11:20)</span>        <span style="   font-family: monospace;  " >11</span>   
<span style="   font-family: monospace;  " >sum(x)</span>      The sum of all the values of `x`       <span style="   font-family: monospace;  " >sum(1:5)</span>          <span style="   font-family: monospace;  " >15</span>   
<span style="   font-family: monospace;  " >prod(x)</span>     The product of all the values of `x`   <span style="   font-family: monospace;  " >prod(1:5)</span>         <span style="   font-family: monospace;  " >120</span>  
<span style="   font-family: monospace;  " >mean(x)</span>     Mean of `x`                            <span style="   font-family: monospace;  " >mean(1:10)</span>        <span style="   font-family: monospace;  " >5.5</span>  
<span style="   font-family: monospace;  " >median(x)</span>   Median of `x`                          <span style="   font-family: monospace;  " >median(1:10)</span>      <span style="   font-family: monospace;  " >5.5</span>  
<span style="   font-family: monospace;  " >range(x)</span>    The minimum and the maximum            <span style="   font-family: monospace;  " >range(1:10)</span>       <span style="   font-family: monospace;  " >1 10</span> 
<span style="   font-family: monospace;  " >sd(x)</span>       Standard deviation of x                <span style="   font-family: monospace;  " >sd(1:10)</span>          <span style="   font-family: monospace;  " >3.03</span> 
<span style="   font-family: monospace;  " >var(x)</span>      Variance of `x`                        <span style="   font-family: monospace;  " >var(1:10)</span>         <span style="   font-family: monospace;  " >9.17</span> 
<span style="   font-family: monospace;  " >cor(x,y)</span>    Correlation between `x` and `y`        <span style="   font-family: monospace;  " >cor(1:10,11:20)</span>   <span style="   font-family: monospace;  " >1</span>    

## Regular sequences


Function                        |  Description                                                   |  Example                   |  Value of Example
--------------------------------|----------------------------------------------------------------|----------------------------|------------------------------
`from:to`                       | generates a sequence from `from=` to `to=` in steps of 1 or -1 | `1:5`                      | `1 2 3 4 5`
`seq(from, to, by, length.out)` | generate regular sequences                                     | `seq(from=2, to=10, by=2)` | `2  4  6  8 10`
`rep(x, times, each)`           | replicate elements of vectors                                  | `rep(x=0, times=3)`        | `0 0 0`
`paste(sep, collapse)`          | concatenate vectors                                            | `paste("No", 1:3, sep="_")`| `"No_1" "No_2" "No_3"`



## Subsetting

+-----------------------------+---------------------------------------+
| Data structure              | Example                               |
+=============================+=======================================+
| - Vector                    | - `x[3]`                              |
| - Factor                    | - `x[1:3]`                            |
| - List                      | - `x[c(2, 3, 1)]`                     |
| - Data frame                | - `x[-2]`                             |
|                             | - `x[-c(1, 2)]`                       |
|                             | - `x["Jane"]`                         |
|                             | - `x[c("Jane", "Mark")]`              |
|                             | - `x[c(T, F, T, T)]`                  |
|                             | - `x[[2]]`                            |
|                             | - `x[["Jane"]]`                       |
+-----------------------------+---------------------------------------+
| - Matrix                    | - `x[1, 2]`                           |
| - Data frame                | - `x[, 2]`                            |
|                             | - `x[2:4, ]`                          |
|                             | - `x[c(2, 3, 1), c("name", "sport")]` |
|                             | - `x[c("Jane", "Mark"), c(T, F, T)]`  |
+-----------------------------+---------------------------------------+
| - Array (3D)                | - `x[1:3, c(2,1), 2:3]`               |
+-----------------------------+---------------------------------------+
| - List, Data frame          | - `x$name`                            |
+-----------------------------+---------------------------------------+


## Packages

+-----------------------------+-------------------------------------+
| Operation                   | Example                             |
+=============================+=====================================+
| Install a package from CRAN | `install.packages("package_name")`  |   
+-----------------------------+-------------------------------------+
| Load a package              | `library(package_name)`             |
+-----------------------------+-------------------------------------+

## Reading/Writing data files

+---------------------------+-----------------------------------------------------------------+
| Operation                 | Example                                                         |
+===========================+=================================================================+
| Import text files         | `read.table(file, sep, dec, header, fileEncoding)`              |
+---------------------------+-----------------------------------------------------------------+
| Import Excel or SPSS files| `rio::import(file)`                                             |
+---------------------------+-----------------------------------------------------------------+
| Export text files         | `write.table(x, file, sep, dec, row.names, quote, fileEncoding)`|
+---------------------------+-----------------------------------------------------------------+
| Export Excel or SPSS files| `rio::export(x, file)`                                          |
+---------------------------+-----------------------------------------------------------------+


## Filter

+-----------------------------+-----------------------------------------+
| Data structure              | Example                                 |
+=============================+=========================================+
| - Vector                    | - `x[x < 2]`                            |
|                             | - `x[x == "Jane"]`                      |
|                             | - `x[x == "Jane" | x == "Mark"]`        |
+-----------------------------+-----------------------------------------+
| - Data frame                | - `x[x$v1 < 2, ]`                       |
|                             | - `x[x$v2 == "Jane", ]`                 |
|                             | - `x[x$v2 == "Jane" | x$v2 == "Mark", ]`|
+-----------------------------+-----------------------------------------+



## Sort

+-----------------------------+---------------------------------------+
| Data structure              | Example                               |
+=============================+=======================================+
| - Vector                    | - `sort(x)`                           |
|                             | - `sort(x, decreasing=T)`             |
+-----------------------------+---------------------------------------+
| - Factor                    | - `sort(table(x))`                    |
|                             | - `sort(table(x), decreasing=T)`      |
+-----------------------------+---------------------------------------+
| - Data frame                | - `x[order(x$name), ]`                |
|                             | - `x[order(x$name, decreasing=T), ]`  |
+-----------------------------+---------------------------------------+



## Data type conversion

+-----------------------------+--------------------------------+
| Conversion                  | Example                        |
+=============================+================================+
| - Numeric vector to factor  | - `factor(x)`                  |
| - Character vector to factor|                                |
+-----------------------------+--------------------------------+
| - Character to numeric      | - `as.numeric(x)`              |
|                             |                                |
+-----------------------------+--------------------------------+
| - Factor to character       | - `as.character(x)`            |
+-----------------------------+--------------------------------+
| - Factor to numeric         | - `as.numeric(as.character(x))`|
+-----------------------------+--------------------------------+


## Transformation

+-----------------------------+--------------------------------+
| Transformation              | Example                        |
+=============================+================================+
| - Numeric to factor         | - `cut(x, breaks, labels)`     |
+-----------------------------+--------------------------------+
| - Factor to factor          | - `car::recode(x, '')`         |
+-----------------------------+--------------------------------+
| - Numeric to numeric        | - mathematical functions       |
|                             |     - `round()`, `log()`       |
|                             |     - `exp()`, `sin()`, etc.   |
|                             | - operators                    |
|                             |     - `+`,`-`, `/`, `*`, etc.  |
+-----------------------------+--------------------------------+

## Descriptive statistics

+------------------------+---------------------------------+
| Descriptive statistics | Example                         |
+========================+=================================+
| -   Measurements       | - `psych::describe()`           |
|                        | - `psych::describeBy()`         |
|                        | - `DescTools::Desc()`           |
+------------------------+---------------------------------+
| -   Tables             | - `table(useNA="ifany")`        |
|                        | - `DescTools::Desc()`           |
+------------------------+---------------------------------+
| -   Plots              | - Traditional graphics          |
|                        |     - `hist()`                  |
|                        |     - `boxplot()`               |
|                        |     - `stripchart()`            |
|                        |     - `plot()`                  |
|                        |     - `barplot()`               |
|                        | - ggplot2 graphics `ggplot() +` |
|                        |     - `geom_histogram()`        |
|                        |     - `geom_boxplot()`          |
|                        |     - `geom_jitter()`           |
|                        |     - `geom_point()`            |
|                        |     - `geom_bar()`              |
+------------------------+---------------------------------+




# Terminology

## Terms in Statistics

Bar chart

:   A graph used to display summary statistics such as the *mean* (in the case of a *scale variable*) or the *frequency* (in the case of a *nominal variable*).

Boxplot

:   a visual representation of data that shows central tendency (usually the median) and spread (usually the interquartile range) of a numeric variable for one or more groups; boplots are often used to compare the distribution of a continuous variable across several groups

Case / Observation

:   A case is the unit of analysis; one person or other entity. In psychology, this is normally the data deriving from a single participant. In some research, the cases will not be people. For example, we may be interested in the average academic attainment for pupils from different schools. Here, the cases would be the schools. In R, a single row of data in a data frame represents a case.

Categorical variable

:   variable measured in categories; there are two types of categorical variables: ordinal variables have categories with a logical order (e.g., Liker scales), while nominal variables have categories with no logical order (e.g., religious affiliation)

Data

:   A set of values. A data set is typically made up of a number of *variables*. In quantitative research, data are numeric.

Descriptive statistics

:   Procedures that allow you to describe data by summarising, displaying or illustrating them. Often used as a general term for summary descriptive statistics: *measures of central tendency* and *measures of dispersion*. Graphs are descriptive statistics used to illustrate the data.

Frequency/ies

:   The number of times a particular value of a variable occurs.

Histogram

:   a visual display of data used to examine the distribution of a numeric variable


Line graph

:     a visual display of data often used to examine the relationship between two continuous variables or for something measured over time

Missing values

:   A data set may be incomplete, for example, if some observations or measurements failed or if participants didn't respond to some questions. It is important to distinguish these missing data points from valid data. Missing values are the values R has reserved for each variable to indicate that a data point is missing. These missing values can either be specified by the user (user missing) or automatically set by R (`NA`).

Nominal data

:   Data collected at a level of measurement that yields nominal data (nominal just means 'named'), also referred to as 'categorical data', where the value does not imply anything other than a label; for example, 1 = male and 2 = female.

Observation / Case

:   An observation is the unit of analysis; one person or other entity. In psychology, this is normally the data deriving from a single participant. In some research, the cases will not be people. For example, we may be interested in the average academic attainment for pupils from different schools. Here, the observation would be the schools. In R, a single row of data in a data frame represents an observation.

Participant

:   People who take part in an experiment or research study. Previously, the word 'subject' was used, and still is in many statistics books.

Population

:   The total set of all possible scores for a particular variable. 

Quantitative data

:   Is used to describe numeric data measured on any of the four levels of measurement. Sometimes though, the term 'qualitative data' is then used to describe data measured with nominal scales.


Sample

:   A subset of observations from some *population* that is often analyzed to learn about the poplulation sampled.

Scatterplot

:     a graph that shows one dot for each observation in the data set

Summary statistics

:   used to provide an overview of the characteristics of a sample; this typically includes measures central tendency and spread for numeric variables and the frequencies and percentages of categorical variables

Statistics

:   A general term for procedures for summarising or displaying data (*descriptive statistics*) and for analysing data (*inferential statistical tests*).

Variable

:   a measured characteristic of some entity (e.g., income, years of education, sex, height, blood pressure, smoking status, etc.); A variable in R is represented by a column in data frame.

## Terms in R

Argument

:   information input into a function that controls how the function behaves

Assigning

:   assigning a value to an object is done by using a left-arrow (`<-`), with the arrow separating the name of the object on the left from the expression itself on the right: `object_name <- expression`


Character

:     a basic data type in R that comprises things that cannot be used in mathematical operations; often, character variables are names, addresses, zip codes, or other similar values


Comment

:   Statements included in code but not analyzed; in R, comment is denoted by hashtag (`#`) and is often used to clarify the codes

Constants

:   Constants, as the name suggests, are entities whose value cannot be altered. Basic types of constant are double constants, integer constants, logical constants and character constants.

csv

:    a file extension indicating that the file contains comma separated values or semicolon separated values


Data frame

:      an object type in R that holds data with values in rows and columns with rows treated as observations and columns treated as variables


Data management

:     the procedures used to prepare the data for analysis; data management often includes recoding variables, ensuring that missing values are treated properly, checking and fixing data types, and other data-cleaning procedures


Data types

:      in R, these include numeric (double, integer), character, logical; the data type suggests how a variable was measured and recorded or recoded, and different analytic strategies are used to manage and analyze different variable types


Expression

:   An expression is an instruction to perform a particular task. An expression is any sequence of R constants, object's names, operators, function calls, and parentheses. An expression has a type as well as a value.


Factor 

:    A categorical variable and its value labels. Value labels may be nothing more than "1," "2,"..., if not assigned explicitly. More formally, a type of object that represents a categorical variable. It stores its labels in its levels attribute. 


Function 

:    a set of machine-readable instructions to perform a task in R; often, the task is to conduct some sort of data management or analysis, but there are also functions that exist just for fun. 

Index

:   The order number of a variable in a data set or the subscript of a value in a object. The number of the component in a list or data frame, or of an element in a vector.

Integer

:    a similar data type to numeric, but containing only whole numbers


Length

:   The number of observations/cases in a variable, including missing values, or the number of variables in a data set. For vectors, it is the number of its elements (including NAs). For lists or data frames, it is the number of its components. 

Levels

:     The values that a categorical variable can have. Actually stored as a part of the factor itself in what appears to be a very short character variable (even when the values themselves are numbers). 

List

:   A set of objects of any class. Can contain vectors, data frames, matrices and even other lists.

Matrix

:   A data set that must contain only one type of variable, e.g. all numeric or character. More formally, a two-dimensional array; that is, a vector with a dim attribute of length 2. Information, or data elements, stored in a rectangular format with rows and columns.


NA

:    the R placeholder for missing values, often translated as “not available.”



NaN

:   A missing value. Stands for Not a Number. Something that is undefined mathematically such as zero divided by zero.

NULL

:   An object you can use to drop variables or values. E.g. `mydata$x <- NULL` drops the variable `x` from the data set `mydata`. Assigning it to an object deletes it.


Numeric

:   A variable that contains only numbers. This can be double and integer. 


Object

:   information stored in R; data analysis and data management are then performed on these stored objects. Includes data frames, vectors, factors, matrices, arrays, lists and functions.

Operators

:   An operator is a symbol that tells the compiler to perform specific mathematical, logical, or other manipulations. R language is rich in built-in operators and provides following types of operators: Arithmetic Operators, Relational Operators, Logical Operators, Assignment Operators, Miscellaneous Operators.


Package

:   a collection of functions and datasets for use in R that usually has a specific purpose, such as conducting partial correlation anaylyses (**ppcor** package)


Precedence of operations

:     the order in which mathematical operations should be performed when solving an equation: parentheses, exponents, multiplication, division, addition, and subtraction (PEMDAS)


Recycling rules

:   If one tries to add two structures with a different number of elements, then the shortest is recycled to length of longest. That is, if for instance you add `c(1, 2, 3)` to a six-element vector then you will really add `c(1, 2, 3, 1, 2, 3)`. If the length of the longer vector is not a multiple of the shorter one, a warning is given.

RMarkdown file

:     RMarkdown provides an authoring framework for data science. You can use a single R Markdown file to both 1) save and execute code; 2) generate high quality reports that can be shared with an audience.

sav

:     the file extension for a data file saved in a format for the Statistical Package for Social Sciences (SPSS) statistical software



Script file

:   a text file in R similar to something written in the Notepad text editor on a Windows computer or the TextEdit text editor on a Mac computer; it is saved with a `.R` file extension


Vector

:   Vectors are one-dimensional and homogenous data structures. It can exist on its own in memory or it can be part of a data frame. More formally, a set of values that have the same base type. A vector can be a vector of characters, logical, integers or double.

Working directory

:   R uses a working directory, where R will look, by default, for files you ask it to load. It also where, by default, any files you write to disk will go.

Workspace

:   A temporary work area in which all R computation happens. Data that exists there will vanish if not saved to your hard drive before quitting R. More formally, the area of your computer's main memory where R does all its work. Data must be loaded into it from files, and packages must be loaded into it from the library, before you can use either.



## Terms in Statistics and R

+-----------------------------+-----------------------------+
| Terms in Statistics         | Terms in R                  |
+=============================+=============================+
| -   dataset                 | -   data frame              |
| -   sample                  |                             |
+-----------------------------+-----------------------------+
| -   observation             | -   rows in a data frame    |
+-----------------------------+-----------------------------+
| -   variable                | -   columns in a data frame |
+-----------------------------+-----------------------------+
| -   categorical variable    | -   factor                  |
| -   qualitative variable    |                             |
|     -   nominal variable    |                             |
|     -   ordinal variable    |                             |
+-----------------------------+-----------------------------+
| -   numeric variable        | -   numeric vector          |
| -   quantitative variable   |     -   double vector       |
|     -   continuous variable |     -   integer vector      |
|     -   discrete variable   |                             |
+-----------------------------+-----------------------------+

: Terms in statistics and R

# Miscellaneous

## Rules of using R

-   use *RStudio*
-   use *RStudio* in project-oriented environment
-   use *RMarkdown* files in *RStudio*
-   use as many comments as possible

## Good to know

-   R is case sensitive: `Apple` and `apple` are different objects.
-   Use a semicolon to put two or more commands on a single line: `a <- 2+2; a`
-   Force R to print the value of expression by using parentheses: `(a <- 2+2)`

## Why is my code broken?

-   Are all your parentheses in the right places?
-   Do you have commas where you should?
-   How's your capitalization?
-   What about continuation prompt?
-   Did you load the package you're trying to use?
-   If none of these fix your problem, try googling the error message R gives you. There's usually a good StackOverflow question on whatever you're trying to accomplish.

## Other resources

-   [R Cheatsheets](https://www.rstudio.com/resources/cheatsheets/) contain information-dense infographics for many of the packages we've used in this course, and plenty other useful tools you may need in your own work.
-   [My collection (in Hungarian)](https://abarik.github.io/roforrasok/)
