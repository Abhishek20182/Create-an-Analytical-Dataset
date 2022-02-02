<p align="center">
  <a href="https://www.udacity.com/">
    <img src='https://course_report_production.s3.amazonaws.com/rich/rich_files/rich_files/5511/s300/udacity-logo.png' alt="Udacity logo" width = 100px>
   </a>
</p>

<h3 align="center"><a href = "https://www.udacity.com/course/predictive-analytics-for-business-nanodegree--nd008t"> Udacity Predictive Analytics for Business</a></h3>
<h4 align="center">Project III: Create an Analytical Dataset</h4>

## Table of Contents
- [Project Overview](#project_overview)
- [Project Details](#details)
  - [The Business Problem](#the_BP)
  - [Steps to Success](#sts)
  - [IQR Steps](#iqrstep)
- [Project Submission](#submission)
- [Results](#results)
- [Licensing, Authors, and Acknowledgements](#licensing)

## Project Overview <a name="project_overview"></a>

This project is the first part of a two-part series. In the first part, you will blend and format data and deal with outliers.

For the second part, you will use your cleaned up dataset to create another linear regression model. The difference this time is that you will have to choose which variable(s) are the most important for the model using new techniques learned in the Selecting Predictor Variables section.
Scenario

Pawdacity is a leading pet store chain in Wyoming with 13 stores throughout the state. This year, Pawdacity would like to expand and open a 14th store. Your manager has asked you to perform an analysis to recommend the city for Pawdacity’s newest store, based on predicted yearly sales.
How Do I Complete this Project?

This project uses skills learned throughout the "Data Preparation” lessons. To complete this project:

- Go through the course.
- Apply the skills learned in the course to solve the business problem given in the project details.
- Use our guidelines and rubric to help build your project.
- When you're ready, submit it to us for review using the submission template found in the supporting materials section.

### Skills Required

In order to complete this project, you must be able to:

- Understand different data types. Review Lesson 1 Understanding Data
- Deal with a variety of data issues. Review Lesson 2 Data Issues
- Format data appropriately. Review Lesson 3 Data Formatting
- Blend data together using joins and unions. Review Lesson 4 Data Blending

## Project Details <a name="details"></a>

### The Business Problem <a name="the_BP"></a>

Pawdacity is a leading pet store chain in Wyoming with 13 stores throughout the state. This year, Pawdacity would like to expand and open a 14th store. Your manager has asked you to perform an analysis to recommend the city for Pawdacity’s newest store, based on predicted yearly sales.

Your first step in predicting yearly sales is to first format and blend together data from different datasets and deal with outliers.

Your manager has given you the following information to work with:
1. The monthly sales data for all of the Pawdacity stores for the year 2010.
2. NAICS data on the most current sales of all competitor stores where total sales is equal to 12 months of sales.
3. A partially parsed data file that can be used for population numbers.
4. Demographic data (Households with individuals under 18, Land Area, Population Density, and Total Families) for each city and county in the state of Wyoming. For people who are unfamiliar with the US city system, a state contains counties and counties contains one or more cities.

<p align=center>
  <img src="https://video.udacity-data.com/topher/2019/August/5d47a493_wyoming-county-map/wyoming-county-map.gif" width=600px>
</p>

### Steps to Success <a name="sts"></a>
<b>Step 1: Business and Data Understanding</b>
Your project should include a description of the key business decisions that need to be made.

<b>Step 2: Building the Training Set</b>
To properly build the model, and select predictor variables, create a dataset with the following columns:

    City
    2010 Census Population
    Total Pawdacity Sales
    Households with Under 18
    Land Area
    Population Density
    Total Families

This dataset will be your training set to help you build a regression model in order to predict sales in the Practice Project in the next lesson. Every row should have sales data because we're trying to predict sales.

<b> Notes</b>

You should be consolidating the data at the city level and not at the store level. We only have data at the city wide level so any analysis at the store level will not be sufficient to complete this analysis. We simply need to focus on cleaning up and blending the data together in this step.

If you’ve done everything correctly, the sum for each of the above columns should be:

- Census Population: 213,862
- Total Pawdacity Sales: 3,773,304
- Households with Under 18: 34,064
- Land Area: 33,071
- Population Density: 63
- Total Families: 62,653
with 11 rows of data

For Alteryx users:

- Use the Autofield Tool to help quickly convert your data fields into the appropriate datafields for analysis.
- Research these three specific formulas to help you get rid of unwanted characters in the Formula tool: ReplaceFirst, Left, FindString

<b>Step 3: Dealing with Outliers</b>

Once you have created the dataset, look for outliers and figure out how deal with your outliers. Use the IQR method to determine if there are outlier cities for each of the variables and then justify which city that has at least one outlier value should be removed.

### IQR Steps <a name="iqrstep"></a>

To calculate the upper fence and the lower fence, here are the exact steps:

1 . Calculate 1st quartile Q1 and 3rd quartile Q3 of the dataset. You can use the Excel function QUARTILE.INC or QUARTILE.EXC

2 . Calculate the Interquartile Range: IQR = Q3 - Q1

3 . Add 1.5 IQR to Q3 to get the upper fence: Upper Fence = Q3 + 1.5 IQR

4 . Subtract 1.5 IQR to Q1 to get the lower fence: Lower Fence = Q1 - 1.5 IQR

5 . Values above the Upper Fence and values below the Lower Fence are outliers

## Project Submission:<a name="submission"></a>
To complete this project, you will be submitting a file in pdf format that contains the answers to the following questions.

## Results: <a name="results"></a>
All the results(including graphs) are in the <a href="https://github.com/Abhishek20182/Create-an-Analytical-Dataset/blob/main/Report.pdf">Report.pdf</a> File.

## Licensing, Authors, Acknowledgements<a name="licensing"></a>
Must give credit to Udacity to providing this data. You can find the Licensing for the data and other descriptive information at Udacity Page.
