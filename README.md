# Singapore Travel Itinerary Optimizer

# 🔎 Problem
Travel planning can be extremely overwhelming. When planning a trip, travelers often struggle with:
- Finding the best itinerary that balances cost, time, and enjoyment.
- Managing different types of activities (food, attractions, tours) within a given time frame.
- ... while also minimizing unnecessary travel time between locations.

There are travel planning tools out there, but tend to lack customized itinerary optimization that adapts to the traveler’s specific constraints.

# 💡 Solution

Our Travel Optimizer uses Mixed Integer Programming (MIP) to generate an optimized travel schedule. It:
- Considers multiple constraints: budget, time windows, travel duration, and enjoyment scores.
- Categorizes activities: Food, Tours, and Attractions are optimally distributed throughout the itinerary.
- Minimizes travel time: Using Google Maps API, the optimizer ensures efficient route planning.
- Maximizes overall satisfaction: The final itinerary balances cost and enjoyment scores.

[Read full problem formulation here](https://drive.google.com/file/d/1CcCCggNauQO3I1GghzhS_mDh2wIXL7he/view?usp=sharing)

# 📊 Use Cases

**7-hour trip during transit**
- Time: 14:00 - 21:00
- Budget: SGD 0 - 500
- Optimal itinerary

<img width="624" alt="Screenshot 2025-02-19 at 3 11 36 PM" src="https://github.com/user-attachments/assets/23b14497-1291-4d9a-bc8b-0cab53fc9aeb" />

Total time spent on road: 41 minutes, Total enjoyment: 93%


**Full day luxury trip from MBS**
- Time: 08:00 - 22:00
- Budget: SGD 500 - 800
- Optimal itinerary:

<img width="622" alt="Screenshot 2025-02-19 at 3 13 51 PM" src="https://github.com/user-attachments/assets/832693f0-607e-4695-8641-9118bc90a727" />

Total time spent on road: 90 minutes, Total enjoyment: 91%

**Full day budget trip from NUS University Town**
- Time: 08:00 - 23:00
- Budget: SGD 0 - 150
- Optimal itinerary:

<img width="615" alt="Screenshot 2025-02-19 at 3 15 29 PM" src="https://github.com/user-attachments/assets/dd5e9f73-a1b8-4552-8a74-12522a0241c3" />

Total time spent on road: 90 minutes, Total enjoyment: 87.5%


# ⚙️ Tech Stack
- Python (for optimization and data processing)
- Gurobi / PuLP (for Mixed Integer Programming)
- Google Maps API (for travel time calculations)

# 📂 Project Files
- Dataset.xlsx: contains data about places (activities) used in the travel optimization model. It includes key details about each place, such as activity type, start/end times, durations, costs, and ratings.

- distance_in_min.xlsx: contains the travel times (in minutes) between all pairs of places in the dataset. It represents the time required to travel from one location to another.

- google_map_api.ipynb: Jupyter Notebook for integrating real-time data from Google Maps API, fetches travel times.

- travel_optimizer.py: Python script that contains the core travel optimization model implemented using the Gurobi Optimizer. It defines the decision variables, constraints, and objective functions required to solve the travel scheduling problem.

- travel_optimizer.ipynb: Jupyter Notebook that contains the use cases and examples that were included in report. It demonstrates the functionality of the travel optimization model with real-world scenarios and parameter setups.
