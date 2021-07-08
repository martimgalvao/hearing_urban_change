# Hearing Urban Change

Using noise incident reports from 311 noise complaints from [NYC Open Data](https://data.cityofnewyork.us/Social-Services/311-Noise-Complaints/p5f6-bkga/data) and observed rent index data from [Zillow Research](https://www.zillow.com/research/data/), we can explore how correlation between noise incident reports and observed rent index can be used as as an indicator of urban change in New York City neighborhoods.

First, we group the available data (from 2014 to 2021) by zip code and remove all data after December 2019 to eliminate abnormal market behavior during the pandemic.

Then, for each zip code, we use the number of noise incident reports per month and the observed rent index of that month to determine correlation.

After discarding zip codes with a p > 0.05 and an r < 0.8, we are left with no significant correlations.

Because the number of noise incidents reported exhibits regular fluctuations based on the time of year, we can also examine this same correlation on a yearly timescale to see if our accuracy improves.

Running the same correlation calculation by year for 2014-2019, we get a list of 20 zip codes with a p < 0.05 and r > 0.8.

A few examples:

<p align="center">
  10030 (Harlem) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_10030.png" />
</p>

<p align="center">
  10034 (Inwood) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_10034.png" />
</p>

<p align="center">
  11201 (Downtown Brooklyn) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_11201.png" />
</p>

<p align="center">
  11206 (East Williamsburg) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_11206.png" />
</p>

<p align="center">
  11221 (Bushwick) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_11221.png" />
</p>

While rent tends to trend upwards, by plotting the observed rent index and number of noise incident reports over time we can see how certain neighborhoods seem to experience a corallated increase in both. If we compare the selected zip codes to areas categorized as being in some state of gentrification by the [Urban Displacement Project](https://www.urbandisplacement.org/maps/ny), the results seem to accurately depict areas of rapid urban change in New York City. 

To better understand these relationships, we can also visualize the 20 significant zip codes on a map:

<p align="center">
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/year_p_map.png" />
</p>

Although the initial results of this study are promising, more data would help to better understand the relationship between noise and urban change in New York City, specifically around the question of what qualifies as 'noise'. Future iterations of this project will incorporate categorized and geo-tagged data of city sounds to compare the frequency of noise sources such as sirens, screeching tires, loud music, jackhammers and the like to the number of noise incidents reported in the area.

A pre-labeled dataset such as NYU's Sound of New York City Urban Sound Tagging ([SONYC-UST](https://wp.nyu.edu/sonyc/)) dataset will be useful in this next phase, as will geo-tagged audio files from publicly available sources such as [Freesound](https://freesound.org). The latter will require the development of an audio event classifier, likely using [Librosa](https://librosa.org), to recognize various categories of noise present in the recordings.
