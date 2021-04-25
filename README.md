# Video Game Sales Data
DATA 115 Personal Dataset Project for Spring 2021

## Motivation
When I was around six-years-old I was introduced to my very first video game by my older brother which happened to be Ratchet & Clank: Up Your Arsenal on the PlayStation 2. Ever since that moment of playing my first video game on my first video game platform, I have been infatuated with various types of games on various platforms. Something that captivated me with video games was the diversity and the different types of platforms that I could play video games on. This infatuation had me producing questions regarding video games such as what is the most popular game of all time, what is the most popular video game platform of all time, and what is the most popular video game genre of all time. Since I couldn't find any metrics for video game ratings and I'm a business student, I figured total sales volume would be a great metric to measure in terms of popularity. After figuring out my research focus I investigated my questions and assumptions.

## Data Source
The data was obtained through <a href="https://www.kaggle.com/gregorut/videogamesales">Kaggle</a> which was generated by a scrape of <a href="https://www.vgchartz.com/">VGChartz</a>. The dataset contains the following fields: rank, name, platform, year, genre, publisher, NA sales, EU sales, JP sales, other sales, and Global sales. The dataset contains a total of 16,598 records that only consist of video games with sales that are greater than 100,000 copies.

## Processing Steps
I originally sourced and collected my data from Kaggle which was generated by a scrape of VGChartz. The single dataset that I obtained from my source contained enough information for me to perform analysis and to create visualizations to depict popularity of games, platforms, and genres. Although before creating visuals and performing my analysis I had steps to perform to ensure that my data was accurate. The first step in my cleaning process involved command searching through my .csv file to find any rows of data that contained NULL or N/A data, after my inital search I found that the only rows that did contain a value of N/A were in the year and publisher fields. Since my analysis was going to draw from specific fields of name, platform, and genre I decided to leave those entries in the dataset. The next step in my cleaning process included using conditional formatting in excel to highlight duplicate rows. No rows were highlighted through my conditional formatting so it was safe to assume that my dataset did not include any duplicate entries. 

After completing my cleaning processes I transformed my data to specifically display sum metrics for video game name, platform, and genre. To transform my data to depict the sum of global sales for just two fields I was focusing on (platform and genre) I created a pivot table for my .csv file on excel. The first pivot table included the platform field to be inputted into the rows area and the global sales field to be inputted into the sum of values area, from this I had a table that neatly displayed each video game platform and the total sum of global sales. From this table I created a separate .csv file and copied and pasted this data into that file called vgsalesplatform. The second pivot table included the genre field to be inputted into the rows area and the global sales field to be inputted into the sum of values area, from this I had a table that neatly displayed each video game genre and the total sum of global sales. From this table I created another separate .csv file and copied and pasted this data into that file called vgsalesgenre. After using my pivot tables I went back to the original cleaned dataset and filtered the entries according to highest global sales where I copied and pasted the top 10 entries into another file called vgsalestop10.

## Visualizations
The first visualization displays the top 10 ranking games according to global sales. The second visualization displays the global sales for video games according to each video game platform. The third visualization displays the global sales for video games according to their genre.

<img src= "https://raw.githubusercontent.com/CheweezyTy/115_personal_dataset/main/Top10VGPlot.png">
<img src="https://raw.githubusercontent.com/CheweezyTy/115_personal_dataset/main/VGPlatformPlot.png">
<img src="https://raw.githubusercontent.com/CheweezyTy/115_personal_dataset/main/VGGenrePlot.png">

The visuals help to provide physical representation to what games, platforms, and genres are most popular according to global sales.

## Analysis
In order to analyze the distribution of data for both video game platforms and video game genres I created boxplots for each field to help determine if there happened to be any outliers. Along with determining any outliers in the distribution of the data I also wanted to observe skewness of these boxplots and to see if there happens to be any symmetry among them. Below are the boxplots created for both video game platforms and video game genres:

<table>
  <tr><td><img src="https://raw.githubusercontent.com/CheweezyTy/115_personal_dataset/main/VGPlatformBoxPlot.png"></td><td><img src="https://raw.githubusercontent.com/CheweezyTy/115_personal_dataset/main/VGGenreBoxPlot.png">
</table>
  
When looking at the boxplot distribution for video game platforms in terms of global sales, you can see six outliers above the maximum. Despite the outliers, when observing for symmetry we can see that the boxplot is negatively skewed only by a little, since the median is closer towards Q3 than it is to Q1. When observing the IQR for platforms we can see a more condensed distribution, with the exception of the outliers, compared to the genres distribution.

When looking at the boxplot distribution for video game genres in terms of global sales, you can see no outliers. When observing for symmetry we can see that boxplot is negatively skewed slightly since the median is closer towards Q3 than it is to Q1. When observing the IQR for genres we can see a more broad distribution than the platforms distribution.

## Code and Materials
The raw data downloaded from the sources described in the "Data Source" section is labeled as vgsales.csv, while the .csv files generated from my processing and transformation of data is labeled as vgsalesgenre.csv, vgsalesplatform.csv, and vgsalestop10.csv. The visuals in this README.md file are labeled as Top10VGPlot.png, VGGenreBoxPlot.png, VGGenrePlot.png, VGPlatformBoxPlot.png, and VGPlatformPlot.png.
