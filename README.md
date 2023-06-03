# NutritionNuts

by Amaris Williams, Madelyn Cruz, Jakeah Phifer
Mentor: Evelyn Huszar

Using USDA's Food and Nutrient Database, we built this project which allows a user to input a food item, and the program spits out a few suggestions for side dishes that would make a balanced meal. 

In the README, we describe the data gathering process, the preprocessing and cleanup, the chosen encodings of the pocasts, and the Streamlit app.

# Table of Contents

1. [Project Goals](https://github.com/mccruz22/NutritionNuts#project-goals)
2. [Preprocessing and cleanup](https://github.com/mccruz22/NutritionNuts#preprocessing-and-cleanup)
3. [Installation](https://github.com/mccruz22/NutritionNuts#installation)
4. [Approach](https://github.com/mccruz22/NutritionNuts#approach)
5. [Files](https://github.com/mccruz22/NutritionNuts#files)

# Project Goals
The goal of this project is to provide end users with an easy to use tool that can help them plan meals and have a healthy diet.

# Preprocessing and cleanup

For this project, we mainly used [USDA National Nutrient Database for Standard Reference, Release 28(2016)](https://www.ars.usda.gov/northeast-area/beltsville-md-bhnrc/beltsville-human-nutrition-research-center/methods-and-application-of-food-composition-laboratory/mafcl-site-pages/sr11-sr28/) which contains data for 8790 food items with corresponding nutrient values presented per 100 grams. At most two household measures per food item are also included in the dataset which makes it possible for users to measure their food based on the common household measures. Using this, we obtain the data frame total_amount_per_common_measure_df. This converted data frame is utilized in the recommendation. We also used the **Reference Daily Intakes provided by the U.S. Food and Drug Administration** to ensure balanced meal suggestions and the **NHANES dietary recall data** so that food suggested are almost readily available (based on the popularity).

We filled all blank fields with a value of ‘0’, removed all unnecessary nutrient columns, and finally, removed baby food and spices. 

# Installation

This desktop application uses pyqt. Install `pyqt6` (for pip, pip install pyqt6).

<div> Icons made by <a href="https://www.flaticon.com/authors/pause08" title="Pause08"> Pause08 </a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com'</a></div>

# Approach

We utilized various clustering methods to categorize the complete dataset of 7,062 foods into different food groups and subgroups based on the USDA classification. The objective was to group similar foods together according to their characteristics. These clustering methods were compared, and the most accurate one was selected.

Once the clustering was completed, we utilized target values from the Reference Daily Intakes dataset and calculated the nutrient content of the foods based on common household measures. This allowed us to optimize the selection of foods for a meal. Our goal was to identify the ideal combination of 3 or 4 foods that would fulfill the desired nutritional requirements and create a well-balanced meal.

# Files

1. **NutritionNuts.ipynb** - Desktop Application
2. **Nutrition.ipynb** - Data Analysis and Unsupervised Learning Methods

