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
| Jupyter Notebook Application 1     | Weather_Database.ipynb          | Generates a random list of cities and finds the current weather for each city.|
|                   | WeatherPy_challenge.csv         | Output File: contains location and current weather information for the randomly generated set of cities.|
| Jupyter Notebook Application 2     | Vacation_Search.ipynb           | Inputs the city information from application 1 and selects all cities with current weather information that meets the user's destination weather criteria. For each city that meets the destination weather criteria, the application executes a google search-nearby API request to find the nearest hotel for that city. Finally, the application plots these selected cities on a google map with individual location markers for each city.|
|                   | WeatherPy_challenge.csv         | Input Flle: output from application with city location and weather information.|
|                   | WeatherPy_vacation.csv          | Output File: contains location, current weather, and hotel information for cities that meet the user's destination weather criteria.|
|                   | WeatherPy_vacation_map.png      | Output File: image of google location map which displays the location each city that meets the user's destination weather criteria. Each city is represented by a location marker which when clicked is configured to display a popup information window with information about that city.|
|                   | WeatherPy_vacation_map_zoom.png | Output File: a zoomed image of the google location map which shows a close up of a city location marker and the popup information window that displays detailed information for that city.|
|  Jupyter Notebook Application 3    | Vacation_Itinerary.ipynb        | Inputs the city information from application 2 and generates a google directional map displaying a sample of 4 cities that are geographically near each other. Each city is represented by an individual location marker. The city location markers are connected by highlighted roads that can be used to travel between the cities. Also, this application generates a marker layer google map with location markers for each city that are configured to display a popup information window with information about the city when the location marker is clicked.|
|                   | WeatherPy_vacation.csv          | Input File: contains location, current weather, and hotel information for the cities selected by application 2.|
|                   | WeatherPy_travel_map.png        | Output File: image of the google directional map for the 4 selected cities with the cities connected by highlighted roads between them.|
|                   | WeatherPy_travel_map_markers.png | Output File: image of the google marker map for the 4 selected cities with  popup informational windows displayed for some of the 4 cities.|

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
   * Configures location markers to display a popup information window when clicked which displayes
       * Hotel name for that city
       * The city name 
       * The country abrieviation
       * A current weather discription including the current max temperature for that day
#### Output: 
1. WeatherPy_vacation.csv
   * A csv file containing location, weather, and hotel information for the cities that meet the user's weather criteria
2. WeatherPy_vacation_map.png
    * A image of the google location map with marker for each city that meets the weather criteria

<img src="https://github.com/berndab/world_weather_analysis/blob/master/WeatherPy_vacation_map.png" width="800" height="250" />

3. WeatherPy_vacation_map_zoom.png
    * A zoomed in image of the google location map showing the city location marker and with the popup information window displayed

<img src="https://github.com/berndab/world_weather_analysis/blob/master/WeatherPy_vacation_map_zoom.png" width="800" height="250" />

### Application 3: Vacation_Itinerary.ipynb
#### Input:
* WeatherPy_vacation.csv
  * Contains location, current weather, and hotel information for the cities selected in application 2 that meet the user's destination weather criteria
#### Description:
* Takes a sample of 4 geographically local cities and 
  * Creates a google direction map
  * Creates a google marker map with a marker at the location of each city selected in application 2
   * Configures city location markers to display a popup information window when clicked which displays
       * Hotel name for that city
       * The city name 
       * The country abrieviation
       * A current weather discription including the current max temperature for that day

#### Output:
* WeatherPy_travel_map.png
  * Image of the google directional map for the 4 selected cities

<img src="https://github.com/berndab/world_weather_analysis/blob/master/WeatherPy_travel_map.png" width="800" height="250" />

* WeatherPy_travel_map_markers.png
  * Image of the google marker map for the 4 selected cities with popup informational windows displayed for some of the cities

<img src="https://github.com/berndab/world_weather_analysis/blob/master/WeatherPy_travel_map_markers.png" width="800" height="250" />

