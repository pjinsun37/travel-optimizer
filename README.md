# travel-optimizer

- Dataset.xlsx: contains data about places (activities) used in the travel optimization model. It includes key details about each place, such as activity type, start/end times, durations, costs, and ratings.

- distance_in_min.xlsx: contains the travel times (in minutes) between all pairs of places in the dataset. It represents the time required to travel from one location to another.

- google_map_api.ipynb: Jupyter Notebook for integrating real-time data from Google Maps API, fetches travel times.

- travel_optimizer.py: Python script that contains the core travel optimization model implemented using the Gurobi Optimizer. It defines the decision variables, constraints, and objective functions required to solve the travel scheduling problem.

- travel_optimizer.ipynb: Jupyter Notebook that contains the use cases and examples that were included in report. It demonstrates the functionality of the travel optimization model with real-world scenarios and parameter setups.
