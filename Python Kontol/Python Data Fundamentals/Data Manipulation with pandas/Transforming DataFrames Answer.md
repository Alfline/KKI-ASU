بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ
Curated by Alfian

## 📊 Inspecting a DataFrame ##
    Instruction 1/4:
        # Print the head of the homelessness data
        print(homelessness.head())

    Instruction 2/4:
        # Print the head of the homelessness data
        print(homelessness.head())

        # Print information about homelessness
print(homelessness.info())

    Instruction 3/4:
        # Print the head of the homelessness data
        print(homelessness.head())

        # Print information about homelessness
        print(homelessness.info())

        # Print the shape of homelessness
        print(homelessness.shape)

    Instruction 4/4:
        # Print the head of the homelessness data
        print(homelessness.head())

        # Print information about homelessness
        print(homelessness.info())

        # Print the shape of homelessness
        print(homelessness.shape)

        # Print a description of homelessness
                print(homelessness.describe())

## 📊 Parts of a DataFrame ##
        # Import pandas using the alias pd
        import pandas as pd

        # Print the values of homelessness
        print(homelessness.values)

        # Print the column index of homelessness
        print(homelessness.columns)

        # Print the row index of homelessness
        print(homelessness.index)

## 📊 Sorting rows ##
    Instruction 1/3:
        # Sort homelessness by individuals (ascending)
        homelessness_ind = homelessness.sort_values(by="individuals")
        print(homelessness_ind.head())

    Instruction 2/3:
        # Sort homelessness by descending family members
        homelessness_fam = homelessness.sort_values(by="family_members", ascending=False)

        # Print the top few rows
        print(homelessness_fam.head())

    Instruction 3/3:
        # Sort homelessness by region, then descending family members
        homelessness_reg_fam = homelessness.sort_values(by=["region", "family_members"], ascending=[True, False])

        # Print the top few rows
        print(homelessness_reg_fam.head())

## 📊 Subsetting columns ##
    Instruction 1/3:
        # Select the individuals column
        individuals = homelessness["individuals"]

        # Print the first few rows of the Series
        print(individuals.head())

    Instruction 2/3:
        # Select the state and family_members columns
        state_fam = homelessness[["state", "family_members"]]

        # Print the first few rows of the DataFrame
        print(state_fam.head())

    Instruction 3/3:
        # Select only the individuals and state columns, in that order
        ind_state = homelessness[["individuals", "state"]]

        # Print the first few rows of the DataFrame
        print(ind_state.head())

## 📊 Subsetting rows ##
    Instruction 1/3:
        # Filter for rows where individuals is greater than 10000
        ind_gt_10k = homelessness[homelessness["individuals"] > 10000]

        # See the result
        print(ind_gt_10k)

    Instruction 2/3:
        # Filter for rows where region is Mountain
        mountain_reg = homelessness[homelessness["region"] == "Mountain"]

        # See the result
        print(mountain_reg)

    Instruction 3/3:
        # Filter for rows where family_members is less than 1000 
        # and region is Pacific
        fam_lt_1k_pac = homelessness[(homelessness["family_members"] < 1000) & (homelessness["region"] == "Pacific")]

        # See the result
        print(fam_lt_1k_pac)

## 📊 Subsetting rows by categorical variables ##
        # The Mojave Desert states
        canu = ["California", "Arizona", "Nevada", "Utah"]

        # Filter for rows in the Mojave Desert states
        mojave_homelessness = homelessness[homelessness["state"].isin(canu)]

        # See the result
        print(mojave_homelessness)

## 📊 Adding new columns ##
        # Import pandas
        import pandas as pd

        # Add total col as sum of individuals and family_members
        homelessness['total'] = homelessness['individuals'] + homelessness['family_members']

        # Add p_homeless col as proportion of total homeless population to the state population
        homelessness['p_homeless'] = homelessness['total'] / homelessness['state_pop']

        # See the result
        print(homelessness)

## 📊 Combo-attack! ##
        # Import pandas
        import pandas as pd

        # Create indiv_per_10k col as homeless individuals per 10k state pop
        homelessness["indiv_per_10k"] = 10000 * homelessness["individuals"] / homelessness["state_pop"]

        # Subset rows for indiv_per_10k greater than 20
        high_homelessness = homelessness[homelessness["indiv_per_10k"] > 20]

        # Sort high_homelessness by descending indiv_per_10k
        high_homelessness_srt = high_homelessness.sort_values(by="indiv_per_10k", ascending=False)

        # From high_homelessness_srt, select the state and indiv_per_10k cols
        result = high_homelessness_srt[["state", "indiv_per_10k"]]

        # See the result
        print(result)

