# Hearing Urban Change

Using noise incident reports from 311 noise complaints from NYC Open Data and observed rent index data from Zillow Research, we can explore how correlation between noise incident reportas and observed rent index can be used as as an indicator of urban change in New York City nighborhoods.

First, we group the available data (from 2014 to 2021) by zip code and remove all data after 12/2019 to eliminate abnormal market behavior during the pandemic.

Then, for each zip code, we use the number of noise incident reports per month and the observed rent index of that month to determine correlation.

After discarding zip codes with a p-value < 0.05, we are left with a list of 37 zip codes.

While rent tends to trend upwards, by plotting the observed rent index and number of noise incident reports over time we can see how certain neighborhoods seem to experience a corellated increase in both. As 

A few examples:

<p align="center">
  10026 (South Harlem) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/months_output/month_output_10026.png" style="background-color:white;" />
</p>

<p align="center">
  10031 (Sugar Hill) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/months_output/month_output_10031.png" />
</p>

<p align="center">
  10034 (Inwood) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/months_output/month_output_10034.png" />
</p>

<p align="center">
  11201 (Downtown Brooklyn) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/months_output/month_output_11201.png" />
</p>

<p align="center">
  11435 (Jamaica, Queens) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/months_output/month_output_11435.png" />
</p>

Many of these area have also seen extensive urban development during the same time period, something to be further examined in a future version of this study.

There is also one case of an inverse relationship:

<p align="center">
  10065 (Upper East Side) <br>
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/months_output/month_output_10065.png" />
</p>

Interestingly, this zip code was named 'America's Most Expensive Zip Code' by Business Insider in 2012.

Mapping the zip code p-values, we can visualize what neighborhoods are experiencing correlated increases in rent and noise reports:

<p align="center">
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/month_p_map.png" />
</p>

Because the number of noise incidents reported seems to exhibit regular fluctuations based on the time of year, we can also examine this same correlation on a yearly timescale.

Running the same correlation calculation for 2014-2019, we get a list of 20 zip codes with a p-value < 0.05.

These results seem to hone in of some of the more rapidly changing neighborhoods in New York City.

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

And again, we can visualize the zip codes with p-values < 0.05 on a map:

<p align="center">
  <img src="https://github.com/martimgalvao/hearing_urban_change/blob/main/year_p_map.png" />
</p>

Although the initial results of this study are promising, more data would help to understand the relationship between noise and urban change in New York City, specifically around the question of what qualifies as 'noise'. Future iterations of this project will incroporate categorized and geo-tagged data of city sounds, allowing us to compare the frequency of noise sources such as sirens, screeching tires, loud music, jackhammers and the like to the number of noise incident reports in the area. NYU's Sound of New York City Urban Sound Tagging (SONYC-UST) dataset will be useful in this next step.
