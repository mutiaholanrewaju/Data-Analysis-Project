
# Analyze Supermarket Data Across the Country - Company XYZ

Company XYZ owns a supermarket chain across the country. Each major branch located in 3 cities across the country recorded sales information for 3 months, to help the company understand sales trends and determine its growth, as the rise of supermarkets competition is seen to increase.

# Project Steps

## Step 1 - Loading Datasets

In this step, the datasets consist of 3 different branches in different files and the files are passsed in a list consisting of the 3 files with .csv. combination was done to the dataset from each branch (3 branches) into one dataset for easy analysis using the concat method.  The combined data was exported to a CSV format. The pd.read_csv was used to read read combined data for further analysis. 

## Step 2 - Data Exploration

In this step, the loaded dataset was explored using some buit-in pandas function like;
* Numpy and pandas libraries were imported
* Matplot libraries for visualization. 

The head() method was used to view the first few rows of the dataset, the .shape attribute was used to know that there are 1000 rows with 17 columns in the combined data, the column attribute was used to get the list of names in all the 17 columns. The describe method was used to explore the statistical summary of the combined data. 

From the data statistical summary, the following can be derived;

* It could also be seen that a female member with invoice ID 845-94-6841 from Lagos has the most common value with fashion accessories products.

* The average quantity is 5.5 with total amount of 116268.

* The minimum unit price is 3628 while the maximum unit price is 35985.

* The maximum rating is 10.

The info() method was used to get the coincise summary of the dataframe. This method prints information about a DataFrame including the index dtype and column dtypes, non-null values and memory usage. 

isnull() method was used to check for null value and it was shown that the dataset has no null value.


## Step 3 - Dealing with DateTime Features

From the summary above, it was observes that the date and time columns are not in the appropriate data type which led us to convert to datetime datatype using the to_datetime() method. After that was done, the type attribute was used to confirm the datatype.

Features like Day, Month, Year and Hour were extracted from the date column using the .dt attributes and all the features were saved into another column each.

unique() and nunique() method were used to accurately determine the unique hours and number of unique hours of sales in the supermarket respectively.


## Step 4 - Unique Values in Columns

Iteration was done through the columns to check if each element is an object datatype. The result was saved to the "categorical_columns" variable as a list.
.unique().tolist() method was used to get the unique values in each categorical columns with object elements. The supermarket has 3 unique branches, situated in 3 different states, 2 types of customers, 2 types of gender, 6 product lines and uses 3 differnt payment mode.

The count figure of the categorical values was generated using the value_counts() method. 


## Step 5 - Aggregation with GroupBy

A groupby object with the "City Column" was created and aggregation function of sum and mean was done on the groupby table.
  
Using the groupby object, a table that shows the gross income of each city was displayed, and Port Harcourt was seen as the city with the highest total gross income.
  
The groupby object with the sum() method was used to explore other columns like Unit price, Quantity, Total and gross margin percentage. It was determined that Lagos has the  highest unit price, quantity and gross margin percentage respectively. Port Harcourt has the highest Total.
   
The groupby object with the sum() method was also used to explore other columns like product line and gross income columns. Food and beverages has the highest gross income from the extraction.
  

## Step 6 - Data Visualization

In this section, answers were provided to some questions by generating charts and making use of different plotting styles. Seaborn visualization library was used to generate plots. For all visualizations, a chart title was included by using the seaborn set_title method.

 * Appropriate use of countplot to determine the branch with the highest sales record.
 * Appropriate use of countplot to determine the most used payment method & city with the most sales.
 * Appropriate use of countplot to determine the highest & lowest sold product line.
 * Result that shows the Payment channel used by most customers to pay for each product line. 


# Insights
* Branch A(Lagos) has the highest sales record.
* Epay is the most payment method used.
* Fashion accessiories has the highest Product line sold 
* Health and beauty has the lowest Product line sold respectively.
* Epay method is mostly used in branch A (Lagos).
* Branch A(Lagos) and B(Abuja) use cash mode of payment equally.
* Branch B has the lowest rating.
* Females get more of Fashion Accessories.
* Health and beauty products are bought mostly by males
* The purchase of Food and beverages, Electronic accessories and Sport and travel are distributive between the two genders.
* Fashion accessories has the lowest quantity bought and the higest unit price respectively.
* Electronic accessories has the highest quantity sold and the lowest unit price respectively.



# Future Work

* Churn prediction analysis to predict customers that are likely to stop patronizing the supermarket.
* Profit prediction analysis to forcast product line, branches and customers that will increase the supermarket profit.


# Standout Section

* I created a DataFrame object to store the unique value of each categorical column to reduce the syntax when using the print function to display the unique values.
* Agrregate function of sum and mean was done and shown on a single DataFrame instead of doing for sum seperately and mean seperately.
* Plt.legend was used to avoid the plot overlapping the legend.
* More Seaborn visualization plots like boxcount, swarm, violin etc were used.

## More Insights
* Female has the lowest rating count.
* Male uses more of Epay method while Female uses more of Cash to transact.
* Lagos has more of Male that patronize the supermarket
* PortHarcourt has more of Female that patronize the supermarket.
* Abuja also have more of male but with little difference to the female count.
* Port Harcourt pay the higest tax since it has the highest sales record.
* Lagos pay the lowest tax.


# Executive Summary.

Executive Summary document can be found in this git repository.
