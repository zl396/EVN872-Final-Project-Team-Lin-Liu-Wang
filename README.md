# <ENV872: EDA Final Project>


## Summary

This repository holds the contents related to a Duke Nicholas School of the Environment course titled Environmental Data Analytics, taught during the Spring of 2023. The data used for our analysis consist of monthly net generation for differenct sectors from EIA. The Data file contains raw data and all processed data are stored in Processed file

## Investigators

Zhenghao Lin, Will.lin@duke.edu
Chenjia Liu, cl652@duke.edu
Shuyi Wang, Lucy.wang@duke.edu

## Keywords

renewable energy, clean energy, energy projection, Clean energy goals

## Database Information

This data set was found using EIA'S ELECTRICITY DATA BROWSER FROM https://www.eia.gov/electricity/data/browser/#/topic/0?agg=2,0,1&fuel=vvvvu&geo=000000000001&sec=g&freq=M&start=200101&end=202308&ctype=linechart&ltype=pin&rtype=s&pin=&rse=0&maptype=0 .It was originally accessed on November 16th, 2023 and later altered for analysis purposes using RStudio. Variables from the original data sets that were repetitive or not relevant for our comparative analysis were removed. The original data can be found in the Data folder, while other data sets created by the authors of this repository can be found in Processed.


## Folder structure, file formats, and naming conventions 

The raw data is stored in Data folder and in .csv format. THe processed data is stored in Processed folder in .csv format as well. The code files for different section are stored in Code folder, and are in .Rmd format.

Files within our folders were kept only if relevant to avoid cluttering up our work space. Our .Rproj file created the workspace in which we worked through creating our final report. Code files were all written using RStudio and are therefore in .Rmd for easy sharing. he final PDF for this project can be found in the Output folder. 

Files are named conventionally, using the original file name for our raw data set that is associated with the .txt file in the Data folder. Processed data is named to distinguish it between the raw dataset and all file names will be explanatory as to the contents held within the file. Each state has a independent file so the file is named using states name. 

## Metadata

| Column Name                               | Description                                      | Class   | Units                  |
|-------------------------------------------|--------------------------------------------------|---------|------------------------|
| All fuels                                 | All fuels                                        | numeric | thousand megawatthours |
| coal                                      | coal                                             | numeric | thousand megawatthours |
| petroleum liquids                          | petroleum liquids                                | numeric | thousand megawatthours |
| petroleum coke                            | petroleum coke                                   | numeric | thousand megawatthours |
| natural gas                               | natural gas                                      | numeric | thousand megawatthours |
| other gases                               | other gases                                      | numeric | thousand megawatthours |
| nuclear                                   | nuclear                                          | numeric | thousand megawatthours |
| conventional hydroelectric                | conventional hydroelectric                       | numeric | thousand megawatthours |
| other renewables                          | other renewables                                 | numeric | thousand megawatthours |
| other renewables:wind                     | other renewables:wind                            | numeric | thousand megawatthours |
| other renewables:geothermal               | other renewables:geothermal                      | numeric | thousand megawatthours |
| other renewables:biomass                  | other renewables:biomass                         | numeric | thousand megawatthours |
| biomass:wood and wood-derived fuels       | biomass:wood and wood-derived fuels              | numeric | thousand megawatthours |
| biomass:other biomass                     | biomass:other biomass                            | numeric | thousand megawatthours |
| hydro-electric pumped storage             | hydro-electric pumped storage                    | numeric | thousand megawatthours |
| other                                     | other                                            | numeric | thousand megawatthours |
| all solar                                 | all solar                                        | numeric | thousand megawatthours |
| small-scale solar photovoltaic             | small-scale solar photovoltaic                   | numeric | thousand megawatthours |
| all utility-scale solar                    | all utility-scale solar                          | numeric | thousand megawatthours |
| all utility-scale solar:utility-scale photovoltaic | all utility-scale solar:utility-scale photovoltaic | numeric | thousand megawatthours |
| all utility-scale solar:utility-scale thermal | all utility-scale solar:utility-scale thermal  | numeric | thousand megawatthours |
| Date                                      | Date                                             | Date    |     D-M-Y                |
| State                                     | State                                            |Categorical|       NA               |


## Scripts and code

Within this repository, you will find a 872 Final project.Rmd which includes all the code used to wrangle, visualize, and evaluate our research questions. This .Rmd file can be found within the Code folder.

## Quality assurance/quality control

Original data for this project was simplified and wrangled to support research questions. Our analysis primarily relies on two single-variable time series forecasts: one for electricity generated by clean energy and another for total electricity generated. However, it's worth noting that these variables may exhibit correlations or dependencies that are not considered in our current approach. Future research could explore multivariate time series models to capture potential interactions and dependencies between different types of fuels, leading to more precise forecasts.
Clean energy has experienced different rates of development over the past two decades, with drastic growth in the past 10 years and more smooth increase in the first decade. This may introduce uncertainty into our forecasts, as past data may not fully reflect future trends. 
Last, our forecasts are based on historical data, which may not account for unforeseen factors that could emerge in the future and significantly impact the development of clean energy. As new technologies, policies, and global events unfold, they may alter the trajectory of clean energy generation. Therefore, our models may not capture the full range of potential influences on future outcomes.