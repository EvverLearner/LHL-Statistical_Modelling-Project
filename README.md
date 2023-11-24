# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
The goal of this project is to practise going through the process of interacting with APIs to gather specific information, then visualize and model the information to discover possible trends. This project specifically seeks to discover how the areas around bike rental stations in London, UK affect the availability of bikes at the stations.

## Process
The process for this project is as follows:
1. Use the `CityBikes` API to gather information about bike stations in the chosen location.
2. Parse and format the received data from Step 1.
3. Use the `Foursquare` and `Yelp` APIs to gather information about points of interest (POI) in locations near the bike rental stations found in Step 1.
4. Parse and format the received data from Step 3. The formatted data can then be joined with the data from Step 1 in order to more easily relate data in future steps.
5. Visualize the joined data in order to discover any patterns that can be used for modeling.
6. Model the data using a regression technique, and interpret the results of the model in the context of the project goals.

## Results
- The results of the API requests actually returned data better than I expected, and there was plenty of relevant information.
- Joining the data from all APIs is simple if the parsing and formatting process is done in a consistent, standard way (ex. column names).
- The model, which compared the number of available bikes at a station in realtion to the average rating of nearby POI, had very low confidence (7%). This means that the best interpretation is that nearby location ratings are not a good indication of whether or not a bike is going to be available at a rental station.
- However, the P-value of the model was low enough to indicate a correlation between POI ratings and bike availability, specifically that there are more likely to be less bikes since it is presumed there are more people in those locations.

## Challenges 
- Lower sample size due to limitations on processing times for some code executions, and the number of API requests available on a free account.
- API authentication was confusing for the `Yelp` API, since it required more than just the token that was provided.
- Perhaps due to low sample size, or perhpas due to their just not being a pattern to being with, the visualizations were hard to decisvely use as a basis for modeling a relationship.
- General uncertainty in the modeling process
- My `Yelp` API requests ran out!

## Future Goals
- Try more models, especially a multi-variable regression model.
- Add more comments, ideally at the time of coding but with more time they can be added in post.
- Make the visualization nicer, and try more visualizations.
- Gather data across more time; the API requests only gather data at the time it is sent. If I had data of different times as well, there would both be another variable to measure (time) and more overall data that could result in a more obvious trend or pattern.
