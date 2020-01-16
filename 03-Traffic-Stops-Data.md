# Analyzing Traffic Stops Data

## Topics
* Replicating *Suspect Citizens* on San Diego Police Data.
* Identifying weaknesses of drawing (causal) conlcusions from
  descriptive statistics (confounders).
* Introduction to the 'Veil of Darkness' experiment.

## Reading and Analyses

* Replicate the analysis of *Suspect Citizens* on post-stop outcomes
  using the [San Diego
  data](https://data.sandiego.gov/datasets/?department=police). Begin
  with the 2015 dataset, expanding to a larger range of years as time
  permits.
  
* Replicate the analysis of *Suspect Citizens* on traffic stop rates
  using the 2015 San Diego data (expanding as time permits). To
  estimate the denominator for stop rates, use the Census data (see
  below).
  
* Read the description of the Veil of Darkness in the [Open Policing
  Tutorial](https://openpolicing.stanford.edu/tutorials/). (You might find the rest of the tutorial useful as
  well). 
  
* Begin reading the [SDSU
  Study](https://www.sandiego.gov/sites/default/files/sdpdvehiclestopsfinal.pdf)
  as you create your analyses (skim it for content; you will read it
  more thoroughly later).
  
### Geo-spatial analysis and 'computing the denominator'

To compute stop-rates for the entire city, one can attempt to compute the
denominator using the demographic 2010 census data for the county of
San Diego, as is done in the Open Policing Tutorial mentioned
above. You will have to clean the 'race/ethnicity codes' to join the
two sources.

If you are feeling ambitious, attempt to compute stop-rates by Police
service area  using a spatial join. For this you will need to download
the [Police Service Area
Shapefiles](https://data.sandiego.gov/datasets/police-beats/) and the
[2010 Census Block Shapefiles](https://www.nhgis.org/user-resources/data-availability#gis-files), as well as the [census demographic
information](https://data2.nhgis.org/main) by census block.

The shapefiles contain polygons delineating boundaries for the
geographical areas. These shapefiles can be read into dataframes using
the `geopandas` library (see this [geopandas
tutorial](https://medium.com/thoughtful-data-science/geopandas-an-introduction-c544a352c662)
for an introduction). As well as the more comprehensive [python +
gis](https://automating-gis-processes.github.io/CSC18/lessons/L2/geopandas-basics.html)
tutorials.

`geopandas` allows one to do [spatial
joins](http://geopandas.org/reference/geopandas.sjoin.html), where two
rows are joined when their boundaries intersect (or alternatively, one
is contained in the other). Try joining census data to police service
area this way. 

A few questions to keep in mind when attempting such a join:
1. Is 'intersection' or 'contained in' more appropriate? What are
   their relative merits?
2. If you use intersection, expect a many-to-many join (why?). Which
   rows do you keep?
3. How do you compute the total population of police service area with
   such a join?

## Discussion questions from reading and analysis

* Interpret the statistics you are calculating! What do you see?
* What data cleaning was necessary to compute the statistics? (Keep
  this code for reuse).
* When computing the stop-rates by race in SD city, what are the ways in which the estimate of the denominator is incorrect? What are some ways you might approach fixing these problems?
* What are the weaknesses of drawing (causal) conclusions from
  your descriptive statistics (confounding). Focus on conclusions
  drawn in *Suspect Citizens*.
* What are you first impressions about the Veil of Darkness technique?

### Participation Submission

Answer the questions on this
[Form](https://forms.gle/C2Aa2U1HssBsX4E78) by the Tuesday morning
before section.
