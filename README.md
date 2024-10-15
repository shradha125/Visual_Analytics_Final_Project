# Analysing Earthquake using JavaScript
DSE_I2700_Visual_Analytics_Final_project Repo

Glitch Link to the Dashboard: https://broad-panoramic-word.glitch.me/ 
Glitch Link to the Code: https://glitch.com/edit/#!/broad-panoramic-word?path=README.md%3A1%3A0 

Introduction
The domain we have chosen for our final project is Geospatial Data Analysis which invloves events with the location on the earth surface. Usually Geospatial data includes geographical coordinates, characteristics and the time span of an event. Here we have particularly chosen Earthquake Analysis because it helps us to analysis a seismic event and its effect on a particular location of the Earth Surface. It helps us to understand the earthquake dynamics and their impacts on the world.

Data Collection
Seismic Events:
The USGS (United States Geological Survey) monitors, reports and assesses earthquake hazards and impacts. Also it conducted targeted reasearch on the causes and effects of Earthquakes. With USGS being the base source, we used a dataset from Kaggle. Link to the Earthquake's Dataset

Data Sources:
The significant earthquake dataset 1900-2023 is a highly detailed dataset compiled by the United States Geological Survey (USGS). It is an extensive and up-to-date collection of significant earthquake events that have occurred globally over the past 123 years that is from the year 1900 to 2023 with magnitude of 5.5 or higher on the Richter scale.

Data Types :
The dataset contains over 37,000 records of earthquake events with around 20 different columns like place, time, magnitude, latitude and longitude, depth and source. These parameters help characterize the earthquake and its potential impact on the affected region.

Data Processing
Data Cleaning:
Like any other data, this earthquake data also contain noise and inconsistencies and numerous columns had many null values. Cleaning involves analysis of the dataset, erroneous entries like <,>,?,!,;,:,-, removing columns with NA values, correcting errors and column names, checking for any duplicates etc.

Fixing important information:
For spatial analysis and mapping few data points are crucial like Time, Place, and Latitude and Longitude coordinates. Making sure that the required data values are in a standard format and based on our requirements create new columns like Country and Year from columns like Place and Time.

Magnitude Scaling:
Earthquakes are categorized by magnitude, a measure of the energy released. Magnitude scaling ensures that earthquake magnitudes are standardized for accurate comparison and analysis.

Data Analysis
Temporal Analysis:
Temporal Analysis is to examine the patterns / trends in the dataset over time. Since we have spatial data for the past few decades, it is required to identify patterns and trends.

We analyzed the earthquakes counts over the year and had some findings like which year faced the most number of earthquakes.
Then we analyzed the data over months for that particular year and find out which month had a most number of earthquakes.
Analyze the data for that particular year to find out which country faced the most number of earthquakes and its magnitude level etc.
Spatial Analysis:
Spatial analysis is to identify earthquake hotspots, regions with higher seismic activity. Since we have geographical coordinates like latitudes and longitudes, it is easier to find the countries which are more prone to earthquakes.

Hotspot Identification: Analyzed the earthquake counts with the country over the years to found out that which country has most numbers of earthquakes.
For the top most country, we have analyzed the magnitude over the time period.
Magnitude Analysis:
Magnitude Frequency Distribution: Created a line plot to visualize the distribution of earthquake magnitudes.
Plotted overall data with different magnitudes in a world map.
Final Visualization:
This HTML document creates a web page displaying earthquake data using Mapbox GL JS and D3.js for data visualization. Below is a summary of the methodology used in the provided code:

HTML Structure: The HTML document is structured with the necessary metadata, including character set and viewport settings. External stylesheets for Mapbox GL JS and a custom stylesheet (style.css) are linked.

JavaScript Libraries: D3.js library is included for data manipulation and visualization. Mapbox GL JS library is included for interactive mapping.

Page Content: The page contains a message div (#message) for displaying a notification when no data is available for selected criteria. A sidebar (#sidebar) includes dropdowns for selecting the year and country of interest.

Map Initialization: A Mapbox GL JS map is initialized with controls for navigation, scale, and fullscreen.

Data Loading: GeoJSON earthquake data is loaded from an external file (earthquake_data.geojson) and added as a source to the map (earthquakes).

Dropdown Population: Unique years and countries are extracted from the GeoJSON data, and dropdowns for year and country are populated dynamically.

Map Layers: Two map layers are added:

a. Heatmap: A heatmap layer representing earthquake density with varying intensity and color based on magnitude.

b. Earthquake-circles: A circle layer representing individual earthquakes with size and color based on magnitude.

Interactive Features: Popup information is displayed on mouse hover over earthquake circles. Cursor changes to a pointer on hover for better user interaction.

Dropdown Interaction: The updateMap function is called when dropdowns are changed to filter earthquakes based on the selected year and country. A new circle layer (filtered-earthquake-circles) is added to represent the filtered data.

Bar Chart: GeoJSON data is loaded using D3.js, and a bar chart is created to showcase the top 5 highest counts of earthquakes based on the selected year and country.

Bar Chart Styling:

a. The width of each bar in the chart is determined by the top count of earthquakes for the corresponding magnitude.

b. Notably, this chart incorporates added transitions for a smoother and more visually engaging experience when updating the data.

c. The width of each bar dynamically adjusts to represent the count of earthquakes corresponding to their magnitudes, contributing to a comprehensive and insightful visualization. The color intensity rises in accordance with the growth in counts.

Customization: The styling of the map layers, including colors, opacities, and radii, is defined based on earthquake magnitudes. The legend (#legend) and a pulsing dot layer are added to enhance the visualization.

Responsive Design: The page is designed to be responsive to different device sizes.

Unused Placeholder Elements: There are placeholder elements like #line-chart and #magnitude-bar that are not utilized in the provided code.

Code Comments: Comments are provided throughout the JavaScript code to explain various sections and functionalities. This methodology creates an interactive and visually appealing web page for exploring earthquake data. Users can filter data based on the selected year and country, visualize earthquake magnitudes on the map, and view a corresponding bar chart representing magnitude counts.
