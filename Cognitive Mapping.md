# 1: Introduction to Cognitive Mapping

Organize yourselves into small groups. Grab some pencil crayons and paper. Individually, sketch a "food tour" of some part of the city where you live (or the city where you're from). Your tour should include a route connecting three of your favourite restaurants or places to get food. 

Constraints and Design Considerations:
- Spend 10 minutes sketching out your map.
- You cannot use any text on it - icons and symbols only. Think about what symbols might have meaning.
- Consider how you will represent movement and direction on the map.
- Think about your audience. Are they tourists? Are they familiar with your city?
- Don't worry about making it look pretty.
- When you're done, share your map with your group members and ask them whether it makes sense to them.

# 2: Sketch

We'll do this in groups, but you'll work individually until you're told to focus on group discussion. You can chat with your group members while you're working.
- Draw Oshawa. Work from memory (in other words, **do not use a map**!). 5 minutes.
- Next, personalize it. Come up with a story. Places you like. Hangouts. Routes. For now, just write as notes. 5 minutes.
- Next, encode the story in the form of abstract visualization elements (path markers; heatmap/clusters; symbols). 5 minutes.
- Finally, annotate your map. Add a legend or key, title, etc. 5 minutes.

Following this, share your map with your group members. See if they can guess where it refers to. Discuss the following questions and jot down your insights:
- What are the local, everyday interactions and encounters with an image (a GPS system; a local map; a subway map) that affect your own calculations about how a "user" should navigate this civic space? How do iconic or otherwise highly stable representations guide our interactions with those objects?
- How would it be different if there was a subway system and a familiar representation (i.e. a subway map) of it? What does the transit map look like where you grew up? Is it composed of 45 and 90 degree angles? Is it radial?
- What's missing? Did you omit anything?
- How did you highlight personal, idiosyncratic, embodied data experience?
What would you do to make this more engaging or interactive? To make it more inclusive and accessible to a wider audience?
- What other methods could you use to sketch and/or display it (e.g. 3D visualization; isometric projection)?
- What additional data "layers" could you add to it (e.g. walking distances; danger zones)?

When you're done, take a photo of your map. Name it Yourlastname.png and put it in the shared drive: /In-Class Exercises/Cognitive Mapping

# 3: Digitize

Learning to work with Google's mapping/GIS platforms will give you very powerful options to create digital maps. While I would normally recommend using Google's My Maps platform, you will not be able to access it with your .net address. Instead, we can use Google Earth, which is considerably more powerful. 
- Sign in at https://earth.google.com/
- Add a New Project
- Add and label placemarks
- Add a path
- Add a polygon to cluster a bunch of placemarks
- Try the slideshow option
- Export a .kml file and load it in another tool like https://geojson.io/ or QGIS (drag it into your layers panel)

# 4: Classify

Get in groups of 5, find the maps that you produced last week, and put them in a sub-folder. Together, you will classify the elements in the maps based on Kevin Lynch's theories. Remember the acronym PEDNL (Paths, Edges, Districts, Nodes, Landmarks). Here's a visual reference: 

![PEDNL](Images/pednl.png?raw=true)

While analyzing your maps, you will want to examine which elements are common. Add a new document in your sub-folder for taking notes, and start to organize them based on the following sample questions. If you like, use a Google Drawing or Miro board to collect ideas or annotate on existing maps.
- Are car paths more common than footpaths?
- Are the edges natural or human-made?
- What sorts of districts turn up? Campuses? Downtown cores? Tourist zones?
- Are the nodes and intersections linked to human or machine paths?
- Do we see any landmarks? Are they natural or human-made? Are they also attractions?
- Does the orientation of the map tell us anything?

What we're doing is, following Lynch, creating an "image" of the city.

# 5: Instruct
Your goal in this step will be to understand how movement works in your image. In order to do this, you will attempt to train a machine to navigate it. First, you will want to trace a path on your initial sketch - Point A to Point Z, with any number of points marked out along the way. Next, imagine that you need to guide a delivery robot to follow the route on your map (For reference, see http://drtechniko.com/how-to-train-your-robot/). Give it basic instructions (e.g. "turn left"; "pause"). Think about the following questions:
- What will it need to know? 
- What is its starting point? 
- Can you use abstraction? 
- What obstacles might it face? 
- How does a robot "see" the world? 

# 6: Experience
Sometime soon, try to walk or travel your route and then re-draw your map afterwards. Does your embodied perception of space and time change the graphic? How does your updated version compare to the one you drew from memory?
