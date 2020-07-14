# Flatiron_Project1

Project1 is a multiple regression based model that predicts house prices for King County, Washington.

## Table of contents
* [General info](#general-info)
* [Key Files](#files)
* [Technologies](#technologies)
* [Setup](#setup)

## General info
The final model has 71 features that explain over 80% of the variability in the price of properties in the King County data set that sold for up to $2 million and exhibit the following features/characteristics:
* bedrooms >1, <=5
* sqft_lot < 250000
* sqft_lot15 < 350000
* sqft_living >= 1000, <= 4000
* long > -122.4, < -122
* lat >= 47.3

All features were either log transformed, scaled or evaluated as categorical variables. Normality and heteroskedasticity were greatly improved, but they remain imperfect for linear regression.

Zipcodes, bedrooms, floors, view, and condition are evaluated as categorical variables, and feature significance was evaluated both including and excluding zipcodes. The final model does include zipcodes, but the zipcodes listed below were dropped based on failing to meet significance criteria (feature p-values must be < 0.05).
Dropped features:
* 'sqft_lot15_log',
* 'long',
* 'floors_3.0', 'floors_3.5',
* 'condition_3',
* 'zipcode_98003', 'zipcode_98023', 'zipcode_98028', 'zipcode_98030', 'zipcode_98031', 
* 'zipcode_98042', 'zipcode_98055', 'zipcode_98148', 'zipcode_98155', 'zipcode_98198

The top 5 non-zipcode features, with ranks shown, are: (5) 'sqft_living', (4) 'waterfront', (3) 'view_3.0', (2) 'view_4.0', (1) 'lat.' Thus, location, square footage, the best views and whether the property is on water impact price the most.

## Key Files
* student.ipynb  - Jupyter notebook, walk through of dataset analysis and model
* kc_house_data.csv - csv file containing the King County house sales dataset
* column_names.md - file containing explanation of file names
* presentation.ppx - Powerpoint presentation of analysis, model summary and results
* README.md

## Technologies
Project is created with:
* Python - Anaconda download recommended for required datascience packages
* Jupyter Notebook
	
## Setup
To run this project, install it locally by forking this project and downloading. Run

```
$ cd ../yournewfolder
$ yournewfolder: jupyter notebook
```

