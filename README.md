# excel-challenge
## first challenge assignment analyzing crowdfunding data
## download and open CrowdfundingBook
## Conditional format "outcome" row. 
![image](https://user-images.githubusercontent.com/127699499/233094564-07bdb612-be93-4b84-9e8f-90d106dad568.png)

## Percent Funded column created and function added: =pledged/goal and then formatted to percent.  Percent Funded then conditionally formatted 
![image](https://user-images.githubusercontent.com/127699499/233095158-7bbb5d72-0db6-4e12-8b1a-138c5c038438.png)

##Average Donation column create and formula of =pledged/backers  and then formatted to currency
##Parent Category created and formula =TEXTBEFORE("category & sub-category","/",1)
##Sub Category created and formula =TEXTAFTER("category & sub-category","/",1)
##Pivot table and pivot chart created to show “Parent Category” in rows and “outcome” in columns
##Pivot table and pivot chart created to show “Sub Category” in rows “outcome” in columns.  Filters for parent category and country added
##“Date Created Conversion” column created and =(((L2/60)/60)/24)+DATE(1970,1,1) pasted from reference website to convert date.  Results were formatted in “short date”.
##“Date Ended Conversion” column created and =(((N2/60)/60)/24)+DATE(1970,1,1) pasted from reference website to convert date.  Results were formatted in “short date”.
##Pivot table and pivot chart created to show the outcome of campaigns by month.

##Analysis written on the three pivot tables


#CROWDFUNDING GOAL ANALYSIS
##New Sheet was created with 8 columns, as directed
##The first row was populated with different goal parameters
##The next column, “Number Successful”, is imported with the follow calculation =COUNTIFS(Crowdfunding!D2:D1001, “<1000",Crowdfunding!G2:G1001, "successful") with the appropriate range changed according to the row
##The next column, “Number Failed”, is imported with the following calculation =COUNTIFS(Crowdfunding!D2:D1001,"<1000",Crowdfunding!G2:G1001, "failed") with the appropriate range changed according to the row
##The next column, “Number Canceled”, is imported with the following calculation =COUNTIFS(Crowdfunding!D2:D1001,"<1000",Crowdfunding!G2:G1001, "canceled") with the appropriate range changed according to the row
##The rows are then summarized with the following calculation to get the “Total Projects” =SUM(B2:D2)
##“Percentage Successful” was created with this calculation “=B2/E2” and then formatted as a percent.
##“Percentage Failed” was created with this calculation “=C2/E2” and then formatted as a percent.
##“Percentage Canceled” was created with this calculation “=D2/E2” and then formatted as a percent
##A line chart was created with the data to show the ranges on the X axis and percentages on the Y axis.  

##An analysis of the chart was added to word.

#STATISTICAL ANALYSIS
##Original Crowdfunding data sheet filtered to “successful” oucome and the list of “successful” campaigns and respective number of backers copied and pasted in the new sheet. 
##This is repeated for the “failed” campaigns.
##The mean for “successful” campaigns was obtained with the =AVERAGE(B2:B566) calculation.  The median for this dataset was obtained with =MEDIAN(B2:B566).  The Minimum was obtained with =MIN(B2:B566).  The maximum was obtained with =MAX(B2:B566).  The variance was obtained with =VAR.P(B2:B566) (though it was originally done with VAR.S because this is a sample of the total population…it was discussed in class that the correct answer is VAR.P).  The standard variation was calculated with a =STDEV.P(B2:B566), again initially done with STDEV.S as this is a sample, but the class discussion changed my answer only because it was provided.

##This process was replicated with the same formulas but different ranges for the “failed” campaigns.
##The values were pasted (values only) at the top of the page for quick and easy reference.

##Box and whisker charts as well as bar charts were created for both data sets to help analyze the data.
##A pivot table of frequency (value changed to count, not sum) was created for both data sets and then placed in a bar chart to analyze the data sets.

##My findings were added to word.
