# 1: Introduction

In this exercise, we're going to create a proportional symbol map. In week three, the lecture notes mention that graduated and proportional symbol maps base variation in the size of symbols on the quantity or value associated with a location. For this map, we'll use indicators from Durham Region's [Health Neighbourhoods](https://www.durham.ca/en/health-and-wellness/health-neighbourhoods.aspx) dataset, which we briefly looked at when we first explored QGIS. We are going to map an indicator known as "Life expectancy in males." The data comes from the Ontario Ministry of Health and Long-Term Care, IntelliHEALTH Ontario, and the Statistics Canada Census. More details can be found here under the "General Health" tab: https://app.powerbi.com/view?r=eyJrIjoiOWQ3N2RkNTktMWRiOS00MTQ5LTk0OTYtMzhiY2E2NjY3YjQwIiwidCI6IjUyZDdjOWMyLWQ1NDktNDFiNi05YjFmLTlkYTE5OGRjM2YxNiJ9\&pageName=ReportSection2080f15a79d0884a7d58

# 2: Select and Download Data

- Go to  https://opendata.durham.ca/ and search for "Health Neighbourhoods." 
- Examine the boundaries map https://opendata.durham.ca/datasets/health-neighbourhoods/explore?location=44.130417%2C-78.898350%2C10.76
- If you didn't already do this previously, download the health neighbourhoods boundaries in Shapefile and GeoJSON formats (we'll use the Shapefile).
- Open and explore the health neighbourhoods data table as well. Set filters for "Life Expectancy in Males" on INDICATORNAME and "2009-2013" on YEAR. Make sure to toggle the filters on. Download in .csv format.
- Repeat these steps with a filter for "2014-2018" on YEAR if you want to make an additional map for comparison.

# 3: Load and Join the Data in QGIS

- It’s very easy to make mistakes combining and exporting different file types (e.g. .shp and .csv) in QGIS, so you can always do your filtering beforehand in a spreadsheet application. If you didn't filter before downloading, open the .csv in your application of choice (e.g. Excel) and filter for "Life Expectancy in Males" in the INDICATORNAME column and "2009-2013" in the YEAR column. Save this new table to a file called life.csv
- Open QGIS and create a new project.
- Add your .shp layer by dragging the .zip file into the Layers panel.
- Go to Layer/Add Layer/Add Delimited Text Layer and add your .csv dataset with "Detect field types" checked on.
- Note: *Sometimes, your numerical values will be in "string" format. You can correct this by right-clicking the .csv layer and selecting "Toggle Editing." Open the attribute table. Click in the first cell of the VALUE column. Press ctrl-I to open the Field Calculator. Make sure that "Create a New Field" is toggled. In "Output field name," write values. Make sure the field type is set to integer. Set the output field length to 2. In the middle column, open the "Fields and Values" drop-down. Double-click on VALUE so that it populates the left column. Click Ok and save your edits. Check that a new column called "values" has been added to your attribute table.*
- In the browser window on the left, open up XYZ tiles and double click OpenStreetMap. This will add a base map layer. Move it below the other two layers in the order.
- Right click your vector (shapefile) layer, open up Properties, and select Joins. Press the \+ symbol. Select life as your Join Layer, "MUNICIPAL_ID" as your Join Field, and "MUNICIPAL_" as your Target Field. Check Custom field name prefix and remove the text. Press Ok, Apply, and then Ok. Open the Attribute Table of your vector layer and inspect. 
- With the vector layer selected, go into the menu bar, select Vector/Geometry Tools/Centroids, and pick your vector as the input layer. Check "Create centroid for each part" and Run.
- With the Centroids layer selected, go into the menu bar, select Processing/Toolbox, and then search for Add X/Y fields to layer. Select Centroids as the input layer and set the coordinate system to EPSG:4326. Run.
- Right-click the new Added Fields layer, go to Export/Save Features As, and output it to an Esri Shapefile with the name life.
- Uncheck all layers except the original vector layer and the basemap.

# 4: Visualize

- Right click life and go to Properties/Symbology. 
- Select Simple Marker. In the Size row, click on the little box on the far right side of the window. A drop down will open. Select Assistant. In the Source tab, select the values option. Press the blue-ish refresh button. Select Ok. Press Apply and then Ok, and then watch your map populate with proportional symbols.
- Go back to Properties/Symbology and change the colours following the same logic as above.
- Consider changing symbols, opacity, etc.

# 5: Explore 3D

- Turn your original shapefile layer back on. Open 3D View and set it to Single Symbol. Set Extrusion to values using the same process as above. Add a 3D Map View in the View menu at the top. Expect it to look ugly. 
- Where do you go from here, given that we've only scratched the surface with QGIS? YouTube! There are lots of good QGIS tutorials out there. You should be able to find everything you need on YouTube and Stack Overflow. Just make sure that they're fairly recent. More information on 3D layers in QGIS can be found here: https://docs.qgis.org/3.34/en/docs/user_manual/style_library/3d_symbols.html
