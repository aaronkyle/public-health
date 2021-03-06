# Institute for Health Metrics and Evaluation (IHME) Dashboard

## Introduction

In this tutorial, we'll create and style multiple individual plots in the Chart Studio, add them to a dashboard, and utilize the crossfilter feature to interact and explore health indicators on a global scale. The data comes from the Institute for Health Metrics and Evaluation (IHME), which is based in Seattle, Washington, USA.

 ## Contents
 
- [Getting Started](##1.-Data)
- [Designing Choropleth Maps](###2.1.-Healthy-Life-Expectancy-Choropleth-Map)
- [Designing Bubble Charts](###2.4.-Overweight-Prevalence-and-Healthy-Life-Expectancy-Bubble-Chart)
- [Building the Dashboard](##3.-Create-a-Dashboard)
- [Using the Crossfilter](##4.-Crossfilter)

## 1. Data

To get started, head to Plotly’s [Chart Studio](https://plot.ly/create/) and add your data. You have the option of typing directly in the grid, uploading your file, or entering a URL of an online dataset. For this tutorial, we'll use data from the IHME in Seattle.

Simply, copy the URL (https://plot.ly/~Dreamshot/8914) or click [**'Fork & Edit'**](https://plot.ly/create/?fid=Dreamshot:8914). If you choose the latter, the Chart Studio ought to have opened and you're all set to go. If the former, navigate to the [Chart Studio](https://plot.ly/create/) and click **Import**, **By URL**, and then paste in the **URL**.

![Fork and Edit](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/1.png)

## 2. Create a Chart

To visualize international health metrics, we'll create six individual charts: (1) a choropleth map to illustrate worldwide healthy life expectancy, (2) a choropleth map to illustrate the prevalence of high risk alcohol consumption, (3) a choropleth map to illustrate daily smoking prevalence, (4) a bubble chart that examines the relationship between overweight prevalence and health life expectancy, (5) a bubble chart that examines the relationship between high risk alcohol consumption and healthy life expectancy, and (6) a bubble chart that examines the relationship between daily smoking prevalence and healthy life expectancy. In this section, we'll look at how to make each of the charts.

### 2.1. Healthy Life Expectancy Choropleth Map

##### 2.1.1. Create
Now that we have the data added to the grid, we can select our chart type. To do so, select *Graph* on the left-hand side, then *Create*. Click *Chart Type*, and **Choropleth** from the *Maps* column.

Now to populate the map with data, in the *Locations* and *Values* dropdown select **Country Code** and **HALE**, respectively. Additionally, for the *Location Format* the **Country Abbreviations (ISO-3)** option should be selected.

![Create Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.1.1.png)

##### 2.1.2. Region and Projection
While we're still in the *Create* tab, we can try out a few different *Map Regions* and *Projections*. Since our data is global, we selected the *Map Region* **World** and *Projection* **Natural Earth**. 

![Select Region and Projection](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.1.2.png)

##### 2.1.3. Traces
Now that we have finished choosing the region and projection, click *Traces* to style your map. There are a host of *Colorscales* to choose from. For this particular map, we chose the second colorscale from the left.

![Choose Colorscale](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.1.3.png)

##### 2.1.4. Layout
Next, navigate to the *Layout* tab to set the margins. To set the margins, select the *Margins and Padding* box and enter the values **0, 0, 0, 0, 0**, respectively.

![Set Margin](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.1.4.png)

##### 2.1.5. Color Bars
Finally, you can style the color bar by navigating to *Color Bars*. For this tutorial, we've decided to **Hide** the *Color Bars* on each map because the data speaks for itself. 

![Hide Colorbar](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.1.5.png)

##### 2.1.6. Save
Congrats, your chart is complete! Click **Save** on the left-hand side of the screen. In the pop-up, enter your filename and select either **Public** (visible to all) or **Private Link** (visible only to those who you share the link with) and hit **Save**. Since these plots are destined for a dashboard, they can't be set to private.

![Finished Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.1.6.png)

### 2.2. Alcohol Consumption Choropleth Map

##### 2.2.1. Create
As demonstrated earlier, the first step is to select our chart type. To do so, select *Graph* on the left-hand side, then *Create*. Click *Chart Type*, and **Choropleth** from the *Maps* column.

Like the previous map, to populate it with data: in the *Locations* and *Values* dropdown select **Country Code** and **Drinking**, respectively. Additionally, for the *Location Format* the **Country Abbreviations (ISO-3)** option should be selected.

![Create Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.2.1.png)

##### 2.2.2. Region and Projection
While we're still in the *Create* tab, we can try out a few different *Map Regions* and *Projections*. Since our data is global, we selected the *Map Region* **World** and *Projection* **Distance Preserving (Equirectangular)**. 

![Select Region and Projection](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.2.2.png)

##### 2.2.3. Traces
Now that we have finished choosing the region and projection, click *Traces* to style your map. As noted earlier, there are a host of *Colorscales* to choose from. For this particular map, we chose the sixth colorscale from the left. Next, we set the *Colorscale Range* to *Min Value* **1** and *Max Value* **20**.

![Choose Colorscale](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.2.3.png)

##### 2.2.4. Layout
Next, navigate to the *Layout* tab to set the margins. In the *Margins and Padding* box, enter the values **0, 0, 0, 0, 0**, respectively.

![Set Margin](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.2.4.png)

##### 2.2.5. Color Bars
Finally, you can style the color bar by navigating to *Color Bars*. For this tutorial, we've decided to **Hide** the *Color Bars* on each map because the data speaks for itself. 

![Hide Colorbar](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.2.5.png)

##### 2.2.6. Save
Congrats, your chart is complete! Click **Save** on the left-hand side of the screen. In the pop-up, enter your filename and select either **Public** (visible to all) or **Private Link** (visible only to those who you share the link with) and hit **Save**. Since these plots are destined for a dashboard, they can't be set to private.

![Finished Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.2.6.png)

### 2.3. Smoking Choropleth Map

##### 2.3.1. Create
First off, let's select our chart type. To do so, select *Graph* on the left-hand side, then *Create*. Click *Chart Type*, and **Choropleth** from the *Maps* column.

Like before, to populate the map with data: in the *Locations* and *Values* dropdown select **Country Code** and **Smoking**, respectively. Additionally, for the *Location Format* the **Country Abbreviations (ISO-3)** option should be selected.

![Create Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.3.1.png)

##### 2.3.2. Region and Projection
As we've seen from earlier maps, you can try out a few different *Map Regions* and *Projections* in the *Create* tab. Since our data is global, we selected the *Map Region* **World** again and *Projection* **Globe (Orthographic)** this time. 

![Select Region and Projection](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.3.2.png)

##### 2.3.3. Traces
Now that we have finished choosing the region and projection, click *Traces* to style your map. Try out different *Colorscales* to see which you'd prefer. For this particular map, we chose the fifth colorscale from the left. Next, we set the *Colorscale Range* to *Min Value* **5** and *Max Value* **35**.

![Choose Colorscale](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.3.3.png)

##### 2.3.4. Layout
Once again, navigate to the *Layout* tab to set the margins. In the *Margins and Padding* box, enter the values **0, 0, 0, 0, 0**, respectively.

![Set Margin](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.3.4.png)

##### 2.3.5. Color Bars
Finally, you can style the color bar by navigating to *Color Bars*. For this tutorial, we've decided to **Hide** the *Color Bars* on each map because the data speaks for itself. 

![Hide Colorbar](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag/2.3.5.png)

##### 2.3.6. Save
Congrats, your chart is complete! Click **Save** on the left-hand side of the screen. In the pop-up, enter your filename and select either **Public** (visible to all) or **Private Link** (visible only to those who you share the link with) and hit **Save**. Since these plots are destined for a dashboard, they can't be set to private.

![Finished Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.3.6.png)

### 2.4. Overweight Prevalence and Healthy Life Expectancy Bubble Chart

##### 2.4.1. Create
As usual, we will select our chart type first. We'll move on from the choropleth maps now to see if we can uncover any relationships in the data. To do so, select *Graph* on the left-hand side, then *Create*. Click *Chart Type*, and **Scatter plot** from the *Business* column.

![Create Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.4.1.png)

To populate this chart with data, for the *X* axis data select **HALE**, for the *Y* axis data select **Obesity**, for the *Hover Text* option select **Country**, for the *Size* option select **Population**, and for the *Color* option pick **Obesity**.

##### 2.4.2. Layout
Before styling the traces we'll first adjust the font size. Hence, navigate to *Layout* under *Style*. Here, open the *Title and Fonts* box and select **20** for the *Title* font size and **14** for the *Global Font* size. For this plot, we'll leave the rest of the layout as is. Now, in the *Margins and Padding* box, enter the values **0, 20, 35, 0, 0**, respectively.

![Select Layout](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.4.2.png)

##### 2.4.3. Traces
Now that we have finished with styling the layout, click *Traces* to style the scatter points. We can redefine the colorscale by simply choosing from the preselected scales. For this one, we selected the fourth colorscale from the left, **blue to red**. Farther down, we set our *Colorscale Range* to **Custom** and then adjusted the *Min Value* of our data to **0** and *Max Value* to **100** and also changed the *Maximum Marker Size* to **60**.

![Choose Colorscale](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.4.3.png)

##### 2.4.4. Axes
Navigate to the *Axes* tab to style the grid lines and tick labels. To style the grid lines, open the *Lines* box and select *X*. Here, press **Hide** for the *Vertical Grid Lines*. Next, navigate to the *Tick Labels* drop down. Here, select *Y* and select **custom** in the *Suffix* box. Then, type the percent (%) symbol in the box, erasing the word **custom**.

![Set Axes](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.4.4.png)

##### 2.4.5. Color Bars
Now, we'll enable the colorbar. Head to *Color Bars* and **Show** the *Color Bar* in the menu. Open the *Size and Positioning* menu and adjust the width to **10**.

![Color Bar](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_3/2.4.4.1.png)

##### 2.4.6. Save
Congrats, your chart is complete! Click **Save** on the left-hand side of the screen. In the pop-up, enter your filename and select either **Public** (visible to all) or **Private Link** (visible only to those who you share the link with) and hit **Save**. Since these plots are destined for a dashboard, they can't be set to private.

![Finished Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_3/2.4.6.png)

### 2.5. Alcohol Consumption and Healthy Life Expectancy Bubble Chart

##### 2.5.1. Create
Like before, we will select our chart type first. Select *Graph* on the left-hand side, then *Create*. Click *Chart Type*, and **Scatter plot** from the *Business* column.

![Create Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.5.1.png)

To populate this chart with data, for the *X* axis data select **HALE**, for the *Y* axis data select **Drinking**, for the *Hover Text* option select **Country**, for the *Size* option select **Population**, and for the *Color* option pick **Drinking**.

##### 2.5.2. Layout
Before styling the traces we'll first adjust the font size. Hence, navigate to *Layout* under *Style*. Here, open the *Title and Fonts* box and select **14** for the *Global Font* size. For this plot, we'll leave the rest of the layout as is. Now, in the *Margins and Padding* box, enter the values **10, 20, 35, 0, 0**, respectively.

![Select Layout](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.5.2.png)

##### 2.5.3. Traces
Now that we have finished with styling the layout, click *Traces* to style the scatter points. We can redefine the colorscale by simply choosing from the preselected scales. For this one, we selected the sixth colorscale from the left, **dark purple to beige**. Farther down, we set our *Colorscale Range* to **Custom** and then adjusted the *Min Value* of our data to **1** and *Max Value* to **20** and also changed the *Maximum Marker Size* to **60**.

![Choose Colorscale](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.5.3.png)

##### 2.5.4. Axes
Navigate to the *Axes* tab to style the grid lines and tick labels. To style the grid lines, open the *Lines* box and select *X*. Here, press **Hide** for the *Vertical Grid Lines*. Next, navigate to the *Tick Labels* drop down. Here, select *Y* and select **custom** in the *Suffix* box. Then, type the percent (%) symbol in the box, erasing the word **custom**. 

You can also feel free to erase the pre-populated *x* and *y* axis titles, as well as the chart title, at this step. We'll consider these again when we reach the dashboard. 

![Set Axes](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.5.4.png)

##### 2.5.5. Color Bars
Now, we'll enable the colorbar. Head to *Color Bars* and **Show** the *Color Bar* in the menu. Open the *Size and Positioning* menu and adjust the width to **10**.

![Color Bar](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_3/2.5.4.1.png)

##### 2.5.6. Save
Congrats, your chart is complete! Click **Save** on the left-hand side of the screen. In the pop-up, enter your filename and select either **Public** (visible to all) or **Private Link** (visible only to those who you share the link with) and hit **Save**. Since these plots are destined for a dashboard, they can't be set to private.

![Finished Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_3/2.5.6.png)

### 2.6. Smoking and Healthy Life Expectancy Bubble Chart

##### 2.6.1. Create
Once again, select your chart type first. Select *Graph* on the left-hand side, then *Create*. Click *Chart Type*, and **Scatter plot** from the *Business* column.

To populate this chart with data, for the *X* axis data select **HALE**, for the *Y* axis data select **Smoking**, for the *Hover Text* option select **Country**, for the *Size* option select **Population**, and for the *Color* option pick **Smoking**.

![Create Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.6.1.png)

##### 2.6.2. Layout
As usual, before styling the traces first adjust the font size. Navigate to *Layout* under *Style*. Open the *Title and Fonts* box and select **14** for the *Global Font* size. Like the previous plots, we'll leave the rest of the layout as is. Now, in the *Margins and Padding* box, enter the values **0, 20, 35, 0, 0**, respectively.

![Select Layout](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.6.2.png)

##### 2.6.3. Traces
Now that we have finished with styling the layout, click *Traces* to style the scatter points. We'll again select one of the predefined scales. For this one, we selected the fifth colorscale from the left, **blue to yellow**. Farther down, we set our *Colorscale Range* to **Custom** and then adjusted the *Min Value* of our data to **5** and *Max Value* to **35** and also changed the *Maximum Marker Size* to **60**.

![Choose Colorscale](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.6.3.png)

##### 2.6.4. Axes
Now, navigate to the *Axes* tab to style the grid lines and tick labels and change the range. As we did earlier, to style the grid lines, open the *Lines* box and select *X*. Here, press **Hide** for the *Vertical Grid Lines*. Next, navigate to the *Tick Labels* drop down. Here, select *Y* and select **custom** in the *Suffix* box. Then, type the percent (%) symbol in the box, erasing the word **custom**. 

Now, scroll back up to the *Range* box and select *Y*. Change the *Selection* to **Custom Range** and your *Min* to **-1** and *Max* to **37**.

You can also feel free to erase the pre-populated *x* and *y* axis titles, as well as the chart title, at this step. We'll consider these again when we reach the dashboard. 

![Set Axes](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_2/2.6.4.png)

##### 2.6.5. Color Bars
Before we finish, we'll enable the colorbar. Head to *Color Bars* and **Show** the *Color Bar* in the menu. Now, open the *Size and Positioning* menu and adjust the width to **10**.

![Color Bar](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_3/2.6.4.1.png)

##### 2.6.6. Save
Congrats, your chart is complete! Click **Save** on the left-hand side of the screen. In the pop-up, enter your filename and select either **Public** (visible to all) or **Private Link** (visible only to those who you share the link with) and hit **Save**. Since these plots are destined for a dashboard, they can't be set to private.

![Finished Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_3/2.6.6.png)

## 3. Create a Dashboard

With the charts completed and saved in your [home folder](https://plot.ly/organize/home), we can now create a dashboard by simply adding these charts, adjusting the layout, and styling the dashboard before sharing and interacting. To get started with creating a dashboard, hover over the *+Create* button and select **Dashboard** from the menu. Alternatively, open this [link](https://plot.ly/dashboard/create).

![Create Dashboard](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.png)

### 3.1. Add Text

Before adding a chart, we'll add a text box to describe the dashboard and its uses. Simply, click the *Text* button, where a text editor ought to appear. In the text editor, add the text you wish to display in the dashboard.

![Add Text](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.1.png)

### 3.2. Add Charts

Now to add your choropleth maps and bubble charts, click *+Plot* in the bottom left corner of the screen. A new box ought to appear with the option to 'Add a Plot'. Click, the *'Your Files'* option and then in the pop-up select one of the **choropleth maps** we made earlier. Now, you ought to see the plot added to your dashboard. Next, in the top left corner of the box where it says, "Enter a title..." insert **"Healthy Life Expectancy"**.

![Add Chart](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.2.png)

Repeat the process for the remainder of the choropleth maps and bubble charts we made earlier, titling each accordingly and placing the choropleth map next to a bubble chart for a clean look.

![Repeat Process](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.3.png)

### 3.3. Style It

Now that we have the structure of our dashboard, we can style it. To do so, navigate to the *Settings Icon* directly opposite the dashboard title. When hovering you'll see the option settings from the menu. After clicking **Settings**, a panel will appear from the right-hand side of the screen. Here, we have the option of headers, colors, text, layout, and filter.

![Dashboard Options](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.png)

In *Headers*, call the *Title* **Institute for Health Metrics and Evaluation**, set the *Logo URL* as **https://upload.wikimedia.org/wikipedia/en/a/ab/Institute_for_Health_Metrics_and_Evaluation_logo_sm.jpg**, and in the *Links* box type **IHME**.

![Dashboard Headers](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.2.1.png)

In *Colors*, set the *Header Background* as **#FFFFFF**, the *Header Font Color* as **#506784**, the *Page Background* as **#B4F582**, the *Box Background*, *Box Border*, and *Box Header Background* as **#FFFFFF**, and *Box Header Font Color* as **#506784**.

![Dashboard Colors](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.2.2.png)

In *Text*, set the *Font Color* as **#506784**, the *Font Family* as **Raleway**, the *Header Font Size* as **1.6em**, the *Header Font Weight* as **400**, the *Text Box Font Size* as **1.6rem**, and the *Text Box Background Color* and *Text Box Font Color* as **#FFFFFF**.

![Dashboard Text](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.2.3.png)

In *Layout*, set the *Page Layout* to **Dashboard**.

![Dashboard Layout](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.2.4.png)

In *Filter*, set the *Search Bar* to **Hide** and *Crossfilter* to **Enable**

![Dashboard Filter](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.2.5.png)

Congrats, your dashboard is complete! Click **Save** on in the bottom right-hand side of the screen. In the pop-up, enter your filename and select either **Public** (visible to all), or **Private Link** (visible only to those who you share the link with), or **Private** (visible only to you) and hit **Save**.

![Dashboard Final](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME/tut_imag_4/3.2.6.png)

## 4. Crossfilter

Finally, we'll briefly demonstrate crossfilter. 

**Crossfilter** is a visual analysis technique for multidimensional data that can help clarify correlations between dimensions.

To use crossfilter, simply click-and-drag on any of the charts and maps in the dashboard you just created. Data sharing common rows between the charts will highlight in red, helping pinpoint complex relationships between various health indicators and location on the globe.

![Dashboard Final](https://raw.githubusercontent.com/plotly/public-health/master/screencasts/IHME_crossfilter_gif.gif)
