

![mod-6-challenge](Images/mod_6_background_img.JPG)

# San Francisco Real Estate Markets

## Requirements
### Calculate and Plot the Housing Units per Year
  * Must use the groupby function to group the data by year. Aggregate the results by the mean of the groups
  * Must use the hvplot function to plot the housing_units_by_year DataFrame as a bar chart. Make the x-axis represent the year and the y-axis represent the housing_units.
  * Style and format the line plot to ensure a professionally styled visualisation.
  * Answer the following question:
    * What’s the overall trend in housing units over the period that you’re analysing?

### Calculate and Plot the Average Sale Prices per Square Foot
To receive all points, you must:
  * Group the data by year, and then average the results. What’s the lowest gross rent that’s reported for the years that the DataFrame includes?
  * Create a new DataFrame named prices_square_foot_by_year by filtering out the “housing_units” column. The new DataFrame should include the averages per year for only the sale price per square foot and the gross rent.
  * Use hvPlot to plot the prices_square_foot_by_year DataFrame as a line plot.
  * Style and format the line plot to ensure a professionally styled visualisation.
  * Use both the prices_square_foot_by_year DataFrame and interactive plots to answer the following questions:
    * Did any year experience a drop in the average sale price per square foot compared to the previous year?
    * Did the gross rent increase or decrease during that year?

### Compare the Average Sale Prices by Neighbourhood
To receive all points, you must:
  * Create a new DataFrame that groups the original DataFrame by year and neighbourhood. Aggregate the results by the mean of the groups.
  * Filter out the “housing_units” column to create a DataFrame that includes only the sale_price_sqr_foot and gross_rent averages per year.
  * Create an interactive line plot with hvPlot that visualises both sale_price_sqr_foot and gross_rent. Set the x-axis parameter to the year (x="year"). Use the groupby parameter to create an interactive widget for neighbourhood.
  * Style and format the line plot to ensure a professionally styled visualisation.
  * Use the interactive visualisation to answer the following question:
    * For the Anza Vista neighbourhood, is the average sale price per square foot for 2016 more or less than the price that’s listed for 2012?

### Build an Interactive Neighbourhood Map
To receive all points, you must:
  * Read the neighbourhood_coordinates.csv file from the Resources folder into the notebook, and create a DataFrame named neighbourhood_locations_df. Be sure to set the index_col of the DataFrame as “Neighbourhood”.
  * Using the original sfo_data_df Dataframe, create a DataFrame named all_neighbourhood_info_df that groups the data by neighbourhood. Aggregate the results by the mean of the group.
  * Review the two code cells that concatenate the neighbourhood_locations_df DataFrame with the all_neighbourhood_info_df DataFrame. Note that the first cell uses the Pandas concat function to create a DataFrame named all_neighbourhoods_df. The second cell cleans the data and sets the “Neighbourhood” column. Be sure to run these cells to create the all_neighbourhoods_df DataFrame, which you’ll need to create the geospatial visualisation.
  * Create a points plot for the all_neighbourhoods_df DataFrame.
    * Use the hvPlot points function.
      * Set the geo parameter to True.
      * Set the size parameter to “sale_price_sqr_foot”.
      * Set the color parameter to “gross_rent”.
      * Set the frame_width parameter to 700.
      * Set the frame_height parameter to 500.
      * Include a descriptive title.
  * Use the interactive map to answer the following question:
    * Which neighbourhood has the highest gross rent, and which has the highest sale price per square foot?
    * _Answer:_ Westwood Park has the highest gross rent which also has the highest sale price per sq/ft

### Compose Your Data Story
To receive all points, you must:
  * Based on the visualisations that you created, answer the following questions:
    * How does the trend in rental income growth compare to the trend in sales prices? Does this same trend hold true for all the neighbourhoods across San Francisco?
    * **Answer:** Trends for Rental Income and sale prices have grown across all the neighborhoods of San Francisco. However, the gross rental of Westwood Highlands is less compared to Bayview, its sales price is lower than Westwood Highlands.
    * What insights can you share with your company about the potential one-click, buy-and-rent strategy that they're pursuing? Do neighbourhoods exist that you would suggest for investment, and why?
    * **Answer:** Potentially, one-click, buy-and-rent strategy would work as investments for neighbourhoods around San Francisco. Housing size may vary but, the trend in Gross rental income shows growth every year.
