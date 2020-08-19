# Module2_final_project

## Files
- pictures folder = pictures used in this readme
- test.ipynb = Jupyter notebook of project
- column_names.md = description of the names of columns in the dataset
- kc_house_data.csv =  the data set used for this project
- module2_final_project.pdf = pdf of the final project presentation

## Introduction
For Years it has been the case that buyers around the US have felt cheated by the housing market. in 2007/8 the systemic issues in the market for houses were exemplified. People thought things would change however this has not been the case.

It was my aim to create a model for house buyers in King County. The goal of the model would be to allow buyers to be able to easily guage the proce of their house compared to similar houses. This would allow them to not be cheated my estate agents and sellers.

## Data analysis and exploration
- the data was explored, columns that were not needed for the regression such as ID etc. were deleted and others were kept
- Nan values, missing values and values that did not make sence in the data set were treated respectfully
- an analysis of all variables was done in order to see if there were certain houses that did not fit the general trend eg. houses proced over $1170,000. These were then deleted
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/Data_anlysis_hist.png)
- continious, ordinal and categorical values were identified and all categorical values were trasformed into dummy variables
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/data_analysis_scat.png)

## Diving deep into the data
- Zip codes, longitude, latitude and their effect on house prices were analysed and clear trends were obsereved
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/zipcode.png)

- the price of houses depending on when there were sold was analysed. there were clear trends depending on which quarter houses were sold. quarters were then made into dummy variables
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/sell_date.png)

## Multicolinearity 
- all varible pairs and the correlation between them were obsereved
- for pairs with a correlation of over 0.75 one of the variables were dropped

## hetroscadisticity, normality
- all varibles were checked for hetroscadisticity and normality however no changes were made as the regression was to be as easily interperatible as possible
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/norm_multi_1.png)
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/norm_multi_2.png)

## Stepwise selection
- stepwise selection was used to analyse all variabels and to decide which to include into the model the threshold in used was 0.01 and the threshold out used was 0.05

## interactions
- the top three interactions were identified and the top 2 were added to the model
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/interactions.png)

## Model
- the model was built and all coefficients were obsereved
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/coeff.png)
The adjusted r-squared was 0.82
The mean absolue error was $61,822
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/actual_vs_pred.png)

## Program
- a program was built where users can easily put in house details and the estimate of their house price would be displayed
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/program.png)
- this was then tested against real houses 
![awesome](https://github.com/SaifuddinAnjarwalla/Module2_final_project/blob/master/Pictures/House%20example.png)

