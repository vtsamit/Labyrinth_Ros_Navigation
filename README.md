<h1 align="center"> Labyrinth_ROS_Navigation </h1>  
<br>  
Labyrinth is a Motion Planning Event using ROS
and Gazebo. Simulate a real-world problem in
which a single agent has to map and navigate
through a complex environment using ROS
Navigation Stack and classical path planning
algorithms with Dynamic Obstacle Avoidance.
<br> 
<br> 
<h2 align="left"> Problem Statement </h2> 

● At your initial position, first scan the (given) ArUco
Marker using the camera .

● Publish the scanned ArUco marker id to the
topic named “/aruco” whose msg type is int8.

● Launch a node provided by us known as the
SPY. The SPY Node will verify the aruco id
and will publish a message in the topic
"/terrorist_location".

● If it is correct, you will get the image of a
terrorist launchpad.

● Using the image provided by SPY, extract the
coordinates of the launchpad.

● Simultaneously map the arena and navigate the
Garuda to the extracted coordinate.

● Once you reach the correct location, you will find
another ArUco Marker.

● Now, scan the new ArUco Marker and publish it’s
id to the same “/aruco” topic.

● If Id is correct, then SPY will provide you another
image. Use this image to extract the exit
coordinates.

● Navigate the Garuda to the exit coordinates to
finish the round.
<br>
<h2 align="center"> Labyrinth Arena </h2>  
<p align="center" style="background-color: rgb(250,250,250)">
<img src="https://github.com/vtsamit/Labyrinth_Ros_Navigation/blob/main/src/Labyrinth_Arena.png"/>
</p>
<br>
<h2 align="center"> Bot Description </h2>  
<p align="center" style="background-color: rgb(250,250,250)">
<img src="https://github.com/vtsamit/Labyrinth_Ros_Navigation/blob/main/src/BOT.png"/>
</p>


The Robot model has the following sensors:

1. 2D LIDAR

2. Intel Realsense D435i RGBD Camera

3. IMU

<h2 align="left"> Approach </h2> 

● Traversing through entire training arena and create a map using G-mapping and teleop packages

● Localizing the bot (AMCL) and make it reach the goal using path planning with the help of ROS navigation
stack

● Scanning Aruco Marker using camera to get marker id and obtain image of terrorist launchpad

● Using OpenCV to extract coordinates of exit point using Image Processing

● Make the bot reach the exit point using Simultaneous Localization and Mapping(SLAM)


<h2 align="left"> Working </h2> 
Final Video of the simulation-
(https://drive.google.com/file/d/1CFbJVxbLxP4gabwmcAitaT45VJuusIf-/view?usp=sharing)
