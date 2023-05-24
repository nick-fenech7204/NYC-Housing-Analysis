# New York City Housing Prices
Our group's capstone project will be focused on investigating NYC housing prices and how different factors may contribute/impact prices. We also want to use machine learning techniques to see if we can predict prices in the year following our data (2022). We plan on using NYC Open Data to pull home details as well as an API call to the Census Bureau to combine our NYC housing data with other attributes such as rental/ownership/income/ages/etc to compare our main data set to supplementary information. The aforementioned data can be found at https://www.nyc.gov/site/finance/taxes/property-annualized-sales-update.page.

# Technical Report

###  What Questions are Being asked?
* How do home costs change throughout NYC and its boroughs? 
* What attributes impact the home prices of the boroughs?
* Are there any noticeable patterns or trends in the types of properties that are being sold or rented in New York? 
* What is the average rental rate compared to mortgage rate for properties in different boroughs in New York? 
* What role does income play in the rental/mortgage rates for properties in different boroughs?
* What is the disparity in home ownership from different age groups?
* Can we predict the home prices in 2022 using past data?”

### What Datasets are being used?
* NYC Open Data
* Contains data from the past 20 years of housing sales by borough
* Also shows many useful descriptive factors about each property
* https://www.nyc.gov/site/finance/taxes/property-annualized-sales-update.page
* Census Bureau
* American Community Survey 5-Year Data contains 60 month aggregations
* Survey collects information on housing attributes, transportation, demographics, and economic factors
* Contains information from federal to local municipality levels
* https://www.census.gov/data/developers/data-sets/acs-5year.html

### ETL Process: 
* Create a Pipeline in Azure Data Factory
* Create two Blob Containers, one for raw and one for long term storage
* Pipeline will trigger when a new file is uploaded into the raw blob container
* Upload all CSVs to the long-term storage blob container
* Create two Databricks Notebooks linked to Data Factory
* One Notebook to read in CSVs
* One Notebook to Call the API
* From there, Databricks Notebooks will conduct transformation processes
* Once Transformation has occurred, both datasets will be loaded into SQL denormalized

### Technologies Used:
* Microsoft Azure 
* Databricks
* Kafka
* SQL Database
* PowerBI
* Machine Learning Algorithm 
* Python and PySpark 

### ML Used:
* XGboost

### Conclusions Drawn:
* Over the past 20 years, housing prices have witnessed a significant increase, nearly tripling in value. A crucial determinant of these prices is the neighborhood in which the properties are located, as determined by our machine learning algorithm. The data also indicates a trend of increasing rental payments, suggesting that a growing number of individuals are having to spend more on rent, and less and saving for affordable homes. Additionally, the majority of home value is found to be owned by middle-aged individuals, highlighting their significant stake in the real estate market. So in conclusion, our EDA/visuals/and machine learning collectively sheds light on the dynamic nature of housing prices, the impact of neighborhood factors, rising rental demands, and the substantial ownership of property by age group.
