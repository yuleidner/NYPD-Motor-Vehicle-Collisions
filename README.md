**Important!** Some of the output of this notebook has not been included, because it makes it too big for GitHub! To see those outputs please follow this link: https://colab.research.google.com/github/CorkCork/NYPD-Motor-Vehicle-Collisions/blob/master/analyze_data/NYPD%20Motor%20Vehicle%20Collisions.ipynb

### Overview
[NYPD Motor Vehicle Collision Dataset](https://data.cityofnewyork.us/Public-Safety/NYPD-Motor-Vehicle-Collisions-Crashes/h9gi-nx95) contains details on the crash events. Each row represents a crash event. The Motor Vehicle Collisions data tables contain information from all police reported motor vehicle collisions in NYC. The dataset can be found by following this link: https://data.cityofnewyork.us/Public-Safety/NYPD-Motor-Vehicle-Collisions-Crashes/h9gi-nx95
***** 
### High-Level Description
The data dates from 2012 to the current day, with data being updated on a daily basis. At the time of this writing, there are 1.59 million rows, each row representing a crash event, and 29 columns. The information about the column contents can be found below.

***Column Contents***

There are two columns that store information about the date and time of the accident:
* **Crash Date**:  Occurrence date of collision
* **Crash Time**:  Occurrence time of collision

There are six columns that store information about where the accident took place:
* **Borough**:  Borough where collision occurred
* **Zip Code**:  Postal code of incident occurrence
* **Latitude**:  Latitude coordinate for Global Coordinate System, WGS 1984, decimal degrees (EPSG 4326)
* **Longitude**:  Longitude coordinate for Global Coordinate System, WGS 1984, decimal degrees (EPSG 4326)
* **Location**:  Latitude, Longitude pair
* **On Street Name**:  Street on which the collision occurred
* **Cross Street Name**:  Nearest cross street to the collision
* **Off Street Name**:  Street address if known

There are eight columns that store information about the number of persons injured or killed in the accident:
* **Number of persons injured**:  Number of persons injured
* **Number of persons killed**:  Number of persons killed
* **Number of pedestrians injured**:  Number of pedestrians injured
* **Number of pedestrians killed**:  Number of pedestrians killed
* **Number of cyclists injured**:  Number of cyclists injured
* **Number of cyclists killed**:  Number of cyclists killed
* **Number of motorist injured**:  Number of vehicle occupants injured
* **Number of motorist killed**:  Number of vehicle occupants killed

There are five columns that store information about the factors contributing to the collision for designated vehicle:
* **Contributing Factor Vehicle 1**:  Factors contributing to the collision for designated vehicle
* **Contributing Factor Vehicle 2**:  Factors contributing to the collision for designated vehicle
* **Contributing Factor Vehicle 3**:  Factors contributing to the collision for designated vehicle
* **Contributing Factor Vehicle 4**:  Factors contributing to the collision for designated vehicle
* **Contributing Factor Vehicle 5**:  Factors contributing to the collision for designated vehicle

There are five columns that store information about the type of vehicles involved in the accident:
* **Vehicle Type Code 1**:  Type of vehicle based on the selected vehicle category (ATV, bicycle, car/suv, ebike, escooter, truck/bus, motorcycle, other)
* **Vehicle Type Code 2**:  Type of vehicle based on the selected vehicle category (ATV, bicycle, car/suv, ebike, escooter, truck/bus, motorcycle, other)
* **Vehicle Type Code 3**:  Type of vehicle based on the selected vehicle category (ATV, bicycle, car/suv, ebike, escooter, truck/bus, motorcycle, other)
* **Vehicle Type Code 4**:  Type of vehicle based on the selected vehicle category (ATV, bicycle, car/suv, ebike, escooter, truck/bus, motorcycle, other)
* **Vehicle Type Code 5**:  Type of vehicle based on the selected vehicle category (ATV, bicycle, car/suv, ebike, escooter, truck/bus, motorcycle, other)

And there is a record code for each accident:
* **Collision ID**:  Unique record code generated by system. Primary Key for Crash table.
***** 
### The Project
In this project, our goal is to understand more about the collisions in NYC and help reduce them by sharing our findings with lawmakers and New Yorkers. To do so, we will explore collision times, seasons, locations, factors and vehicle times as well as look into the results of collisions. 

We will be doing the following:

* Ingest some data from the [NYPD Motor Vehicle Collision Dataset](https://data.cityofnewyork.us/Public-Safety/NYPD-Motor-Vehicle-Collisions-Crashes/h9gi-nx95). We will use Socrata Open Data API to just select a limited number of rows.
* Clean the dataset to make it ready for analysis.
* Make analysis and visualizations to see the boroughs and times when collisions occur mostly. 
* Explain our findings by using markdown as we go along.
*****
### Dependencies
In order to use make analysis, you need to ingest 3000000 rows from the [NYPD Motor Vehicle Collision Dataset](https://data.cityofnewyork.us/Public-Safety/NYPD-Motor-Vehicle-Collisions-Crashes/h9gi-nx95) via Socrata Open Data API and its `limit` parameter. 
`pd.read_csv("https://data.cityofnewyork.us/resource/h9gi-nx95.csv?$limit=3000000")` 
***** 
### Authors
Esin Alpturk<br/>
Alan Leidner<br/>
Kristin Medlin
