# ETL_CRASH
 
## Team "CRASH" ETL Project

## GOAL

Our goal is to extract data from different sources that and clean it so it's easier to analyze and create a database to store that data

# Type and source of data

### Data used for this project is for housing industry

There are two data sets used for this project

#### 1. Mortgage Data
Mortgage rates for 1 - 4 family homes for 30 year mortgage on a weekly basis from 2006 - 2009 and 2016 - 2019. This data was downloaded from FRED and was provided by Freddie Mac

#### 2. New Construction across the nation
Number of new single family homes being constructed on a monthly basis for same terms. This data was downloaded from Google Cloud 

### Why did we select these years?

...............


### How data was filtered through original source 
#### 1. Mortgage Data
Fred provided the Data for 30 years motgage rates from 1970's until today on a weekly basis. To get two data sets for terms 2006 - 2009 and 2016 - 2019 there is an option to edit graph by dates. Once the data was selected we downloaded the csv files to modify it according to our needs 


#### 2. New Construction across the nation


### Data Clean up process

#### 1. Mortgage Data
Mortgage data had two columns and was avau=ilable in csv ...................


#### 2. New Construction across the nation
This data set was extracted in two formats, csv and json. We used csv to import it in pandas and analyzed the data. Each set had over 10,000 rows and 20 columns. After going through the data it was filtered to extract the the number of single family homes that were contructed throughout the nation on a monthly basis. This data set can be compared it with the mortgage rates to check if one effects the other


## Data Storage
All four tables are stored in csv format in clean data folder 

## Data base 





 ETL_CRASH is an in-class Data Analytics Project wherein this team is tasked with creating a new database on any subject from existing worldwide web resources. The subjectmatter we chose is comparative financial data. Collecting financial data surrounding the Great Recession, and pairing it with same categories' data from 3-years prior to present day, we hope to create an efficient and compact database for use in comparative analysis of the two periods.

 ETL is the data science acronymn for Extract - Transform - Load ("data-13-1-extract-transform-load.pptx"), the process in which data integration into a database is accomplished: 
 1) Extracting data subsets from various resouces including API's, webforms, webscraping, existing databases, and spreadsheets or tables.
 2) Transforming each subset such that it is internally consistent in format, syntax, structure; and externally consistent with other data subsets to be included in the final integration. 
 3) Loading the data subsets into a database. Depending on the relational vs. non-relational structure of the new database, this step includes database design (and relations).

The earlier grouping of data is from two years prior to the fall of Lehman Brothers, September 15, 2008, to one year after same. The later grouping of data is three years prior to present day. By assembling various data sources in this single resource we are creating a compact resource that can be efficiently accessed for comparative study. 

We decided to use Mongodb as the database framework.....
