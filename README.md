# Distillation profile of Crude oil mixture

## Introduction
1. Given any two crude oils with their given distillation profiles, create a model which will give an
approximate distillation profile of the mixture of the two oils with specified volumes. (Note: thinking
of the distillation profiles as snapshots of functions is the recommended view.) The percentages to
use (and get at the end) are the same as the ones in the above example, namely: [ 5, 10, 20, 30,
40, 50, 60, 70, 80, 90, 95, 99].
2. Explain any assumptions or simplifications made.
3. Collect data from Crude Monitor for a couple of real crudes, and cleaning recent data, run the
distillation profiles through your program with volumes of your choosing.


## Data sources 

The data source is  https://www.crudemonitor.ca/home.php from where it is downloaded in a csv format. 

The csv files have been saved in the data_files folder for the following crude oils:
```1. Light Smiley
2. Peace
3. Federated
4. Pembina 
5. Secure Sask Light 
6. Mixed Sweet Blend 
7. Rainbow 
8. BC Light
9. Boundary Lake
10. Koch Alberta 
11. Moose Jaw Tops 
12. Pembina Light Sour 
13. Hardisty Light 
14. Medium Gibson Sour 
15. Midale 
16. Peace Pipe Sour 
17. Conventional Heavy
```

## Assumptions

1. Mixing of two crude oils doesn’t change the composition and their properties i.e. changing the evaporation temperatures, specific heat etc
2. Quantity of oil does not affect the distillation profile
3. Alternative way of getting a more intuitive model is by using month to month data available in the csv files (but data was missing for many time periods therefore decided to take only recent records)

## Program flow

1. User enters the name of crude oil from the given list
2. The csv files are named after the crude oils
3. When user enters the choice of their crude oil the csv is directly pulled from data_files folder
4. Converted the user entered oil name(uppercase or lowercase)  to lowercase string in order to handle errors
5. Cleaned the data files by selecting only required columns and rows
6. Removed the null records
7. Transposed the dataframe
8. Joined the two dataframes and calculated the mean of the two for the temperature
9. User inputs the volume (%) of evaporated mixture and the code returns the distillation profiles of his/her choosing




