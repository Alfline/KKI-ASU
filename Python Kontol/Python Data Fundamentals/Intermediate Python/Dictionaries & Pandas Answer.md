بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ
Curated by Alfian

## 📊 Motivation for dictionaries ##
# Definition of countries and capitals
countries = ['spain', 'france', 'germany', 'norway']
capitals = ['madrid', 'paris', 'berlin', 'oslo']

# Get index of 'germany'
ind_ger = countries.index('germany')

# Use ind_ger to print out capital of Germany
print(capitals[ind_ger])

## 📊 Create dictionary ##
# Definition of countries and capitals
countries = ['spain', 'france', 'germany', 'norway']
capitals = ['madrid', 'paris', 'berlin', 'oslo']

# Create dictionary europe
europe = {countries[0]: capitals[0], countries[1]: capitals[1], countries[2]: capitals[2], countries[3]: capitals[3]}

# Print europe
print(europe)

## 📊 Access dictionary ##
# Definition of dictionary
europe = {'spain': 'madrid', 'france': 'paris', 'germany': 'berlin', 'norway': 'oslo'}

# Print out the keys in europe
print(europe.keys())

# Print out value that belongs to key 'norway'
print(europe['norway'])

## 📊 Dictionary Manipulation (1) ##
# Definition of dictionary
europe = {'spain': 'madrid', 'france': 'paris', 'germany': 'berlin', 'norway': 'oslo'}

# Add italy to europe
europe['italy'] = 'rome'

# Print out italy in europe
print('italy' in europe)

# Add poland to europe
europe['poland'] = 'warsaw'

# Print europe
print(europe)

## 📊 Dictionary Manipulation (2) ##
# Definition of dictionary
europe = {'spain': 'madrid', 'france': 'paris', 'germany': 'bonn',
          'norway': 'oslo', 'italy': 'rome', 'poland': 'warsaw',
          'australia': 'vienna'}

# Update capital of germany
europe['germany'] = 'berlin'

# Remove australia
del europe['australia']

# Print europe
print(europe)

## 📊 Dictionariception ##
# Dictionary of dictionaries
europe = { 
    'spain': { 'capital': 'madrid', 'population': 46.77 },
    'france': { 'capital': 'paris', 'population': 66.03 },
    'germany': { 'capital': 'berlin', 'population': 80.62 },
    'norway': { 'capital': 'oslo', 'population': 5.084 }
}

# Print out the capital of France
print(europe['france']['capital'])

# Create sub-dictionary data
data = {'capital': 'rome', 'population': 59.83}

# Add data to europe under key 'italy'
europe['italy'] = data

# Print europe
print(europe)

## 📊 Dictionary to DataFrame (1) ##
# Import pandas as pd
import pandas as pd

# Pre-defined lists
names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
dr = [True, False, False, False, True, True, True]
cpc = [809, 731, 588, 18, 200, 70, 45]

# Create dictionary my_dict with three key:value pairs
my_dict = {
    'country': names,
    'drives_right': dr,
    'cars_per_cap': cpc
}

# Build a DataFrame cars from my_dict
cars = pd.DataFrame(my_dict)

# Print cars
print(cars)

## 📊 Dictionary to DataFrame (2) ##
import pandas as pd

# Build cars DataFrame
names = ['United States', 'Australia', 'Japan', 'India', 'Russia', 'Morocco', 'Egypt']
dr = [True, False, False, False, True, True, True]
cpc = [809, 731, 588, 18, 200, 70, 45]
cars_dict = {'country': names, 'drives_right': dr, 'cars_per_cap': cpc}
cars = pd.DataFrame(cars_dict)
print(cars)

# Definition of row_labels
row_labels = ['US', 'AUS', 'JPN', 'IN', 'RU', 'MOR', 'EG']

# Specify row labels of cars
cars.index = row_labels

# Print cars again
print(cars)

## 📊 CSV to DataFrame (1) ##
# Import pandas as pd
import pandas as pd

# Import the cars.csv data as a DataFrame
cars = pd.read_csv('cars.csv')

# Print out cars
print(cars)

## 📊 CSV to DataFrame (2) ##
# Import pandas as pd
import pandas as pd

# Fix import by including index_col
cars = pd.read_csv('cars.csv', index_col=0)

# Print out cars
print(cars)

## 📊 Square Brackets (1) ##
# Import cars data
import pandas as pd

# Read the CSV file with index_col set to 0
cars = pd.read_csv('cars.csv', index_col=0)

# Print out country column as Pandas Series
print(cars['country'])

# Print out country column as Pandas DataFrame
print(cars[['country']])

# Print out DataFrame with country and drives_right columns
print(cars[['country', 'drives_right']])

## 📊 Square Brackets (2) ##
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col=0)

# Print out first 3 observations
print(cars[0:3])

# Print out fourth, fifth and sixth observation
print(cars[3:6])

## 📊 loc and iloc (1) ##
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col=0)

# Print out observation for Japan as a Series
print(cars.loc['JPN'])
# Alternatively, using iloc:
# print(cars.iloc[2])

# Print out observations for Australia and Egypt as a DataFrame
print(cars.loc[['AUS', 'EG']])
# Alternatively, using iloc:
# print(cars.iloc[[1, 6]])

## 📊 loc and iloc (2) ##
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col=0)

# Print out drives_right value of Morocco
print(cars.loc['MOR', 'drives_right'])
# Alternatively, using iloc:
# print(cars.iloc[5, 1])

# Print sub-DataFrame with observations for Russia and Morocco, and columns country and drives_right
print(cars.loc[['RU', 'MOR'], ['country', 'drives_right']])
# Alternatively, using iloc:
# print(cars.iloc[[4, 5], [0, 1]])

## 📊 loc and iloc (3) ##
# Import cars data
import pandas as pd
cars = pd.read_csv('cars.csv', index_col=0)

# Print out drives_right column as Series
print(cars.loc[:, 'drives_right'])
# Alternatively, using iloc:
# print(cars.iloc[:, 1])

# Print out drives_right column as DataFrame
print(cars.loc[:, ['drives_right']])
# Alternatively, using iloc:
# print(cars.iloc[:, [1]])

# Print out cars_per_cap and drives_right as DataFrame
print(cars.loc[:, ['cars_per_cap', 'drives_right']])
# Alternatively, using iloc:
# print(cars.iloc[:, [2, 1]])
