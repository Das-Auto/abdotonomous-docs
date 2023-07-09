## Why Abdotonomous?

We provide a highly practical architecture for autonomous and semi-autonomous vehicles. Our system offers numerous features and can accommodate additional ones without requiring extensive manual intervention. The system supports a variety of vehicles, including electric cars, remotely operated vehicles (ROVs), autonomous underwater vehicles (AUVs), and unmanned aerial vehicles (UAVs).

### Extensibility

Adding a new feature is just a piece of cake. Whenever you have a feature, implement it and add a new node to the system.

### Portability

With our docker image, you can use the system anywhere regardless of the hosting platform.

### Creative Commons License

Under the license of Attribution-NonCommercial 4.0 International, the source code is available and you are free to use and modify it for non-commercial use. We are also happy to receive pull requests from you!

## Features*

Our system boasts several advanced features, including:

- **TTC Feature:** This feature utilizes both camera and lidar data to evaluate the Time-to-Collision with the vehicle in front of you.
- **Kalman Filter:** This feature takes input data from various sensors such as lidar and radar to generate a more precise approximation of the system's quantities.
- **Lidar Obstacle Detection:** This feature leverages Point Cloud Data (PCD) coordinates to cluster and detect obstacles surrounding the vehicle.
- **GPS:** Our system employs the Google Maps API (non-free) to determine the global location of your vehicle.

*\*Adapted from [Sensor Fusion Nano Degree Program](https://www.udacity.com/course/sensor-fusion-engineer-nanodegree--nd313)*

## Technologies & Frameworks

Our system is built using the following technologies and frameworks:

- OpenCV
- C++
- Python
- ROS II
- Carla
- Docker
- Jetson Nano

