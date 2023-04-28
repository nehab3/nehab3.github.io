---
name: Final Project Part 3.1 - Group 6
tools: [Python, HTML, Altair]
image: assets/pngs/electric-car.png
description: This is a submission for Final Project Part 3.1 by Neha Bharadwaj and Asmita Khode!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Building a future with EV's : A deeper dive into the capabilities and affordability of electric vehicles in the US  
## By Neha Bharadwaj & Asmita Khode  
### Final Project 3.1  


<img src="/assets/pngs/electric-car.png"/>

###### Image Source : https://pixabay.com/illustrations/electric-car-gas-station-environment-2728131/  

### Introduction
This article is aimed at describing a data driven analysis of how affordable electric cars are along with understanding what sort of capabilities they have vs their affordability. The main two parameters we will discuss in our article would be the Electric range and the Base MSRP of the electric vehicles. The data used for this article is limited to the state of washington in USA.  

These registered electric vehicles are majorly of two types : Battery Electric Vehicle(BEV) and Plug-In Hybrid Electric Vehicle (PHEV) , going forward we will be discussing these with their abbreviations which are BEV and PHEV as mentioned respectively.  

### Visualization 1  

<vegachart schema-url="{{ site.baseurl }}/assets/json/Final_plot1.json" style="width: 100%"></vegachart> 

In this interactive visualization we have three plots. The main barplot at the top left shows the total count of Electric Vehicles by Model Year. The below two plots interacts with this main plot. When the Model Year is selected(click) by user, the scatter plot in bottom left changes accordinlgy to depict the distribution of electric vehicle by Make based on the year selected. Similarly, the barplot to the right of this shows the ditribution by County and Make for that particular year. All the plots have tooltips to shows user what data it is representing like the main plot has Model Year and Count of vehicles, the scatterplot has Model Year, Count along with Make whereas the second barplot has County, Model Year, Make and Count respectively. By default the two dependent plots shows cumulative data from all the year.  

### Visualization 2
<vegachart schema-url="{{ site.baseurl }}/assets/json/Final_plot2.json" style="width: 100%"></vegachart>

This visualization here gives a measure of the electric range and base msrp for our vehicles in our primary dataset. This is an interactive visualization. As we can see in the plot there are 3 sets of bar plots.  

- First bar plot describes count of electric vehicles for different types of Make
- Second plot gives the mean electric rannge for both BEV and PHEV , this mean as of now is calculated based on the mean electric range of all vehicles irrespective of their make
- The third bar plot describes the mean BASE msrp for BEV and PHEV irrespective of Make , as it takes full database into account just like our second plot.  

Now we can click on one of the bar charts in our primary plot such as selecting (BMW/Cadillac/Tesla) and as u click on these bars you will see that the 2 bar plots below it will change to show you the mean electric range and BASE msrp of electric vehicles of that make and will also depict on the x-axis wether the selected make manufactures only BEV , only PHEV or both.This particular visualization can help us understand and compare the electric vehicles of different vehicles in terms of capability and affordability.

You can find the links to the data and Source code for Visualization 1 and 2 below

<div class="left">
{% include elements/button.html link="https://github.com/nehab3/nehab3.github.io/blob/main/python_notebooks/Electric_Vehicle_Population_Data.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/nehab3/nehab3.github.io/blob/main/python_notebooks/Final%20Project%20part%203.1%20-%201.ipynb" text="The Analysis" %}
</div>  

<br>

### Visualization 3   

<vegachart schema-url="{{ site.baseurl }}/assets/json/Final_plot3.json" style="width: 100%"></vegachart>  

This visualization is aimed at taking a deeper look in to the number of electric vehicles registered in washington county wise.We can see two plots in the visualization and this is an interactive visualization as well.
- The first plot is a simple scatter plot showing the total number of electric vehicles registered in each county.
- The second visualization as is depicts a stacked bar chart showing the number of BEV and PHEV registered in each county.Here the red portion depicts the count of PHEV's and the blue part depicts the count of BEV's and you can see the same by hovering on this bar plot.

The intereactivity here allows you to drag and select certain scatter points on the first plot and the second plot will modify to give you the distribution of only those counties that are selected. This detailed visualization helps us understand which type of electric vehicle people are preffering BEV or PHEV and why are they doing so. In our first visualization we saw that the electric range for the BEV's is much higher than the mean range for the PHEVs while the BASE MSRP was comparable for both. So a real point to investigate here would be to see if these are the only two parameters affecting the choice of the car purchased or are there more attributes such as location and weather that are also playing a role in the choice the consumers are making.  
Because looking at the data closesly there are some counties where people have preferred PHEV over BEV and some counties where it is the opposite.  

You can find the links to the data and Source code to this visualization below

<div class="left">
{% include elements/button.html link="https://data.wa.gov/api/views/3d5d-sdqb/rows.csv?accessType=DOWNLOAD" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/nehab3/nehab3.github.io/blob/main/python_notebooks/Final%20Project%20Part%203.1-2.ipynb" text="The Analysis" %}
</div>  

### Visualization 4   

<vegachart schema-url="{{ site.baseurl }}/assets/json/Final_plot4.json" style="width: 100%"></vegachart>

This visualization is created from "Electric Vehicle Title and Registration Activity" dataset. We have dropped the null values and also removed the duplicates to get exact number of register vehicles for State of Washington. For this visualization we had more than 5000 rows and by deafult altair allows only 5000 rows. To plot our full dataset we have disabled the max_rows parameter.  

Here, we are using a scatter plot which shows the readings of Odometer by Vehicle Primary Use. From this plot we can see that the most Electric Vehicles are used as Passenger Vehicles and Passenger Vehicles have much higher Odometer readings. This plot has a click functionality. As user clicks on any type of Primary Use the line plot associated with this changes according to selection made. The line plot shows the Mean Odometer Readings by Year. It shows how mean Odometer readings for each type of Primary Use changed over the years

Note: Due to the extrememly large size of the contextual dataset we have used a subset of random 5000 rows from the dataset to generate this plot

You can find the links to the data and Source code to this visualization below

<div class="left">
{% include elements/button.html link="https://data.wa.gov/api/views/rpr4-cgyd/rows.csv?accessType=DOWNLOAD" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/nehab3/nehab3.github.io/blob/main/python_notebooks/Final%20Project%20Part%203.1%20-3.ipynb" text="The Analysis" %}
</div>

### Sources  
- Hosting using jekyll : https://uiuc-ischool-dataviz.github.io/is445_oauoag_spring2023/week10/installation_instructions_week11.html  
- Electric Vehicle Title and Registration Activity Dataset: https://catalog.data.gov/dataset/electric-vehicle-title-and-registration-activity/resource/d045f505-3b06-4471-953c-1a754c295a9c
- Electric vehicle population size by county Dataset : https://catalog.data.gov/dataset/electric-vehicle-population-size-history-by-county/resource/de0258e2-3542-4703-aad4-dcebd9d1f195  
- Altair Documentation : https://pypi.org/project/altair/
- Altair User guide : https://altair-viz.github.io/user_guide/interactions.html
- Code : https://uiuc-ischool-dataviz.github.io/is445_oauoag_spring2023/nbv.html?notebook_name=%2Fis445_oauoag_spring2023%2Fweek12%2FinClass_week12.ipynb


