# Kickstarting with Excel 
## Overview of Project 
### Purpose
This analysis was performed to help an up and coming playright, who wants to start a Kickstarter crowdfunding campaign to fund her new play. The playright, Louise, has an estimated budget of over $10,000 to be allocated for operating expenses such as sets, costumes, props, makeup, lighting, rehearsal space, advertising, programs and actors. Louise is hesitant about undertaking her first campaign and has aksed for an analysis of Kickstarter campaign data to determine whether there are specific factors that make a project's campaign successful in relation to their launch dates and funding goals. She will use the results of the analysis to taylor her own Kickstarter campaign for success. The Kickstarter data set used for this analysis contains information about campaigns that were created globally between May of 2009 and March of 2017. There were a total of 4,113 campains created during this time frame. An analysis of Kickstarter crowdfunding for theater campaigns based on launch date and outcomes based on goals revealed that there were 1,369 of these campaigns launched between July 19, 2010 and March 15, 2017. The results of the analysis are illustrated in the next sections of this report.   
## Analysis and Challenges
### Analysis of Outcomes Based on Launch Date
![Theater Outcomes vs Launch](https://github.com/LleeMcD/Kickstarter-Analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
![Outcomes vs Goals](https://github.com/LleeMcD/Kickstarter-Analysis/blob/main/Resources/Outcomes_vs_Goals.png)
### Challenges and Difficulties Encountered
Some of the challenges with working with the Kickstarter data set were as follows:
- The deadline and launched dates were not readable because they were Unix timestamps instead of dates. For clarification, Unix timestamps measure time as the number of seconds since midnight of January 1, 1970 (https://courses.bootcampspot.com/courses/630/pages/1-dot-3-3-timing-success?module_item_id=209206). Columns labeled Date Created Conversion and Date Ended Conversion were created to convert the Unix time stamps to usable dates. 
- The average donation amounts had to be rounded to make the results more accurate.
- Average donation values of zero needed to be debugged with the IFERROR() function to prevent error #DIV/0!from being displayed. 
- The categories and subcategories were lumped together in one column. The column titled Category and Subcategory was split into two separate columns using the text to columns function. The resulting columns are labeled Parent Category and Subcategory.
- A separate Years column had to be created from the Date Created Conversion Column.

## Results
Conclusions that can be drawn about outcomes based on launch date are that it would be advisable to launch a campaign in May or June and to avoid lauching a campaign in December. The rationale for these conclusions are as follows:
- The most successful campaigns were launched in May and June, with May having the most successes. This could be because expenses tend to be lower for countries in the Nothern hemisphere at this time of the year due to milder Spring temperatures and or fewer competing priorities.
- The least successful campaigns were lauched in December, which could be due to people having less money due to the costs of utilities such as heating in countries in the Northern hemisphere, or cooling for countries in the Southern hemisphere. In addition, people may be less interested in making donations during this time of year due to competing priorites with holidays, religious observances and family gatherings. 

Conclusions that can be drawn about outcomes based on goals are that it would be advisalble to have a goal that is between $1,000 and $4,999 but additional analysis of measures of central tendency and spread are recommended to get more specific information. The rationale for these conclusions are as follows:
- The most successful campaigns had goals that were less than $1,000; with a total of 141 successful projects out of 186 followed closely by those with goals between $1,000 and $4,999; with a total of 388 successful projects out of 534.
- The least successful project had goals between $45,000 and $49,000 but this was for one campaign, which failed.
- Campaigns with goals greater than $50,000 only had a success rate of 17%, but the two successful campaigns each had a goal of $100,000.

Additional tables and/or graphs could be created to analyze campaign outocmes based on any combination of the following elements:
- The number of backers
- The number staff picks
- How many plays were in the spotlight
- Country of campaign
- Pledged amounts
- Average donation amounts
- Measures of central tendency 
- Measures of spread


