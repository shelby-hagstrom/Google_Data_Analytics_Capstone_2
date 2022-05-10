# Google-Data-Analytics-Capstone-2
## Introduction
The eighth course in the Google Data Analytics Certificate is a Capstone Project. In the course, you have the option to create a case study by either working with existing questions and datasets or creating your own questions and datasets. 
<br>
<br>
For my second project, I have selected the Bellabeat data share analysis case study to work on. For the case study, I will perform the real-world tasks of a junior data analyst for Bellabeat, a high-tech company that manufactures health-focused smart products for women.  

To answer key business questions, I followed the six steps of the data analysis process taught in the course which are: Ask, Prepare, Process, Analyze, Share and Act.

## Ask
In the Ask phase, we learned how to define the problem, determine business objectives and deliverables, and ask effective questions to make data-driven decisions, while connecting with stakeholders’ needs. 

### Scenario
Bellabeat is a successful small company that has the potential to become a larger player in the global smart device market. Collecting data on activity, sleep, stress, and reproductive health has allowed Bellabeat to empower women with knowledge about their own health and habits. 

Since it was founded in 2013, Bellabeat has grown rapidly and quickly positioned itself as a tech-driven wellness company for women. By 2016, Bellabeat had opened offices around the world and launched multiple products. Bellabeat products became available through a growing number of online retailers in addition to their own e-commerce channel on their website. The company has invested in traditional advertising media, such as radio, out-of-home billboards, print, and television, but focuses on digital marketing extensively. Bellabeat invests year-round in Google Search, maintaining active Facebook and Instagram pages, and consistently engages consumers on Twitter. Additionally, Bellabeat runs video ads on Youtube and displays ads on the Google Display Network to support campaigns around key marketing dates. 

### Business Task
Urška Sršen, cofounder and Chief Creative Officer of Bellabeat, believes that analyzing smart device fitness data could help unlock new growth opportunities for the company. You have been asked to focus on one of Bellabeat’s products and analyze smart device data to gain insight into how consumers are using their smart devices. The insights you discover will then help guide marketing strategy for the company.

### Key Stakeholders
* Urška Sršen: Bellabeat’s cofounder and Chief Creative Officer 
* Sando Mur: Mathematician and Bellabeat’s cofounder; key member of the Bellabeat executive team 
* Bellabeat marketing analytics team: A team of data analysts responsible for collecting, analyzing, and reporting data that helps guide Bellabeat’s marketing strategy. 

### Bellabeat’s Products
* Bellabeat app: Provides users with health data related to their activity, sleep, stress, menstrual cycle, and mindfulness habits. This data can help users better understand their current habits and make healthy decisions. The Bellabeat app connects to their line of smart wellness products. 
* Leaf: Classic wellness tracker can be worn as a bracelet, necklace, or clip. The Leaf tracker connects to the Bellabeat app to track activity, sleep, and stress. 
* Time: Wellness watch combines the timeless look of a classic timepiece with smart technology to track user activity, sleep, and stress. The Time watch connects to the Bellabeat app to provide you with insights into your daily wellness. 
* Spring: Water bottle that connects to the Bellatbeat app to track daily water intake using smart technology to ensure that you are appropriately hydrated throughout the day. 

### Business Objectives
* What are some trends in smart device usage? 
* How could these trends apply to Bellabeat customers? 
* How could these trends help influence Bellabeat marketing strategy?

### Deliverables
* A clear summary of the business task 
* A description of all data sources used 
* Documentation of any cleaning or manipulation of data 
* A summary of your analysis 
* Supporting visualizations and key findings 
* Your top high-level content recommendations based on your analysis 

## Prepare
In the Prepare phase, we learned how to use tools like spreadsheets and SQL to extract and make use of the right data for your objectives and how to organize and protect our data.

### Data Source
For the purposes of this case study, I downloaded files from the FitBit Fitness Tracker Data (CC0: Public Domain, dataset made available by Mobius). This Kaggle data set contains personal fitness tracker from 30 fitbit users who consented to the submission of personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring. It includes information about daily activity, steps, and heart rate that can be used to explore users’ habits. 
<br>
<br>
There are 18 files within the FitBit Fitness Tracker, which I have downloaded to my computer. Yet, the daily_activity and sleep_day files are the 2 I focused on.
This dataset was generated by respondents to a distributed survey via Amazon Mechanical Turk between 04/12/2016 - 05/12/2016. 

This dataset doesn’t ROCCC
* Reliable: This data is not reliable, as a very small sample size (30 participants) has been used, which can limit the amount of analysis that can be done.
* Original: The data is not original, as it is provided by a third party, that being Amazon  Mechanical Turk
* Comprehensive: The data looks to be comprehensive, in the sense that it looks to provide the minimum amount of data needed to answer our questions.
* Current: With the data being collected in 2016, it is not current and may no longer be relevant.
* Cited: Since the data was collected from a third party, we don’t have any information on whether this is a credible source

While the data isn’t perfect, it’s the best available and can be considered reliable and representative for this scenario.

## Process
In the Process phase, we learned about data cleaning tools and techniques and how to use those tools to get our data ready for analysis.

The 7th course of the Google Data Analytics certificate taught us about the R programming language. In that course, we learned how to clean, organize, analyze, visualize, and report data in new and more powerful ways. RStudio Desktop is the tool I've used to prepare, process, analyze, and visualize the data for this Capstone project. 

In RStudio, I inspected the daily_activity and sleep_day data frames by using the following functions
* colnames()
* nrow()
* dim()
* head()
* str()

Next, within the daily_activity data frame, I added a TotalMinutes column by adding the each of the minute columns together, converted the ActivityDate column into a date column with a date format, and added a column for the day of week.

Within the sleep_day data frame, I separated the SleepDay column into a Date and Time column, converted the new SleepDate column into a date column with a date format, and added a column for the day of week.

Those steps allowed me to join the daily_activity and sleep_day data frames together by the Id, date, and day of week columns.

Before doing that, I used the n_distinct() and table() functions to count the number of Ids within each data frame. While there were 33 Ids in the daily_activity data frame, there were only 24 in the sleep_day data frame. The table() function helped me see the frequency of each Id across the data frames. 

That knowledge helped me to be aware of the fact that not all data found in the sleep_day data frame would join into the daily_activity data frame. Since there were less Ids in the sleep_day data frame, I was prepared for all the N/A values in the new merged_data data frame.

## Analyze
In the Analyze phase, we learned how to organize and format our data using spreadsheets and SQL to help us look at and think about our data in different ways. We also found out how to perform complex calculations on our data to complete business objectives and how to use formulas, functions, and SQL queries as we conduct our analysis.


## Share
In the Share phase, we learned how data visualizations, such as visual dashboards, can help bring your data to life. 

## Act

### Summary of insights gained from visualizations in RStudio
* In joining the sleep_day data frame with the daily_activity data frame, I see the participants of this study favored tracking their daily activity while awake versus when asleep.

### Recommendations 


