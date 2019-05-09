# application_localization
This package contains an application consisting of different launch files that execute diferent localization algorithms using [BLUE robot](https://github.com/AUROVA-LAB/robot_blue) and nodes for adapt sensor data. Next we describe two example of how to run two different localization applications.

### AMCL based application:
**Dependences:** [navigation_stack](https://github.com/ros-planning/navigation) (AMCL package and map server package), [robot_blue](https://github.com/AUROVA-LAB/robot_blue), [aurova_reactives](https://github.com/AUROVA-LAB/aurova_reactives), and [aurova_preprocessed](https://github.com/AUROVA-LAB/aurova_preprocessed).
* Step 1: run amcl_blue_online.launch.
* Step 2: localize the robot in the map using rviz functionality.

