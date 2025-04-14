بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ
Curated by Alfian

## 📊 Equality ##
# Comparison of booleans
print(True == False)  # Output: False

# Comparison of integers
print(-5 * 15 != 75)  # Output: True

# Comparison of strings
print("pyscript" == "PyScript")  # Output: False

# Compare a boolean with an integer
print(True == 1)  # Output: True

## 📊 Greater and less than ##
# Comparison of integers
x = -3 * 6
print(x >= -10)  # Output: False

# Comparison of strings
y = "test"
print("test" <= y)  # Output: True

# Comparison of booleans
print(True > False)  # Output: True

## 📊 Compare arrays ##
# Create arrays
import numpy as np
my_house = np.array([18.0, 20.0, 10.75, 9.50])
your_house = np.array([14.0, 24.0, 14.25, 9.0])

# my_house greater than or equal to 18
print(my_house >= 18)  # Output: [ True  True False False]

# my_house less than your_house
print(my_house < your_house)  # Output: [False  True  True False]

## 📊 and, or, not (1) ##
# Define variables
my_kitchen = 18.0
your_kitchen = 14.0

# my_kitchen bigger than 10 and smaller than 18?
print(my_kitchen > 10 and my_kitchen < 18)  # Output: False

# my_kitchen smaller than 14 or bigger than 17?
print(my_kitchen < 14 or my_kitchen > 17)  # Output: True

# Double my_kitchen smaller than triple your_kitchen?
print((2 * my_kitchen) < (3 * your_kitchen))  # Output: True

## 📊 and, or, not (2) ##
B. False

## 📊 Boolean operators with NumPy ##
# Create arrays
import numpy as np
my_house = np.array([18.0, 20.0, 10.75, 9.50])
your_house = np.array([14.0, 24.0, 14.25, 9.0])

# my_house greater than 18.5 or smaller than 10
print(np.logical_or(my_house > 18.5, my_house < 10))  
# Output: [False  True False  True]

# Both my_house and your_house smaller than 11
print(np.logical_and(my_house < 11, your_house < 11))  
# Output: [False False False  True]

## 📊 Warmup ##
B. Medium

## 📊 if ##
# Define variables
room = "kit"
area = 14.0

# if statement for room
if room == "kit":
    print("looking around in the kitchen.")

# if statement for area
if area > 15:
    print("big place!")

## 📊 Add else ##
# Define variables
room = "kit"
area = 14.0

# if-else construct for room
if room == "kit":
    print("looking around in the kitchen.")
else:
    print("looking around elsewhere.")

# if-else construct for area
if area > 15:
    print("big place!")
else:
    print("pretty small.")

## 📊 Customize further: elif ##
# Define variables
room = "bed"
area = 14.0

# if-elif-else construct for room
if room == "kit":
    print("looking around in the kitchen.")
elif room == "bed":
    print("looking around in the bedroom.")
else:
    print("looking around elsewhere.")

# if-elif-else construct for area
if area > 15:
    print("big place!")
elif area > 10:
    print("medium size, nice!")
else:
    print("pretty small.")

## 📊 Driving right (1) ##
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col=0)

# Extract drives_right column as Series: dr
dr = cars['drives_right']

# Use dr to subset cars: sel
sel = cars[dr]

# Print sel
print(sel)

## 📊 Driving right (2)
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col=0)

# Convert code to a one-liner
sel = cars[cars['drives_right']]

# Print sel
print(sel)

## 📊 Cars per capita (1) ##
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col=0)

# Create car_maniac: observations that have a cars_per_cap over 500
car_maniac = cars[cars['cars_per_cap'] > 500]

# Print car_maniac
print(car_maniac)

## 📊 Cars per capita (2) ##
# Import pandas and numpy
import pandas as pd
import numpy as np

# Load the cars dataset
cars = pd.read_csv('cars.csv', index_col=0)

# Create medium: observations with cars_per_cap between 100 and 500
cpc = cars['cars_per_cap']
between = np.logical_and(cpc > 100, cpc < 500)
medium = cars[between]

# Print medium
print(medium)
