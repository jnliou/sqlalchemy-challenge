## SQLAlchemy-Challenge
This repository contains code for performing climate analysis and exploration using SQLAlchemy and Flask. The purpose of this project is to analyze climate data in Hawaii stored in a SQLite database and provide query results through a web browser using Flask.

# Part 1 - Climate Analysis and Exploration 
File named: [climate_starter.ipynb](SurfsUp/climate_starter.ipynb)

1. Connect to the SQLite database using SQLAlchemy and reflect the tables into classes using SQLAlchemy's automap_base() function.

2. Performed precipitation analysis:

- Found the most recent date in the dataset.
- Retrieved the last 12 months of precipitation data by querying the 12 preceding months of data.
- Selected only the date and precipitation values.
- Loaded the query results into a Pandas DataFrame and set the index to the date column.
- Sorted the DataFrame values by date.
- Plotted the results using the DataFrame plot method. 
![Precipitation in Hawaii from 2016-08-23 to 2017-08-23](<SurfsUp/Precipitation in Hawaii from 2016-08-23 to 2017-08-23.png>)
- Printed the summary statistics for the precipitation data.

3. Performed station analysis:

- Calculated the total number of stations in the dataset.
- Found the most active stations by listing the stations and their observation counts in descending order.
- Determined the station with the highest number of observations.
- Calculated the lowest, highest, and average temperature for the most active station.
- Retrieved the last 12 months of temperature observation data (TOBS) for the most active station.
- Plotted the results as a histogram with bins=12 
![Temperature from 2016-08-23 to 2017-08-23 for station USC00519281](<SurfsUp/Temperature from 2016-08-23 to 2017-08-23 for station USC00519281  .png>)

# Part 2 - Climate App
File named: [app.py](SurfsUp/app.py)

Designed a Flask API based on the analysis and queries developed in Step 1. The following routes are available:

- /: Home page that lists all available routes.
- /api/v1.0/precipitation: Returns the last 12 months of precipitation data as a JSON object.
- /api/v1.0/stations: Returns a JSON list of stations from the dataset.
- /api/v1.0/tobs: Returns the last 12 months of temperature observation data (TOBS) for the most active station as a JSON list.
- /api/v1.0/start: Returns the minimum, average, and maximum temperature for all dates greater than or equal to the given start date.
- /api/v1.0/start/end: Returns the minimum, average, and maximum temperature for dates between the given start and end dates (inclusive).

Note: In the routes /api/v1.0/start and /api/v1.0/start/end, replace start and end with the actual dates in the format YYYY-MM-DD.

# Usage
- Clone the repository to your local machine.
- Ensure you have the necessary dependencies installed.
- Update the code with the appropriate SQLite database file and table names, if needed.
- Run the script or launch the application.
- Access the routes in your web browser or make API requests to retrieve the climate data.

Feel free to explore and modify the code as per your requirements. 