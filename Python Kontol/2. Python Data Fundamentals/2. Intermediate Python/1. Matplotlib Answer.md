بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ
Curated by Alfian

## 📊 Line plot (1) ##
    # Print the last item from year and pop
    print(year[-1])
    print(pop[-1])

    # Import matplotlib.pyplot as plt
    import matplotlib.pyplot as plt

    # Make a line plot: year on the x-axis, pop on the y-axis
    plt.plot(year, pop)

    # Display the plot with plt.show()
    plt.show()

## 📊 Line Plot (2): Interpretation ##
Answer: 2060

## 📊 Line plot (3) ##
    # Print the last item of gdp_cap and life_exp
    print(gdp_cap[-1])
    print(life_exp[-1])

    # Make a line plot, gdp_cap on the x-axis, life_exp on the y-axis
    plt.plot(gdp_cap, life_exp)
    plt.xlabel('GDP per Capita (USD)')
    plt.ylabel('Life Expectancy (Years)')

    # Display the plot
    plt.show()

## 📊 Scatter Plot (1) ##
    # Change the line plot below to a scatter plot
    plt.scatter(gdp_cap, life_exp)

    # Put the x-axis on a logarithmic scale
    plt.xscale('log')

    # Show plot
    plt.show()

## 📊 Scatter plot (2) ##
    # Import package
    import matplotlib.pyplot as plt

    # Build Scatter plot
    plt.scatter(pop, life_exp)
    plt.xlabel('Population (in millions)')
    plt.ylabel('Life Expectancy (Years)')

    # Show plot
    plt.show()

## 📊 Build a histogram (1) ##
    # Import matplotlib.pyplot
    import matplotlib.pyplot as plt

    # Create histogram of life_exp data
    plt.hist(life_exp)

    # Add labels and title for better understanding (optional)
    plt.xlabel('Life Expectancy (Years)')
    plt.ylabel('Frequency')
    plt.title('Histogram of Life Expectancy')

    # Display histogram
    plt.show()

## 📊 Build a histogram (2): bins ##
    import matplotlib.pyplot as plt

    # Sample data for demonstration purposes
    life_exp = [50, 55, 60, 65, 70, 75, 80, 85, 90, 95, 100, 105, 110, 115, 120]

    # Build histogram with 5 bins
    plt.hist(life_exp, bins=5)
    plt.xlabel('Life Expectancy (Years)')
    plt.ylabel('Frequency')
    plt.title('Histogram of Life Expectancy with 5 Bins')
    plt.show()
    plt.clf()

    # Build histogram with 20 bins
    plt.hist(life_exp, bins=20)
    plt.xlabel('Life Expectancy (Years)')
    plt.ylabel('Frequency')
    plt.title('Histogram of Life Expectancy with 20 Bins')
    plt.show()
    plt.clf()

## 📊 Build a histogram (3): compare ##
    import matplotlib.pyplot as plt

    # Sample data for demonstration purposes
    life_exp = [50, 55, 60, 65, 70, 75, 80, 85, 90, 95, 100, 105, 110, 115, 120]
    life_exp1950 = [40, 45, 50, 55, 60, 65, 70, 75, 80, 85, 90, 95, 100, 105, 110]

    # Histogram of life_exp (2007), with 15 bins
    plt.hist(life_exp, bins=15)
    plt.xlabel('Life Expectancy (Years)')
    plt.ylabel('Frequency')
    plt.title('Histogram of Life Expectancy (2007) with 15 Bins')
    plt.show()
    plt.clf()

    # Histogram of life_exp1950 (1950), with 15 bins
    plt.hist(life_exp1950, bins=15)
    plt.xlabel('Life Expectancy (Years)')
    plt.ylabel('Frequency')
    plt.title('Histogram of Life Expectancy (1950) with 15 Bins')
    plt.show()
    plt.clf()

## 📊 Choose the right plot (1) ##
C. Histogram

## 📊 Choose the right plot (2) ##
B. Scatter Plot

## 📊 Labels ##
    import matplotlib.pyplot as plt

    # Sample data for demonstration purposes
    gdp_cap = [1000, 5000, 10000, 20000, 50000]
    life_exp = [50, 60, 70, 75, 80]

    # Basic scatter plot, log scale
    plt.scatter(gdp_cap, life_exp)
    plt.xscale('log') 

    # Strings
    xlab = 'GDP per Capita [in USD]'
    ylab = 'Life Expectancy [in years]'
    title = 'World Development in 2007'

    # Add axis labels
    plt.xlabel(xlab)
    plt.ylabel(ylab)

    # Add title
    plt.title(title)

    # After customizing, display the plot
    plt.show()

## 📊 Ticks ##
    # Scatter plot
    plt.scatter(gdp_cap, life_exp)

    # Previous customizations
    plt.xscale('log') 
    plt.xlabel('GDP per Capita [in USD]')
    plt.ylabel('Life Expectancy [in years]')
    plt.title('World Development in 2007')

    # Definition of tick_val and tick_lab
    tick_val = [1000, 10000, 100000]
    tick_lab = ['1k', '10k', '100k']

    # Adapt the ticks on the x-axis
    plt.xticks(tick_val, tick_lab)

    # After customizing, display the plot
    plt.show()

## 📊 Sizes ##
    # Import numpy as np
    import numpy as np
    import matplotlib.pyplot as plt

    # Store pop as a numpy array: np_pop
    np_pop = np.array(pop)

    # Double np_pop
    np_pop = np_pop * 2

    # Update: set s argument to np_pop
    plt.scatter(gdp_cap, life_exp, s=np_pop)

    # Previous customizations
    plt.xscale('log')
    plt.xlabel('GDP per Capita [in USD]')
    plt.ylabel('Life Expectancy [in years]')
    plt.title('World Development in 2007')
    plt.xticks([1000, 10000, 100000], ['1k', '10k', '100k'])

    # Display the plot
    plt.show()

## 📊 Colors ##
    import numpy as np
    import matplotlib.pyplot as plt

    # Create NumPy array for population and double the values
    np_pop = np.array(pop) * 2

    # Correctly specify s and other arguments inside plt.scatter()
    plt.scatter(x=gdp_cap, y=life_exp, s=np_pop, c=col, alpha=0.8)

    # Previous customizations
    plt.xscale('log')
    plt.xlabel('GDP per Capita [in USD]')
    plt.ylabel('Life Expectancy [in years]')
    plt.title('World Development in 2007')
    plt.xticks([1000, 10000, 100000], ['1k', '10k', '100k'])

    # Show the plot
    plt.show()

## 📊 Additional Customizations ##
    import numpy as np
    import matplotlib.pyplot as plt

    # Create NumPy array for population and double the values
    np_pop = np.array(pop) * 2

    # Scatter plot
    plt.scatter(x=gdp_cap, y=life_exp, s=np_pop, c=col, alpha=0.8)

    # Previous customizations
    plt.xscale('log')
    plt.xlabel('GDP per Capita [in USD]')
    plt.ylabel('Life Expectancy [in years]')
    plt.title('World Development in 2007')
    plt.xticks([1000, 10000, 100000], ['1k', '10k', '100k'])

    # Additional customizations
    plt.text(1550, 71, 'India')
    plt.text(5700, 80, 'China')

    # Add gridlines to the plot
    plt.grid(True)

    # Show the plot
    plt.show()

## 📊 Interpretation ##
A. The countries in blue, corresponding to Africa, have both low life expectancy and a low GDP per capita.
