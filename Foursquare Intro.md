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
