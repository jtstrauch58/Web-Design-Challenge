# Web-Design-Challenge

For this homework we were tasked with developing a visualization dashboard website using visualizations created in a past assignment.

The dashboard contains individual pages for each plot and their corresponding data analysis explanations.

The dashboard also includes a landing page, a comparison page and data table page where we can view the data used to build the data plots.

# Website Requirements

Basic requirements for the webites:
* Links to each visualization page.
* A sidebar containing preview images of each plot, and clicking an image should take the user to that visualization.
* A descriptive title and heading tag.
* A paragraph describing the plot and its significance.
* A comparisons page that contains all of the visualizations. The page must use Bootstap grid elements and be responsive to screen size.
* A data table page using Bootstrap responsive table.

The website has a navigation menu that:

* Has the name of the site on the left of the nav which allows users to return to the landing page from any page.
* Contains a dropdown menu on the right of the navbar named "Plots" that provides a link to each individual visualization page.
* Provides two more text links on the right: "Comparisons," which links to the comparisons page, and "Data," which links to the data page.
* Is responsive (using media queries). 

Finally, the website must be deployed to GitHub pages.

# Local Weather vs Latitude Study
## About the study
This study examined weather conditions of randomly-selected cities across the globe, ultimately comparing average weather characteristics to the city’s latitude.
Ultimately, weather data for 500 global cities was examined. The study found that (a) maximum temperature was inversely proportional to a city’s latitude
(ie, lower temperatures observed for increasing latitude); (b) though no correlation could be found between latitude and humidity, some clustering of humidity
values was observed amongst some latitude ranges; (c) no correlation was observed between cloudiness and latitude; (d) wind speeds tended to fall in a range from 0 – 20 mph, but no correlation with latitude was found.

## Data Generation
To generate the weather data, cities were first selected by utilizing the citipy python module and randomly-generated latitude and longitude data.
Specifically, nearest cities were located within a 500 km radius of latitude-longitude pair. It should be called out here that the city located using citypy may
be 100’s of km away from the lat-long pair used in the citipy function call. To resolve this distance issue, each city-name & country-name pair was sent to
OpenWeatherMap’s API to determine actual lat-long data. Finally, the lat-long pair of each city, country was used to call a weather forecast-specific OpenWeatherMap API.
The forecast data was returned in the form of JSON data. Pandas and python tools were used to plot specific weather characteristics vs a city’s latitude.

## Observations (for the cities in the study)
(1)	Maximum temperatures vs Latitude
a.	Temperatures ranged from approximately -30F to 110F.
b.	Maximum temperatures were higher for cities in closer proximity to the equator.
c.	The data showed a nice negative correlation of max temperature with latitude, meaning the max temperature tended to decrease with increasing latitude.
(2)	Humidity vs Latitude
a.	% humidity values ranged from near-zero to 100%
b.	The humidity data did not indicate a correlation with latitude.
c.	Latitudes from 0 to -20 showed humidity values between 50 – 80; latitudes 50 – 90 humidity values ranged 75 – 90; all other latitude ranges had humidity values of approximately 20 – 90.
(3)	Cloudiness vs Latitude
a.	Cloudiness measurements ranged from 0 – 100%.
b.	All latitudes had cloudiness values from 0 – 100%.
c.	No correlation was observed between latitude and cloudiness.
(4)	Wind Speed vs Latitude
a.	Average wind speeds ranged from 0 to a high of approximately 50 mph.
b.	More commonly, wind speeds tended to range between 0 – 20 mph.
c.	No correlation was observed between a city’s average wind speed and latitude.
