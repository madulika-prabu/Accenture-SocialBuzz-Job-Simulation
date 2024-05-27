# Accenture SocialBuzz Job Simulation

## Overview

Welcome to the Accenture SocialBuzz Job Simulation! This README will guide you through the data sets provided, the data model, and the steps to analyze the data to answer specific business questions.

### Data Sets

There are 3 data sets provided, each containing different columns and values. These data sets are crucial for understanding social media trends and interactions. They include:

1. **Reaction**: Contains data on user reactions to various social media content.
2. **Content**: Provides information about the social media content itself.
3. **Reaction Types**: Defines different types of reactions users can have.

### Data Model

The data model illustrates the relationships between all data sets and any links that can be used to merge tables. Understanding this model is essential for effectively analyzing the data.
 
 ![image](https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/6ff99910-aa97-4fd6-b7c2-77cac457bb88)

### Steps for Analysis

To ensure you're using the correct data to answer business questions, follow these steps:

1. **Requirements Gathering**
2. **Data Cleaning**
3. **Data Modelling**
4. **Data Analysis**
5. **Data Visualization**
6. **Presentation in the form of storytelling**

### Business Question

The primary business question for this simulation is to determine the top 5 categories with the largest popularity on social media.

## Steps to Answer the Business Question

1. **Create a Final Data Set**

   Merge the relevant data sets together to form a final comprehensive data set. We recommend using the Reaction table as the base table, then joining relevant columns from the Content data set, and finally adding data from the Reaction Types data set. You can use formulas like "VLookUp" to facilitate this process.

2. **Figure Out the Top 5 Performing Categories**

   Calculate the total scores for each category by summing up the relevant metrics. You can utilize formulas like "Sum If" to efficiently perform this calculation.

## Conclusion

By following these steps and leveraging the provided data sets and model, you can effectively analyze social media trends and identify the top-performing categories. Good luck with the simulation!
