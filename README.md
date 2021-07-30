# World_Weather_Analysis  

## Purpose  

The purpose of this analysis was to create an application on the travel company's website that would enable clients to select vacation destinations already pre-filtered for optimal weather conditions.  

## Resources/Dependencies  

Citipy  
Gmaps & Gmaps.datasets  
Json  
Matplotlib.pyplot  
Numpy  
Pandas  
Python  
Random  
Requests  
Scipy.Stats - Lingregress  
Time  
Google Cloud Developer API  
Open Weather Map API  

## Findings  

First random cities had to be created (approximately 500) in order to have enough for a viable analysis and selection for clients.  

- coordinates were created based on the entire world not just the United States  

OpenWeatherMaps API to plot Linear Regression were utilized to visualize the correlation between the Northern and Southern Hemispheres and four different weather parameters:  

- Latitude vs. Northern Hemisphere Maximum Temperature
- Latitude vs. Southern Hemisphere Maximum Temperature
- Latitude vs. Northern Hemisphere Percent Humidity
- Latitude vs. Southern Hemisphere Percent Humidity
- Latitude vs. Northern Hemisphere Percent Cloudiness  
- Latitude vs. Southern Hemisphere Percent Cloudiness  
- Latitude vs. Northern Hemisphere Wind Speed  
- Latitude vs. Southern Hemisphere Wind Speed  

As shown by the Regression Line for Temperature(and is pretty much common knowledge) on both the Northern and Southern Hemisphere plots, the closer to the equator, the warmer the temperature. Rather than plotting this metric, maybe a metric of weather based on the time of year would have served more of a purpose to our client.

Looking at the Regression Line for Humidity, it is evident that there is almost no correlation between the % Humidity and the latitude and therefore humidity is an unpredictable weather parameter. That is why I question using this weather condition as a factor in planning a vacation that may or may not be happening in the short term.

Percent Cloudiness is another weather parameter that proves to have no correlation with the latitude. Again, I am not sure how useful this information would be when planning trips or vacations for a time well into the future.

Wind Speed, again is another weather parameter that proves to have little or no correlation with latitude. Planning an itinerary based on this would not be helpful.

## Deliverables

By making an API call to the OpenWeatherMap API I was able to retrieve from and provide the first of three deliverables:

- Weather_Database - A spreadsheet (WeatherPy_Database.csv) that contained the following data:
  - City
  - Country
  - Latitude and longitude
  - Maximum temperature
  - Percent humidity
  - Percent cloudiness
  - Wind speed
  - Weather description (for example, clouds, fog, light rain, clear sky)  

- Vacation_Search - A database (WeatherPy_vacation.csv) that contains a cleaned database of only those randomly created cities which have hotels within a 5000 meter radius and an application that allows client to search potential travel destinations based on weather criteria that provided each with the following:
  - Marker layer map with pop-up markers visualizing the following information about that destination:
    - Hotel Name
    - City
    - Country
    - Current Weather

- Vacation_Itinerary - An interactive directions layer map that allows client to plot visits to up to 4 cities while visiting any country within our Vacation_Search database.
  - Markers with the following information is included on the directions layer map:
    - Hotel Name
    - City
    - Country
    - Current Weather
    - Maximum Temperature

## Conclusion

While there is benefit in the client having the ability to choose a destination based on temperature preferences, making the application more customizable would add more flexibility for the client. For example, allowing the customer to choose a location based on the season, festivals or other attractions, landmarks, natural resources, or even tourist levels at certain times of year will not only give the client more options but may prove to be an enticement to choose PlanMyTrip over another application or like service provider.
