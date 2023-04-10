---
name: Homework 10 
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a submission for homework 10 by Neha Bharadwaj and Asmita Khode!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


## Plot 1

<vegachart schema-url="{{ site.baseurl }}/assets/json/Viz1.json" style="width: 100%"></vegachart>

### Note  

This particular visualization utilizes ordinal encoding for the x and y axes since we have categorical data for seasons and states the ordinal encoding turned these categorical labels into numerical values that could be plotted using the heat map . Further the color scheme is decided based on average temperature_high acheived in a particular season in a particular state.

While exploring the data we found that there was data available for 4 distinct season along with some rows where the season was listed as "Unknown".

Since the number of rows recognised as "unknown" were only 9 we decided to drop them and visualize the 4 seasons. The color scheme chosen for this particular heatmap is a mix of yellow orange and red wherein yellow depicts lower temperatures and as the color gets towards a darker orange and red it depicts a higher average temperature_high. This colour choice was very conscious as it is easier to identify higher temperature regions with deeper colours specifically red which depicts somewhat of a caution with rising temperatures.

## Plot 2  

<vegachart schema-url="{{ site.baseurl }}/assets/json/Viz2.json" style="width: 100%"></vegachart>  

### Note  

In this scatter plot we have used quantitative encoding for both the axes since we have the numerical data. This plots depicts the relation between humidity level and respective precipitation probability during different seasons. We also have an associated bar plot below the scatter plot which changes according to the area selected in the scatter plot.
On selecting a certain area on the scatter plot the bar plot below it changes to depic the mean precipitation probability for each season within the selected region.
We have used different colors to represent different season so can be identified separately.

## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/nehab3/nehab3.github.io/blob/main/python_notebooks/Homework%2310.ipynb" text="The Analysis" %}
</div>

