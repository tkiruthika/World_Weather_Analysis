# World_Weather_Analysis

## Overview

Te overview of this module is to collect and analyze weather data across cities worldwide.
## Purpose

The purpose of the analysis is to 
  - Retrieve Weather Data
  - Create a Customer Travel Destinations Map
  - Create a Travel Itinerary Map
## Deliverable 1 : Retrieve Weather Data

  - A new set of 2,000 random latitudes and longitudes are created.
  - The **citipy** module is used to get the nearest city.
  - API call is performed with the **OpenWeatherMap** to retrieve **Latitude and longitude, Maximum temperature, Percent humidity, Percent cloudiness, Wind speed, and Weather description (for example, clouds, fog, light rain, clear sky)**
  - The retrieved data is added to the new dataframe and saved in [WeatherPy_database.csv](https://github.com/tkiruthika/World_Weather_Analysis/files/8009838/WeatherPy_database.csv)
  
## Deliverable 2: Create a Customer Travel Destinations Map

  - **WeatherPy_Database.csv** file is imported as a DataFrame.
  - Two input statements that prompt the user to enter their minimum and maximum temperature criteria for their vacation are written.
  - The **loc** method to filter the DataFrame for minimum and maximum temperature.
  - The dataframe is checked for empty rows.
  - The new dataframe is created **hotel_df**, to hold the hotel names from the hotel search.
  - The search parameters are used to search for a hotel for each city.
  - Iterate through the **hotel_df** DataFrame, retrieve the latitude and longitude of each city to find the nearest hotel based on the search parameters.
  - Output file to store the hotel_df DataFrame as [WeatherPy_vacation.csv](https://github.com/tkiruthika/World_Weather_Analysis/files/8009860/WeatherPy_vacation.csv)
  - Format the **info_box_template** to add the city name, the country code, the weather description, and the maximum temperature for the city.
  - Retrieve the city data from each row, which will then be added to the formatting template and saved in the **hotel_info** list.
  - Create a marker layer map that will have pop-up markers for each city on the map.
  
  ![WeatherPy_vacation_map](https://user-images.githubusercontent.com/95719819/152675069-e0ca3007-9e91-48f1-8020-7f2d816475c8.png)
  
 ## Deliverable 3: Create a Travel Itinerary Map
  - The "Directions API" is enabled in our Google account for our API key.
  - The WeatherPy_vacation.csv file from your Vacation_Search folder from Deliverable 2 is imported as a DataFrame.
  - A marker layer map of the vacation search results is created.
  - From the vacation search map, four cities are chosen that a customer might want to visit.
  - Separate DataFrames for each city is created using **loc** method.
  - Retrieve the latitude-longitude pairs as tuples from each city using **to_numpy()** function with the list indexing.
  - Directions layer map is created with the help of gmaps documentation.
   
 ![WeatherPy_travel_map](https://user-images.githubusercontent.com/95719819/152675426-56212cd9-af63-4eb6-b552-d3e8c0e722db.png)

  - The four seperate city DataFrames are combined into one DataFrame using **concat()** function.
  - Marker layer map of the cities on the travel route is created.
  
  ![WeatherPy_travel_map_markers](https://user-images.githubusercontent.com/95719819/152675517-b57a912b-8268-4858-97be-4bc335375d17.png)
