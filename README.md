# PA#3
### Name: AGAPITO, Catalino D.R.
### Section: 2ECE-C
### Date Submitted: September 10, 2026

In this Program Assignment, three different problems were given to demonstrate the use of Pandas for data analysis. Each problem focuses on different ways of working with data, such as selecting specific rows and columns, finding particular car models, and choosing records based on certain conditions. The activities also show how to organize and view specific information from a dataset while keeping the original data unchanged. Through these problems, the car dataset can be examined more easily and the required information can be selected according to the given instructions.

# Problem 1: Positional and Label-Based Slicing

````
import pandas as pd
````
In this part of the code, it prepares the program to work with the car data.

````
cars = pd.read_csv('cars.csv')
cars
````
In this part of the code, it loads the car data from the CSV file and displays the information in the table.


````
print(cars.shape)
print(cars.columns.tolist())
````
This part of the code shows the number of rows and columns in the table and provides a list of the information included in the dataset.

````
cars_6_to_10 = cars.iloc[5:10]
cars_6_to_10
````
In this part of the code, it selects cars 6 to 10 from the list and displays the information for those cars.

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
