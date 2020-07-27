### BankingDesertHeatMap-

* Analysed relationship between poverty, age, and population with the number of banks in a given area
* Pulled Data using census data for every zip code across the country.  
* Visualizing data by creating layered maps with Google maps and API.

## WeatherPy-

### Goal
Analyze at least 500 randomly selected cities around the world to prove that the weather gets hotter as one approaches the equator using the Open Weather Map API.

### Process
The first step was to generate a random list of at least 500 cities around the world for an unbiased sampling. Random latitudes and longitudes were created using the NumPy library and the city nearest those coordinates were found using citipy and stored in a list.

### An empty data frame was then created to store data pulled from the Open Weather Map API. Using df.iterrows(), the API was pinged and information on cloudiness, country name, date, humidity, latitude, longitude, max temperatures, and wind speed were pulled. The data was stored in the empty data frame and exported as a csv file.

Next was to create scatter plots for four comparisons:

* Latitude vs. Temperature ![Plot1](https://github.com/SurabhiSood/Python_API_Visualizations/blob/master/WeatherPy/Plot1.png)
* Latitude vs. Humidity ![Plot2](https://github.com/SurabhiSood/Python_API_Visualizations/blob/master/WeatherPy/Plot2.png)
* Latitude vs. Cloudiness ![Plot3](https://github.com/SurabhiSood/Python_API_Visualizations/blob/master/WeatherPy/Plot3.png)
* Latitude vs. Wind Speed ![Plot4](https://github.com/SurabhiSood/Python_API_Visualizations/blob/master/WeatherPy/Plot4.png)

Because all four charts would share similar attributes, I created a function to plot each chart, so that I would only have to input the y-values and labels. However, the data types in the data frame were all strings, so I used pd.to_numeric() on all relevant columns in order to plot the data.

 

### VacationPy-

* Based on data drawn from WeatherPy VacationPy narrows down cities on selective weather conditions
* Using google places API,listed the first hotel for each city located within 5000 meters of your coordinates.
* Plotted hotels on gmap using markers