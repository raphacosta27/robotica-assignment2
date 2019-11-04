# robotica-assignment2

## Directory structure

    .
    ├── catkin_ws                
        ├── src
            ├── motion_plan
                ├── scripts
                    ├── follow_wall.py
                ├── src
                ├── CMakeLists.txt
                ├── package.xml  
    ├── simulation_ws
        ├── src
            ├── ag2
                ├── launch
                    ├── rviz.launch
                    ├── spawn.launch
                ├── urdf
                    ├── ag2.gazebo
                    ├── ag2.xacro
                    ├── macros.xacro
                    ├── materials.xacro
                ├── worlds
                    ├── mundo
                ├── CMakeLists.txt
                ├── package.xml                
    ├── LICENSE
    └── .gitignore

## Requirements
- The project was built using the <i> ROS Kinetic Kame </i> and <i>Ubuntu Xenial (16.04 LTS)</i>. But if you have <i>ROS Melodic Morenia</i> under <i>Bionic (18.04 LTS)</i> and fulfill all other requirements it will also work.
- Gazebo multi-robot simulator, version 7.16.0 or later.
## How to compile
```
    cd simulation_ws
    catkin_make 
    cd ../catkin_ws
    catkin_make 
```

## How to execute

In one terminal: <br>
```
cd simulation_ws 
source devel/setup.bash 
roslaunch ag2 spawn.launch 
```

Open another terminal:<br>
```
cd catkin_ws 
source devel/setup.bash 
chmod +x src/motion_plan/scritps/follow_wall.py 
rosrun motion_plan follow_wall.py 
```