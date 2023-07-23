---

## Lidar Obstacle Detection 
???+ note inline end 
    \* The feature nodes do not make decisions themselves but rather provide status updates based on the data they collect from the sensors. These updates reflect the current state of the vehicle and its surrounding environment.

Abdotonomous utilizes Point Cloud Data (PCD) coordinates to detect and cluster points forming obstacles surrounding the vehicle. By analyzing the PCD data, the system can identify objects in the vehicle's path and adjust its trajectory accordingly to avoid collisions*. The Lidar Obstacle Detection feature is particularly useful for vehicles operating in challenging environments, such as construction sites or busy city streets.

<!-- Although this feature currently utilizes only lidar points, we can enhance its performance by fusing the output from both lidar and radar sensors, as an input. -->


----
## Time to Collision


???+ info inline end
     It should be noted that this feature assumes that the car is driving at a {==constant velocity==}.

The Time-to-Collision (TTC) feature in Abdotonomous evaluates the distance between your vehicle and the vehicle in front of you using a combination of camera and lidar data and make use of descriptors of successive image frames and the focal length of the camera. By fusing these data sources, the system can estimate how long it will take for the two vehicles to collide if they continue on their current paths. This information can be incredibly valuable for preventing collisions and ensuring safe driving.

Because of budget constraints, we have employed a single camera mounted on the car's windshield along with lidar points to estimate distance using openCV descriptors.




    
---

## Unscented Kalman Filter

Abdotonomous utilizes a Kalman Filter to generate a more accurate estimation of the system's variables. The Kalman Filter takes input data from various sensors, such as lidar and radar, and produces a refined estimate of the vehicle's position, velocity, and other relevant parameters, which is known as _localization_. This feature is particularly useful for autonomous vehicles operating in challenging environments where sensor data may be noisy or incomplete. By using the Kalman Filter to fuse sensor data, autonomous vehicle systems can achieve more precise and reliable localization and navigation, which is crucial for safe and effective autonomous driving. Additionally, the Kalman Filter enables the vehicle to make real-time adjustments to its trajectory and speed, based on changes in the environment and the behavior of other vehicles and obstacles on the road.

---

## GPS Navigation System

???+ warning inline end
     Google Maps API is a third-party tool used to enhacne the functionality of the self-driving car system. However, it is {== not provided free of charge ==}.

Google Maps API is used to integrate GPS functionality into the self-driving car system. The API provides the system with access to Google Maps data, including maps, routes, and real-time traffic information.

The GPS data obtained through the Google Maps API is used by the decision-making node to determine the best route to the vehicle's destination and to adjust the vehicle's driving behavior in real-time based on current traffic conditions.


Currently, the GPS node operates similarly to having a mobile phone with Google Maps to follow directions. However, this feature is intended for {++future use++}, where the vehicle can take control and drive autonomously based on instructions from Google API, as well as constraints derived from other sensors.

<br>