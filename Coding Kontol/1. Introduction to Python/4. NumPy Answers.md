
## 📊 Subsetting NumPy Arrays:
    import numpy as np

    # Predefined variables (must have sufficient elements)
    np_weight_lb = np.array(weight_lb)  # Requires ≥51 elements
    np_height_in = np.array(height_in)  # Requires ≥111 elements

    # Print weight at index 50
    print(np_weight_lb[50])  # Only works if len(weight_lb) > 50

    # Print sub-array of heights (indices 100-110 inclusive)
    print(np_height_in[100:111])  # Only works if len(height_in) > 110

## 📊 Baseball data in 2D form
    import numpy as np

    # Use predefined baseball list (do not redefine it)
    np_baseball = np.array(baseball)  # Creates 2D array from existing data

    # Print the array's dimensions
    print(np_baseball.shape)

## 📊 2D Arithmethic
    import numpy as np

    np_baseball = np.array(baseball)

    # 1. Add np_baseball and updated arrays
    updated_stats = np_baseball + updated
    print("Updated player stats:")
    print(updated_stats)

    # 2. Create conversion array
    conversion = np.array([0.0254, 0.453592, 1])
    print("\nConversion array:")
    print(conversion)

    # 3. Convert units using element-wise multiplication
    metric_stats = np_baseball * conversion
    print("\nMetric conversions:")
    print(metric_stats)

## 📊 Explore the baseball data
    import numpy as np

    # Mean height (already provided)
    avg = np.mean(np_baseball[:, 0])
    print("Average: " + str(avg))

    # Median height
    med = np.median(np_baseball[:, 0])  # Correctly calculate the median of the first column
    print("Median: " + str(med))

    # Standard deviation of height
    stddev = np.std(np_baseball[:, 0])  # Correctly calculate the standard deviation of the first column
    print("Standard Deviation: " + str(stddev))

    # Height-weight correlation
    corr = np.corrcoef(np_baseball[:, 0], np_baseball[:, 1])  # Compute correlation matrix
    print("Correlation matrix:\n" + str(corr))
    print("Correlation between height and weight: " + str(corr[0, 1]))  # Extract specific correlation coefficient
