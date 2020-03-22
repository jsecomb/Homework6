Homework 6 - Weather Dashboard

by Julian Secomb

Objective: To build a weather app that pulls weather data from Openweather APIs, updating dynamically. When the user enters a location, the app should render current weather conditions for that location, as well as a five day forecast. Each search should also be added to a search history section that includes buttons that can be clicked to re-search previously searched locations. When the page is opened, it should automatically load the last search.

Work done: Using an input field and a click listener, the user's search input is saved into a variable. This variable is passed into two functions that access Openweather's APIs using ajax. The first function (renderCurrent) pulls current weather conditions from Openweather's Weather API and formats/appends them to the page's html. It also pulls the geographical coordinates from the weather API response and passes them into the UV API so that UV conditons can also be rendered (UV data is not available in the Weather API). Once a search is performed, a corresponding button is created in the Search History section.

The second function (renderForecast) accesses Openweather's forecast API and pulls 5 day forecast data for the search input. A for loop is used to create a card for each of the five days and populate them with html elements that display the forecast data. A timeConverter function is used to convert the dates in the response from UNIX to conventional date format so that they display legibly on each day's card.

Finally, local storage is used to store the search input for the latest search done in the app. When the page is opened or refreshed, a search is automatically initiated on this value.


