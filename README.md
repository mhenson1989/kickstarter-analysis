# **Kickstarter Analysis**

## **Overview & Purpose**

The purpose of this project was to create a comparative analysis of fundraising campaigns, specifically looking at the theater and play subcategories. Within this analysis I focused specifically on **Outcomes Based on Goals** and **Theater Outcomes by Launch Date**. 

Ultimately, the goal of this analysis was to determine the success of Louise's fundraiser in comparison to other fundraising projects. This will help Louise assess future fundraisers, as well as a possible extension of her existing fundraiser. 

## **Analysis and Challenges**

### *Analysis of Outcomes Based on Launch Date*

In my **Theater Outcomes by Launch Date** analysis, I looked at total number of theater specific fundraisers, categorized by successful, failed, and cancelled outcomes, as well as by month in order to glean which months yielded better fundraising results compared to others.

I utilized the pivot table function in Excel and added the following criteria:

	1. In the Filters Field
  	  - Parent Category
  	  - Years
	2. In the Columns Field
  	  - Outcomes
   	  - Successful
  	  - Failed
   	  - Cancelled
	3. In the Rows Field
  	  - Date created
   	  - By Months
	4. In the Values sorted by Field
  	  - Count of Outcomes  

I then created a corresponding line graph that mapped these three outcomes, using **Months** along the *X-Axis* and **Total Number of Outcomes** along the *Y-Axis*. 

![Theater Outcomes by Launch Date Chart](https://github.com/mhenson1989/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

Based on this data, one can infer that the most successful fundraising campaigns are happening within your summer months of May, June and July, with May being the most ideal month to launch a theater fundraising campaign. 
Second to this, campaigns starting in February and August have decent rates of success as well. However, it is ill advised to launch a fundraising campaign in Q4 as there is a higher liklihood of failed campaigns and less overall successful campaigns. 

### *Analysis of Outcomes Based on Goals*

Within my **Outcomes Based on Goals** analysis, I analyzed the total number of successful, failed, and cancelled projects, in terms of overall count, as well as percentage. These totals and percentages were categorized by a goal range starting at *Less than 1000* all the way up to *50000 or More*. 
In this analysis, I utilized the **CountIf** function in Excel to categorize the total counts within the three categories of outcomes:
	-Number of Successful Campaigns
	-Number Failed Campaigns; and
	-Number Cancelled Campaigns

I've included one example of my CountIf equation below. This example is based on cell B2, which is looking at the **Number of Successful Fundraising Campaigns** with a goal of **Less than 1000*.
	-*Example:* 
```
=COUNTIFS(Kickstarter!$D:$D, "<1000",Kickstarter!$F:$F, "successful", Kickstarter!$R:$R, "plays")
```

I then calculated the percentage of these three outcome categories within each goal range by dividing the number of the outcome by the total project number within that goal range, times 100. 
Finally, I graphed these outcomes using a line graph, where the **Goal Range** is the *X-Axis* and **Percentage** is the *Y-Axis*. 

![Outcomes Based on Goals Chart](https://github.com/mhenson1989/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

Overall, the data shows that fundraising campaigns with smaller goals, specifically Less than 1000 and 1000 to 4999 have an overall higher percentage of success compared to larger campaigns. These campaigns see an approximate success rate of 75%, whereas the next most successful campaigns average approximately 67%. Interestingly, these campaigns with a success average of 67% had overall goals of between 35000 and 45000.
It's possible that the overall scale of the campaign is an important factor to success when looking at this analysis. To clarify, donors might have interest in a smaller campaign because it's less dollars contributed, and therefore less risk. Conversely, a donor might also find value in investing large dollars into a large campaign because the revenue yield overall could result in much higher dollars earned. 

### *Challenges and Difficulties Encountered*

I experienced some difficulty utilizing the CountIf function in Excel, particuarly when establishing a specific range. Initially, I added my range criteria as one block, where the >=Value was directly next to the <=Value; only then did I add my additional criteria to specifically filter the data by outcome and subcategory. 
However, I found that my CountIf function was more successful if I nested filter criteria (i.e. outcome and subcategory) within my range. Once I was able to fix this equation, I was able to copy and paste across each goal range and simply update the values. 

I experienced less challenges in the Theater Outcomes by Launch Date analysis. The only challenge I faced was in my initial pivot table, the actual values of my columns and rows were blank. I realized this is because I had not added a field to the Value column. Once I remembered to do so, the pivot table populated easily. 

## **Results**

*1. What are two conclusions you can draw about the Outcomes based on Launch Date?*
  - The best month to launch a Theater Fundraising Campaign is within the Month of May.
  - Overall, it is ill advised to launch a Theater Fundraising Campaign within Q4.

*2. What can you conclude about the Outcomes based on Goals?*
  - Campaigns with smaller fundraising goals, under 5000, are more likely to succeed than fail. 
  - Campaigns with a goal of 45000 or More have a very low liklihood of success.

*3. What are some limitations of this dataset?*
  - The dataset does not include information on tactics of each campaign. Though Louise can generally glean when to start a campaign and how much to ask for, it does not categorize the type of fundraising campaign.
      - Was this a grass roots campaign?
      - Was this a complete marketing campaign?
      - Was this campaign based on lifetime donors or first time donors?
  - These types of questions will ultimately be the make or break contributing factor to the overall success of a fundraising campaign. 

*4. What are some other possible tables and/or graphs that we could create?*

 - I might also consider creating an analysis that cross references the Outcomes Based on Goal and segment it again by Launch Date. This might help pinpoint an exact campaign to start, or might shed some light on if certain goals correlate and are more successful during certain launch date time periods. 
 - Additionally, I might also create a clustered bar chart that looks at Number of Outcomes by Category compared to Goal. 
