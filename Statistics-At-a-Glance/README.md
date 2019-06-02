### Project Overview

 The rise of superheroes and supervillains is at an all time high. The 'Academy of Super Beings(ASB)' was formed to bring order to it. We have with us the data of more than 500 super humans but we need your knowledge of descriptive statistics in figuring out the important insights from it.


### Learnings from the project

 After completing this project, you will have a better grip on the applications of descriptive statistics. In this project, you will be applying the following concepts:

Bar plotting
Boxplot plotting
Pie-chart plotting
Subplot operations
Feature Correlation
IQR operations


### Approach taken to solve the problem

 The dataset has details of 594 super hero characters with the following 17 features.

**Feature	Description**
ID	Unique character ID
Name	Name of the character
Gender	Male/Female
Intelligence	Intelligence points of the character
Strength	Strength points of the character
Speed	Speed points of the character
Durability	Durability points of the character
Power	Power points of the character
Combat	Combat points of the character
Total	Total sum of all the above points of the character
Height	Height of the character(-99 value equates to 'immeasurable')
Weight	Weight of the character(-99 value equates to 'immeasurable')
SkinColor	Skin color of the the character
EyeColor	Eye color of the character
HairColor	Hair color of the character
Race	Which race the character belongs to


**Data loading**
First, we have to load data to do any sort of descriptive statistics

Load the dataframe from the variable 'path' and store the dataframe in a variable called 'data'.

In the column Gender, replace '-' with 'Agender' using "replace()" function.

            Example of  replace function:
df = pd.DataFrame({ 'ID': [0, 1, 2, 3, 4],
                    'Name': ['A', 'B', 'C', 'D', 'E'],
                    'Score': [10, 4, 13, 7, 25]})
print(df)
df['Score'].replace(10, 15,inplace=True)
print("\nAfter replacing value in score column:")
print(df)
Output:

ID Name  Score
0   0    A     10
1   1    B      4
2   2    C     13
3   3    D      7
4   4    E     25

After replacing value in score column:
   ID Name  Score
0   0    A     15
1   1    B      4
2   2    C     13
3   3    D      7
4   4    E     25
Save the value counts of Gender in a variable called 'gender_count' using "value_counts()".

Plot a bar graph of 'gender_count'
****
Heroes Alignment****
Heroes Alignment
Next we are interested to know what's the stand of the members of 'ASB'. Does good overpower evil or does evil overwhelm good? Let's find out.

Save the value counts of Alignment in a variable called 'alignment' using "value_counts()".

Plot the pie chart of 'alignment'.

Label the plot as Character Alignment

Things to ponder upon:
        - Would there be any change in the majority 'alignment' if the ones in neutral all took one side?
**Combat Correlation**
Combat Correlation
For any of the members, combat skills are really important to survive when they find themselves in unwanted situtations. But does combat relate to person's strength or it's intelligence? Let's find out

Create a subset of 'data' having only the columns ['Strength','Combat'] and save it in a variable called 'sc_df'.

Calcaulate the covariance between two variables and save the value into a variable named sc_covariance.

Find the standard deviation of column Strength and store it in a variable called 'sc_strength'.

Find the standard deviation of column Combat and store it in a variable called 'sc_combat'.

Using the above created variables, find the pearson's correlation coefficient between Strength & Combat and store it in a variable called sc_pearson.

Do the above steps similarly for the columns Intelligence and Combat and store them in appropriate variable names(i.e. Save the covariance between them in a variable called 'ic_covariance' and so on and so forth)

Things to ponder upon:
            - Based on the above calculations, which attribute is more correlated to combat? Strength or Intelligence?

            - Why did we use Pearson's correlation instead of Spearman?
**Overpowered Super Beings?**
Who are the best of the best in this superhero universe? Let's find out.

Calculate the value of quantile=0.99 for the column Total and store the value in variable named total_high.

Subset the dataframe 'data' based on column Total's value greater than 'total_high' and store the dataframe subset in a variable called 'super_best'

Create a list of the names from 'Name' assosicated with 'super_best' dataframe and save it in a variable called super_best_names

Print the list to see the top superheroes/villains
**Statistics for Survival**
Of the top 1% members of 'ASB', we want to measure certain attributes in case they go rogue and become threatening to the human kind.

Create three subplots with axes as 'ax_1', 'ax_2', 'ax_3'.

Plot a boxplot of Intelligence column using ax_1. Set axis title as Intelligence.

Plot a boxplot of Speed column using ax_2. Set axis title as Speed

Plot a boxplot of Power column using ax_3. Set axis title as Power

Things to ponder upon:
        - Given the fact that the above atributes have their ranges from 0-100, which among them is the 
          one with the most disperse values(i.e. spread across a larger range of values)? least disperse values?

        - If the entire humanity has to fight against any one of these top super beings, improving what 
          atribute of a normal human would be our best chance for survival



