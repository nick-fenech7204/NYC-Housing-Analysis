# New York City Housing Prices
Our group's capstone project focused on investigating New York City housing prices and how different factors impacted prices. We also used machine learning techniques to attempt to predict prices in the later years of the dataset. We used NYC Open Data to access property details as well as an API call to the Census Bureau. This was done to combine the NYC housing data with other attributes such as rental/ownership/income/ages/etc and compare our main data set to supplementary information. The aforementioned NYC Open Data can be found at https://www.nyc.gov/site/finance/taxes/property-annualized-sales-update.page.

## Our GitHub Repository
This repository contains the major steps of our project from beginning to end. There is a folder with some of the data that we used as well as a folder containing exploratory data analysis to make sure that the datasets in question were usable and could be analyzed extensively. There is a folder where our group planned for the future steps of the project such as the ETL phase and the ERD diagram for our SQL database. One can also view our Databricks notebooks in which we performed our ETL steps to prepare the data for analysis. This allowed us to perform machine learning and create visualizations in Power BI before combining everything into a final presentation. All of these files can be accessed through their respective folders. Happy viewing!

## Technical Report

###  What Questions are Being asked?
* How do home costs change throughout NYC and its boroughs? 
* What attributes impact the home prices of the boroughs?
* Are there any noticeable patterns or trends in the types of properties that are being sold or rented in New York? 
* What is the average rental rate compared to mortgage rate for properties in different boroughs in New York? 
* What role does income play in the rental/mortgage rates for properties in different boroughs?
* What is the disparity in home ownership from different age groups?
* Can we predict the home prices in 2022 using past data?”

### What Datasets are being used?
##### NYC Open Data
* Contains data from the past 20 years of housing sales by borough
* Also shows many useful descriptive factors about each property
* https://www.nyc.gov/site/finance/taxes/property-annualized-sales-update.page
##### Census Bureau
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
* XGboost is one of the most popular machine learning algorithms used today
* Trained our model on data from years 2003-2017 and tested it on data from years 2018-2022
* Used a variety af factors to attempt to predict the sale price of properties
* Removed outliers with very high prices since they were not representative of the population
* Test set accuracy score of 0.64
* The two most important features to the model were the borough and the nieghborhood in which the property was located

![MicrosoftTeams-image](https://github.com/prateekbardhan/Illidan/assets/128511132/4e7a8c3e-ad2f-47aa-88b1-2bbcf0415a67)

### Conclusions Drawn:
* Over the past 20 years, housing prices have witnessed a significant increase, nearly tripling in value
* A crucial determinant of these prices is the neighborhood in which the properties are located, as determined by our machine learning algorithm
* The data also indicates a trend of increasing rental payments, suggesting that a growing number of individuals are having to spend more on rent, and less and saving for affordable homes
* Additionally, the majority of home value is found to be owned by middle-aged individuals, highlighting their significant stake in the real estate market
* So in conclusion, our EDA/visuals/and machine learning collectively sheds light on the dynamic nature of housing prices, the impact of neighborhood factors, rising rental demands, and the substantial ownership of property by age group

### Example Charts: 

![Screenshot (119)](https://github.com/prateekbardhan/Illidan/assets/128511132/c825d00e-a492-49c1-ab52-0caf3e3580cc)

![Screenshot (120)](https://github.com/prateekbardhan/Illidan/assets/128511132/9692fdca-d390-41d9-9faa-7c55f18f65b6)



