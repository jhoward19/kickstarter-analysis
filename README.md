**#Kickstarting Analysis**

## Overview of Project
In this analysis you will find two excel worksheets that describes the campaign outcomes numerically in pivot tables and line charts. In the first worksheet, Theater Outcome by Launch Date, will provide a detailed information on the outcomes of projects in theater by each month of the year. In the second worksheet, Outcome Based on Goal, will provide detailed information on the outcomes of projects based on their funding goals. 

### Purpose
The purpose of this analysis is to provide Louise’s with a detailed explanation on how different campaigns performed in relation to their launch dates and their funding goals. Since Louise’s play Fever came close to its fundraising goal in a short time frame this analysis will also provide Louise with suggestions or information on how to proceed in the future or her next production. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

The Outcomes Based on Launch Date worksheet, pivot table and line chart show how many successful, failed and canceled projects in theater for each month of the year. In order to obtain the information showed in the worksheet I had to create a pivot from the original Kickstarter workbook and filtering it to Parent Category and Years. Then I put outcomes in the columns and values box, date created conversion in the rows column. In order to get the months of the year I grouped the column just to show the months of the year. 
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/91230916/137475206-5c03be90-15cf-4631-a7d0-a0d43fb8c760.png)

### Analysis of Outcomes Based on Goals

The Outcomes Based on Goals worksheet and line chart overall shows the percentage of successful, failed and canceled plays performed in relations to their fundraising goals. 
In the header row I labeled each column with the respective title goals, number successful, number failed, number canceled, total projects, percentage successful, percentage failed, percentage canceled. In the number successful column I used the =countsifs formula, (=COUNTIFS ('Kickstarter Book'!$D:$D,"<1000",'Kickstarter Book'!$F:$F, "successful",'Kickstarter Book'!$R:$R, "plays")), and I just changed the range to calculate the correct number in each row and each column. In order to calculate the total projects, I used the =sums function. To calculate the percentage columns, I used the percentage formula. 
![Outcome_vs_Goals](https://user-images.githubusercontent.com/91230916/137475221-d18dd17b-2bed-4e4f-a3ab-09a2389736ea.png)

### Challenges and Difficulties Encountered
Analyzing the data, I have come across several challenges in order to generate the results. The first challenge was in the in the Theater Outcomes Launch Date data. The year function kept returning an error because I was pulling from the wrong row from the Kickstarter workbook. I didn’t realize my workbook had filters on it. In order to ensure I was pulling from the correct rows I had frozen the panes to make sure I was using the year function correctly. 

The second challenge was using the =COUNTSIFS function in the Outcome Based on Goals worksheet. I wasn’t entering the goal ranges correctly therefore I was getting an error message that stated that I had too few arguments for the function to generate the correct number of successful, failed and canceled plays. In order to rectify the error I had to repeat the goal in the formula to look like this =COUNTSIFS(Kickstarter!$D:$D, “<= 1000”, Kickstarter! $F:$F, “successful”, Kickstarter! $D:$D, “>=4999”, Kickerstarter! $R:$R, “plays”)

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
The number of successful projects in theaters by launch date was most successful between the months of May and June around the beginning of the summer and its starts to decline thereafter when the weather seems to be cooling down leading into winter months.  Also, there were no canceled projects in theater in the month of October even though that’s when the projects failed increased. 

- What can you conclude about the Outcomes based on Goals?
The number of plays and projects that was more successful their funding goal wasn’t any more than $4999. We can conclude that Louise can set a reasonable funding goal of $5000 and be very successful. 

- What are some limitations of this dataset?
The dataset analyzed plays or projects in multiple countries so the currencies doesn’t hold the same weight which may cause the numbers to not be accurate or reflective of what Louise really want to understand how her play did compared to other plays. Another limitation of this dataset is that the genre of the plays is different in this analysis, so the comparison maybe skewed.

- What are some other possible tables and/or graphs that we could create?
This dataset was huge enough to create more pivot tables that were filtered by genre and other possible graphs could have been histograms or box and whiskers. These other possible tables and charts could provide a true comparison to Louise’s play. 

