# Overview of the Dataset
The dataset used in this assignment is the Heart Failure Clinical Records dataset provided by UC Irvine's Machine Learning Repository.  This dataset has the medical records of 299 patients who had heart failures.  I chose this dataset because I am interested in AI/ML for medical use cases and was searching for a dataset that matched these interests.  

# Variables
| Variable                 | Type    | Description                                               |
|--------------------------|---------|-----------------------------------------------------------|
| age                      | integer | age of the patient                                        |
| anaemia                  | bool    | decrease of red blood cells of hemoglobin                 |
| creatinine_phosphokinase | integer | level of the CPK enzyme in the blood                      |
| diabetes                 | bool    | if the patient has diabetes                               |
| ejection_fraction        | integer | percentage of blood leaving the heart at each contraction |
| high_blood_pressure      | bool    | if the patient has hypertension                           |
| platelets                | float   | platelets in the blood                                    |
| serum_creatinine         | float   | level of serum creatinine in the blood                    |
| serum_sodium             | integer | level of serum sodium in the blood                        |
| sex                      | bool    | woman or man                                              |


# Cleansing Applied to Dataset
This dataset had minimal cleansing to it because there was no missing or incorrect data in the dataset (correct as far as we know that is).  There were a few mappings applied to make the data easier to read.  The labels created for this are:
- Death Event Label
0: Survived
1: Died

- Sex Label
0: Female
1: Male

- Smoking Label
0: Non-Smoker
1: Smoker

- Diabetes Label
0: Non-Diabetic
1: Diabetic

- High Blood Pressure Label
0: No High Blood Pressure
1: High Blood Pressure


# A narrative description of each visualization type in your dashboard 

A discussion of how these visualizations complement each other and when each should be used, Dashboard-specific considerations like interactivity options 

# Visualizations Used
- Histogram
- Box Plot
- Scatterplot
- Heatmap


# Why Each Visualization Was Chosen
### Hisogram
The histogram was chosen to show the distribution of one selected variable at a time.  This would show how spread out each variable is, where most of the data fell, as well as a the range of the data.  This helps to reveal how values are spread out and where most of the records are identified for each variable.  It will also help us see how close to a normal distribution the data falls.

### Box Plot
The box plot was selected because it clearly shows the range of the data, the q1 and q3 quartiles, the median, and the outliers for each filter selection.  This allows us to easily make comparisons between the group that survived and the group that died.  

### Scatterplot
The scatterplot was chosen to show relationships between two variables and see if there are interesting relationships between two variables in the data.

### Heatmap
The heatmap was chosen becxause it allows us to see all the variables compared against each other to see in one visualization the corelations and relationships between all the variables

### Data Table
I also added a data table because, in my experience working as a data scientist and with visualization software, I've noticed that at some point, users are going to want access to the underlying data as well.  To accomodate for this, I often put data tables in the dashboards I've created (to help mitigate the immediate rush to "how can I get this data in excel" that I commonly get).  

### Why these visualizations work together
These visualziations work together because the histogram allows us to view one variable in isolation, to gain an understanding of it on its own.  Then the box plot allows us to take that variable and split it into survival or death groups to see, based on the outcome, how the variable changes.  The scatterplot allows us to look at two variables at once, as opposed to just a single variable from before, to see if there are any relationships between two variables.  Finally, the heat map lets us take this relationships exploration to the next level by looking at all relationships between all variables at once.  


# Visualization Library
### Visualization Libraries - Panel and Plotly Express
Panel was chosen because it looked very interesting from the lecture shown by Dr. Bobby and I wanted to learn this framework more.  I particularly like that this could be embedded into an app, similar to other frameworks I've used like Streamlit.

Plotly Express was chosen mainly because the visualization library I wanted to choose, seaborn, wasn't allowed and I noticed from the slack channel another student in the class was using Plotly, so that was how I discovered it

### Panel
Panel is an open-source python framework to help with the development of dashboards within python.  I found it particularly interesting because it can be embedded within python apps using frameworks like fastapi.  I also liked that Panel is a declarive means of creating an app.  What I mean by this is, in most applications, you need to created html files and specific exactly where everything should go.  Panel minimizing the need to explicitly say this and instead provide a few details to quickly build a POC of what the app should look like.  This reminded me of similar frameworks I've used in the past, such as Streamlit or Gradio.  Since Panel is an open source project, it requires installation via either pip or anaconda.  The docs also recommended the installation of other modules named watchfiles, jupyter_bokeh, and ipykernal (because I am using VS Code) so I installed that as well.  For my build, I chose to install it to a virtual environment via pip, so I installed it via:
```
pip install panel watchfiles jupyter_bokeh ipykernel
```


### Plotly Express
This library is a built in part of the plotly library which is an open-source project.  It provides a simplified interface for creating various graphs based on pandas dataframes.  I chose it because it works well with Panel.    I also chose it because it is largely declarative.  I didn't want to have to spend a lot of time specifiying exactly how I wanted a visualization to work; I simply wanted something where I gave a few details and I was able to see the output.  That's one of the things that drove me to plotly, because it allows for that quick POC type work, without having to specifiy exactly how I wanted everything to look.   Since it is an open source project, it requires installation via either pip or anaconda.  For my build, I chose to install it to a virtual environment via pip, so I installed it via:
```
pip install plotly
```

### Other Observations
I noticed from Dr. Bobby's video that Panel would not work in Vorcareum, so I instead built this locally in jupyter notebooks through VS Code (just like what Dr. Bobby was using).  I did notice issues getting the dashboards to display in VS Code, where the widgets were displaying, but not the charts themselves, but my intention was to display this in a browser anyway (which is what made me interested in Panel to begin with), so this wasn't an issue for me, but it's important to note that for others who may wish to display this directly in a Jupyter notebook.  I tried working aroudn this for a while with suggestions I found on Panel's docs page: https://panel.holoviz.org/getting_started/installation.html but could never get it to work properly (including the quickstart on Panel's docs themselves).  It's important to also note that I built everything on python 3.13.5 on a mac running Sequioa 15.7 and that Panel's docs state it requires Python 3.9 or higher and Plotly Express, I couldn't find what version of python it required, including when I did a pip show plotly command in terminal (which is something in my software engineering life is a common requirement I've seen in coding standards). Since I was building in VS Code, I also followed the instructions for VS Code notebooks here: https://panel.holoviz.org/how_to/notebook/other_nb.html which included the installation of jupyter_bokeh and the steps for VS Code configuration here: https://panel.holoviz.org/how_to/editor/vscode_configure.html



# Setup Instructions



