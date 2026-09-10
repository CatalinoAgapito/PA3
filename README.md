# PA#3
### Name: AGAPITO, Catalino D.R.
### Section: 2ECE-C
### Date Submitted: September 10, 2026

In this Program Assignment, three different problems were asked to demonstrate proficiency in Pandas data analysis. Each problem focuses on different aspects of data manipulation, from positional and label-based indexing to Boolean filtering and conditional selection 

# Problem 1: Positional and Label-Based Slicing
````
import pandas as pd
````
````
cars = pd.read_csv('cars.csv')
cars
````
In this part of the code, it shows the list of cars
````
print(cars.shape)
print(cars.columns.tolist())
````
````
cars_6_to_10 = cars.iloc[5:10]
cars_6_to_10
````
````
cars_6_to_10 = cars.iloc[6:11]
cars_6_to_10.loc[0:11,['Model', 'mpg', 'cyl', 'hp', 'gear']]
````

# Problem 2: Model Lookup
````
toyota = cars[cars["Model"] == "Toyota Corolla"]
toyota
````
````
pontiac = cars.loc[cars["Model"] == "Pontiac Firebird", ["Model", "mpg", "hp", "wt"]]
pontiac
````
# Problem 3: Multi-Model Subsetting
````
selected_cars = cars.loc[cars["Model"].isin(["Datsun 710", "Lotus Europa", "Ferrari Dino"]), ["Model", "mpg", "cyl", "hp", "gear"]]
selected_cars
````
