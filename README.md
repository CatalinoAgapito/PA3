# PA#3
### Name: AGAPITO, Catalino D.R.
### Section: 2ECE-C
### Date Submitted: September 10, 2026

In this Program Assignment, three different problems were asked to demonstrate proficiency in Pandas data analysis. Each problem focuses on different aspects of data manipulation, from positional and label-based indexing to Boolean filtering and conditional selection 

# Problem 1: Positional and Label-Based Slicing

````
import pandas as pd
````
In this part of the code, it imports the Pandas library and gives it the name pd. This allows Pandas functions to be used later in the program to work with and analyze the data.

````
cars = pd.read_csv('cars.csv')
cars
````
In this part of the code, the cars.csv file is loaded into a DataFrame named cars. The cars DataFrame contains the information about the different vehicles that will be used for the activity.


````
print(cars.shape)
print(cars.columns.tolist())
````
This part of the code shows the size of the cars DataFrame and the complete list of column names. The shape shows the number of rows and columns, while columns.tolist() displays all the column names in a list.

````
cars_6_to_10 = cars.iloc[5:10]
cars_6_to_10
````
In this part of the code, positional indexing with iloc selects rows 6 through 10 from the dataset. The selected rows are then stored in a new DataFrame named cars_6_to_10 without changing the original cars DataFrame.

````
cars_6_to_10 = cars.iloc[6:11]
cars_6_to_10.loc[0:11,['Model', 'mpg', 'cyl', 'hp', 'gear']]
````
In this part of the code, it selects specific columns from cars_6_to_10, including Model, mpg, cyl, hp, and gear. This displays only the information needed for this part of the activity while keeping the selected columns in the required order.


# Problem 2: Model Lookup
````
toyota = cars[cars["Model"] == "Toyota Corolla"]
toyota
````
In this part of the code, Boolean indexing is used to search the Model column for Toyota Corolla. The complete row containing Toyota Corolla is selected and stored in a new DataFrame named toyota.

````
pontiac = cars.loc[cars["Model"] == "Pontiac Firebird", ["Model", "mpg", "hp", "wt"]]
pontiac
````
In this part of the code, Boolean indexing is used to search for Pontiac Firebird in the Model column. It then selects only the Model, mpg, hp, and wt columns and stores the result in a DataFrame named pontiac.

# Problem 3: Multi-Model Subsetting
````
selected_cars = cars.loc[cars["Model"].isin(["Datsun 710", "Lotus Europa", "Ferrari Dino"]), ["Model", "mpg", "cyl", "hp", "gear"]]
selected_cars
````
In this part of the code, the isin() function is used to search for three specific models: Datsun 710, Lotus Europa, and Ferrari Dino. It then selects only the Model, mpg, cyl, hp, and gear columns and stores the results in a new DataFrame named selected_cars.
