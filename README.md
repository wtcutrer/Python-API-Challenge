# Python API Homework- What's the Weather Like?

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: "Duh. It gets hotter..."

But, if pressed, how would you prove it?

## Part I - WeatherPY

In this example, I created a Python script to visualize the weather of 550 cities across the world of varying distance from the equator. To accomplish this, I utilized a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.

The first requirement was to create a series of scatter plots to showcase the following relationships:

* Latitude vs Max Temperature (F)

![City Latitude vs Max Temperature](https://user-images.githubusercontent.com/85977271/128943041-5962024b-30c6-45c6-9c05-1b1dae91561a.png)

* Latitude vs Humidity (%)

![City Latitude vs Humidity](https://user-images.githubusercontent.com/85977271/128943055-4e8fcecf-5b5a-4814-b7c9-1b4088012f74.png)

* Latitude vs Cloudiness (%)

![City Latitude vs Cloudiness](https://user-images.githubusercontent.com/85977271/128943076-28049641-7e0f-4edf-946a-b413310250f7.png)

* Latitude vs Wind Speed (mph)

![City Latitude vs Wind Speed (mph)](https://user-images.githubusercontent.com/85977271/128943092-7f7568ee-9005-4a0f-a2b2-b608ef2adf71.png)

The second requirement was to run linear regression on each relationship. This time, I separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Max Temperature (F) vs Latitude

![Northern Hemisphere - Max Temp vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128943120-65749db3-64ca-42b2-a454-3d1e70bb7ee8.png)

* Southern Hemisphere - Max Temperature (F) vs Latitude

![Southern Hemisphere - Max Temp vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128943227-9a26c480-8b97-43f4-afda-f64762977c8d.png)

* Northern Hemisphere - Humidity (%) vs. Latitude

![Northern Hemisphere - Humidity (%) vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128943154-60f1fa25-bca2-441a-a986-a09456e93abf.png)

* Southern Hemisphere - Humidity (%) vs. Latitude

![Southern Hemisphere - Humidity (%) vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128943253-9d88bb0b-766f-4d92-9ba0-321d10dfe0c7.png)

* Northern Hemisphere - Cloudiness (%) vs. Latitude

![Northern Hemisphere - Cloudiness (%) vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128943173-9a2b26ee-5163-41a6-9598-c271bea56f2b.png)

* Southern Hemisphere - Cloudiness (%) vs. Latitude

![Southern Hemisphere - Cloudiness (%) vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128943273-57ac20d1-4ba0-407e-9714-4e9e421e07cf.png)

* Northern Hemisphere - Wind Speed (mph) vs. Latitude

![Northern Hemisphere - Wind Speed vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128943194-72c17c29-67b6-4676-83ac-fd369e69825a.png)

* Southern Hemisphere - Wind Speed (mph) vs. Latitude

![Southern Hemisphere - Cloudiness (%) vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128943291-d649fd92-2249-4bbc-bb04-ccbb778db95b.png)

## Part II - VacationPy
On this part, I leveraged my skills in working with weather data to plan future vacations. I used jupyter-gmaps and the Google Places API for this part of the assignment.

To complete this part of the assignment, I did the following:

* Created a heat map that displays the humidity for every city from Part I.

![VacationPy_Humidity_Map](https://user-images.githubusercontent.com/85977271/128943310-49c7a059-d547-415e-b624-99a3d9ea4f26.PNG)

* I then narrowed down the DataFrame to find your ideal weather conditions.
  * A max temperature lower than 80 degrees but higher than 70.
  * Wind speed less than 10 mph.
  * Zero cloudiness.
  * And dropped any rows that don't contain all three conditions just to be sure the weather is ideal.
* I used Google Places API to find the first hotel for each city located within 5000 meters of my coordinates.
* And finally, I plotted the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

![VacationPy_Hotel_Map](https://user-images.githubusercontent.com/85977271/128943320-bb369bda-d42a-42bd-92a2-5229d150af46.PNG)

## It's Five O'clock Somewhere! Enjoy Your Vacation!

![Keep Calm](https://user-images.githubusercontent.com/85977271/128940504-a15ea54a-d97e-450d-91c0-2e2e4ce537d6.PNG)


