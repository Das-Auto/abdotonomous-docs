## Lidar Obstacle Detection

Abdotonomous utilizes Point Cloud Data (PCD) coordinates to detect and cluster obstacles surrounding the vehicle. By analyzing the PCD data, the system can identify objects in the vehicle's path and adjust its trajectory accordingly to avoid collisions*. The Lidar Obstacle Detection feature is particularly useful for vehicles operating in challenging environments, such as construction sites or busy city streets. To activate the feature, simply enable it in the Abdotonomous system and let the system do the rest.

Although this feature currently utilizes only lidar points, we can enhance its performance by using the output of the Kalman filter, which fuses data from both lidar and radar sensors, as its input.


\* The feature nodes do not make decisions themselves but rather provide status updates based on the data they collect from the sensors. These updates reflect the current state of the vehicle and its surrounding environment.




