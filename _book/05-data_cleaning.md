# Data cleaning

In the domain of data science, R reigns supreme as a tool for transforming raw data into actionable insights. 
Data cleaning, a core competency of R, empowers us to clean, filter, transform, and aggregate data, paving the way for meaningful analysis. This introductory paragraph delves into the world of data manipulation and data cleaning in R, highlighting its significance and exploring the key concepts involved.

There are several methods used for data cleansing, including:

1) Adressing data Inconsistencies: 

Suppose the dataset combines data from different sources, which are stored differently. We can standardise these inconsistencies as follows:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *Data Standardisation*:

We can standardise the names to follow a consistent format. For example below, the column names “Age” and “Score” have been standardised to “age” and “score” in the dataframe. This lowercase naming convention is consistent with the other column names.
    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *Data Integration*:

When combining data from multiple sources, ensure that all data fields align correctly.


2) Handling Missing Data: 

Missing data, also known as missing values, is a common challenge encountered in data analysis. It refers to the absence of information for specific variables in certain observations within your dataset. To deal with missing data we have two options: impute data or remove data.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.1) Imputation

we can use imputation by mean, median or mode.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *Imputation by mean*:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *Imputation by median*:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *Imputation by mode*:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.2) Removing data

There are three primary methods for deleting data when dealing with missing data: listwise, pairwise and dropping variables.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *Listwise*:

In this method, all data for an observation that has one or more missing values are deleted. The analysis is run only on observations that have a complete set of data. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- *Dropping variables*:

If data is missing for a large proportion of the observations, it may be best to discard the variable entirely if it is insignificant.


3) Removing duplicates: 
Removing duplicates ensures that each data point is represented only once, leading to more accurate and consistent data for analysis.


4) Checking data structure: 

Checking data types is a crucial step in data analysis because it ensures you're working with the data in the way it's intended in order to avoid errors later in the analysis.