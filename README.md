# Singapore Travel Itinerary Optimizer

This project employs Mixed Integer Programming concepts to create a travel itinerary optimization model that helps maximize the enjoyment and travel time efficiency for travelers exploring Singapore. 

We created an optimization model that includes sets of activities categorized by type (e.g., breakfast, lunch, dinner, tours, attractions) and parameters such as cost, duration, and enjoyment ratings. 

To fit the model for real-world applications, we collected comprehensive data using the Google Maps API, including place names, ratings, price levels, opening/closing hours, and distances between locations. We also sourced data on tours, activities, and restaurants from popular travel platforms and online communities.

- Dataset.xlsx: contains data about places (activities) used in the travel optimization model. It includes key details about each place, such as activity type, start/end times, durations, costs, and ratings.

- distance_in_min.xlsx: contains the travel times (in minutes) between all pairs of places in the dataset. It represents the time required to travel from one location to another.

- google_map_api.ipynb: Jupyter Notebook for integrating real-time data from Google Maps API, fetches travel times.

- travel_optimizer.py: Python script that contains the core travel optimization model implemented using the Gurobi Optimizer. It defines the decision variables, constraints, and objective functions required to solve the travel scheduling problem.

- travel_optimizer.ipynb: Jupyter Notebook that contains the use cases and examples that were included in report. It demonstrates the functionality of the travel optimization model with real-world scenarios and parameter setups.

# Use Cases

**7-hour trip during transit**
- Time: 14:00 - 21:00
- Budget: SGD 0 - 500
- Optimal itinerary:

<img width="624" alt="Screenshot 2025-02-19 at 3 11 36 PM" src="https://github.com/user-attachments/assets/23b14497-1291-4d9a-bc8b-0cab53fc9aeb" />

**Full day luxury trip from MBS**
- Time: 08:00 - 22:00
- Budget: SGD 500 - 800
- Optimal itinerary:

<img width="622" alt="Screenshot 2025-02-19 at 3 13 51 PM" src="https://github.com/user-attachments/assets/832693f0-607e-4695-8641-9118bc90a727" />

**Full day budget trip from NUS University Town**
- Time: 08:00 - 23:00
- Budget: SGD 0 - 150
- Optimal itinerary:

<img width="615" alt="Screenshot 2025-02-19 at 3 15 29 PM" src="https://github.com/user-attachments/assets/dd5e9f73-a1b8-4552-8a74-12522a0241c3" />

