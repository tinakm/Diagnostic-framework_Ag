This directory includes 3 text files (cells, hydro_crop_sample_1, hydro_crop_sample_2) and 
3 folders (soil_weather, Historical, Future). The description of these files and folders are as following order:
A-cells.txt
B-hydro_crop_sample_1.txt
C-hydro_crop_sample_2.txt 
D-hydro_crop_sample_3.txt
E-soil_weather
F-Historical
G-Future
The following section briefly describes items A to F:
A- ########################################################################################
cells.txt >> contains the name of 16 locations that considered in this study, and in this data repository.
For example in this file, we do not have term "CF_1" which is in what have been used in the manuscript. Instead, it is named as "476411993_CF".

B,  C, and D- ##################################################################################
hydro_crop_sample_1, hydro_crop_sample_2, and hydro_crop_sample_3 >> are 136,000 sample sets of 33 parameters that are used in the manuscript. The first and second filse contain 45300 samples (rows) and the third file contains the rest of the samples (#45400).
E- ########################################################################################
soil_weather Folder >> contains one folder for each of the 16 locations (e.g. 476411993_CF subfolder). 
Inside each of these subfolders, there are 2 files:
Files:
"soil_file_TestCase" which is the VIC-CropSyst soil file for that location, and "data_47.65625_-119"  (data_coordinates) which is the daily historical weather data for that location.

For the cells that are selected for the future climate experiment (453911731_CCF, 461411652_CC, and 476411993_CF), there are also 3 folders inside these subfolders:
Folders:
"BNU-ESM", "MIROC5","MIROC-ESM-CHEM" which are the name of the 3 selected GCMs for the future climate scenario experiment. Each of these folders contains the daily weather data corresponding to that GCM under RCP 8.5 scenario.

F- ########################################################################################
Historical Folder >> contains 16 folders for each of the 16 locations considered in the manuscript and "Baseline" and "Best samples" folders (total of 18 folderes).
16 Folders with location's ID:
Inside each of the 16 folders, there are 12 CSV files:
"period_hydro.csv" and "period_yield.csv" contain the historical average model outputs (yield and hydrological variables) for all the samples.
"indices_yield_period_S1_ST.csv" contains total and first-order indices for 33 parameters for average historical yield.
"sobol_yield_period_S2.csv" contains the second-order interaction indices for average historical yield.
There is the same information available for average historical hydrological variables (Actual_ET, Baseflow, Soil_Evap, Soil_Moisture) with the same format as historical yield.

Baseline Folder:
Contains one CSV file for each of 16 locations based on the deterministic calibrated parameter set for the historical period that includes annual simulated yield for 30 years (e.g. real_season_numbers_dataframe_476411993_CFcsv).
Also, this folder contains "hydro.csv" file that has the corresponded simulated hydrological variables.
Best samples Folder: 
Contains 3 CSV files corresponded to 3 selected locations for the future climate experiment. Each file contains the behavioral samples (out of 136,000 samples). Each file has several columns including:
"sample": The number of samples which is selected out of the file that has 136,000 samples.
"Yield": The average of 30 years historical yield based on the corresponded sample parameter set. 	
"Yield_diff": The difference (%) between the previous column ("Yield") and the historical average yield based on the calibrated parameter set.	
"class": the previous column "Yield_diff" is classified into few classes: 
3_2: 3% to 2% difference in Yield
2_1: 2% to 1% difference in Yield
1_0: 1% to 0 difference in Yield
-1_0: -1% to 0 difference in Yield
-2_-1: -2% to -3% difference in Yield
-3_-2: -3% to -2% difference in Yield

G- ##########################################################################################
Future Folder >> contains 3 folders for 3 selected GCMs-RCP8.5 considered in the manuscript and a "Baseline" folder.

3 GCMs Folders: 
Each GCM folder contains 3 subfolders. Each subfolder is named based on one of the 3 locations that were selected for the future climate scenario experiment (453911731_CCF, 461411652_CC and 476411993_CF). 
Each of these subfolders contains several CVS files, similar to what is explained in above section:
E/Historical Folder/16 Folders with location's ID
The difference is that these results are based on future climate scenarios (RCP8.5).

Baseline Folder:
Contains two CSV files for each of 3 GCMs, one contains the annual simulated yield (e.g. Yield_BNU-ESM_with_calibrated_param.csv) and one includes the simulated hydrological variables (e.g. hydro_BNU-ESM_with_calibrated_param.csv). 
The deterministic calibrated parameter set based on the historical data was used to simulate yield and hydrological variables for 3 GCMs.
