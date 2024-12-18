Repo for experiments using the SoftLeg (3 DoFs SEA-robot). 
[Paper](https://ieeexplore.ieee.org/abstract/document/10529546)

Training has been done by implementing RL-baseline PPO via the NVIDIA Omniverse framework [softleg_jump_cinque.py](https://github.com/michelepierallini/OmniIsaacGymEnvs/blob/main/omniisaacgymenvs/tasks/softleg_jump_cinque.py)

The interference Node is mainly adapted from [loco_sim](https://github.com/CentroEPiaggio/locosim_ws)

# Usage in Simulations
(i)
```
source /opt/ros/humble/setup.bash
colcon build --symlink-install && . install/setup.bash
export ROS_DOMAIN_ID=10
ros2 launch softleg_gazebo sim.launch.py
 ```
(ii)
```
source /opt/ros/humble/setup.bash
colcon build --symlink-install && . install/setup.bash
export ROS_DOMAIN_ID=10
ros2 launch rlg_quad_controller softleg_simulation.launch.py
```

# Usage in Exp

(i) Raspberry interface.
(ii) local
```
source /opt/ros/humble/setup.bash
colcon build --symlink-install && . install/setup.bash
export ROS_DOMAIN_ID=10
ros2 launch jumping_experiments controller_start.launch.py
ros2 run jumping_experiments getup
ros2 launch jumping_experiments experiment.launch.py exp:='experiment_number_1' csv:='Data.csv' height:='1.0' duration:='3.0'
```


# Please
Change the path of ```.stl``` files to the ```softlegisaac.urdf```
