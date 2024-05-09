# Business Finder from Geospatial NoSQL Data

 - Find business based on city and location from geospatial NoSQL data.
 - This repository contains Python code implementing functions for searching businesses based on city and location using a NoSQL database.

## Functionality

- FindBusinessBasedOnCity(cityToSearch, saveLocation1, collection): Finds businesses in a specified city from a NoSQL collection and saves their details (name, address, city, state) in a txt file.

- FindBusinessBasedOnLocation(categoriesToSearch, myLocation, maxDistance, saveLocation2, collection): Finds businesses within a given distance from a specified location based on categories (optional) and saves their names in a separate file.

- A distance algorithm will need to be used. Given two pairs of latitude and longitude as [lat2, lon2] and [lat1, lon1], you can calculate the distance between them using the formula given below:

DistanceFunction(lat2, lon2, lat1, lon1):
- var R = 3959; // miles
- var φ1 = lat1.toRadians();
- var φ2 = lat2.toRadians();
- var Δφ = (lat2-lat1).toRadians();
- var Δλ = (lon2-lon1).toRadians();

- var a = Math.sin(Δφ/2) * Math.sin(Δφ/2) + Math.cos(φ1) * Math.cos(φ2) * Math.sin(Δλ/2) * Math.sin(Δλ/2);
- var c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1-a));
- vard=R*c;

- d is the distance between the given pair of latitude and longitude. The distance is in
miles.
