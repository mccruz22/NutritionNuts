# NutritionNuts

by Amaris Williams, Madelyn Cruz, Jakeah Phifer

Using USDA's Food and Nutrient Database, we built this project which allows a user to input a food item, and the program spits out a few suggestions for side dishes that would make a balanced meal. 

In the README, we describe the data gathering process, the preprocessing and cleanup, the chosen encodings of the pocasts, and the Streamlit app.


# Project Goals
The goal of this project is to provide end users with an easy to use tool that can help them plan meals and have a healthy diet.

# Preprocessing and cleanup

For this project, we mainly used [USDA National Nutrient Database for Standard Reference, Release 28(2016)](https://www.ars.usda.gov/northeast-area/beltsville-md-bhnrc/beltsville-human-nutrition-research-center/methods-and-application-of-food-composition-laboratory/mafcl-site-pages/sr11-sr28/) which contains data for 8790 food items with corresponding nutrient values presented per 100 grams. At most two household measures per food item are also included in the dataset which makes it possible for users to measure their food based on the common household measures. Using this, we obtain the data frame total_amount_per_common_measure_df. This converted data frame is in the recommendation. We also used the Reference Daily Intakes provided by the U.S. Food and Drug Administration to ensure balanced meal suggestions and the NHANES dietary recall data so that food suggested are almost readily available (based on the popularity).

We filled all blank fields with a value of ‘0’, removed all unnecessary nutrient columns, and finally, removed baby food and spices. 

# Installation

This desktop application uses pyqt. Install `pyqt6` (for pip, pip install pyqt6).

<div> Icons made by <a href="https://www.flaticon.com/authors/pause08" title="Pause08"> Pause08 </a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com'</a></div>

# Approach

We employed different clustering methods to cluster food groups, then compared them and used the most accurate clustering method. Our aim was to group similar foods together based on their characteristics. After clustering, we utilized target values from the Reference Daily Intakes data set and computed food nutrients based on the common household measures to optimize the selection of foods for a meal. We aimed to find the ideal combination of 3 or 4 foods that would meet the desired nutritional requirements and create a balanced meal.

# Files

1. **NutritionNuts.ipynb** - Desktop Application
2. **Nutrition.ipynb** - Data Analysis and Unsupervised Learning Methods

