# Introduction to Datawrapper

Datawrapper is a web-based platform with an easy-to-use interface for creating custom charts, maps, and tables. You can explore it at https://www.datawrapper.de/

Gregor Aisch, one of the founders of Datawrapper, was Graphics Editor at the New York Times from 2014-2017 and now works at Zeit Online, so there is a strong connection between this tool and the field of data journalism. Notably, he also writes a very informative blog called vis4.net: https://www.vis4.net/blog/

## Data Preparation

For this exercise, we're going to use the Durham Regions Health Neighbourhoods data that a few groups might have looked at. If we wanted to explore the question that I posed at the end of the Dataset Biography - whether Oshawa is healthy/affordable/prosperous/diverse for newcomers to Canada - how might we begin?

- We'll start by exploring the table at https://opendata.durham.ca/datasets/8e4af909fd1947daaa50d5df15140afa_46/explore
- There are almost 100 indicators, and we can explore filtering them (e.g. for "Recent newcomers") in the Durham Open Data interface, but it will probably make more sense to download the data and import it into a spreadsheet application like Google Sheets or Excel. There is a sheet in the Shared Drive under /In-Class Exercises/Durham Health/ called "Health_Neighbourhoods_-_Data_Table."
- Let's freeze the top row and create filters on columns B-G.
- Then, we'll create a new sheet and name it Key Indicators.
- Finally, we'll filter for indicators of interest (e.g. Recent newcomers; Life expectancy; Smoking; Cardiovascular disease) and year, then sort by MUNICIPALITY_NAME. In the Key indicators sheet, we'll copy in a column for MUNICIPALITY_NAME and add a new column with the specific indicator of interest (e.g. Recent newcomers) as the column name. Make sure that the sheet is sorted according to MUNICIPALITY_NAME. Copy the cells in the original VALUE column and paste them underneath the new column. There should be 50 cells. Repeat this for other indicators of interest. 

## Visualization

- Open up https://www.datawrapper.de/ and click on the Start Creating button. 
- Copy and paste in the data from the Key Indicators sheet.
- Check it and make sure it looks alright.
- Make a scatterplot comparing cardiovascular disease and life expectancy for men by setting those columns in the Refine section.
- Add a trendline.
- Refine your chart to clean things up, add a title, etc., and then explore the various other options, including colour blindness checks. Lay it out at a size that is appropriate, and figure out what format you want to use it in. Downloading .png files is usually a good approach.

# Introduction to Flourish Studio

Now that we know how to use Datawrapper to begin an exploration into a research question (e.g. whether Oshawa is healthy/affordable/prosperous/diverse for newcomers to Canada), we might also want to explore more advanced tools. One very robust tool is Flourish, a powerful data visualization platform that makes it easy to develop interactive charts and to tell engaging stories with data. You can explore it at https://flourish.studio/

## Data Preparation

- In the previous exercise, we filtered Durham Region health data to select indicators and time periods we were interested in, sorted them by municipality, and then plotted life expectancy and cardiovascular disease in a Datawrapper scatterplot to visually explore possible correlations.
- If we were going to follow the original prompt - to see whether Oshawa is healthy for newcomers to Canada - we might also want to select only the neighbourhoods that fall above a threshold value for recent immigrants. We might select the top 25 neighbourhoods in this filtered column, and we'll find that they all share the attribute that more than 5% of their population is composed of residents who immigrated to Canada between 2011 and 2021. So, let's prune our key indicators data and then download it as a .csv file.

## Visualization

- Next, we'll log in to Flourish. First things first, take some time to explore all of the "new visualization" styles.
- Make a scatterplot and upload your .csv.
- Set your X values to the column containing cardiovascular disease values, your Y values to the column containing life expectancy, and Name to your municipality name column.
- Hit preview.
- Add a trendline.
- Again, try out the different options. Turn on and off the data labels. Change the colours, try out some different chart types, etc. 
- The nice thing about working with Flourish is that you can hit the "Create Story" button and add either a slide-based story, or a scrolling one if you want to pay for a license.
- More important, Flourish was recently bought by Canva, so there is also an option to publish your interactive chart to use in Canva. Try inserting it into a "data infographic" template and think about what story you might tell.

# Exploring Alternatives and Possibilities

- Now, let's leverage ChatGPT to explore new directions. Log in to https://chatgpt.com/
- Attach your larger data file and feed it a prompt like this: "Given the attached data, what would be some interesting queries that would generate data-driven insights?" When it asks whether you want to run the analyses, consider starting a Colab file to run the Python code that it generates.
- Follow that with a prompt like this: "What would be some interesting visualizations that would help illuminate these insights?"
- Then prompt it with: "What might go into an interesting and detailed report or data story based on these insights? Script a data story that includes 3 key insights."
- For 1 bonus mark, go through this process and engineer a series of at least four ChatGPT prompts that produce results *you find interesting*.
- For 1 additional bonus mark, critique ChatGPT's approach (in a few lines of text). Did it get anything wrong? What did it miss? What would you have done differently? Do you consider its output to be valid?

# Open-Ended Brainstorming

- Let's combine all of these methods in a more open-ended brainstorming process. Find one of the metrics we discussed in the Miro board https://miro.com/app/board/uXjVLsWHcD8=/
- Explore the resources sheet https://github.com/gbby/Teaching-Activities/blob/main/Resources.md
- Look for and download appropriate data using Google Dataset Search https://datasetsearch.research.google.com/
- Go through the Chart Selection tools and find 3 appropriate chart types to explore your data visually and communicate its insights.
- Make these charts in Flourish. Publish them to Canva.
- Use them to storyboard an interesting data story in Canva.
- Ask ChatGPT (or a similar tool) to assist with your process, but don't rely on it exclusively. Be creative! 
