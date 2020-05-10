# World Weather Analysis

## Purpose
Generate weather data to assist in selecting travel destinations

## Project Files

1. Weather_Database.ipynb
   * Jupyter Notebook application 
      * Generates a random list if cities and finds the current weather for those cities
   * Output: 
      * WeatherPy_challenge.csv
          * A csv file of the cities and current weather data for those cities 

2. Vacation_Search.ipynb
   * Input:
      * WeatherPy_challenge.csv from Weather_Database Jupyter Notebook
   * Jupyter Notebook application
      * Prompts user to enter the weather conditions desired for travel destination cities
      * Selects a list of cities from cities current weather database that meet the desired destination weather conditions
      * Finds a nearby hotel in each city
      * If no nearby hotel is found for a city, the city is deleted from the list
      * Creates a google map
         * The map has a marker for each city that meets user's destination weather criteria 
         * Clicking a map city marker display a popup with the following information
             * Hotel name for that city
             * The city name 
             * The country abrieviation
             * A current weather discription including the current max temperature for that day
   * Output: 
      1. WeatherPy_vacation.csv
         * A csv file of all the cities where a hotel can be located along with current weather data for that city
      2. WeatherPy_vacation_map.png
          * A image of the google map with marker for each city
      3. WeatherPy_vacation_map_zoom.png
          * A zoomed in image of the google map with a marker clicks and the marker popup displayed

3. Vacation_Search.ipynb
   * Jupyter Notebook application 
