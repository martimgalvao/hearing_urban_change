# Hearing Urban Change

Several studies to date have looked into the significance of noise incident reports as an indicator of gentrification in urban areas ([Vo 2018](https://www.buzzfeednews.com/article/lamvo/gentrification-complaints-311-new-york), [Misra 2018](https://www.bloomberg.com/news/articles/2018-10-18/in-new-york-city-gentrification-brings-more-311-calls)). While the research seems to suggest a connection between increased noise incident reports and gentrification, this project seeks to further investigate how changing perceptions of noise at a local level might be used to identify urban change. Using 311 noise incident reports from [NYC Open Data](https://data.cityofnewyork.us/Social-Services/311-Noise-Complaints/p5f6-bkga/data) and observed rent index data from [Zillow Research](https://www.zillow.com/research/data/), the following analyses explore whether correlation between noise incident reports and observed rent index can serve as as an indicator of urban change in New York City neighborhoods. Proposed expansions of this study, outlined in the conclusion, seek to further explore the question of what qualifies as noise in these neighborhoods through audio event analysis of geo-tagged recordings.

In the first step of this analysis, available data for both noise incident reports and observed rent index from 2014 to 2021 were grouped by zip code. Then, data after December 2019 was removed from the dataset to eliminate abnormal market behavior caused by the pandemic.

Then a correlation coefficient is generated for the relationship between the number of noise incident reports and the observed rent index of each zip code. This was first attempted using data for each month but resulted in no correlations. Upon examining the data further it appeared that noise incident reports varied depending on the time of year, so another correlation was calculated based on average yearly data.

After discarding zip codes with a p > 0.05 and r < 0.8, a list of 20 correlated zip codes remained.

A few examples:

<p align="center">
  10034 (Inwood) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/year_plot_rent_noise_output/year_plot_rent_vs_noise10034.png" />
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_10034.png" />
</p>

<p align="center">
  10457 (Bronx) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/year_plot_rent_noise_output/year_plot_rent_vs_noise10457.png" />
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_10457.png" />
</p>

<p align="center">
  10458 (Bronx) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/year_plot_rent_noise_output/year_plot_rent_vs_noise10458.png" />
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_10458.png" />
</p>

<p align="center">
  11201 (Downtown Brooklyn) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/year_plot_rent_noise_output/year_plot_rent_vs_noise11201.png" />
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_11201.png" />
</p>

<p align="center">
  11221 (Bushwick) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/year_plot_rent_noise_output/year_plot_rent_vs_noise11221.png" />
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_11221.png" />
</p>

<p align="center">
  11435 (Briarwood) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/year_plot_rent_noise_output/year_plot_rent_vs_noise11435.png" />
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/years_output/year_output_11435.png" />
</p>

While rent tends to trend upwards, by plotting the observed rent index and number of noise incident reports over time we can see how certain neighborhoods seem to experience a correlated increase in both. If we compare the selected zip codes to areas categorized as being in some state of gentrification by the [Urban Displacement Project](https://www.urbandisplacement.org/maps/ny), the results seem to accurately depict areas of rapid urban change in New York City. 

To better understand these relationships, we can also visualize the correlations of the 20 significant zip codes on a map:

<p align="center">
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/year_r_map.png" />
</p>

Although the initial results of this study are promising, more data would help to better understand the relationship between noise and urban change in New York City, specifically around the question of what qualifies as 'noise'. Future iterations of this project will incorporate categorized and geo-tagged data of city sounds to compare the frequency of noise sources such as sirens, screeching tires, loud music, jackhammers and the like to the number of noise incidents reported in the area.

A pre-labeled dataset such as NYU's Sound of New York City Urban Sound Tagging ([SONYC-UST](https://wp.nyu.edu/sonyc/)) dataset will be useful in this next phase, as will geo-tagged audio files from publicly available sources such as [Freesound](https://freesound.org). The latter will require the development of an audio event classifier, likely using [Librosa](https://librosa.org), to recognize various categories of noise present in the recordings.
