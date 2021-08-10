# Python API Homework- What's the Weather Like?

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: "Duh. It gets hotter..."

But, if pressed, how would you prove it?

## Part I - WeatherPY

In this example, I created a Python script to visualize the weather of 550 cities across the world of varying distance from the equator. To accomplish this, I utilized a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.

The first requirement was to create a series of scatter plots to showcase the following relationships:

* Latitude vs Max Temperature (F)

![City Latitude vs Max Temperature](https://user-images.githubusercontent.com/85977271/128939524-7bfebace-2bce-40a6-988f-1589fd8c4ea5.png)

* Latitude vs Humidity (%)

![City Latitude vs Humidity](https://user-images.githubusercontent.com/85977271/128939625-37eda1ed-040b-466a-a3ca-d79341fd928b.png)

* Latitude vs Cloudiness (%)

![City Latitude vs Cloudiness](https://user-images.githubusercontent.com/85977271/128939751-790084f8-278e-4e06-92c6-bd65eefcb6af.png)

* Latitude vs Wind Speed (mph)

![City Latitude vs Wind Speed (mph)](https://user-images.githubusercontent.com/85977271/128939835-e56978e2-eb5a-4797-933b-97f3803ac5e9.png)

The second requirement was to run linear regression on each relationship. This time, I separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Max Temperature (F) vs Latitude

![Northern Hemisphere - Max Temp vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128939905-babc39f8-6524-4b26-aafd-25af17f92869.png)

* Southern Hemisphere - Max Temperature (F) vs Latitude

![Southern Hemisphere - Max Temp vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128939981-1ed2dd27-82f3-4b8b-8ae0-99e2d6dac21e.png)

* Northern Hemisphere - Humidity (%) vs. Latitude

![Northern Hemisphere - Humidity (%) vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128940070-cd61dec4-f687-4b2a-80ff-a26b9de479d2.png)

* Southern Hemisphere - Humidity (%) vs. Latitude

![Southern Hemisphere - Humidity (%) vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128940102-f715ff44-f82e-43ec-b190-d24b9c978485.png)

* Northern Hemisphere - Cloudiness (%) vs. Latitude

![Northern Hemisphere - Cloudiness (%) vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128940178-85c45c23-07f6-4ecc-8a48-a95b32c3301a.png)

* Southern Hemisphere - Cloudiness (%) vs. Latitude

![Southern Hemisphere - Cloudiness (%) vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128940160-587d4875-a41e-48d5-8f3a-7417e3e4b6ef.png)

* Northern Hemisphere - Wind Speed (mph) vs. Latitude

![Northern Hemisphere - Wind Speed vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128940218-0a3a2681-c75f-4e4e-8f43-6444460142a3.png)

* Southern Hemisphere - Wind Speed (mph) vs. Latitude

![Southern Hemisphere - Wind Speed vs  Latitude Linear Regression](https://user-images.githubusercontent.com/85977271/128940247-825816ba-cb91-4f64-8e47-f230be8d4a9c.png)

## Part II - VacationPy
On this part, I leveraged my skills in working with weather data to plan future vacations. I used jupyter-gmaps and the Google Places API for this part of the assignment.

To complete this part of the assignment, I did the following:

* Created a heat map that displays the humidity for every city from Part I.

![VacationPy_Humidity_Heatmap](https://user-images.githubusercontent.com/85977271/128940674-8245b7e6-e21c-4856-a107-9740f9eda838.PNG)

* I then narrowed down the DataFrame to find your ideal weather conditions.
  * A max temperature lower than 80 degrees but higher than 70.
  * Wind speed less than 10 mph.
  * Zero cloudiness.
  * And dropped any rows that don't contain all three conditions just to be sure the weather is ideal.
* I used Google Places API to find the first hotel for each city located within 5000 meters of my coordinates.
* And finally, I plotted the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

![VacationPy_Hotels_Heatmaps](https://user-images.githubusercontent.com/85977271/128940338-9b2cf05a-49db-4cec-8090-38b0d6d306ca.PNG)

## It's Five O'clock Somewhere! Enjoy Your Vacation!

![Keep Calm](https://user-images.githubusercontent.com/85977271/128940504-a15ea54a-d97e-450d-91c0-2e2e4ce537d6.PNG)


