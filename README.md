# application_localization
This package contains an application consisting of different launch files that execute diferent localization algorithms using [BLUE robot](https://github.com/AUROVA-LAB/robot_blue) and nodes for adapt sensor data. Next we describe two example of how to run two different localization applications.

### AMCL based application:
**Dependences:** [navigation_stack](https://github.com/ros-planning/navigation) (AMCL package and map server package), [robot_blue](https://github.com/AUROVA-LAB/robot_blue), [aurova_reactives](https://github.com/AUROVA-LAB/aurova_reactives), and [aurova_preprocessed](https://github.com/AUROVA-LAB/aurova_preprocessed).
* Step 1: run amcl_blue_online.launch. If you want to run offline, you can run amcl_blue_offline.launch, but you need to modify the file adding the path of your .bag file.
* Step 2: localize the robot in the map using rviz functionality.

![](/documentation/exec_arch.png)

### GNSS-AMCL fusion based application:
**Dependences:** [navigation_stack](https://github.com/ros-planning/navigation) (AMCL package and map server package), [robot_blue](https://github.com/AUROVA-LAB/robot_blue), [aurova_reactives](https://github.com/AUROVA-LAB/aurova_reactives), [aurova_preprocessed](https://github.com/AUROVA-LAB/aurova_preprocessed), [aurova_localization](https://github.com/AUROVA-LAB/aurova_localization), and [robot_localization](https://github.com/cra-ros-pkg/robot_localization) modifying these [files](https://drive.google.com/open?id=1pPElDahEh2vnyUuyCoKvNNV2gxFJLkmA).
* Step 1: run amcl_blue_online.launch. If you want to run offline, you can run amcl_blue_offline.launch, but you need to modify the file adding the path of your .bag file.
* Step 2: localize the robot in the map using rviz functionality.
* Step 3: run navsat_blue.launch.
* Step 4: run ekf_blue.launch.

![](/documentation/exec_arch_gps.png)

