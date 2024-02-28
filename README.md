# Evaluation_of_Pressure-Gradient_Method
This repository contains the code required to reproduce the results presented in my paper on evaluating a pressure-gradient based algorithm for locating cyclone centers over Southern Australia.
Guide to Repository

This code repository is to reproduce the results of the paper “Evaluation of a Pressure-Gradient Method to Identify Midlatitude Cyclones over Southern Australia”. It is organised in the following way:


1)	Preliminary processing of the cyclone datasets
-	Pressure Gradient method
-	Melbourne University tracking scheme
-	Portmann Potential Vorticity cutoffs
-	R13 Manual dataset
2)	3.1 Comparison of individual cyclones in automated datasets (include PV vs MU for completeness)
3)	3.1.3 Monthly and Interannual variability of datasets
4)	3.2 Comparisons of automated schemes to R13
-	Include the AGCD code to generate the rainfall composites for each dataset


The code in each of the directories of the folder “Preliminary_Processing” need to be run first. They extract the data of the cyclone systems from each of the different methods being compared, and arrange it in a simple format that can be used by the code for the rest of the paper. In addition, the directory “Pressure-Gradient_Method” contains the code of the pressure-gradient cyclone identification algorithm. The pressure-gradient cyclone identification algorithm needs to be run with 500 hPa geopotential height data from the ERA5 reanalysis to compare against the Melbourne University and R13 datasets, and also with 500 hPa geopotential height data from the ERA-Interim reanalysis to compare against the Portmann PV cutoff dataset. 

The code in the directory Results_Section_3-1 needs to be run next, using the reshaped cyclone dataset output from the Preliminary Processing code. The code in this folder computes the CSI and percentage of match values, and also contains code to plot the system-centred composite fields of the matching and extra systems. 

The code in the directory Results_Section_3-1-3 can also now be run, to generate figures 5 and 6 on the monthly and interannual variability of the cyclone datasets. There is also code to compute the standard deviations of the annual cyclone days before and after the year 2001 (tables 2 and 3). Note that these figures also include the data from the R13 manual dataset for the months April-October, so the code Preliminary_Processing/R13_Manual_Dataset will also need to be run. 

The code in the final directory Results_Section_3-2 reproduces the results of the comparisons between each of the automated schemes and the R13 manual dataset. The code in each of the sub-directories computes the CSI values, and the remaining code extracts the AGCD precipitation fields associated with each of the cyclone systems, and computes the RCSI composites. 
