# Zungailia_Davidson_McClaugherty
Final Project for EDA


Names: Isabel Zungailia, Kelly Davidson, & Megan McClaugherty

Course Project Information:

Analysis of Soil Moisture and Precipitation Trends in the Coweeta Basin LTER
  The Coweeta Basin Long Term Ecological Research (LTER) site is deemed one of the oldest continuous environmental studies in North America. It is managed by the USDA Forest Service in collaboration with the University of Georgia. This site is located in the southern portion of the Appalachian Mountains and is primarily composed of deciduous forest.

# Zungailia_Davidson_McClaugherty


## Summary

This repository was developed for our final project in Environmental Data Analytics (ENV 872). The GitHub repository wascreated at the beginning of the project to serve as the workspace between collaborators. The repository contains folders for data (raw and processed), code and output. Separate files were created for the various components of the analysis. The file names include: (1) Data Processing and Wrangling, (2) Data Exploration, and (3) Data Analysis. The team members have made sure to commit and push changes following a work session, and have communicated closely to avoid merge conflicts associated with working on the documents simultaneously.

The goal of this analysis was to use skills that we have learned throughout the semester to generate and answer a specific research question. This investigation was intended to analyze trends in soil moisture throughout the Coweeta Basin, and we used soil moisture data from four sites (at four different elevations) to explore our research questions. In addition to soil moisture, we decided to include precipitation into our analysis to explore the relationship between these two variables. 

Our main research question was the following: Has soil moisture in the upper 30 cm increased or decreased in Coweeta Basin from 2000 to 2013 in each of the four research sites?

Other questions that were explored include: 
    Which sites experienced the greatest change in soil moisture over time?
    What is the impact of elevation on soil moisture?
    Is there a relationship between soil moisture and precipitation that can be observed these four study sites?

Null Hypothesis A: There was no change in soil moisture in the upper 30 cm from 2000 to 2013.
Alternative Hypothesis A: There was a change in soil moisture in the upper 30 cm from 2000 to 2013.

Null Hypothesis B: There is no relationship between soil moisture and precipitation at the four study sites. 
Alternative Hypothesis B: There is a relationship between soil moisture and precipitation at the four study sites. 

## Investigators

Isabel Zungailia
  Student - Master's of Environmental Management at Duke University
  Ecosystem Science and Conservation Concentration
  Email: ibz@duke.edu
Kelly Davidson
  Student - Master's of Environmental Management at Duke University
  Ecosystem Science and Conservation Concentration
  Email: kelly.davidson@duke.edu
Megan McClaugherty
  Student - Master's of Environmental Management at Duke University
  Water Resources Management Concentration
  Email: megan.mcclaugherty@duke.edu

## Keywords


LTER, precipitation, soil moisture, climate, North Carolina, Coweeta, hydrology, Appalachian Mountains


## Database Information


Soil moisture data were collected from the EDI Data Portal for Coweeta LTER 
(https://portal.edirepository.org/nis/home.jsp). Coweeta LTER (248) was selected as the LTER Site and "Continuously measured forest soil moisture at four sites in the Coweeta Basin"" was selected as the dataset of interest. Accessed 11/21/22.
The following selections were downloaded: 
 * 1040_2000_2014
 * 1040.kml 
 
Precipitation data were collected from the US Forest Service Southern Research Station (https://www.srs.fs.usda.gov/coweeta/tools-and-data/). Daily precipitation data from recording rain gages (RRG) at Coweeta Hydrologic Lab, North Carolina was selected under Coweeta Datasets on the USFS Research Data Archive (https://www.fs.usda.gov/rds/archive/Catalog/RDS-2017-0031). Accessed 11/30/22.

The investigators generated four new datasets combining the monthly average precipitation with monthly average 30 cm soil moisture at the 4 sites monitored at the Coweeta LTER. 

## Folder structure, file formats, and naming conventions 

The repository contains 3 folders. The Data folder contains 3 folders: Raw (containing csv files of data downloaded from sources), Processed (wrangled datasets containing only pertinent information for analysis in csv format), and Metadata (containing a md file of relevant information about the investigators, data, and analysis.) The code folder contains three R Markdown files, one for data processing and wrangling, one for data exploration, and one for data analysis. The outpout folder contains an R Markdown file of the final project report. 


The .csv file format allows for data to be stored in a table. This file format can readily be read into RStudio in the dataframe format, a tabular data structure convenient for the purposes of our analyses. 

The Rmd file format is a file type that allows for both blocks of R code and sections of regular text. It is a useful format for running code with space for organized text descriptions that would otherwise have to be commented out for code to run smoothly.

Raw data files retained the name given by the data source. Processed data files were given more descriptive names (e.g. Coweeta Site 1 or RG6 Monthly) and contained "processed" in their file name for clarity. 

## Metadata

RAW DATA

1040_Hourly_CR10_1_2080 (Soil Moisture Dataset):

 * site→Site Code, class=integer
 * Year→Calendar year, class=integer
 * YearDay→Numerical year day (day number within the current year), class=numerical
 * Time→hour of observation, class=numeric
 * stemp05→hourly average of soil temperature 5cm below mineral soil measured every minute, class=numeric
 * Flag_stemp05→QA/QC flags for stemp05, class=character
 * stemp20→Hourly average of soil temperature 20cm below mineral soil measured every minute, class=numeric
 * Flag_stemp20→QA/QC flags for stemp20, class=character
 * atemp100→hourly average of air temperature 100 cm above ground surface measured every minute, class=numeric
 * smois30→Hourly average of soil moisture, as percent water content, measured every minute, 0-30cm below       mineral soil, class=numeric
 * Flag_smois30→QA/QC flag for smois30, class=character
 * smois60→Hourly average of soil moisture, as percent water content, measured every minute 30-60 cm below      mineral soil, class=numeric
 * Flag_smois60→QA/QC flag for smois60, class=character
 * battvolt→hourly average of battery voltage from the datalogger taken every minute, class=numeric
 * Flag_battvolt→QA/QC flag for battery voltage, class=character
 * reftemp→hourly average of datalogger panel temperature, class=numeric
 * Flag_reftemp→QA/QC flag for reftemp, class=character
 * parbot→Hourly average of PAR 2m from ground measured every minute, class=numeric
 * Flag_parbot→QA/QC flag for parbot, class=character
 * partop→Hourly average of PAR 20m from ground measured every minute, class=numeric
 * Flag_partop→QA/QC flag for partop, class=character

RG05_daily_1992_2021, RG06_daily_1936_2021, & RG31_daily_1958_2021 (precipitation datasets):
 * YEAR→Calendar year, class=integer
 * MONTH→Calendar month, class=integer
 * DAY→Calendar day, class=integer
 * RRG(*Gage Number)→amount of precipitation (units=inches), class=number


PROCESSED DATA
coweeta_site#_processed:
 * Year→Calendar year, class=integer
 * Month→Calendar month, class=integer
 * AverageMonthlySmois30: Average monthly 30 cm soil moisture as percent water content, class=numeric
 * YearMonth→Date in format YYYY-MM-DD, class=character, class=character 

Coweeta_wrangled3_processed:
 * site→site number, class=integer
 * Year→calendar year, class=integer
 * YearDay→Numerical day of year, class=integer
 * smois30→Hourly average of soil moisture, as percent water content, measured every minute, 0-30cm below       mineral soil, class=numeric
 * Date→Date in format YYYY-MM-DD, class=character
 
 RG#_Monthly_Processed: 
  * Year→Calendar year, class=integer
  * Month→Calendar month, class=integer
  * AverageMonthlyPrecip→Average monthly precipitation (inches), class=numeric
  * YearMonth→Date in format YYYY-MM-DD, class=character


## Scripts and code

Dplyr: facilitates data manipulation by using straightforward functions
Lubridate: Intuitive date-time manipulation beyond what base R offers 
Tidyverse: A suite of packages such to assist with organizing datasets and processing data
Cowplot: A ggplot2 add-on to create plot grids and enhance other plot features 
Ggplot2: A data visualization package that creates more appealing and customizable plots/graphs compared to base R
Ggpubr: an add-on for ggplot2 to add regression lines and other useful enhancements to plots 
Kendall: computes the Kendall rank correlation and Mann-Kendall trend test for time series analysis


## Quality assurance/quality control

Data collection procedures and metadata were reviewed for all of the raw datasets to ensure understanding of each of the variables and collection methods. The soil moisture dataset (1040_Hourly_CR10_1_2080) had a built-in QA/QC feature to flag for measurements outside of specified ranges which facilitated the process of identifying outliers due to error. These values were removed from our processed datasets. Rain gage datasets were also checked for precipitation amounts that seemed extreme given the locations in which the data were collected. Processed dataset files were given descriptive names followed by "_processed" to ensure clarity and raw and processed data were kept in separate folders to further minimize the possibility of confusion. The steps of the project were split into data wrangling/processing, data exploration, and data analysis files. Organizing the code in this manner minimized redundancy, ensured wrangled datasets were saved for further analysis, kept the code concise, and made it easier to identify issues. Copies of each code file were made, as well as a copy of the entire project folder in case files were lost or corrupted. Files were saved at regular intervals and changes were committed and pushed to GitHub promptly to ensure other users could access updated files without issue.
