# Kickstarting with Excel

## Overview of Project

Louise wants to put on a play called Fever, and she has been fundraising for its production. She would like to know how other similar campaigns performed based on their fundraising goals and their launch dates.

### Purpose
The purpose of this analysis is to determine the best time of the year for Louise to launch a theater production, and also to determine the best fundraising goal for plays based on the success or failure of other theater productions. 

## Analysis and Challenges
To perform this analysis, I analyzed the database of other kickstarter campaigns for theater productions and plays. First, I wanted to know what were the outcomes of theater productions based on the month of the year that they launched. To do that, I built a pivot table that used the launch date and the outcome to show how many productions were successful, canceled, or failed based on the month they launched. I also filtered the pivot table to only show me theater kickstarters. I then inserted a line chart to visually show how the theater outcomes performed month to month. 


Second, I wanted to understand the outcome of kickstarters for plays based on their fundraising goal. I created different buckets of fundraising amounts that started at under 1000 dollars and went to over 50000 dollars. I used the countifs function to analyze the kickstarter data to give me a count of how many plays failed, succeeded, or were canceled based on the fundraising goal that they had.


### Analysis of Outcomes Based on Launch Date

The first analysis showed that theater productions launched in the middle of the year fared the best. That is, theater productions with a launch date between April and August performed better than between September and March, and May and June were the best months for launching theater productions. Louise should try to launch her play Fever in May or June to optimize her chance of success.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/14280739/154776265-62fbe2f5-2b5a-487a-bab5-213a5689fe60.png)

### Analysis of Outcomes Based on Goals

The second analysis showed that there is a positive correlation between the fundraising goal and the chance of failure for plays. In general, the lower the fundraising goal for a play, the more likely it will succeed. Even though there was a higher percentage of successful vs failed plays with a fundraising goal between 35k and 45k dollars, there were only a small number of plays that tried to raise this much money. Hundreds of plays succeeded trying to raise under 10k dollars, and the success rate was higher than the failure rate in this fundraising range. Louise should try to raise a lower amount of money for Fever, ideally 5000 dollars or less, to increase her chance of success. 

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/14280739/154776277-62000f9d-2d1f-415d-a3e2-b5357530efe0.png)

### Challenges and Difficulties Encountered

For analyzing the theater outcomes by launch date, one challenge was to correctly group the launch dates. Excel populates several types of groupings for dates, so I had to remember to remove all groupings besides the one that showed the month of launch. I also needed to play around to figure out how to sort the columns in descending order, so that the outcomes showed successful launches first and canceled launches last.

For the outcomes based on goals analysis, it was a challenge to make sure my countifs formulas were including all of the right outcomes based on the filters. We had to use three criteria for 36 different results, so it would be easy to accidentally miss using the right criteria in the formula. I double checked by results by spot checking a few of them against the kickstarter data using manual filters and looking at the count of the results myself. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

The best months to launch a theater production are May and June, and the worst month to launch is October. 

- What can you conclude about the Outcomes based on Goals?

In general, the higher the fundraising goal, the higher the failure rate of the plays. 

- What are some limitations of this dataset?

We didn't filter by country, so we aren't comparing Fever to plays that were produced in the same country. Also, this means that our fundraising goal categories are mixing currencies, which could lead to some erroneous data points about how plays did based on how much money they raised. 

- What are some other possible tables and/or graphs that we could create?

I would first consider adding the same graphs but filtering the data by the country where Louise plans to put on the play Fever, and filtering for the latest year only to show the most recent trends. I would also add a new new analysis which would be a pivot table that shows the values for the average of average donations and the average for the total number of backers filtered for the theater parent category, with the rows being the outcomes of the theater productions. That would give Louise a sense of how many backers she will need to get for a successful play. I would visualize this with a bar chart, that maps the average donation amount and the average amount of backers on the y axis against the outcomes of the play along the x axis. 
