# 1: Intro to Blender

Blender is a free 3D design software application. There are many comparable tools, like Maya and Fusion from Autodesk, but Blender is free and there's a great support community. 

# 2: Explore the Interface

Start by opening up Blender. The first thing we're going to do is explore a few important parts of the interface.
- Use a mouse
- Switch to edit mode
- Vertices/Edges/Faces
- Transform tool
- Extrude tool
- Subdivide faces
- Switch back to object mode
- Press n to get the object transformation window

# 3: BlenderGIS

Now, we'll use a Blender plugin called BlenderGIS that serves to make the bridge between Blender and geographic data. 

- Go to https://github.com/domlysz/BlenderGIS and open the quick start guide. Follow the installation instructions in the Preamble section on the right.
- We will use Durham Region life expectancy data, so make sure you've downloaded the health.zip shapefile from the Shared Drive (In-Class Exercises/Durham Health).
- Delete the default cube in Blender.
- Once you have BlenderGIS installed and configured, open the new GIS panel and import the shapefile.
- Set elevation to none.
- Set extrusion from VALUES and extrude along the z-axis. 
- Separate objects and set name from COMMON_NAM 
- Set CRS to WGS84 latlon
- N to get dimensions
- Make sure z-axis is scaling properly. A to select all. S to scale. Z to scale only the z-axis.
- Consider assigning materials to colour/texture your object(s) for other formats (e.g. AR/VR).
- Either change your units to kilometres or scale to .1 when exporting. Instructions for changing units can be found here: https://www.blenderbasecamp.com/how-to-change-my-unit-measurements-in-blender/
- Export to .stl or .obj or .fbx.
  
# 4: 3D Printing

We can explore preparing our 3D map for physicalization via a 3D printer. Depending on your printer, you will ahve different slicing software. In my case, I use Cura, and most of the printers you encounter, including the ones in the library, probably will as well, so you can download Ultimaker Cura to see what it might look like if you were to 3D print it. 
- Download and install https://ultimaker.com/software/ultimaker-cura
- Import an .stl of your Blender-created file. Scale it until it fits on the virtual printer bed at a size that looks right.
- Slice and preview the printing operation.
  
# 5: Alternatives

- Sometimes, Blender is just too complex for quick, simple 3D creation. When that is the case, I almost always just use Tinkercad.
- Go to https://www.tinkercad.com/
- Sign up for an account and log in. 
- Click the Create button. 
- Consider importing your .stl file. 
- Pull a cube onto the grid. Reshape it.
- Pull a clear cube onto some part of it. Select both items. Hit the Group button (or press Ctrl-G) to cut the clear section from the original. 
- For 1 bonus point, make a 3D infographic (including 3D text) that includes your original Durham Region health .stl in 3D format. 
