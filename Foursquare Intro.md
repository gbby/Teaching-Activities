# 1: Intro to Foursquare Studio

Foursquare Studio is a powerful, comprehensive platform that lets you conduct geospatial data analysis from your browser. With it, you can:
- Visualize large amounts of location data in your browser.
- Perform geospatial analytics by grouping and joining your data.
- Gain insights by filtering and correlating your location data.
- Quickly publish and share your results.
- Access it at https://studio.foursquare.com/

# 2: Download and Prepare Data

We're going to try to replicate what we did in QGIS. Here are the basic steps:
- Get the health neighbourhoods shapefile from https://opendata.durham.ca/
- Get the health neighbourhoods table from there as well, but set filters for "Life Expectancy in Males" on INDICATORNAME and "2009-2013" on YEAR. Make sure to toggle the filters on. Download in .csv format.
- You can load each and join in QGIS (on "MUNCIPAL_ID" and "MUNICIPAL_"), and then export to a new Shapefile that can be loaded into Foursquare Studio following the steps in the QGIS_Symbol.md instructions. 
- Alternatively, open Foursquare Studio and create a new map. 
- Load each file in your map. Select the Columns tab in the menu bar, and select join using the "more options" feature on one of the datasets. Join on the columns listed above.

# 3: Visualize in 3D

- Click on the Layers tab in the menu bar. Click on that layer to access aesthetic features in a drop-down format. Set your fill colour to be based on VALUE.
- Click the tab to turn on the Height value. Click the three dots beside Height and set Height to VALUE. 
- On the menu to the right of the map, change from a 2D view to a 3D view. 
- For a bonus mark, export your earlier life layer from QGIS in GeoJSON format with a WGS 84 CRS. Import it into Foursquare Studio and switch to a Hexbin map. Set Lat to the Y column and Lng to the X column. Set color to values and height to values. Make sure to change what Aggregate Value is set to. Play around with the Radius, Colour, Height Scale, and Height Range settings until you get something you like.
- For an additional bonus mark, use 3D tools in Foursquare Studio to visually explore whether there is a correlation between Life Expectancy in Males and another variable in the Health Indicators dataset.
- For one final bonus mark, find the Google Dataset Search tool in the Resources page. Use it to find and download an interesting GeoJSON or Shapefile that you might want to work with. Make a 3D map of it in QGIS or Foursquare Studio. 

# 4: Alternatives

An elegant, fast alternative to what we've done in QGIS and Foursquare is Datawrapper, which some of you will be familiar with from my other course. Using it, we can make choropleth and symbol maps, as well as annotated journey maps. It is very easy to use, but not as robust or flexible as the more detailed GIS tools we've already learned. We'll make a quick symbol map.
- Go to https://www.datawrapper.de/maps
- Upload the health.geojson file I've put in the Shared Drive.
- For data, upload the life.csv. It should recognize the x and y columns as lon and lat. 
- Set the size and colour to VALUE.
- Play around with the other features. Try, for example, a divergent colour palette.
- See if you can figure out how to make a choropleth.

Another alternative would be to use Flourish Studio, which will also be familiar to those of you in my other course. 
- Go to https://flourish.studio/
- Log in and create a new visualization. 
- Select the "simple point map" option.
- Open the Data tab, switch to Points, upload the life.geojson, and set Latitude to AE and Longitude to AD, Scale to O, and Color to O.

# Misc

- You can also explore the Unfolded/Studio plugin for QGIS if you want to try an integrated approach to moving layers between the two platforms https://docs.foursquare.com/analytics-products/docs/integrations-qgis
