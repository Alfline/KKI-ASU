بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ
Curated by Alfian

## 📊 Random float ##
    # Import numpy as np
    import numpy as np

    # Set the seed
    np.random.seed(123)

    # Generate and print random float
    random_float = np.random.rand()
    print(random_float)

## 📊 Roll the dice ##
    # Import numpy and set seed
    import numpy as np
    np.random.seed(123)

    # Use randint() to simulate a dice
    first_roll = np.random.randint(1, 7)
    print(first_roll)

    # Use randint() again to simulate a second dice roll
    second_roll = np.random.randint(1, 7)
    print(second_roll)

## 📊 Determine your next move ##
    # NumPy is imported, seed is set
    import numpy as np
    np.random.seed(123)

    # Starting step
    step = 50

    # Roll the dice
    dice = np.random.randint(1, 7)

    # Finish the control construct
    if dice <= 2:
        step = step - 1
    elif dice <= 5:
        step = step + 1
    else:
        step = step + np.random.randint(1, 7)

    # Print out dice and step
    print(f"Dice: {dice}")
    print(f"Step: {step}")

## 📊 The next step ##
    # NumPy is imported, seed is set
    import numpy as np
    np.random.seed(123)

    # Initialize random_walk
    random_walk = [0]

    # Complete the for loop
    for x in range(100):
        # Set step: last element in random_walk
        step = random_walk[-1]

        # Roll the dice
        dice = np.random.randint(1, 7)

        # Determine next step
        if dice <= 2:
            step = step - 1
        elif dice <= 5:
            step = step + 1
        else:
            step = step + np.random.randint(1, 7)

        # Append next_step to random_walk
        random_walk.append(step)

    # Print random_walk
    print(random_walk)

## 📊 How low can you go? ##
    # NumPy is imported, seed is set
    import numpy as np
    np.random.seed(123)

    # Initialize random_walk
    random_walk = [0]

    for x in range(100):
        step = random_walk[-1]
        dice = np.random.randint(1, 7)

        if dice <= 2:
            # Use max to make sure step doesn't go below 0
            step = max(0, step - 1)
        elif dice <= 5:
            step = step + 1
        else:
            step = step + np.random.randint(1, 7)

        random_walk.append(step)

    print(random_walk)

## 📊 Visualize the walk ##
    # NumPy is imported, seed is set
    import numpy as np
    import matplotlib.pyplot as plt
    np.random.seed(123)

    # Initialization
    random_walk = [0]

    for x in range(100):
        step = random_walk[-1]
        dice = np.random.randint(1,7)

        if dice <= 2:
            step = max(0, step - 1)
        elif dice <= 5:
            step = step + 1
        else:
            step = step + np.random.randint(1,7)

        random_walk.append(step)

    # Plot random_walk
    plt.plot(random_walk)

    # Show the plot
    plt.show()

## 📊 Simulate multiple walks ##
    # NumPy is imported; seed is set
    import numpy as np
    np.random.seed(123)

    # Initialize all_walks (don't change this line)
    all_walks = []

    # Simulate random walk five times
    for i in range(5):

        # Code from before
        random_walk = [0]
        for x in range(100):
            step = random_walk[-1]
            dice = np.random.randint(1,7)

            if dice <= 2:
                step = max(0, step - 1)
            elif dice <= 5:
                step = step + 1
            else:
                step = step + np.random.randint(1,7)
            random_walk.append(step)

        # Append random_walk to all_walks
        all_walks.append(random_walk)

    # Print all_walks
    print(all_walks)

## 📊 Visualize all walks ##
    # numpy and matplotlib imported, seed set
    import numpy as np
    import matplotlib.pyplot as plt

    # initialize and populate all_walks
    all_walks = []
    for i in range(5):
        random_walk = [0]
        for x in range(100):
            step = random_walk[-1]
            dice = np.random.randint(1, 7)
            if dice <= 2:
                step = max(0, step - 1)
            elif dice <= 5:
                step = step + 1
            else:
                step = step + np.random.randint(1, 7)
            random_walk.append(step)
        all_walks.append(random_walk)

    # Convert all_walks to NumPy array: np_aw
    np_aw = np.array(all_walks)

    # Plot np_aw and show
    plt.plot(np_aw)
    plt.show()

    # Clear the figure
    plt.clf()

    # Transpose np_aw: np_aw_t
    np_aw_t = np.transpose(np_aw)

    # Plot np_aw_t and show
    plt.plot(np_aw_t)
    plt.show()

## 📊 Implement clumsiness ##
    # numpy and matplotlib imported, seed set
    import numpy as np
    import matplotlib.pyplot as plt
    np.random.seed(123)

    # clear the plot so it doesn't get cluttered if you run this many times
    plt.clf()

    # Simulate random walk 20 times
    all_walks = []
    for i in range(20):  # Changed from 5 to 20
        random_walk = [0]
        for x in range(100):
            step = random_walk[-1]
            dice = np.random.randint(1,7)
            if dice <= 2:
                step = max(0, step - 1)
            elif dice <= 5:
                step = step + 1
            else:
                step = step + np.random.randint(1,7)

            # Implement clumsiness
            if np.random.rand() <= 0.005:  # 0.5% chance of falling down
                step = 0

            random_walk.append(step)
        all_walks.append(random_walk)

    # Create and plot np_aw_t
    np_aw_t = np.transpose(np.array(all_walks))
    plt.plot(np_aw_t)
    plt.show()

## 📊 Plot the distribution ##
    # Import libraries
    import numpy as np
    import matplotlib.pyplot as plt

    # Set seed for reproducibility
    np.random.seed(123)

    # Simulate multiple random walks
    def simulate_walks(num_walks=500, num_steps=100, clumsiness=0.001):
        # Initialize all_walks list
        all_walks = []
        
        # Perform simulation num_walks times
        for i in range(num_walks):
            # Start at position 0
            random_walk = [0]
            
            # Take num_steps steps
            for x in range(num_steps):
                # Get current position
                step = random_walk[-1]
                
                # Roll the dice
                dice = np.random.randint(1, 7)
                
                # Determine next step based on dice roll
                if dice <= 2:
                    step = max(0, step - 1)  # Can't go below 0
                elif dice <= 5:
                    step = step + 1
                else:
                    step = step + np.random.randint(1, 7)
                    
                # Implement clumsiness - chance of falling down
                if np.random.rand() <= clumsiness:
                    step = 0
                    
                # Add step to random_walk
                random_walk.append(step)
                
            # Add this random_walk to all_walks
            all_walks.append(random_walk)
        
        return all_walks

    # Run simulation
    all_walks = simulate_walks(500, 100, 0.001)

    # Convert to NumPy array and transpose
    np_aw = np.array(all_walks)
    np_aw_t = np.transpose(np_aw)

    # Create first plot - visualize the random walks
    plt.figure(figsize=(10, 6))
    plt.plot(np_aw_t)
    plt.title('500 Random Walks')
    plt.xlabel('Step Number')
    plt.ylabel('Position')
    plt.grid(True, alpha=0.3)
    plt.show()

    # Clear the plot
    plt.clf()

    # Create second plot - histogram of endpoints
    ends = np_aw_t[-1]  # Get the last row (final positions)

    plt.figure(figsize=(10, 6))
    plt.hist(ends, bins=25, color='#30BFDD', edgecolor='white')
    plt.title('Distribution of Random Walk End Points')
    plt.xlabel('End Point')
    plt.ylabel('Frequency')
    plt.grid(True, alpha=0.3)
    plt.show()

    # Calculate probability of reaching at least 60 steps
    prob_success = np.mean(ends >= 60) * 100
    print(f"Probability of reaching at least 60 steps: {prob_success:.1f}%")

## 📊 Calculate the odds ##
C. 78.4%

## **ALHAMDULILLAH MODUL 2 KELAR**