# Weather App (Assignment 7)

## Description
This is a simple Weather App developed for Assignment 7 (Data & Networking).
The application allows users to search for a city and view current weather data and a short forecast.

## Features
- Search weather by city name
- Current temperature, humidity, and wind speed
- 3-day weather forecast
- Unit switch (Celsius / Fahrenheit)
- Offline mode using cached data
- Error handling for invalid city names

## API Used
- Open-Meteo Weather API
- Open-Meteo Geocoding API

## Technologies
- Kotlin
- Android Studio
- Jetpack Compose
- Retrofit + Gson
- MVVM Architecture
- SharedPreferences (offline cache)

## How to Run
1. Open the project in Android Studio
2. Run the app on an emulator or physical device
3. Enter a city name and press Search

## Offline Mode
The last successful weather response is saved locally.
If there is no internet connection, the app shows cached data with an OFFLINE indicator.
