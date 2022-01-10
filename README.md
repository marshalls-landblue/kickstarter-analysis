# Kickstarting with Excel

## Overview of Project

This analysis focuses on a dataset of Kickstarter campaigns including their funding goals, progress, and categories. Using this data, we highlight the success rate of projects in the Theater category across different date ranges and subcategories.

### Purpose

After Louise's play was funded so quickly, we want to dig deeper into Kickstarter campaigns as a a whole and how they perform considering how ambitious the goals are and also taking into account the seasonality of backer behaviour.
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

In this excercise, we used a Pivot Tables and a line chart to visualise the number of campaigns that were either successful, failed, or canceled, based on the date they were originally launched. 

This dataset included a Category/Subcategory field. It is useful to create more granular data, so we split that info into 2 categories by delimiter (/)
![image](https://user-images.githubusercontent.com/17416097/148721623-c2b27486-5302-43ea-bc6c-356d9a7d265a.png)

Then it was necessary to convert the start date and end date fields to Excel date format. They were provided in Unix Timestamps which need to be converted to days and added to the date 1 Jan, 1970.
![image](https://user-images.githubusercontent.com/17416097/148722211-ff664889-0a03-4b84-a14a-842428caf96a.png)

Next we examined the data, filtering by the entire "Theater" Category in a Pivot table. Using the Starting Dates we converted earlier, we can look at each calendar month individually and graph that data
![image](https://user-images.githubusercontent.com/17416097/148722277-a640e84b-ea1f-48a3-bbd2-55733716fa5e.png)


### Analysis of Outcomes Based on Goals

Next we decided to look more closely at the campaign outcome compared to the goal dollar amount that was set. Projects with a lower goal could have a higher likelyhood of meeting it, while perhaps having less interest if it is a simpler project.

Note: for this excercise, we focused only on the plays subcategory

To aid in this analysis, we manipulated the dataset to create more useful and presentable information.

First we binned the campaigns by Goal amount ranges of $5000 each. 
![image](https://user-images.githubusercontent.com/17416097/148722820-48428a05-250f-42eb-a752-98cea058f6df.png)

Looking at just the number of campaigns doesn't give us a full view of the information though, so we converted this to a percentage of campaigns that were either successful, failed, or canceled. Using this information we can see how each Goal bracket compares to the others.
![image](https://user-images.githubusercontent.com/17416097/148723004-14f608b7-0ddc-4d6b-9a6f-057cfe3e868e.png)

Then finally, using this new table, I created a graph to present the information. You can use this graph to observe trends of the percentage of each outcome compared to its goal.
![image](https://user-images.githubusercontent.com/17416097/148723102-fde568e1-355a-46ec-8188-cd68e8ca8a09.png)

### Challenges and Difficulties Encountered

This project was pretty straightforward, so I did not encounter any real difficulties. I do think it could be a bit challenging to work with this data in Excel. For example, someone could run into an issue using COUNTIF() in the Outcomes Based on goals by not using $ operators and dragging the formula down so that it references the wrong range. I also have had troubles in the past working with dates, you have to be very careful, because Excel uses different date object formatting than other programming languages you may be used to.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1. More campaigns are successful when launched in the spring-summer months of the year. Yes, there are a lot more campaigns launched in total; but if you compare the trend of failed/canceled campaigns to that of the successful ones, it still has a substantial jump. This suggests that perhaps more people will back theater campaigns in a season when they are more interested in going to the theater.

2. The amount of canceled campaigns is very low and doesn't seem to have any correlation to the launch date at all.

- What can you conclude about the Outcomes based on Goals?

Campaigns with lower goals have a higher success rate, and trend down as the goal amount inreases, except for goals between 35000 and 45000 where there are more successful than failing.

- What are some limitations of this dataset?

There are many limitations to this analyis. For one, there are a lot less campaigns with higher value goals. That makes our Outcomes based on Goals chart less reliable to draw conclusions off of, because some of the bins of data have a much smaller sample size which is more prone to error or outliers.

- What are some other possible tables and/or graphs that we could create?

I think it would be interesting to look at theater "Theater" Kickstarter Success percentage compared to Kickstarter campaigns as a whole. We could easily do this by calculating the percentage succeeded for the whole dataset and creating a pivot table.

I think it would also be interesting to utilize the geographical information provided, and compare different countries.
