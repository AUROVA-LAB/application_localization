# application_localization
This package contains an application consisting of different launch files that execute diferent localization algorithms using [BLUE robot](https://github.com/AUROVA-LAB/robot_blue) and nodes for adapt sensor data. Next we describe two example of how to run two different complete applications. 

## Navigation application using Gazebo model of BLUE.

### Requirements to use this package:

- System requirements: Ubuntu 16.04 and ROS Kinetic.
- Libraries: [lib_planning](https://github.com/AUROVA-LAB/lib_planning), Eigen, and PCL.
- BLUE model for Gazebo: Follow instruction in [robot_blue_gazebo](https://github.com/AUROVA-LAB/robot_blue_gazebo).
- ROS packages: [aurova_preprocessed](https://github.com/AUROVA-LAB/aurova_preprocessed), [aurova_localization](https://github.com/AUROVA-LAB/aurova_localization), and [aurova_planning](https://github.com/AUROVA-LAB/aurova_planning). 
- ROS application packages: [application_navigation](https://github.com/AUROVA-LAB/application_navigation), and [application_localization](https://github.com/AUROVA-LAB/application_localization).

### Usage instructions:

- Step 0: You should change the parameter ~global_planning/url_path in "application_navigation/blue/gazebo.yaml" file, to indicate your local PC path. 

- Step 1: To run the local and global path planning, and the utm->map /tf, run following command:
```shell
roslaunch application_navigation blue_gazebo.launch
```

- Step 2: To run the complete localization system, run the following command:
```shell
roslaunch application_localization blue_gazebo.launch
```

- Step 3: After that, to start the autonomous navigation, you should send a goal usin rviz button "2D Nav Goal" and the mouse.

![](/documentation/approach.png)

**Dataset for example in offline mode:** [dataset link](https://drive.google.com/drive/folders/1JylIt_s6RiW5Y0EOHebXSuj3hUjQmQpG?usp=sharing).

