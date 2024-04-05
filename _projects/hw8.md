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


# Example including vega-lite

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).


<vegachart schema-url="{{ site.baseurl }}/assets/json/plot1.json" style="width: 100%"></vegachart>


<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2.json" style="width: 100%"></vegachart>


### Plot 1

#### Description of Visualization:
The visualization is a bar chart that presents data on Bigfoot sightings during Fall 2022. Each bar represents a state, showcasing the total number of sightings on the y-axis and the states on the x-axis. Additionally, the color of each bar represents the average pressure recorded in each state, providing a visual comparison of both variables across different states. As we see there are more number of sightings when the pressure is between 1016 - 1018 Pascals.

#### Design Choices and Encoding Types:
Encoding Types:
The x-axis (x=alt.X('state:N', title='State')) encodes the states' names.
The y-axis (y=alt.Y('total_sightings:Q', title='Total Sightings')) encodes the total number of sightings.
The color encoding (color=alt.Color('avg_pressure:Q', scale=alt.Scale(scheme='viridis'), title='Average Pressure')) represents the average pressure, with the color scheme set to 'viridis' for a visually appealing and intuitive representation of pressure levels.

#### Data Transformations and Analysis:
It aggregates the data by state using df.groupby('state').agg({'number': 'count', 'pressure': 'mean'}) to calculate the total number of sightings and the average pressure for each state.
The reset_index() method is used to reset the index after aggregation for clarity in further operations.
These transformations are crucial as they summarize the raw data into meaningful insights, allowing for a clear visualization of Bigfoot sightings and average pressure by state.




In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.


## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:


<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>
