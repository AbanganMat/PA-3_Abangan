# EXPERIMENT 3 - Python Data Analysis - Abangan

# I. Intended Learning Outcomes:
1. To identify the codes and functions incorporated in the Pandas library.
2. To be able to apply and use the different codes and functions in creating a Python program using a Pandas library.

# II. Instructions 
Write a Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter notebook in the dedicated submission bin.

++ Download the csv file named 'cars.csv' for the proper demonstration of data analysis.

# PROBLEM 1: Abangan_Pandas-P1.py
a. Load the corresponding .csv file into a data frame named cars using pandas.

b. Display the first five and last five rows of the resulting cars.
_________________________________________________________________________________________________________________________________________________________
a. Loading the .csv file into the data frame
```
#Start Program

import pandas as pd  #Importing pandas library

cars = pd.read_csv('cars.csv')
cars
```
b. Display the first five rows of the resulting car

```
cars.head()
```
b. Display the last five rows of the resulting car
```
cars.tail()
```

# PROBLEM 2: Abangan_Pandas-P2.py
Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and
indexing operations.

a. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars.

b. Display the row that contains the ‘Model’ of ‘Mazda RX4’.

c. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?

d. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4
Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.

_________________________________________________________________________________________________________________________

a. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7...) of cars.
```
a = cars.iloc[:5, 0::2]
a
```

b. Display the row that contains the ‘Model’ of ‘Mazda RX4’.
```
b = cars.loc[(cars['Model']=='Mazda RX4 Wag'),]
b
```

c. How many cylinders (‘cyl’) does the car model ‘Camaro Z28’ have?
```
c = cars.loc[(cars['Model']=='Camaro Z28'),['Model', 'cyl']]
c

```

d. Determine how many cylinders (‘cyl’) and what gear type (‘gear’) do the car models ‘Mazda RX4
Wag’, ‘Ford Pantera L’ and ‘Honda Civic’ have.

```
d = cars.loc[(cars['Model']=='Mazda RX4 Wag') | (cars['Model']=='Ford Pantera L')| (cars['Model']=='Honda Civic'), ['Model', 'cyl', 'gear']]
d
```
