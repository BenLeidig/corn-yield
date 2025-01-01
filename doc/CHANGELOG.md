# Changelog

----------------------------------------------------------------------------------------------------------------------
## [YYYY-MM-DD] - Contributor Name
### Commit Message (lower case)
- **Description:** A brief explanation of the change.
- **Details:** More detailed information, if necessary (e.g., reasons for the change, affected files, methods, or NA).
----------------------------------------------------------------------------------------------------------------------

## [2024-10-15] - Benjamin Leidig
### established repo structure
- **Description:** Created the repository structure in accordance with our established team guidelines (found here: https://docs.google.com/document/d/1PKLeBzV-NbG2x-MXYqghzYJAg18T88Vd7VJBzXDfFPA/edit?usp=sharing)
- **Details:** Created `doc/changelog.txt`, `results/`, `src/`, `LICENSE.md`, and `requirements.txt`.

## [2024-10-15] - Benjamin Leidig
### cleaned time series variables
- **Description:** Cleaned each of the variables used in the time series analysis part of project and checked for NaN values.
- **Details:** Created `src/time-series/` to contain all source files pertaining to the time series analysis. Also created `src/time-series/wrangling.ipynb` for all time series-related data wrangling. Made sure all variables are formatted correctly and contain only information useful for the purpose of the project. Also created print loops to display NaN values.

## [2024-10-17] - Benjamin Leidig
### updated data
- **Description:** Uploaded and changed structure of data.
- **Details:** Data is now structured according to state by the top six corn producers. All of data is now time series.

## [2024-10-17] - Joshua Lee
### test
- **Description** Git pull test.
- **Details** Git pull error. Test required.

## [2024-10-18] - Ryan Sponzilli
### finished applications cleaning
- **Description:** Cleaned state/application.csv for all states.
- **Details:** Kept relevant columns, grouped by `domain` and aggregated with `sum`, pivoted on `domain`, and cleaned up column names, types and formatting. Output file is in `data/all/processed`.

## [2024-10-18] - Benjamin Leidig
### finsihed temp, precip, pdsi cleaning
- **Description:** Cleaned {state}/raw/{month}-[avg-temp/precipitation/pdsi].csv for all states and months.
- **Details:** Concatenated all {month}-[avg-temp/precipitation/pdsi].csv into one CSV in ../data/all/processed/avg-temp-precipitation-pdsi.csv organized by `year` and `state` using loops, comprehensions, and itertools.

## [2024-10-20] - Max Zhang
### illinois price-received processing
- **Description:** filtered the raw Illinois price-received file per requirements.
- **Details:** NA.

## [2024-10-21] - Benjamin Leidig
### uploaded population data
- **Description:** Added the historical population data for Indiana, Iowa, Minnesota, Missouri, and Nebraska.
- **Details:** NA.

## [2024-10-21] - Benjamin Leidig
### uploaded state area data
- **Description:** Added `data/all/raw/state-area.csv`, which contains the land area (square miles) of every US state.
- **Details:** NA.

## [2024-10-21] - Benjamin Leidig
### created population-density.csv
- **Description:** Added `data/all/processed/population-density.csv`, which contains the population density of each state through time.
- **Details:** Used loops and itertools to make `population-density.csv`, organized by `year` and `state` with land area and population data from Kaggle and Macrotrends, respectively.

## [2024-10-21] - Chavosh Khazeni
### minnesota price-received processing
- **Description:** filtered the raw Minnesota price-received file per requirements.
- **Details:** NA.

## [2024-10-22] - Ryan Sponzilli
### finished applications cleaning
- **Description:** Cleaned moisture.csv for all states.
- **Details:** Kept relevant columns, pivoted on `Data Item`, grouped by `month`, computed `topsoil score` and `subsoil score`, and cleaned up column names, types and formatting. Output file is in `data/all/processed`.

## [2024-10-22] - Joshua Lee
### indiana price-received processing
- **Description:** filtered the raw Indiana price-received file per requirements.
- **Details:** NA.

## [2024-10-24] - Max Zhang
### illinois yield.csv processing
- **Description:** filtered the raw Illinois yield file based on grain/silage and columns of interest.
- **Details:** NA.

## [2024-10-24] - Ryan Sponzilli
### did price-received and yield for nebraska and missouri
- **Description:** cleaned price-received and yield for nebraska and missouri
- **Details:** NA.

## [2024-10-24] - Chavosh Khazeni
### minnesota yield.csv procesing
- **Description:** filtered the raw Minnesota yield file based on grain/silage and columns of interest.
- **Details:** NA.

## [2024-10-24] - Max Wong
### iowa yield.csv procesing
- **Description:** filtered the raw Iowa yield file based on grain/silage and columns of interest.
- **Details:** NA.

## [2024-10-24] - Benjamin Leidig
### created price-received.csv
- **Description:** Added `data/all/processed/price-received.csv`, which contains the price received and lagged price received of each state through time.
- **Details:** Used loops to make `price-received.csv`, organized by `year` and `state`.

## [2024-10-27] - Joshua Lee
### minnesota yield.csv procesing
- **Description:** filtered the raw Indiana yield file based on grain/silage and columns of interest.
- **Details:** NA.

## [2024-10-28] - Benjamin Leidig
### created april-november-avg-temp-precipitation.csv and yield.csv
- **Description:** Added `data/all/processed/yield.csv`, which contains the grain and silage yield of each state per year. Also added `data/all/processed/april-november-avg-temp-precipitation.csv`, which contains the average temperature from April through November of each state per year.
- **Details:** Used itertools, loops, and comprehensions to create CSVs.

## [2024-10-29] - Benjamin Leidig
### improved dataset creation algorithms
- **Description:** Changed dataset creation algorithms for `april-november-avg-temp-precipitation.csv`, `avg-temp-precipitation-pdsi.csv`, `population-density.csv`, `price-received.csv`, and `yield.csv` to use the .map() function instead.
- **Details:** Algorithms no longer use itertools method, improving speed and ensuring consistency. Also fixed the `avg-temp-precipitation-pdsi.csv` to include measures separately for each month.

## [2024-10-29] - Benjamin Leidig
### fixed population-density.csv
- **Description:** Fixed the `population-density.csv` after breaking its algorithm in the last push.
- **Details:** NA.

## [2024-10-29] - Benjamin Leidig
### added yearly average pdsi
- **Description:** Added yearly average PDSI into `april-november-avg-temp-precipitation.csv`, and changed the dataset name to `april-november-avg-temp-precipitation-pdsi.csv`.
- **Details:** NA.

## [2024-10-30] - Benjamin Leidig
### added dirty.csv and yearly/monthly variants
- **Description:** Added `dirty.csv` which contains all variables in one dataset, uncleaned.
- **Details:** Also created `yearly-dirty.csv` and `monthly-dirty.csv`, which are the same as `dirty.csv` but only yearly or monthly variables, respectively. Variables `subsoil-score` and `topsoil-score` are yet to be included.

## [2024-10-30] - Ryan Sponzilli
### fixed moisture
- **Description:** Reformatted mositure.csv into correct layout.
- **Details:** Removed all value columns except `topsoil score` and `subsoil score` and then pivoted on `month` and renamed columns.

## [2024-10-30] - Ryan Sponzilli
### fixed bug that missed november in moisture cleaning
- **Description:** Fixed bug that missed november in moisture cleaning.
- **Details:** NA.

## [2024-10-30] - Benjamin Leidig
### updated dirty.csv
- **Description:** Updated `dirty.csv` with the fixed `moisture.csv` and added `april-november-moisture.csv`.
- **Details:** NA.

## [2024-10-30] - Benjamin Leidig
### cleaned data
- **Description:** Used linear interpolation to clean all missing values.
- **Details:** Split data into 'yearly' and 'monthly' groups. Then, split each group into sub-groups starting from 1919 or 1995 with variables that are available accordingly. Used linear interpolation to clean each dataset, and exported to `data/final`.

## [2024-11-02] - Ryan Sponzilli
### updated README
- **Description:** Added information on datasets.
- **Details:** NA.

## [2024-11-03] - Ryan Sponzilli
### updated README
- **Description:** Added information on variables.
- **Details:** NA.

## [2024-11-04] - Benjamin Leidig
### imputations eda
- **Description:** Created basic EDA visualizations of imputed values for moisture scores.
- **Details:** NA.

## [2024-11-05] - Benjamin Leidig
### created boxplots and histograms
- **Description:** Created basic EDA visualizations, boxplots and histograms for every numerical explanatory variable.
- **Details:** NA.

## [2024-11-06] - Benjamin Leidig
### saved eda pngs to results
- **Description:** Saved boxplots, histograms, heatmaps, and imputation graphs as PNG files in `../results`.
- **Details:** NA.

## [2024-11-07] - Benjamin Leidig
### added correlation visualizations
- **Description:** Saved correlation scatterplots as PNG files in `../results`. Also, optimized the boxplot and histogram generating algorithms.
- **Details:** NA.

## [2024-11-09] - Benjamin Leidig
### normalization and basic svr
- **Description:** Normalized the explanatory variables of `df_monthly_1919` and created a basic SVR.
- **Details:** Model yielded high R<sup>2</sup> as well as a high RMSE (not great results). Aside, also added a ECDF line over each variable histogram.

## [2024-11-13] - Ryan Sponzilli
### added lagged moisture columns
- **Description:** Added lagged moisture columns.
- **Details:** NA.

## [2024-11-13] - Ryan Sponzilli
### made some graphs
- **Description:** Made some graphs in `ryan-eda.ipynb`.
- **Details:** Made a yield vs year plot by state for both grain and silage.

## [2024-11-16] - Benjamin Leidig
### svr modeling
- **Description:** Explored SVR models with normalized and lagged variaels.
- **Details:** Used RandomizedSearchCV to ideal SVR models.

## [2024-11-16] - Benjamin Leidig
### added lagged csvs
- **Description:** Created `monthly/yearly-1919/1995-lag.csv`.
- **Details:** NA.

## [2024-11-17] - Benjamin Leidig
### updated readme
- **Description:** Updated the README.md.
- **Details:** Also, did some PCA work that will be expanded upon later.

## [2024-11-18] - Benjamin Leidig
### pca modeling
- **Description:** Created `pca.ipynb`, where PCA is done and performance of different datasets is reviewed.
- **Details:** It was found that a model trained on a dataset with only the top ten variables with the highest cumulative loadings had statistically significant higher performance that a model trained on a PCA transformed dataset.

## [2024-11-19] - Benjamin Leidig
### changed data structure and modeling
- **Description:** Changed the "final" datasets to be just `1919.csv` and `1995.csv`. Also, finalized PCA model selection for `1919.csv` dataset and added code comments.
- **Details:** It was found that the previous conclusion was inaccurate--a model trained using the PCs has a much better performance than a model trained on the top variables with the highest cumulative loadings.

## [2024-11-19] - Ryan Sponzilli
### random forest model
- **Description:** Looked into a random forest model.
- **Details:** Tested various numbers of features and used 5-fold cross validation to find the model with the highest R^2.

## [2024-11-19] - Benjamin Leidig
### svr model visualizations
- **Description:** Added ECDF line to Scree Plot and an Actual vs. Predicted plot for the PCA SVR model.
- **Details:** NA.

## [2024-11-20] - Benjamin Leidig
### xgboost model optimization
- **Description:** Added XGBoost model optimization and basic model comparisons visualizations.
- **Details:** Used `RandomizedSearchCV()` in the exact same manner as for the SVR model.

## [2024-11-21] - Benjamin Leidig
### finished lin mod
- **Description:** Added a linear regression model optimization cell and added its performance to the comparison line plot.
- **Details:** It was found that a linear regression model (traditional, alpha=0, L1 Ratio=NaN) had the lowest RMSE. All fitted linear regression models had very similar $R^2$ scores.

## [2024-11-21] - Benjamin Leidig
### organized wrangling.ipynb
- **Description:** Moved all wrangling processes to a single Jupyter Notebook, `wrangling.ipynb`, and added a table of contents.
- **Details:** NA.

## [2024-11-25] - Benjamin Leidig
### added state forecasts
- **Description:** Added state forecast graphs for the best model (linear regression model).
- **Details:** NA.

## [2024-11-25] - Benjamin Leidig
### added slope interpretations
- **Description:** Added slope importance interpretations in `modeling.ipynb` and corrected the heatmaps in `wrangling.ipynb`.
- **Details:** NA.

## [2024-11-26] - Benjamin Leidig
### improved model visualizations
- **Description:** Added each models' predictions to the stately predictions graphs and their respective confidence intervals.
- **Details:** NA.

## [2024-12-02] - Benjamin Leidig
### fixed visualizations
- **Description:** Tidied some visualizations for improved appearance on the presentation.
- **Details:** NA.

## [2024-12-03] - Benjamin Leidig
### added reduced model
- **Description:** Using variable importance measures, created an lr model with the top 6 most importance features.
- **Details:** NA.

## [2024-12-03] - Ryan Sponzilli
### graphs and ci %
- **Description:** Modified grain yield graph for presentation. Calculated percent of actual data witin CI.
- **Details:** NA.

## [2024-12-03] - Benjamin Leidig
### minor fix to ci
- **Description:** NA.
- **Details:** NA.

## [2024-12-03] - Benjamin Leidig
### xlabel fix to `performance-vs-n-variables.png`
- **Description:** NA.
- **Details:** NA.

## [2024-12-03] - Benjamin Leidig
### minor graph fixes
- **Description:** NA.
- **Details:** NA.

## [2024-12-05] - Benjamin Leidig
### readme.md changes
- **Description:** Added some information on population density in the `README.md`.
- **Details:** NA.