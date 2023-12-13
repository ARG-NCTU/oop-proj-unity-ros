# oop-proj-unity-ros
This repo is a starter kit tutorial of ROS (python) side with rosbridge to connect to unity.
It is a easy project to move a cube with keyboard or VR joystick  
You need another repo for unity side to run this project.  
https://github.com/ARG-NCTU/oop-proj-unity  

# Setup: run with docker and build the rospackage
1. run with docker 
```
$ cd ~/oop-proj-unity-ros
$ source docker/docker_run.bash
```
2. build rospackage
```
(docker) # cd catkin_ws
(docker) # catkin_make
```

# Usage: how to run after set up
1. Terminal1: roscore
 ```
$ cd ~/oop-proj-unity-ros
$ source docker/docker_run.bash
(docker) # source environment.sh
(docker) # roscore
```

2. Terminal2: Publisher & Subscriber code of cube   
 ```
$ cd ~/oop-proj-unity-ros
$ source docker/docker_join.bash
(docker) # source environment.sh
(docker) # rosrun example cube_position.py
```
If you can see cube position:[0, 0] shows up, it means you are doing right.

3. Terminal3: Rosbridge server for unity to connect
```
$ cd ~/oop-proj-unity-ros
$ source docker/docker_join.bash
(docker) # source environment.sh
(docker) # roslaunch rosbridge_server rosbridge_websocket.launch
```