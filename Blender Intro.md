# 1: Intro to Blender

Blender is a free and open source 3D design software application. There are many comparable tools, like Maya and Fusion from Autodesk, but Blender is free and there's a great support community. Explore it at https://www.blender.org/

# 2: Explore the Interface

Start by downloading and opening up Blender. The first thing we're going to do is explore a few important parts of the interface.
- Protip: use a mouse!
- Press tab to toggle between object and edit modes.
- Switch between vertex, edge, and face selection tools (to the right of the mode dropdown). Learn the difference between these three things.
- Explore the tools on the left-side tool bar. 
- Move your object around with the transform tool.
- Extrude a face with the extrude tool.
- Right-click and subdivide a face. 
- Switch back to object mode.
- Press n to get the object transformation window and figure out what each of the items in it do.

# 3: BlenderGIS

Next, we'll use a Blender plugin called BlenderGIS that serves to create a bridge between Blender and geographic data analysis tools. 

- Go to https://github.com/domlysz/BlenderGIS and open the quick start guide. Follow the installation instructions in the Preamble section on the right.
- We will use Durham Region life expectancy data, so make sure you've downloaded and unzipped the health.zip shapefile from the Shared Drive (In-Class Exercises/Durham Health).
- Delete the default cube in Blender.
- Once you have BlenderGIS installed and configured, open the new GIS panel and import the shapefile.
- Set elevation to none.
- Set extrusion from VALUES and extrude along the z-axis. 
- Separate objects and set name from COMMON_NAM. 
- Set CRS to WGS84 latlon.
- Press n to get dimensions.
- Make sure z-axis is scaling properly. You can press a to select all, then s to scale and z to scale only the z-axis.
- Consider assigning materials to colour/texture your object(s) for other formats (e.g. AR/VR).
- Either change your units to kilometres or scale to .1 when exporting. Instructions for changing units can be found here: https://www.blenderbasecamp.com/how-to-change-my-unit-measurements-in-blender/
- Export to .stl or .obj or .fbx.
  
# 4: 3D Printing

We can explore preparing our 3D map for physicalization via a 3D printer. Depending on the printer you have available, you will use different slicing software. In my case, I use Cura, and most of the printers you encounter, including the ones in the library, probably will as well, so you can download Ultimaker Cura to see what it might look like if you were to 3D print it. 
- Download and install https://ultimaker.com/software/ultimaker-cura
- Import an .stl of your Blender-created file. Scale it until it fits on the virtual printer bed at a size that looks right.
- Slice and preview the printing operation.
- Take it to the library and ask them about printing on one of their machines.
  
# 5: Alternatives

Sometimes, Blender is too complex for quick, simple 3D object creation. When that is the case, I almost always turn to Autodesk's Tinkercad platform.
- Go to https://www.tinkercad.com/
- Sign up for an account and log in. (Note that your Ontario Tech email will get you access to a wide array of professional software from Autodesk https://www.autodesk.com/education/edu-software/overview/) 
- Click the Create button.
- Consider importing your .stl file. 
- Pull a cube onto the grid. Reshape it.
- Pull a clear cube onto some part of it. Select both items. Hit the Group button (or press Ctrl-G) to cut the clear section from the original.
- Try different tools and importing additioanl objects.
- For 1 bonus point, make a 3D infographic (including 3D text) that includes your original Durham Region health .stl in 3D format.
