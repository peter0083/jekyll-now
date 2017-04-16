---
layout: post
title:  "A R Visualization Exercise - Shiny App Edition"
date:   2017-04-15
excerpt: "My first attempt using R Shiny"
project: true
tag:
- R
- viz
- ggplot2
- RStudio
- Shiny
comments: true
---


================
Peter Lin


April 15, 2017




# crime_data_shiny_app
a visualization exercise using R Shiny app

Link to web app: [https://peter0083.shinyapps.io/crimedataviz/](https://peter0083.shinyapps.io/crimedataviz/)

Link to source code: [https://github.com/peter0083/crime_data_shiny_app](https://github.com/peter0083/crime_data_shiny_app)


Design Considerations:
1. Overall goal of this shiny app: The goal is to create a simple interactive plot to find trends in normalized crime data over time in selected US cities. Considering the growing tech demand in the US, this visualization tool will be useful for those who wish to relocate to major cities where most data science openings are present. The US marshall data set includes many cities. To create a more focused subset for tech job seekers to find a city with low crime rate, 10 cities that have the most job openings are selected based on the report released by Glassdoor.com in 2016.
2. Scatter plot: Scatter plot expresses two quantitative attributes in the data. In the graph, year and crime per 100k people are the two quantitative attributes. Magnitude channels of horizontal and vertical position encode the quantitative attributes crime per 100k people and year in point marks. Point mark encodes a crime rate at a particular year. Scatter plot is effective in finding trends in data. Categorical attribute city is encoded using color hue. Each city has its own color.
3. Line chart: Line chart encodes one quantitative attribute crime per 100k people and one ordered key attribute year. Points are a mark of the line chart that each point encodes a crime rate at a particular year. Line connection marks to link between points. A line chart is an effective visualization to help users in identifying trends.
4. Change parameters: 5 different widgets are incorporated into the shiny app to assist users in viewing the plots in parameters of their choice. Although widgets take up screen space, the advantages of widgets are clear affordances and self-documenting with labels. The widgets in this shiny app have pre-defined choices to minimize user making erraneous inputs.
5. Slider widget: Slider widget allows the user to indicate a range of years from the data set. Once the user specifies the range, the x-axis of the graph will change. It allows developers to set a default value as well. Date range and date input widgets are not as effective in this case because they do not display any visual information the maximum and minimum year range permitted in this data set. There are several ways a user can enter a date (ie. YYYY-MM-DD or DD/MM/YYYY). These variations may result in input errors.
6. Select box widget: The select box widget creates a drop down menu with pre-defined choices for 5 types of crime, and two cities. It allows developers to set a default value as well.
7. Numeric input widget: The numeric input widget has clickable buttons to increase the numeric value by a preset interval. It allows developers to set a default value as well.
8. Checkbox widget: The choice of color vision deficiency adjustment is available for users to enable. Once enabled, the colors will be adjusted using viridis package.
9. Radio button widget: User can specify the graph type by clicking the two radio buttons: scatter plot or line chart.
10. Main panel/side bar panel layout: All parameter-changing widgets are grouped on the side bar panel for simplicity. Some additional interactive features are placed under the plot output in the main panel.
11. Graph title colour feature: A font colour selector feature is present for users to pick a colour for graph title.
12. Click/double click feature: Click and double-click features are added to allow users to compare any two points of interest for a more accurate comparison in addition to overall trend observation.

