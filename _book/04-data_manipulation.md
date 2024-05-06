# Data manipulation

Data manipulation involves modifying data to make it easier to read and to be more organized. We manipulate data for analysis and visualization. At times, the data collection process done by machines involves a lot of errors and inaccuracies in reading. Data manipulation is also used to remove these inaccuracies and make data more accurate and precise.

## Importation of data
Data import is an essential step in the data analysis process. It involves retrieving data from various sources, such as local files, databases, APIs or real-time feeds. This step acquires the data needed for analysis and decision-making, and is often the starting point for analytical work.

In this part, we will learn to load commonly used **CSV**, **Excel**, **JSON**, **Database**, and **XML/HTML** data files in R. Moreover, we will also look at less commonly used file formats such as **SAS**, **SPSS** and **Stata**. 

Importing data from csv to R:

```r
children_anemia <- read.csv("./data/children_anemia.csv")
```

Importing data from excel to R:



Importing data from json to R:



Importing data from database to R:

Importing data from spss to R:

Importing data from stata to R:


## Basic exploration of data

Data exploration helps you explore and think about the data you're working. The goal with data exploration is to understand,  and visualize data so that you can discover insights, relationships, patterns, and anomalies.
To explore data in R we have many functions to achieve that.

+ Function head(): is used to view the first few rows of your dataset.

+ Function tail(): is used to view the last few rows of your dataset.

+ Function str(): is used to provide the structure of your data frame, showing you the data types. 

+ Function dim(): is used to know about the number of rows and columns.

+ Function summary(): it gives you an overview of your data, including minimum and maximum values, quartiles, and more.

+ Function table(): used to build a contingency table of the counts at each combination of factor levels.

+ Function unique(): The unique() function in R is used to eliminate or delete the duplicate values or the rows present in the vector, data frame, or matrix as well.

+ Function hist(): function to plot a basic histogram to view distribution of a variable.

+ Function boxplot(): function to plot a boxplot, it provides a compact summary of the data's central tendency, spread, and potential outliers.

## Data manipulation with dplyr

In order to manipulate and clean the data, R provides a library called dplyr which consists of many built-in methods to manipulate the data. So to use the data manipulation function, first need to import the dplyr package using library(dplyr) line of code. Below is the list of fundamental data manipulation verbs that you will use to do most of your data manipulations.

+ filter(): 

  The filter() function is used to produce the subset of the data that satisfies the condition specified in the filter() method. In the condition, we can use conditional operators, logical operators, NA values, range operators etc. to filter out data. Syntax of filter() function is given below:

        filter(dataframeName,condition)

+ distinct(): 

  The distinct() method removes duplicate rows from data frame or based on the specified columns. The syntax of distinct() method is given below:
  
        distinct(dataframeName, col1, col2,.., .keep_all=TRUE)

+ arrange():

  In R, the arrange() method is used to order the rows based on a specified column. The syntax of arrange() method is specified below:
  
        arrange(dataframeName, columnName)

+ select():

  The select() method is used to extract the required columns as a table by specifying the required column names in select() method. The syntax of select() method is mentioned below:
        
        select(dataframeName, col1,col2,…)

+ rename():

  The rename() function is used to change the column names. This can be done by the below syntax:
  
        rename(dataframeName, newName=oldName)

+ mutate():

  The mutate() function creates new variables without dropping the old ones. The syntax of mutate() is specified below:
  
        mutate(dataframeName, newVariable=formula)

+ transmute():

  The transmute() function drops the old variables and creates new variables. Here is the syntax:
  
        transmute(dataframeName, newVariable=formula)

+ summarize():

  Using the summarize method we can summarize the data in the data frame by using aggregate functions like sum(), mean(), etc. The syntax of summarize() method is specified below:
  
        summarize(dataframeName, aggregate_function(columnName))
        

**Putting it all together with %>%**:
One of the more useful ways to use dplyr is with the pipe operator. The pipe operator looks like this: %>% ,and it is common practice to use the pipe operator to “pipe” dplyr commands together. It is a way to chain multiple operations together in a concise and precise way. The %>% operator takes the output of the expression on its left and passes it as the first argument to the function on its right.

Example: