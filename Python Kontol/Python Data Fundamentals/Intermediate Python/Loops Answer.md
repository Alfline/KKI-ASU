بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ
Curated by Alfian

## 📊 while: warming up ##
D. 3

## 📊 Basic while loop ##
# Initialize offset
offset = 8

# Code the while loop
while offset != 0:
    print("correcting...")
    offset = offset - 1  # Decrease offset by 1
    print(offset)  # Print the updated value of offset

## 📊 Add conditionals ##
# Initialize offset
offset = -6

# Code the while loop
while offset != 0:
    print("correcting...")
    if offset > 0:
        offset = offset - 1  # Decrease offset if it's positive
    else:
        offset = offset + 1  # Increase offset if it's negative
    print(offset)  # Print the updated value of offset

## 📊 Loop over a list ##
# areas list
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Code the for loop
for area in areas:
    print(area)

## 📊 Indexes and values (1) ##
# areas list
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Change for loop to use enumerate() and update print()
for index, area in enumerate(areas):
    print("room " + str(index) + ": " + str(area))

## 📊 Indexes and values (2) ##
# areas list
areas = [11.25, 18.0, 20.0, 10.75, 9.50]

# Code the for loop
for index, area in enumerate(areas):
    print("room " + str(index + 1) + ": " + str(area))

## 📊 Loop over list of lists ##
# house list of lists
house = [["hallway", 11.25], 
         ["kitchen", 18.0], 
         ["living room", 20.0], 
         ["bedroom", 10.75], 
         ["bathroom", 9.50]]

# Build a for loop from scratch
for room in house:
    print(f"the {room[0]} is {room[1]} sqm")

## 📊 Loop over dictionary ##
# Definition of dictionary
europe = {'spain': 'madrid', 'france': 'paris', 'germany': 'berlin',
          'norway': 'oslo', 'italy': 'rome', 'poland': 'warsaw', 'austria': 'vienna'}

# Iterate over europe
for country, capital in europe.items():
    print(f"the capital of {country} is {capital}")

## 📊 Loop over NumPy array ##
# Import numpy as np
import numpy as np

# For loop over np_height
for x in np_height:
    print(f"{x} inches")

# For loop over np_baseball
for x in np.nditer(np_baseball):
    print## 📊

## 📊 Loop over DataFrame (1) ##
# Import cars data
import pandas as pd

# Load the cars dataset
cars = pd.read_csv('cars.csv', index_col=0)

# Iterate over rows of cars
for lab, row in cars.iterrows():
    print(lab)  # Print row label
    print(row)  # Print row contents

## 📊 Loop over DataFrame (2)
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col=0)

# Adapt for loop
for lab, row in cars.iterrows():
    print(f"{lab}: {row['cars_per_cap']}")

## 📊 Add column (1) ##
# Import cars data
import pandas as pd

# Load the cars dataset
cars = pd.read_csv('cars.csv', index_col=0)

# Code for loop that adds COUNTRY column
for lab, row in cars.iterrows():
    cars.loc[lab, 'COUNTRY'] = row['country'].upper()

# Print cars
print(cars)


## 📊 Add column (2) ##
# Import cars data
import pandas as pd

# Load the cars dataset
cars = pd.read_csv('cars.csv', index_col=0)

# Use .apply(str.upper) to create the COUNTRY column
cars["COUNTRY"] = cars["country"].apply(str.upper)

# Print cars
print(cars)
