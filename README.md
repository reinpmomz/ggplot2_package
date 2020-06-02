# ggplot2_package
Data Visualization

install.packages(c("tidyverse", "ggforce", "ggrepel", "gtable", "gganimate", "patchwork",
                   "plotly"))

## What is ggplot2

  * R package for doing data visualisation
  
  * uses the underlying `grid` package for graphics
  
  * inspired on the <i>Grammar of Graphics</i> by Leland Wilkinson (where the name comes from)
  
  * very popular, especially for publication quality graphics
  


---
## The layers of the grammar of graphics


---
### Brief explanation of the layers

  * <b>data</b>: the underlying data 


  * <b>mapping</b>: associating variables in the data with characteristics in the plot
  
  * statistic: translating the raw values in the data to statistics of interest e.g. identity, count 
  
  * scales: mapping the range of variables onto the range of the property
  
  * <b>geometries</b>: what type of chart
  
  * facets: criteria - if any - to show sub-graphs for
  
  * coordinates: the actual position of the objects on the screen or paper 

  * theme: aspects that have to do with appearance
  
---
## The essentials: what you really need to remember 


  Essential elements for using `ggplot2`:
    * data
--

    * mapping 
--

    * geometry
    
--

  All the other layers will get filled in with sensible defaults most of the time. (Except the default theme which I dislike all the time. Your mileage may vary.)
  
  
---
## Common geometries

  * `geom_bar`: to make a bar chart with counts
  
  * `geom_col`: to make a bar chart with totals
  
  * `geom_histogram`: histograms
  
  * `geom_boxplot`: boxplots
  
  * `geom_point`: scatter plots, dot plots
  
  * `geom_line`: line graphs, trend lines, time series
  
  
  
  
---
## Common aesthetics

  * <i>x</i>
  
  * <i>y</i> 
  
  * <i>colour</i> or <i>color</i>
  
  * <i>fill</i> 
  
  * <i>size</i>
  
  * <i>group</i> 
  
  * <i>shape</i> 
  
<b>Not every aesthetic is applicable to every geometry</b>


---
## The objects/data involved

You need to create two objects:

  * a `ggplot` object
  
  * at least one geometry object, `geom_*`

Inputs/arguments

  * <i>data</i>: a dataframe
  
  * <i>mapping</i>: an aesthetic mapping created using the `aes` function.
  
<i>data</i> and <i>mapping</i> can be placed either into the parent `ggplot` object or into the `geom_*`

