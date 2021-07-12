# kickstarter-analysis
Module 1 Challenge  - Qian Dong <just4qd@gmail.com>

---

## Overview of Project
This report is based on the analysis and visualizations of Kickstarter dataset. In this challenge, two new analyses have been created: outcomes based on goals and outcomes based on launch date. Because Louise is interested in starting a campaign for theater, those two new analyses can help Louise to know how different campaigns fared in relation to their launch dates and their funding goals. 

---

## Analysis and Challenges
### Deliverable 1: Outcomes Based on Launch Date Chart
#### Analysis
- Used the ``YEAR() ``function to extract the year from the “Date Created Conversion” column, and created a new column labeled "Years".
<img width="873" alt="1" src="https://user-images.githubusercontent.com/86527347/125212593-20d75a00-e274-11eb-9de9-362aa4806440.png">

- Created a pivot table from the KickStarter worksheet, filters on "Parent Category" and "Years", and placed the pivot table in a new Theater Outcomes by Launch Datesheet.
<img width="187" alt="2" src="https://user-images.githubusercontent.com/86527347/125212899-fa1a2300-e275-11eb-92c5-05af7ceb2680.png">
<img width="260" alt="3" src="https://user-images.githubusercontent.com/86527347/125212890-f7b7c900-e275-11eb-8c79-2264bd7334df.png">

- Created a line chart which showing the number of successful, failed, or canceled projects by month, and it is saved as png file.
<img width="350" alt="4" src="https://user-images.githubusercontent.com/86527347/125212891-f8505f80-e275-11eb-9325-e1d11a93a4c7.png">

#### Challenges
- Not much challenge for this one. I forgot to unselect the live column labels at the first time, which gives me the different total population. Then I realized and edited it.




### Deliverable 2: Outcomes Based on Goals Chart

#### Analysis
- Created a new sheet and labeled it "Outcomes Based on Goals."
<img width="433" alt="5" src="https://user-images.githubusercontent.com/86527347/125212892-f8505f80-e275-11eb-93eb-e82220e09589.png">

- Used ``COUNTIFS()`` function to populate the "Number Successful," "Number Failed," and "Number Canceled" columns by filtering on the Kickstarter "outcome" column. 

- ``=COUNTIFS(Kickstarter!F:F,"successful",Kickstarter!R:R,"plays",Kickstarter!D:D,"<1000")``is used in B2 and change number filed for other rows.

- Change "successful" to "failed" and "canceled" for other two columns.

- Used the ``SUM()`` function to populate the "Total Projects" column with the number of successful, failed, and canceled projects for each row. The formula in E2 is`` =SUM(B2:D2)`` and then apply it to other rows.

- Calculated the percentage of successful, failed, and canceled projects for each row. The formula for F2 is ``=ROUND(B2/E2,2)`` then apply to other cells.

- Created a line chart titled "Outcomes Based on Goal" .
<img width="427" alt="9" src="https://user-images.githubusercontent.com/86527347/125212898-f9818c80-e275-11eb-8450-5f6d08f73c4f.png">

#### Challenges
- Not much challenge for this one. Just need to edit and double check the formula to make sure it refers to the correct number filed and condition.


---

## Results

- The Launch Date of fundraising campaigns is correlated with its success. To help Louise plan her campaign timeline, May will be the best month of the year when campaigns tend to be more successful. We can say that theater is a great type of campaign, and it follows the overall trend: there is a spike of successful campaigns in May. While June, July and October had roughly the same number of failed campaign. And December had the least number of successful campaign, so we can suggest Louise to avoid doing the campaign by end of the year.

- About the Outcomes based on Goals, less than 1000 had the most successful percentage, followed by 35000-39999 and 40000-49999, which had the same percentage. While 45000-49999 had 100% failed percentage. Since there is no canceled project, the successful and failed percentage is negative related. So we can suggest Louise to set goal less than 1000.

- This dataset has some limitations. For example, the number of sample is not big enough, and the data could be incomplete and inaccurate. And the data source is unknown, because data collected from different sources can vary in quality and format. 

- A recommendation for additional tables or graphs. I might create a line chart to see the correlaction between the number of backers and outcomes. Is it certain that the more backers donate, the better outcomes they will get, or these two factors are not related at all.



---
