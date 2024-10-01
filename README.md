Overview

This project is divided into two main parts: WeatherPy and VacationPy. In WeatherPy, we analyze the relationship between weather variables and latitude using Python requests, APIs, and JSON traversals. Specifically, we explore how temperature, humidity, cloudiness, and wind speed vary as we move closer to the equator. In VacationPy, we take this analysis further by narrowing down cities based on ideal weather conditions and identifying nearby hotels for vacation planning using the Geoapify API.
Part 1: WeatherPy
Objectives

Using the OpenWeatherMap API, we gather weather data from a randomly generated list of cities worldwide. We then create several scatter plots to analyze the relationship between latitude and various weather factors.
Features

    Weather Data Retrieval: Uses the OpenWeatherMap API to pull temperature, humidity, cloudiness, and wind speed data for a list of cities.
    Scatter Plots: Visualizes the relationship between latitude and four weather variables:
        Latitude vs. Temperature
        Latitude vs. Humidity
        Latitude vs. Cloudiness
        Latitude vs. Wind Speed
    Linear Regression Analysis: Computes and visualizes linear regressions for each weather variable by hemisphere (Northern and Southern) to identify trends.

Installation

    Clone the repository:

    bash

git clone https://github.com/the-eva-a/python-api-challenge.git

Install required libraries: The project uses pandas, matplotlib, requests, and citipy. Install them using pip:

bash

pip install pandas matplotlib requests citipy

Obtain API Keys: You will need API keys for:

    OpenWeather
    Geoapify

Run the analysis: The main script for weather data retrieval and analysis is located in the WeatherPy directory.

bash

    python WeatherPy/weather_analysis.py

Plots

You will generate the following scatter plots:

    Latitude vs. Temperature
    Latitude vs. Humidity
    Latitude vs. Cloudiness
    Latitude vs. Wind Speed

Additionally, the following linear regressions will be created:

    Northern Hemisphere vs. Southern Hemisphere for:
        Temperature vs. Latitude
        Humidity vs. Latitude
        Cloudiness vs. Latitude
        Wind Speed vs. Latitude

Part 2: VacationPy
Objectives

In this section, we build a map-based application to help users find vacation destinations with ideal weather conditions. We use the weather data collected in WeatherPy to filter cities based on desired temperature ranges. The Geoapify API is then used to locate hotels near those cities.
Features

    Mapping Cities: Displays a map with markers for each city in the dataset.
    Ideal Weather Filter: Filters the dataset for cities with specific weather conditions (e.g., comfortable temperature range).
    Hotel Search: Finds hotels within 10,000 meters of the filtered cities using the Geoapify API.
    Hover Information: Includes hotel names and countries in the hover messages for each city on the map.

Installation

Ensure you have the same libraries installed as in Part 1, and use the VacationPy script to run the vacation planning analysis.
How to Use

To find cities with ideal weather conditions:

    Adjust the temperature or weather conditions in the script.

    Run the following script in the VacationPy folder:

    bash

    python VacationPy/vacation_planning.py

    The map output will display cities and hotels based on your selected criteria.

Data

The data used in this project includes:

    Cities List: Generated using the citipy library based on random geographic coordinates.
    Weather Data: Fetched in real-time from the OpenWeatherMap API.
    Hotel Data: Retrieved using the Geoapify API based on city coordinates.

Results

Through the analysis, we observe:

    Latitude vs. Temperature: Temperature tends to increase as we move closer to the equator, with variations due to local climate factors.
    Latitude vs. Humidity/Cloudiness/Wind Speed: Similar relationships are explored, offering insights into how weather conditions change geographically.
    Vacation Planning: We successfully identified cities with ideal weather conditions and found nearby hotels to aid in vacation planning.

Acknowledgements

This project is part of the curriculum in the edX Data Analytics Bootcamp. Special thanks to my instructors and peers for their support and guidance.