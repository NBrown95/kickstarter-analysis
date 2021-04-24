# Kickstarting with Excel

## Overview/Purpose of Project

Louise is interested in fundraising goals of plays that are similar to her play Fever. She came close to her fundraising goal in a short amount of time and wants to know how other fundraising campaigns fared in relation to their goals and launch dates. Kickstarter data is analyzed to examine and visualize campaign outcomes based on their launch dates and their funding goals.

## Analysis and Challenges

To visualize campaign outcomes based on launch date, a pivot table was created in Excel. Then, a new worksheet in Excel was created to visualized the percentage of successful, failed, and canceled plays based on the funding goal amount.

### Analysis of Outcomes Based on Launch Date

First, to easily filter outcomes by month, it is important to create a new column representing the years that each campaign was launched. This is seen in the following image.

![Screenshot 1](https://user-images.githubusercontent.com/81498850/115948330-62394400-a493-11eb-9cef-0e8a55a217db.png)

Then, the pivot table was created in a new worksheet. Since we are interested in outcomes of plays by launch date, we add the “Years” column to the Filters section while formatting the pivot table. Similarly, we add “Parent Category” to the Filters section as well as we are only interested in one category, which is theater. We then place “Outcomes” in the Columns section as well as “Outcomes” in the Values section as we are interested in the count of each outcome. In the Rows section, we put “Date Created Conversion.” The following image displays the fields for the pivot table.

![Screenshot 2](https://user-images.githubusercontent.com/81498850/115948365-9c0a4a80-a493-11eb-9618-30ea89c6e3df.png)

Once the pivot table is created, the column labels were sorted from Z to A to show “successful” outcomes first and “canceled” outcomes last. Also, the Parent Category was filtered to only show “theater.” This ensures that we are only looking at the outcomes of plays. Finally, the row labels were grouped into months by selecting the whole column, right-clicking on the column, and then selecting “Group.” The following image is how the pivot table now looks.

![Screenshot 3](https://user-images.githubusercontent.com/81498850/115948383-b3e1ce80-a493-11eb-86d8-f0d1a4c104b0.png)

To fully visualize this table, we created a line chart. Line charts are used to visualize data over time. Therefore, we displayed the months of the year on the x-axis and the count of outcomes on the y-axis. The lines themselves represent successful, failed, and canceled fundraising campaigns for plays. This line chart is seen below.

![Theater Outcomes by Launch Date](https://user-images.githubusercontent.com/81498850/115948513-20f56400-a494-11eb-9368-13b348a6fdb8.png)

### Analysis of Outcomes Based on Goals

Now, we want to visualize the percentage of successful, failed, and canceled plays based on the fundraising goal. To do this, we created a new worksheet and created eight columns representing (in order): Goal, Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Failed, and Percentage Canceled. In the Goal column, twelve rows were created representing dollar-amount ranges. This column can be seen in the following screenshot.

![Screenshot 4](https://user-images.githubusercontent.com/81498850/115948555-4da97b80-a494-11eb-870b-f6e81f5eab5e.png)

In order to count the number of plays that were successful, failed, or canceled, we used the COUNTIFS() function in Excel. This function allows us to select ranges and criteria for multiple columns. For example, to count the number of plays that were successful that had a goal of less than $1000, we use the following formula. The column D represents the goal that was set for each campaign. Column F represents the outcome of the campaign and column R represents the subcategory. In this instance, the subcategory is plays. The formula can be seen below.

![Screenshot 5](https://user-images.githubusercontent.com/81498850/115948562-6154e200-a494-11eb-9c3a-7a5b211c662c.png)

Each goal range is totaled in Column E by using the sum function. To complete the percentages, each cell has a formula that divides the total number of that outcome by the total amount of projects. This process is completed for all the outcomes and all goal ranges. The final table is shown in the following image.

![Screenshot 6](https://user-images.githubusercontent.com/81498850/115948575-729dee80-a494-11eb-90c0-998a84adc1d1.png)

To visualize this table, we created a line chart with the dollar-amount goals on the x-axis and the percentage of outcomes on the y-axis. The lines themselves represent successful, failed, and canceled campaigns. We notice there were no canceled campaigns for plays. The line chart is seen below.

![Outcomes vs Goals](https://user-images.githubusercontent.com/81498850/115948590-86e1eb80-a494-11eb-887e-bb79cb1f70ca.png)

### Challenges and Difficulties Encountered

The only challenge encountered during this analysis was that the data collected from Kickstarter required the launch dates and deadline dates to be converted into readable dates. This was solved by using a formula that takes the number given in the raw dataset, divides it by 60, divides it by 60 again, and then divides it by 24. Then, this result is added to the date January 1, 1970. This gave the readable date of when the campaign was launched and ended.

## Results

One interesting conclusion about the relationship between outcomes and launch dates is that the campaigns had more success when launched in May or June. In both of these months, more than twice the number of theater campaigns were successful rather than failed. There were more theater campaigns started in these months as well which shows that it may be a good idea to start the fundraising in the beginning of summer. 

Another conclusion is similar to the first. Theater campaigns that are started in the later months were not as successful. In fact, in December, there were 37 successful campaigns, 35 failed campaigns, and 3 canceled campaigns which shows that less than half of all theater campaigns started in December were successful. 

As expected, we can conclude that the lower the goal amount for a theater campaign, the more likely it is to be successful. Over 73% of theater campaigns were successful with goals under $5,000. As the goal amount increases, the success rate drops and the failure rate increases. 

One limitation of this dataset is there are only a total of 42 projects with a goal of over $25,000. That means in this dataset, only about 4% of theater campaigns had a goal over $25,000. Therefore, it is difficult to conclude that campaigns with such high goals aren’t as likely to succeed. Intuitively, smaller goals are easier to reach, but we should not rule out the possibility of having a higher or lower success rate for higher goal amounts. 

Other possible tables or graphs that can be created include a table showing the successful theater campaigns as well as a brief description of the play as well as the failed campaigns with a description. This can help identify if there are other factors that influence the success of a fundraising campaign such as more interest by the public in the topic or style of the play. 
