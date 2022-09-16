

![mod-6-challenge](Images/mod_6_background_img.JPG)

# San Francisco Real Estate Markets

## Requirements
### Calculate and Plot the Housing Units per Year
  * Must use the groupby function to group the data by year. Aggregate the results by the mean of the groups
  * Must use the hvplot function to plot the housing_units_by_year DataFrame as a bar chart. Make the x-axis represent the year and the y-axis represent the housing_units.
  * Style and format the line plot to ensure a professionally styled visualisation. (2 points)
  * Answer the following question:
    * What’s the overall trend in housing units over the period that you’re analysing? (4 points)

### Calculate and Plot the Average Sale Prices per Square Foot (10 points)
To receive all points, you must:
  * Group the data by year, and then average the results. What’s the lowest gross rent that’s reported for the years that the DataFrame includes?
  * Create a new DataFrame named prices_square_foot_by_year by filtering out the “housing_units” column. The new DataFrame should include the averages per year for only the sale price per square foot and the gross rent. (2 points)
  * Use hvPlot to plot the prices_square_foot_by_year DataFrame as a line plot. (2 points)
  * Style and format the line plot to ensure a professionally styled visualisation. (2 points)
  * Use both the prices_square_foot_by_year DataFrame and interactive plots to answer the following questions:
    * Did any year experience a drop in the average sale price per square foot compared to the previous year? (1 point)
    * Did the gross rent increase or decrease during that year? (1 point)

### Compare the Average Sale Prices by Neighbourhood (20 points)
To receive all points, you must:
  * Create a new DataFrame that groups the original DataFrame by year and neighbourhood. Aggregate the results by the mean of the groups. (4 points)
  * Filter out the “housing_units” column to create a DataFrame that includes only the sale_price_sqr_foot and gross_rent averages per year. (4 points)
  * Create an interactive line plot with hvPlot that visualises both sale_price_sqr_foot and gross_rent. Set the x-axis parameter to the year (x="year"). Use the groupby parameter to create an interactive widget for neighbourhood. (4 points)
  * Style and format the line plot to ensure a professionally styled visualisation. (4 points)
  * Use the interactive visualisation to answer the following question:
    * For the Anza Vista neighbourhood, is the average sale price per square foot for 2016 more or less than the price that’s listed for 2012? (4 points)

### Build an Interactive Neighbourhood Map (20 points)
To receive all points, you must:
  * Read the neighbourhood_coordinates.csv file from the Resources folder into the notebook, and create a DataFrame named neighbourhood_locations_df. Be sure to set the index_col of the DataFrame as “Neighbourhood”. (3 points)
  * Using the original sfo_data_df Dataframe, create a DataFrame named all_neighbourhood_info_df that groups the data by neighbourhood. Aggregate the results by the mean of the group. (3 points)
  * Review the two code cells that concatenate the neighbourhood_locations_df DataFrame with the all_neighbourhood_info_df DataFrame. Note that the first cell uses the Pandas concat function to create a DataFrame named all_neighbourhoods_df. The second cell cleans the data and sets the “Neighbourhood” column. Be sure to run these cells to create the all_neighbourhoods_df DataFrame, which you’ll need to create the geospatial visualisation. (3 points)
  * Create a points plot for the all_neighbourhoods_df DataFrame.
    * Use the hvPlot points function. (1 point)
      * Set the geo parameter to True. (1 point)
      * Set the size parameter to “sale_price_sqr_foot”. (1 point)
      * Set the color parameter to “gross_rent”. (1 point)
      * Set the frame_width parameter to 700. (1 point)
      * Set the frame_height parameter to 500. (1 point)
      * Include a descriptive title. (2 points)
  * Use the interactive map to answer the following question:
    * Which neighbourhood has the highest gross rent, and which has the highest sale price per square foot? (3 points)

### Compose Your Data Story (10 points)
To receive all points, you must:
  * Based on the visualisations that you created, answer the following questions:
    * How does the trend in rental income growth compare to the trend in sales prices? Does this same trend hold true for all the neighbourhoods across San Francisco? (5 points)
    * What insights can you share with your company about the potential one-click, buy-and-rent strategy that they're pursuing? Do neighbourhoods exist that you would suggest for investment, and why? (5 points)
