# Team Corn Fall 2024

## Preface:

This was a team project for the Illinois Data Science Club for the Fall 2024 semester. I, along with my five team members, Ryan Sponzilli, Joshua Lee, Chavosh Khazeni, Max Wong, and Max Zhang, as well as our project lead, Danny Silverstein, contributed to this project. My teammates and I presented the final form of the project to professional data scientists in the agricultural industry to be graded in the Data Dive competition. In the end, we were selected as fourth place among twenty-five other teams.

## Overview

Our project is analyzing what factors affect corn yields in the midwest, specifically focusing on the states of Illinois, Indiana, Iowa, Minnesota, Missouri, and Nebraska.

## Datasets

### Sources

Data on crop appications was downloaded from the USDA's National Agricultural Statistics Service (NASS) for Illinois, Indiana, Iowa, Minnesota, Missouri, and Nebraska from 1990 to 2024. This dataset classified four domains of applications: Fungicide, Herbicide, Insecticide, Other, and Fertilizer. It further subdivided each domain into specific chemicals as well. For our purposes, we decided to group by the major domains. The data values are measured in lb applied per acre for each year.

Data on price received was downloaded from NASS for Illinois, Indiana, Iowa, Minnesota, Missouri, and Nebraska from 1909 to 2023. This values in this dataset represent the price received measured in dollars per bushel for each year.

Data on corn yields was downloaded from NASS for Illinois, Indiana, Iowa, Minnesota, Missouri, and Nebraska from 1866 to 2024. This dataset classifies two types of yields: Silage measured in tons per acre and grain measured in bushels per acre. Silage yield consists of the entirety of the corn plant and is used to feed livestock. Grain corn is only the kernals of corn. This dataset provides these values for each year, except prior to 1919 where only grain yields are accounted for.

Data on soil moisture was downloaded from NASS for Illinois, Indiana, Iowa, Minnesota, Missouri, and Nebraska from 1995 to 2024. This dataset contains 8 different data items for each week of each year: subsoil moisture (pct very short), subsoil moisture (pct short), subsoil moisture (pct adequte), subsoil moisture (pct surplus), topsoil moisture (pct very short), topsoil moisture (pct short), topsoil moisture (pct adequte), and topsoil moisture (pct surplus). For our purposes, we grouped the data by month and then calculated a "score value" for both subsoil and topsoil by weighting each of the 4 moisture levels.

Data on average temperature was downloaded from the National Oceanic and Atmospheric Administration's (NOAA) National Center for Environmental Information (NCEI) database. Data was dowloaded for Illinois, Indiana, Iowa, Minnesota, Missouri, and Nebraska from 1895 to 2024. Data was only downloaded for the months of April through November, and each individual data file contains values for one state and one month. The values are measured in degrees Fahrenheit and are a monthly average.

Data on average precipitation was downloaded from the NCEI database for Illinois, Indiana, Iowa, Minnesota, Missouri, and Nebraska from 1895 to 2024. Data was only downloaded for the months of April through November, and each individual data file contains values for one state and one month. The values are measured in inches of rainfall and are a monthly average.

Data on the Palmer Drought Severity Index (PDSI) was downloaded from the NCEI database for Illinois, Indiana, Iowa, Minnesota, Missouri, and Nebraska from 1895 to 2024. Data was only downloaded for the months of April through November, and each individual data file contains values for one state and one month.

Data on population density was derived from [Macrotrends](www.macrotrends.net). Data downloaded from the Macrotrends website represents historical Illinois population figures. Each record was divided by Illinois land area to derive population density over time.

### Integrated *Fit for Use* and *Tidy* Dataset Variables

`year` --> an index variable that indicates the year that the values of this observation represent.

`state` --> an index variable that indicates the state in which the values of this observation belong to.

`fungicide (lb/acre)` --> average amount of fungicide applied given in pounds per acre.

`herbicide (lb/acre)` --> average amount of herbicide applied given in pounds per acre.

`insecticide (lb/acre)` --> average amount of fungicide applied given in pounds per acre.

`other chemicals (lb/acre)` --> average amount of other chemicals applied given in pounds per acre.

`fertilizer (lb/acre)` --> average amount of fertilizer applied given in pounds per acre.

`april-nov-avg-temp` --> average temperature for the months April through November.

`april-nov-precipitation` --> total precipitation for the months April through November.

`april-nov-pdsi` --> average PDSI for the months April through November.

`population-density` --> population density in population per square mile of total land area.

`price-received` --> the price receieved in dollars per bushel.

`price-received-lagged` --> the price received in dollars per bushel for the year prior.

`grain-yield` --> total grain (kernals) measured in bushels per acre.

`silage-yield` --> total silage (whole plant, livestock feed) measured in tons per acre.

`april-nov-subsoil-score` --> average subsoil moisture score score for the months April through November.

`april-nov-topsoil-score` --> average topsoil moisture score score for the months April through November.

`{month}-avg-temp` --> the average temperature for the month of {month} in the given year.

`{month}-pdsi` --> the PDSI score for the month of {month} in the given year.

`{month}-precipitation` --> the total precipitation for the month of {month} in the given year.