# Dependencies (Grad Project)
---

## Getting Started

First things first. I installed neofetch to check my micro-computer specs

![](/docs/assets/nano/dependencies_1.png)

<img src="../../assets/nano/dependencies_1.png">

<!-- <img src="assets/nano/dependencies_1.png"> -->

## Other Dependencies

### PCL

`sudo apt install libpcl-dev`

### Python 3

`sudo apt install python3.7-dev`

### OpenCV

Best explanation ever is available [here](https://github.com/udacity/SFND_2D_Feature_Tracking/issues/3)

1. If you have not installed OpenCV, follow the below steps
   ```python

   git clone https://github.com/opencv/opencv.git
   cd opencv
   git checkout 4.1.0
   cd .. #get out of opencv folder
   ```
2. now get opencv_contrib
   ``` python
   git clone https://github.com/opencv/opencv_contrib/
   git checkout 4.1.0
   cd .. #get out of opencv_contrib folder
   ```
3. let's create a build directory inside opencv folder and install opencv where we will refer opencv_contrib
   ```python
   cd opencv
   mkdir build && cd build
   cmake -D CMAKE_BUILD_TYPE=RELEASE -D OPENCV_ENABLE_NONFREE=ON -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules -D WITH_GTK=ON ..
   make && sudo make install
   ```

???+ Info
    The setup may take long time (> 3 hrs). You may then need to reboot the device and restart the setup
    OpenCV installation takes long time. More than 2 hours.

<br>

![](/docs/assets/nano/dependencies_2.webp)



### g++ (already installed)

`sudo apt-get install g++`

### cmake
`sudo snap install cmake -classic`

### net-tools (already installed)
`sudo apt-get install -y net-tools`

### Docker (already installed)
`sudo apt install docker.io`


### ROS II Foxy


???+ Warning
    
    ROS II Foxy requires Ubuntu 20. Remember `neofetch`? We use Ubuntu 18. So, we have to use docker to install it.


![](/docs/assets/nano/dependencies_3.png)


`docker run -it ros:foxy`


???+ Tip
    Please check ROS official [website](https://discourse.ros.org/t/announcing-ros-foxy-docker-images-availability/14511) for further inforamation
