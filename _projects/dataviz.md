---
name: Vega Lite Example Project
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# DATA VISUALIZATION ASSIGNMENT 8


<vegachart schema-url="{{ site.baseurl }}/assets/json/bar.json" style="width: 100%"></vegachart>






#### Description of Visualization of PLOT 1:
- The code creates a bar chart with Altair, displaying building counts by acquisition year and status. Bars are colored to represent different statuses (active, inactive, demolished), showing their distribution over time.
- Chosen based on "Bldg Status" to visually differentiate statuses for easier interpretation.
- Aggregated data to count buildings by acquisition year and status using count().
- Added tooltip for detailed info (year acquired, status, count) on hover, enhancing interactivity and insights. Made chart interactive with .interactive() for clearer understanding and engagement.


<vegachart schema-url="{{ site.baseurl }}/assets/json/scatter_plot.json" style="width: 100%"></vegachart>


#### Description of Visualization of PLOT 2:
- The code generates a scatter plot with Altair, showing the relationship between building "Square Footage" and "Year Acquired." Each circle represents a building, colored by its "Bldg Status" (e.g., active, demolished).
- Color Scheme is based on "Bldg Status" to visually differentiate statuses.
- Added .interactive() for hover tooltip with detailed info (Agency Name, Year Acquired, Square Footage, Bldg Status), enhancing engagement and clarity.

  
<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Rushabhnm/rushabh_dataviz/blob/main/python_notebooks/HW8.ipynb" text="The Analysis" %}
</div>
