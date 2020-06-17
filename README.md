# nyc-fare-evasion
Repository for our data, notebooks and figures for [https://nyc-fare-evasion.csail.mit.edu/](https://nyc-fare-evasion.csail.mit.edu/)

# Data
The data sets to complete the entire project are in the "data" subdirectory except the raw arrests data which can be found [here](https://data.cityofnewyork.us/Public-Safety/NYPD-Arrests-Data-Historic-/8h9b-rp9u).

If you want to cut to the chase and examine our dataset of subway fare evasion arrests look no further than the "arrests_assigned_250m.csv" this file contains all arrests within 250m of a subway stop. The locations of those subway stops are found in "SUBWAY_STATIONS.csv". The station usage data during 2010-2018 can be found in the "turnstile" subdirectory. We've helpfully labeled that data with the same station id column from "SUBWAY_STATIONS.csv" and the arrests data which is the "objectid" column. This column should be used to combine datasets.

# Notebooks
If you wish to recreate the analysis from scratch, the notebooks are intended to be used in this manner:

First:

	Arrest data filtering -> fare evasion arrests
	Assign arrests to stations -> arrests at each station

Then:

	Turnstile data cleaning -> gets and cleans turnstile data from the MTA

Next:

	Merge arrests and turnstile swipes -> combine turnstile data and arrests at stations

Finally:
	
	Perform data analysis using the other notebooks
