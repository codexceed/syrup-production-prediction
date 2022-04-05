# Grople Syrup Production Prediction using Machine Learning

## Premise
This is a solution to a machine learning challenge involving analysis of the seasonal factors for the production of **Grople Syrup** and predicting production given seasonal data (i.e. dates)

## Goal:
We have been given the monthly production quantity for a certain agricultural product (let’s call it Grople syrup, note - no relation to actual Maple Syrup) in 10 different provinces of a country between January 2015 to December 2020. This Grople syrup comes from a fruit. It takes a few months for the fruits to grow on the trees which bear them. It also takes a few days to extract the syrup from the fruits after they have been harvested.

**We would like to predict the production quantity for Grople syrup from Jan 2021 to Dec 2021.** 
### Data:
- **`Production Quantity.csv`** has 4 columns:
  - `start_day` and `end_day` of each month between January
  2015 to Dec 2020. 
  - `prod`: production quantity of Grople syrup in tonnes at monthly frequency 
  - `region_id`: A unique identifier for the 10 provinces
- **`Daily Precipitation.csv`** has 4 columns
  - `start_day` and `end_day` at a daily frequency between January 1, 2014 to Mar 13, 2022.
  - `precip`: Precipitation quantity (in mm) at daily frequency
  - `region_id`: A unique identifier for the 10 provinces 
- **`Daily Soil Moisture.csv`** has 4 columns 
  - `start_day` and `end_day` at daily frequency between January 1, 2014 to Mar 6, 2022. 
  - `smos`: Soil Moisture at 5cm depth (measured by the ratio Vol/Vol) at daily frequency
  - `region_id`: A unique identifier for the 10 provinces
- **`Daily Temperature.csv`** has 4 columns 
  - `start_day` and `end_day` at daily frequency between January 1, 2014 to Mar 13, 2022.
  - `temp`: Average daily temperature on the surface of the land (in celsius) at daily frequency 
  - `region_id`: A unique identifier for the 10 provinces : has 4 columns
- **`Eight Day NDVI.csv`**: has 4 columns
   - `start_date`,`end_date`: start day and end day at 8-day frequency between Dec 27, 2013 to Mar 13, 2022. 
   - `ndvi`: Normalized Difference Vegetation Index (NDVI is a ratio which ranges between $$[-1, 1]$$ and captures the vegetation abundance of an area) at 8 day frequency between the given periods
   - `region_id`: A unique identifier for the 10 provinces
- **`predicted_production_qty.csv`**: has 4 columns 
  - `start_day` and `end_day` of each month between Jan 2021 to Dec 2021. 
  - `prod`: This column needs to be filled by the candidate with their predictions of Grople syrup. 
  - `region_id`:A unique identifier for the 10 provinces

## Notebook Solution
- Install requirements
```shell
pip install -r requirements.txt
```
- Run a jupyter notebook session
```shell
jupyter notebook
```
- Run all blocks in the notebook