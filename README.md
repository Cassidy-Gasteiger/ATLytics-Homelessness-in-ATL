# ATLytics-Homelessness-in-ATL
Winning submission for the 2024 ATLytics datathon, assessing homelessness trends over time in Atlanta

## Presentation File
●	Slide Deck_TeamIndigo.pdf: PPT presentation containing our analysis and visualizations, as well as links to a Tableau dashboard to further explore the data

## Code Files
●	EDA_and_Tableau_Manip.ipyn: This dataframe takes as its inputs the raw PIT and HIC data in the format shared by the ATLytics team and outputs a series of dataframes:
  ○	A time series PIT dataframe from 2007 - 2022 with indicators available across all years
  ○	A time series PIT data from from 2015 - 2022 with more detailed demographic indicators
  ○	A time series HIC dataframe from 2007 - 2022
●	It then uses those inputs to conduct EDA and create some visualizations of changes in homelessness by demographic groups across time in Atlanta
●	Finally, it creates two filterable dataframes for use in Tableau:
  ○	A PIT dataframe with filterable columns based on demographic group
  ○	An integrated HIC-PIT dataframe that joins related columns between the two datasets and calculates percentage sheltered potential for individual demographic groups based on year-round available beds

●	HIC_data_viz.ipynb: Takes the time series-formatted HIC data as an input, and uses string functions to extract information from the designation, regarding program type (e.g. ES, TH, SH), subcategory (e.g. Veteran, Youth), and whether a household has adults, childen, or both. The file filters on Atlanta area (GA-500) and ES, TH, and SH program types before proceeding to produce multiple graphs for the aforementioned designations.
●	HIC_GAvsUSA.ipyn: Takes the raw HIC data as an input, and after some manipulations, creates a time-series-formatted dataframe, showing the number of total beds in every state across the country, from 2018 until 2022, as well as the percentage (%) year-to-year change for ES, TH, and SH program types.
●	HIC_GAvsUSA_Overall_and_Unsheltered.ipyn: Takes the raw PIT data as an input, and after some manipulations, creates a time-series-formatted dataframe showing the number of overall and unsheltered homeless people per state, in every year from 2018 until 2022. Subsequently, it creates one more dataframe, showing the percentage year-to-year change in each category, for the same span.
