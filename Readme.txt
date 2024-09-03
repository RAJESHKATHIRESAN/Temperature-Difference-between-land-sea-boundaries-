<<<<<<< HEAD
Overview of NetCDF files:

->HadSST.4.0.1.0 (The Hadley Centre Sea Surface Temperature Dataset) dataset spans from 1850 to present, providing the gridded temperature anomalies at spatial resolution of 5-degree latitude by 5-degree longitude grid. This dataset is created by situ measurements of SST from ships and buoys, rejecting measurements that fail quality checks, converting measurements to anomalies, and then making a robust mean on a monthly grid. The SST data from 1850 to 2014 come from release of 3.0.0 of the ICOADS (International Comprehensive Ocean-Atmosphere Data Set) and from 2015 data taken from ICOADS 3.0.1, augmented with drifting buoy observations from 2016.

->CRUTUM.5.0.2.0 dataset runs from 1850 to present and it includes the gridded temperature anomalies at spatial resolution of 5 degrees. This data is collaborated with the Climatic Research Unit at the University of East Anglia, the Met Office Hadley Centre, and the National Centre for Atmospheric Science. Standard and alternative versions of CRUTUM temperature anomalies are based on monthly- mean temperature records from 10,639 weather stations, in these 7,893 records are used to create the gridded dataset. 

->HadNMAT.2.0.1.0 (The Hadley Centre and National Oceanography Centre Night Marine Air Temperature) dataset spans from 1880 to 2010 with monthly fields of night marine air temperature anomalies on a 5-degree latitude by 5-degree longitude grid. The NMAT data version 2.5 from the ICOAD dataset. HadNMAT2 was created using the situ measurements of marine air temperature on board ships between one hour after sunset and one hour before sunrise. Bias corrections reduce the influence of changes in deck height and non-standard thermometer exposure. 

->The Global Surface Air Temperature Dataset - MAT (GloSATMAT) spans from 1781 to 2021,
providing gridded marine air temperature anomalies at a 5-degree spatial resolution. This dataset includes variables such as temperature anomalies (tas), time, latitude, and longitude, offering a comprehensive view of marine air temperature changes over a long historical period, particularly in the lower boundary layer of the atmosphere over the oceans. GloSATMAT_filled_masked and GloSATMAT_2.4.0.0 (unfilled version of GloSATMAT dataset) provides an overview of marine air temperature anomalies across a long historical period. 

->GLOSATLAT_5.0.1.3 (The Global Surface Air Temperature) offers a comprehensive view of global land and sea surface temperature anomalies from 1781 to 2021. This dataset includes variables such as land and sea surface temperature anomalies (tas), time, latitude, and longitude, all at a 5-degree spatial resolution, providing a broad perspective on global temperature changes over an extensive period. It is built on CRUTUM and provides a broader view on temperature changes in the globe over a long period.

Overview of the ipynb files:

This Folder contains a series of Jupiter notebooks designed to analyze the temperature anomalies and related climate data across different time periods. All the datasets are in netCDF format, and the analyses involve statistical methods, linear regression analysis, and various visualization techniques. The primary focus is on comparing temperature-related coefficients across different periods, identifying outliers, and performing spatial and statistical analyses.

Notebooks Included:

Crutum VS Hadnmat 1970-1990 and 1990-2010
GlosatLAT vs GloSATMAT Filled 1961-1990 and 1991-2020
GlosatLAT vs GloSATMAT Unfilled 1961-1990 and 1991-2020
Hadsst and Crutum 1961-1990 and 1991-2020

Libraries Used:

1. pandas: For data manipulation and analysis.
2. NumPy: For numerical operations.
3. matplotlib.pyplot: For plotting and visualizations.
4. cartopy.crs: For map projections and spatial visualizations.
5. netCDF4: For reading and handling netCDF data files.
6. scipy.stats.pearsonr: For statistical correlation analysis.
7. statsmodels.api: For performing OLS regression analysis.

Key Sections Across Notebooks:

Data Reading and Preparation:

-> Functions to read and handle netCDF data files.
-> Function to reduce the grid size from 5 degree to 10 degree to make datasets more manageable and suitable for analysis.

Coefficient Calculation:

->Calculating the coefficients values A, B, C of the equation 2 from Chan et al.,(2023) through OLS regression models. Separate analyses for different time periods.

Outlier Detection and Removal:

->Statistical methods  Z score and IQR are used to identify and removing outliers from the coefficient values before analysis.

Visualization Techniques:

->Scatterplots, spatial plots to visually assess the distribution of coefficient values.

->Latitudinal boxplots with median values to analyze temperature distribution by latitude.

Statistical Pearson Correlation Analysis:

->Calculating the Pearson correlation coefficient values of A, B, C for all dataset relations of SSTs and SATs between different time periods.

Key Functions:

->read_nc: Reads netCDF files and loads the data into a manageable format.

->reduce_grid_size: Reduce the grid size from 5 degree to 10 degree to make datasets more manageable and suitable for analysis.

->series_from_monthly_means: Generates time series data from monthly mean values.

->series_from_monthly_means_incomplete: Handles incomplete monthly data and generates series.

->identify_outliers: Identifies outliers within the data using statistical methods.

->remove_outliers: Removes the identified outliers to clean the dataset.

->scatter_plot_coefficients: Creates scatterplots to visualize coefficient relationships.

->plot_coefficient_spatially: Plots coefficients spatially on a map to observe geographical trends.

->plot_custom_boxplot_with_medians: Creates boxplots with median values for detailed distribution latitudinal analysis.

->calculate_pearson_correlation: Computes Pearson correlation between two sets of coefficient values from different time periods.


Usage:

These notebooks and datasets are intended for researchers and analysts working on climate data. Before running the notebooks, ensure that all necessary libraries are installed and that the netCDF data files are available in the appropriate directories.

Conclusion:

Each dataset and ipynb in this folder serves a specific purpose in the analysis of climate data. By comparing different datasets of SSTs with SATs across various time periods contribute to a robust framework for evaluating historical temperature trends and improving the understanding of climate variability.



=======
Overview of NetCDF files:

->HadSST.4.0.1.0 (The Hadley Centre Sea Surface Temperature Dataset) dataset spans from 1850 to present, providing the gridded temperature anomalies at spatial resolution of 5-degree latitude by 5-degree longitude grid. This dataset is created by situ measurements of SST from ships and buoys, rejecting measurements that fail quality checks, converting measurements to anomalies, and then making a robust mean on a monthly grid. The SST data from 1850 to 2014 come from release of 3.0.0 of the ICOADS (International Comprehensive Ocean-Atmosphere Data Set) and from 2015 data taken from ICOADS 3.0.1, augmented with drifting buoy observations from 2016.

->CRUTUM.5.0.2.0 dataset runs from 1850 to present and it includes the gridded temperature anomalies at spatial resolution of 5 degrees. This data is collaborated with the Climatic Research Unit at the University of East Anglia, the Met Office Hadley Centre, and the National Centre for Atmospheric Science. Standard and alternative versions of CRUTUM temperature anomalies are based on monthly- mean temperature records from 10,639 weather stations, in these 7,893 records are used to create the gridded dataset. 

->HadNMAT.2.0.1.0 (The Hadley Centre and National Oceanography Centre Night Marine Air Temperature) dataset spans from 1880 to 2010 with monthly fields of night marine air temperature anomalies on a 5-degree latitude by 5-degree longitude grid. The NMAT data version 2.5 from the ICOAD dataset. HadNMAT2 was created using the situ measurements of marine air temperature on board ships between one hour after sunset and one hour before sunrise. Bias corrections reduce the influence of changes in deck height and non-standard thermometer exposure. 

->The Global Surface Air Temperature Dataset - MAT (GloSATMAT) spans from 1781 to 2021,
providing gridded marine air temperature anomalies at a 5-degree spatial resolution. This dataset includes variables such as temperature anomalies (tas), time, latitude, and longitude, offering a comprehensive view of marine air temperature changes over a long historical period, particularly in the lower boundary layer of the atmosphere over the oceans. GloSATMAT_filled_masked and GloSATMAT_2.4.0.0 (unfilled version of GloSATMAT dataset) provides an overview of marine air temperature anomalies across a long historical period. 

->GLOSATLAT_5.0.1.3 (The Global Surface Air Temperature) offers a comprehensive view of global land and sea surface temperature anomalies from 1781 to 2021. This dataset includes variables such as land and sea surface temperature anomalies (tas), time, latitude, and longitude, all at a 5-degree spatial resolution, providing a broad perspective on global temperature changes over an extensive period. It is built on CRUTUM and provides a broader view on temperature changes in the globe over a long period.

Overview of the ipynb files:

This Folder contains a series of Jupiter notebooks designed to analyze the temperature anomalies and related climate data across different time periods. All the datasets are in netCDF format, and the analyses involve statistical methods, linear regression analysis, and various visualization techniques. The primary focus is on comparing temperature-related coefficients across different periods, identifying outliers, and performing spatial and statistical analyses.

Notebooks Included:

Crutum VS Hadnmat 1970-1990 and 1990-2010
GlosatLAT vs GloSATMAT Filled 1961-1990 and 1991-2020
GlosatLAT vs GloSATMAT Unfilled 1961-1990 and 1991-2020
Hadsst and Crutum 1961-1990 and 1991-2020

Libraries Used:

1. pandas: For data manipulation and analysis.
2. NumPy: For numerical operations.
3. matplotlib.pyplot: For plotting and visualizations.
4. cartopy.crs: For map projections and spatial visualizations.
5. netCDF4: For reading and handling netCDF data files.
6. scipy.stats.pearsonr: For statistical correlation analysis.
7. statsmodels.api: For performing OLS regression analysis.

Key Sections Across Notebooks:

Data Reading and Preparation:

-> Functions to read and handle netCDF data files.
-> Function to reduce the grid size from 5 degree to 10 degree to make datasets more manageable and suitable for analysis.

Coefficient Calculation:

->Calculating the coefficients values A, B, C of the equation 2 from Chan et al.,(2023) through OLS regression models. Separate analyses for different time periods.

Outlier Detection and Removal:

->Statistical methods  Z score and IQR are used to identify and removing outliers from the coefficient values before analysis.

Visualization Techniques:

->Scatterplots, spatial plots to visually assess the distribution of coefficient values.

->Latitudinal boxplots with median values to analyze temperature distribution by latitude.

Statistical Pearson Correlation Analysis:

->Calculating the Pearson correlation coefficient values of A, B, C for all dataset relations of SSTs and SATs between different time periods.

Key Functions:

->read_nc: Reads netCDF files and loads the data into a manageable format.

->reduce_grid_size: Reduce the grid size from 5 degree to 10 degree to make datasets more manageable and suitable for analysis.

->series_from_monthly_means: Generates time series data from monthly mean values.

->series_from_monthly_means_incomplete: Handles incomplete monthly data and generates series.

->identify_outliers: Identifies outliers within the data using statistical methods.

->remove_outliers: Removes the identified outliers to clean the dataset.

->scatter_plot_coefficients: Creates scatterplots to visualize coefficient relationships.

->plot_coefficient_spatially: Plots coefficients spatially on a map to observe geographical trends.

->plot_custom_boxplot_with_medians: Creates boxplots with median values for detailed distribution latitudinal analysis.

->calculate_pearson_correlation: Computes Pearson correlation between two sets of coefficient values from different time periods.


Usage:

These notebooks and datasets are intended for researchers and analysts working on climate data. Before running the notebooks, ensure that all necessary libraries are installed and that the netCDF data files are available in the appropriate directories.

Conclusion:

Each dataset and ipynb in this folder serves a specific purpose in the analysis of climate data. By comparing different datasets of SSTs with SATs across various time periods contribute to a robust framework for evaluating historical temperature trends and improving the understanding of climate variability.



>>>>>>> eef3a5972340e19468a7afff237c15f3399e505d
