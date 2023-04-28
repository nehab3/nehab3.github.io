---
name: Final Project Part 3.1 
tools: [Python, HTML, vega-lite]
description: This is a submission for Final Project Part 3.1 by Neha Bharadwaj and Asmita Khode!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Building a future with EV's : A deeper dive into the capabilities and affordability of electric vehicles in the US  
## By Neha Bharadwaj & Asmita Khode  
### Final Proejct 3.1

<vegachart schema-url="{{ site.baseurl }}/assets/json/Viz1.json" style="width: 100%"></vegachart>

### Note  



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

