# An Analysis of Kickstarter Campaigns

## Overview of Project

This project consists of analyzing data from the Kickstarter dataset, referring to a set of events held in several countries, with category, goal, pledged, launch date. 

You can click on the link below to access the Excel File.

[Kickstarter Excel](https://github.com/lfhoepers/kickstarter-analysis/blob/f0d3460b40500744cf69abda476ed9e6b13773b7/Kickstarter_challenge.zip) 

I am demonstrating below the results of the following analyses:

**1 - Outcomes Based on Launch Date**

This analysis can be found in the Theater Outcomes by Launch Date table in the Kickstarter_challenge spreadsheet.
It consists of verifying the behavior of the events of the Parent Category Theater over the months, giving the option to be filtered by year. After checking the results in numbers, I also set up a trend chart to have a better view of the results.

#### Tool/formulas used: Pivot

**2 - Outcomes Based on Goals Chart**

This analysis can be found in the Outcomes Based on Goals Chart also in the Kickstarter_challenge Spreadsheet.
This second analysis aimed to understand the percentage of success, failure and cancellations of projects in the "play" subcategory for a pre-established goal range that varied from around 5k to 5k dollars. In this case, we are also providing, in addition to the worksheet, an inline graph demonstrated by the range x percentage, thus being able to have a macro view of the "play" projects.

#### Tool/Formulas used: **CountIFS**

=COUNTIFS(Kickstarter!$D:$D;">=20000";Kickstarter!$D:$D;"<=24999";Kickstarter!$F:$F;"successful";Kickstarter!R:R;"plays")

## Analysis and Challenges

Firstly our datasource in this case was the Kickstarter_Challenge excel file. The dataset lacked some items for better analysis, such as year, dates turned into unix timestamp, which we had to use formulas to get better results.
Formula used for conversion:

=(((J2/60)/60)/24)+DATE(1970;1;1)

As well as some information breaking treatments, for example separating Category and Subcategory in two fields. In this case, the delimiter process is used.

To do the analysis, we use the Excel Pivot table to which we can easily categorize the data according to the final objective of the analysis. In the case of the second analysis, we use the countifs function that allows us to count the data we want by filtering through several expressions.

## Results:

**Theater Outcomes by launch Date:**

1 - It was found that in May the number of successful theater projects is much higher than the rest of the months. This is an interesting conclusion to which, thinking about future projects, we can estimate that this month the chance of success is greater.

2 - On the other hand, I identified that in October the number of successful projects is very close to the number of failed projects, and from then on until December it drops. Maybe because of the winter the public doesn't go to the theater as much or isn't willing to spend. A better research in this period can help to understand why people's behavior is like this in this period.

![This is an image](https://github.com/lfhoepers/kickstarter-analysis/blob/f0d3460b40500744cf69abda476ed9e6b13773b7/Resources/Theater_Outcomes_vs_Launch.PNG)

**Outcomes based on Goals**

This analysis in percentages, initially shows us a certain planning error in the goals of the larger projects, but the amount of larger projects in relation to the smaller goals is much smaller. Well this can be explained by overestimated goals or why more projects with goals above 20000 should be done.

![This is an image](https://github.com/lfhoepers/kickstarter-analysis/blob/f0d3460b40500744cf69abda476ed9e6b13773b7/Resources/Outcomes_vs_Goals.PNG)

**Limitations**

I would particularly like to have access to the costs of each project, so that we can better evaluate their results and not just goal x pledged. In this way, we could have a completely different scenario, where eventually a failed project can become profitable if it has a low cost.

**What are some other possible tables and/or graphs that we could create?**

A table and graph of Average Donation by Category and subcategory can show us which audience donates the most.

A suggestion of mine in this project would be to create a more dynamic dashboard for the user to be able to see their data better.

Please see below a sample of this table and 2 samples of slicer to be easier to users filter what they want.

![Capturar](https://user-images.githubusercontent.com/100812079/156947113-3d2facf9-07b3-494e-89e5-5cd38aa779c5.PNG)

I appreciate the opportunity to present this project, I am available for any clarification.

**Luiz Fernando Hoepers**  
###### UofT SCS Data Analytics Boot Camp
