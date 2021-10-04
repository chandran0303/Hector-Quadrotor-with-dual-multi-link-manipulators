# Hector Quadrotor with Dual Arm, Multi Link Manipulators

Modifications were made to the Hector Quadrotor offered by TU Darmstadt. I added 2 arms on either end. Currently they dont have grippers. Its a work in progress. This work is being done as a part of my internship at IIT Bombay


# Prerequisites

 1. ROS Kinetic
 2. Gazebo/RViz
 3. I personally used Ubuntu 16.04 for this project

# Steps to be followed

 After downloading this package the following commands need to be run on your Linux terminal in order to ensure the necessary installations for proper simulation of the quadcopter and arms

    sudo apt-get install ros-kinetic-geographic-info
    sudo apt-get install ros-kinetic-ros-control
    sudo apt-get install ros-kinetic-gazebo-ros-control 
    sudo apt-get install ros-kinetic-joy

Run the following command to start the simulation

    roslaunch hector_quadrotor_demo outdoor_flight_gazebo.launch

Next run the following line in another terminal inorder to initialise joint state controller to control the manipulators

    roslaunch hector_quadrotor_demo rrbot_control.launch

Finally run a modified version of teleop keyboard in another terminal to control the flight of the quadcopter

    roslaunch hector_quadrotor hector_control.py 

# Image of the simulation

<a href="https://ibb.co/VSnFcRv"><img src="https://i.ibb.co/PhX2vK5/2-3armquadrotor.png" alt="2-3armquadrotor" border="0"></a>
