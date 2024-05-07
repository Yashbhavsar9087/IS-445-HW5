---
name: Part 3 
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


<vegachart schema-url="{{ site.baseurl }}/assets/json/plot1.json" style="width: 100%"></vegachart>






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

#### For Interactivity: 
Here, we use tooltip for detailed info (state, total sightings, avg pressure) on hover, enhancing interactivity and insights. Made chart interactive with .interactive() for clearer understanding and engagement.


<vegachart schema-url="{{ site.baseurl }}/assets/json/plot2.json" style="width: 100%"></vegachart>

### Plot 2

#### Description of Visualization:
The visualization is a bar chart that presents data on Bigfoot sightings during Fall 2022. Each bar represents a month, showcasing the total number of sightings on the y-axis and the months on the x-axis. The color of each bar represents the month, providing a visual distinction between different months. Hovering over each bar displays detailed information about the month and the count of sightings, enhancing interactivity and insights.

#### Design Choices and Encoding Types:
Encoding Types:
The x-axis encodes the months' names with a custom axis label angle for better readability.
The y-axis encodes the total number of sightings.
The color encoding represents each month with a distinct color using a custom color scheme for visual distinction.

#### Data Transformations and Analysis:
The code performs data cleaning by removing rows with missing values in the 'date' column and extracting the month from the date variable. It then aggregates the data by month to calculate the total number of sightings for each month.

#### For Interactivity:
The chart is made interactive with tooltips that provide detailed information (month, count) on hover, enhancing interactivity and allowing users to gain insights by exploring the data visually.
  
<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Yashbhavsar9087/IS-445-HW5/edit/main/_projects/Workbook.ipynb" text="The Analysis" %}
</div>
