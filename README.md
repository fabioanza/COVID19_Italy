# COVID19_ITA
Data analysis on the Coronavirus epidemic that is happening in Italy - Comments and suggestions are more than welcome!


The source of the the data will be the website http://opendatadpc.maps.arcgis.com/apps/opsdashboard/index.html#/b0c68bce2cce478eaac82fe38d4138b1

The data is availbe in CSV format at the public repository here

Regional Data
https://github.com/pcm-dpc/COVID-19/tree/master/dati-regioni
National Data
https://github.com/pcm-dpc/COVID-19/tree/master/dati-andamento-nazionale

# How to use it?
There are three Jupyter Notebook files:
- COVID19_CompartmentalModels.ipynb

This file contains a brief explanation of what are the Compartmental Models used in modeling the spread of infectious diseases. It is based on the standard SIR Model and on the variation necessary to model the spread of COVID19, the SIS model. This is presented using the language of population dynamics, where the SIS model is called the Verhulst Model or the Logistic Growth

- COVID19_Italy_DataAnalysis.ipynb

This file contains the code to perform a least-square fit on the available data on Italy. It performs the fit and stores the outcome in the folder Fit_Data. It contains no output. You can simply run it and then close it.

- COVID19_Italy_Plots.ipynb

This file contains the code to visualize, data, the corresponding fit and save your plot. Two functions will be used to look at the data: **plot_fit_by_indicator** and **plot_fit_by_region**. The notebook contains the explanation about how to use these two functions. Here we simply report, at readers' convenience, the indicators you will be able to look at are

Available indicator are:
- region = Name of the italian region of interest - Use 'Italia' to look at national data
- total_admitted = Total number of people checked in at the Hospital
- intensive_care = Number of patients in intensive care
- checked_in = Number of patients at the Hospital, but not in intensive care
- home_isolation = Number of positive cases in isolation at home
- currently_positive = Daily count of confirmed cases
- new_positives = Number of daily new positive cases
- recovered = Daily number of people who left the hospital because of healing
- deceased = Total count of deceased people
- total_cases = Total records of people with COVID19
- swabs = Number of COVID19 tests that have been done

# What else is in it?

- Two figures which will be loaded into COVID19_CompartmentalModels.ipynb to explains some basic concepts: Overview.png and SIR_Graphic.png
- A folder Fit_Data where the output of COVID19_Italy_DataAnalysis.ipynb will be stored in the form of .CSV files. These files are organized in two sub-folders: Indicators, Regions, where the respective data are stored.
- A folder Plots where the output of COVID19_Italy_Plots.ipynb will be saved, in the form of a .PNG file. These plots are organized in subfolders, consistently with the way the data is analized: ByRegion and ByIndicator
