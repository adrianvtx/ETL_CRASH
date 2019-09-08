# ETL_CRASH
 
## Team "CRASH" ETL Project

## GOAL

Our goal is to extract data from multiple sources, clean it for ease of analysis for end users, and store the data in a newly created Mongodb database

# Type and source of data

### Data used for this project is for housing industry

There are three data sets used for this project:

#### 1. Mortgage Data
Mortgage rates for "single family" (actually 1 - 4 family) homes for 30 year mortgage on a weekly basis from 2006 - 2009 and 2016 - 2019. This data was downloaded from FRED (Federal Reserve Economic Data) and was provided by Freddie Mac

#### 2. New Construction across the nation
New construction "starts" for single family homes; monthly, also from 2006 - 2009 and 2016 - 2019. This data was downloaded from Google Cloud Services Big Data database.

#### 3. 30-Year Treasury Constant Maturity Rate
The 30-Year Treasury Constant Maturity Rate is an interpolated representation of long term bond yields. This data was downloaded from FRED (Federal Reserve Economic Data), as provided by the Board of Governors of the Federal Reserve System (US).


### Why did we select these years?
We selected these periods to create a database in which current economic indicators can easily be compared to the same indicators surrounding the Great Recession.

...............


### How data was filtered through original source 
#### 1. Mortgage Data
Fred provided the Data for 30 years motgage rates from 1970's until today on a weekly basis. To get two data sets for terms 2006 - 2009 and 2016 - 2019 there is an option to edit graph by dates. Once the data was selected we downloaded the csv files to modify it according to our needs.


#### 2. New Construction across the nation
We accessed the "new housing sonstruction statrs" data from Google Cloud Services Big Data database, with a SQL query in the GCS Big Query portal. Once the target time periods were returned, we donloaded them in both csv and json formats. 


#### 3. 30-Year Treasury Constant Maturity Rate
Fred also provided the 30-Year Treasury Constant Maturity Rate from the 1970's through present on a weekly basis. As above, to get two data sets for terms 2006 - 2009 and 2016 - 2019 we selected the begin and end dates in each period. Once the data selected was returned we downloaded the csv file and then repeated the process for the next period.

### Data Clean up process

#### 1. Mortgage Data
The downloaded csv Mortgage data had two columns (date, and value in %) and was stored on the team repository. The csv files were read into a Jupyter Notebook and the column headers revised for clarity. The date column was then set as the index, and the table converted to a dataframe. 


#### 2. New Construction across the nation
This data set was extracted in two formats, csv and json. We used csv to import it in pandas and analyzed the data. Each set had over 10,000 rows and 20 columns. After going through the data it was filtered to extract the the number of single family homes were contruction began nationwide on a monthly basis. Our rationale for choosing new housing startsis as an economic indicator of availability of capital. In contrast to other data that was dropped from the original dataset, housing starts represents projects planned and permitted but with the crutial additional qualities of being fully financed and then funded for commencement.

#### 3. 30-Year Treasury Constant Maturity Rate
The downloaded csv Treasury data had two columns (date, and value in %) and was stored on the team repository. The csv files were read into a Jupyter Notebook and the column headers revised for clarity. The date column was then set as the index. Before the table was converted to a dataframe, we converted the missing values from the string representation of a "." (decimal point) to the 'float' value of 0.00; although these values still printed as the "." representation.


## Data Storage
All six tables are stored in csv format in the "clean data" folder 

## Data base 
The cleaned tables are loaded individually into a Mongodb database. We chose this structure because of the indirect relationships among the datasets. We were limited to creating these colllections on a single-user instance of Mongodb as we did not have access to a shared resource of same.



# Project Overview and Proposal
 ETL_CRASH is an in-class Data Analytics Project wherein this team is tasked with creating a new database on any subject from existing worldwide web resources. The subjectmatter we chose is comparative financial data. Collecting financial data surrounding the Great Recession, and pairing it with same categories' data from 3-years prior to present day, we hope to create an efficient and compact database for use in comparative analysis of the two periods.

 ETL is the data science acronymn for Extract - Transform - Load ("data-13-1-extract-transform-load.pptx"), the process in which data integration into a database is accomplished: 
 1) Extracting data subsets from various resouces including API's, webforms, webscraping, existing databases, and spreadsheets or tables.
 2) Transforming each subset such that it is internally consistent in format, syntax, structure; and externally consistent with other data subsets to be included in the final integration. 
 3) Loading the data subsets into a database. Depending on the relational vs. non-relational structure of the new database, this step includes database design (and relations).

The earlier grouping of data is from two and a half years prior to the fall of Lehman Brothers, September 15, 2008, to one and a half years after same. The later grouping of data is three years prior to present day. By assembling various data sources in this single resource we are creating a compact resource that can be efficiently accessed for comparative study. 
