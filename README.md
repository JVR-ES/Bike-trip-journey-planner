# Bike trip journey planner
An application to plan bike trips.

## Summary
This application will suggest a bike trip and will split it into the right number of stages, based on the user’s preferences, like duration or accumulated effort. It will also suggest a train journey from the user’s home to the starting point and back from the end point to the user’s home.

## Background
This application is intended for Cycle Touring amateurs in Spain. Based on existing, well-known, routes, it helps the user splitting the track into the most convenient number of stages, also affording the complex work of designing a train route in a country where not all trains allow you to travel with a bicycle.
As one of these cycling amateurs, very often I found the train trip was most important drawback when trying to plan my own bike trips.
Adding the train path to the journey plan would help many cycling amateurs to would venture to design their own cycling trips.

## Data sources and AI methods 
* The so-called Greenways [Greenways](https://datos.gob.es/en/catalogo "Vías verdes de España. Public dataset") are a selection of old railway tracks, currently converted into cycle paths and/or hiking trails. Linear regression algorithms can be applied to estimate the route’s difficulty based on certain parameters. 
* Train stations can be searched using [Google Maps](https://developers.google.com/maps/apis-by-platform?hl=es-419 "Google Maps API Directory"). Nearest neighbor algorithm can be used to find the ones nearest to our starting and ending points. 
* [RENFE](https://data.renfe.com/dataset?res_format=GTFS&tags=horarios "RENFE datasets"), the National Railway Company, provides all the necessary information to prepare the trip: timetables, ticket prices and so on.
* If the user wants to split the trip into several stages, accommodation shall be a requirement. Some specialized services, like [Tripadvisor](https://developer-tripadvisor.com/content-api/ "TripAdvisor API"), offer APIs that this application could integrate with. 

## How is it used?
Access to this solution can be provided via web browser or mobile app.
Users can lean on this application to choose a destination as well as to program their bike trip.
* First step would be to set some filtering conditions that would allow to make a short list among all options available. This filtering would allow parameters to be narrowed down such as the location of the starting point, the total length of the route or the level of effort required.
* Second step would be choosing one option among the routes available and splitting it into the desired number of stages
* Then, a final set of options would be set according to the user’s choice, such as the start date or the means of transport.

## Challenges
The biggest challenge is to integrate all inputs from different sources and to optimize the result so it can be bundled and offered to the user as a block. There’s a big programming work behind.

Some pieces of this application should be easy to implement. After unit testing, the project would putting them all together.

## What Next?
Once the application is fine-tuned in the provided context, the second challenge would be to make it grow. More datasets could be added to cover additional routes and other countries.

## Acknowledgements
This is not a completely new idea. Similar services exist (e.g. [Wikiloc](https://www.wikiloc.com/ "Wikiloc. Trails of the World") or [Garmin Connect](https://connect.garmin.com/ "Garmin Connect. Courses")), which cover at least part of this functionality. Nevertheless, the railway connection or accommodation would be valuable add-ons to those.
