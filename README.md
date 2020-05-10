# World Weather Analysis

## Purpose
Generate weather data to assist in selecting travel destinations

## Project Files

|      Type         |             Name                |             Description            | 
--------------------|---------------------------------|------------------------------------|
| Programming Tools | Jupyter Notebook                |                                    |
| Program Language  | Python 3.7.7                    |                                    |
| APIs and Modules  | Anaconda 4.8.3                  |                                    |
|                   | Pandas 1.0.3                    |                                    |
|                   | Matplotlib 3.1.3                |                                    |
| Application 1     | Weather_Database.ipynb          | Generates a random list of cities and finds the current weather for each city|
|                   | WeatherPy_challenge.csv         | Output File: contains location and current weather information for the randomly generated set of cities|
| Application 2     | Vacation_Search.ipynb           | Inputs the city information from application 1 and selects all cities with current weather information that meet the user's destination weather criteria. For cities whose current weather meets the user's weather preferences, the application executes a google search-nearby request to find the neareast hotel for that city. Finally, the application plots the selected cities on a google map wih a marker for each selected city.|
|                   | WeatherPy_challenge.csv         | Input Flle: output from application 1|
|                   | WeatherPy_vacation.csv          | Output File: contains location, current weather, and hotel information for cities that meet the user's destination weather preferences|
|                   | WeatherPy_vacation_map.png      | Output File: image of google location map which displays a location marker for each selected city, When a location marker is clicked is has been configured to display a popup information window with information about that city|
|                   | WeatherPy_vacation_map_zoom.png | Output File: zoomed image of google location map markers which have been clicked and are displaying the popup information window for that city marker|
|  Application 3    | Vacation_Itinerary.ipynb        | Inputs the city information from application 2 and generates a google directional map linking a sample of 4 cities. In addition, the application generates a marker layer map with a location marker for each city in the 4 city sample which is configure to display a popup information window with information about that city when the location marker is clicked|
|                   | WeatherPy_vacation.csv          | Input File: contains location, current weather, and hotel information for the cities selected by application 2 |
|                   | WeatherPy_travel_map.png        | Output File: image of the google directional map for the 4 selected cities
|                   | WeatherPy_travel_map_markers.png | Output File: image of the google marker map for the 4 selected cities with  popup informational windows displayed for some of the 4 cities|

## Jupyter Notebook Applications Overview
### Application 1: Weather_Database.ipynb
#### Input:
None
#### Description:
This application generates a random list if cities and finds the current weather for all the cities in the generated list 
#### Output:
* WeatherPy_challenge.csv
   * A csv file of the cities and current weather data for those cities 

### Application 2: Vacation_Search.ipynb
#### Input:
* WeatherPy_challenge.csv 
  * The csv file from Weather_Database.ipynb containing city location and weather information
#### Description:
This application
* Prompts user to enter the desired weather desired for the travel destination
* Creates a list of cities whose current weather information meets the users's destination weather criteria
* For each city that the meets user's weather criteria the application:
  * Finds a hotel for each selected city
      * If no nearby hotel is found the city is deleted from the list
* Creates a google map with a location markers for each city that meets the weather criteria
   * Configures location markers to display a popup information window when clicke
   * The popup information window has the following information
       * Hotel name for that city
       * The city name 
       * The country abrieviation
       * A current weather discription including the current max temperature for that day
#### Output: 
1. WeatherPy_vacation.csv
   * A csv file containing location, weather, and hotel information for the cities that meet the user's weather criteria
2. WeatherPy_vacation_map.png
    * A image of the google location map with marker for each city that meets the weather criteria
3. WeatherPy_vacation_map_zoom.png
    * A zoomed in image of the google location map showing the city location marker and with the popup information window displayed
