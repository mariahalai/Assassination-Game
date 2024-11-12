# Bomb Plan Algorithm

This R script predicts bombing times and locations based on past GPS data patterns. 
This algorithm calculates the optimal time and location to "place a bomb" on a moving target, following rules to avoid stationary zones and place the bomb mid-transit.

### Prerequisites

Ensure you have the following R packages installed:
- dyplr
- lubridate
- geosphere 

To install these, run the following command in R:
install.packages(c("dplyr", "lubridate", "geosphere"))

### How It Works-- The algorithm to test is at the bottom. 
The algorithm follows these main steps:

Calculate Bomb Time: Determines mid-transit time, offset by 5 minutes to avoid early fluctuations.
Predict Bomb Location: Uses common transit points to select a central point for accurate targeting.
Avoid Stationary Zones: Ensures the bomb location is at least 5 meters away from known stationary "safe" zones.

### Example Use:
Run generate_bomb_plan with start location, start time, average transit duration, and safe zones to output the ideal day, time, and coordinates for the bomb.
