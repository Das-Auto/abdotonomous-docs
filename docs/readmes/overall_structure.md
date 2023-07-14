# Project Structure

The project is a modular system that allows for the addition or modification of nodes and features based on specific requirements.

The current features include time-to-collision analysis, obstacle detection, Google Maps GPS integration, and Kalman filtering for sensor data fusion between lidar and radar.*

Each feature is encapsulated within a ROS (Robot Operating System) node, which can be executed simultaneously and work in coordination with one another.

Each sensor is represented by a separate node that retrieves data either from the surrounding environment or from a simulator.

To test the functionality of the nodes, a simulator like Carla is employed, provided that the necessary drivers for sensors are available. This is why careful consideration was given to sensor selection.

To ensure reliability and consistency across different environments, Docker was used.

\* The concepts of time-to-collision analysis, obstacle detection, and Kalman filtering were inspired by Udacity, but the integration of these concepts with the ROS system was developed independently by the project team.

A separate node, typically referred to as the decision-making node, is responsible for processing the data from all the enabled feature nodes. It analyzes the combined information and uses algorithms and rules to make decisions about the vehicle's actions, such as accelerating, braking, or steering.

By separating the feature nodes from the decision-making node, the system is designed to be more modular and flexible. This allows for easy customization of the decision-making process and the addition or removal of features as needed.


> Add Image for the overall structure
> 
> Add an image for ROS nodes