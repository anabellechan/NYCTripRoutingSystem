# NYCTripRoutingSystem
This Routing System maps vehicles’ coordinates from an origin to a destination in every intervals of 10 minutes and finds a more efficient route for the vehicle to travel.
-Since it is a big data record (6.8mil), it requires data cleaning before it can be migrated for software development.
This system uses Real-Time New York City Bus Data for a month which has more than 6 million data records per CSV.
-Each data consists of geo-spatial lat-long points that maps vehicles’ coordinates from an origin to a destination in every intervals of 10 minutes. 
Such similar examples of an app widely used today would be Singapore’s SG Bus app.

For the full CSV data you can refer to https://www.kaggle.com/datasets/stoney71/new-york-city-transport-statistics.
The folder in this repository called New York City Bus Data has the python jupyter code for data cleaning before doing a migration to PostGres after creation of the following tables:
coordinates, trip and fullnycdata. the full data is split into their respective trips, which refers to origin->destination = 1 trip, and a column for the no. of trips.
These trips' coordinates are stored in the coordinates table with coordinatesid as the PK.
The following are a snippet of the table and its columns.  
  Full Table: 
<img width="628" alt="image" src="https://user-images.githubusercontent.com/97331839/226262153-fe8b2556-0e7c-42b0-9bf2-e074e03ed628.png">
  Continuation of Full Table:  
<img width="599" alt="image" src="https://user-images.githubusercontent.com/97331839/226262219-2c66b830-4474-493e-810f-72f99a737e6e.png">

  Trip Table:  
<img width="374" alt="image" src="https://user-images.githubusercontent.com/97331839/226262539-d3215cf9-ae93-4e61-ba62-52c2c2e4c04c.png">

  Coordinates Table:  
<img width="569" alt="image" src="https://user-images.githubusercontent.com/97331839/226262662-15ecadfb-240c-46f9-a1a0-630bd7a097f6.png">

