## TITLE: Distribution of K-12 Texas Student Enrollment by Ethnicity (African American, Hispanic, White) From 1999 Through 2018 

## OBJECTIVE: this project will present the number and percentage of K-12 student enrollment within three ethnicity groups in all the schoold districts in the past 20 years from 1999 through 2018 school year in Texas, and build a web-based dashboard application using Dash to illustrate the interactive Choropleth Map.

Dashborad demo:
https://github.com/marklu729/tx_k12_enrollees/blob/master/Dash_Demo.gif


## DATA: All the data sets used in this project are public data that can be downloaded from TEA website:
     (1) AEIS: Academic Excellence Indicator System (campus level and district level)
         https://rptsvr1.tea.texas.gov/perfreport/aeis/index.html
     (2) TAPR: Texas Academic Performance Reports (campus level and district level)
         https://tea.texas.gov/texas-schools/accountability/academic-accountability/performance-reporting
     (3) Spatial data: http://schoolsdata2-tea-texas.opendata.arcgis.com/

## PROCEDURES:
    (1) Data Preparation: data exploration, merging, wrangling, aggregation
        (a) Process district level data to obtain district related information
        (b) Process campus level data to obtain student enrollment information by ethnicity, and do dimentionality reduction to keep the interested features only
        (c) Merge the processed year-based data to generate the aggreaged data including the student enrollment information from 1999 through 2018
        (d) Explore the data by using decriptive statistcs
        (e) Apply feature engineering to the data set 
            e.g. campus_ID/1000 to get district_ID, use groupby to calculate the # of enrollees per year & district in each ethnic group etc.
            
    (2) Data Visulization: distribution of student counts plotted in static and interactive graphs
        (a) Seaborn: statically illustrate the distribution of the enrollees by ethnicity groups from 1999 through 2018
        (b) Plotly: interactively illustrate the distribution of the enrollees by ethnicity groups

    (3) Geographically Illustration of Distribution of K-12 Enrollees Across Texas School Districts in Three Ethnic Groups 
        (a) GeoPandas: process the saptial data to merge with the dataframe
        (b) Geoplot & mapclassify: geographically plot the choropleth maps in different classifiers defined with mapclassfiy.quantiles   
        
    (4) Build a web-based Dashboard with Dash and Plotly
        (a) Plotly Graph Part:
            Data preparation: import pre-pocessed dataframe, load and process GeoJSON file
        (b) Dash Component Part:
            App layout: declare dash components (a Slider, a Dropdown, a RadioItems)   
        (c) Callback Part:
            Connect the plotly graphs with dash components          

The interactive barplot of student counts from 1999 to 2018 generated using Plotly:
https://htmlpreview.github.io/?https://github.com/marklu729/tx_districts/blob/master/barplot_student_counts_from_1999_2018_by_three_ethnic_group.html

## DISCLAIMER:This disclaimer informs readers that the views, graphs, opinions, codes belongs solely to the author, and not necessarily to the author's employer, organization or other groups or individuals, and in no way driven by any other hidden agenda.
