```toc
title: "## Table of contents"
```

## Making a workspace for ROS

```bash
cd
mkdir catkin_ws
cd catkin_ws 
mkdir src
catkin_make

```

>For executing our own packages written by ourself we need to repeat catkin_make


>To automatically execute commands type the below command a window will open add the commond on that window that is to be executed automaticaly
```bash
gedit ~/.bashrc
```

### Creating a Package inside workspace

```bash
catkin_create_pkg package_name dependency_libraries_nodes_etc
```
eg,
```bash
cd catkin_ws/src/
catkin_create_pkg my_robot_controller rospy turtlesim
```

Here we can see that workspace is created inside src file.
A workspace can have many number of packages.A package will contain nodes.

## ROS Nodes

### Creating Node inside Package

1. First we need to enter inside package folder

```bash
cd catkin_ws/src/my_robot_controller/
```

2. Make a folder for storing python codes

```bash
mkdir scripts
```

3. Enter inside scripts and make a python file 

```bash
cd scripts/
touch my_first_node.py
```

4. Make the python file executable

```bash
chmod +x my_first_node.py
```

5. Open src folder on vs code and edit the python file

```bash
cd ../../
code .
```


### Running a Node

1. Rosrun allows you to use the package name to directly run a node within a package (without having to know the package path).
Note : [[Ros imported things to note]] 

```bash
rosrun [package_name] [node_name]
```

```bash
rosrun my_robot_controller my_first_node.py
```

### Killing  a node

```bash
rosnode kill /test_node
```

### Reference Links

**1. [[Ros imported things to note]]**
2. [Reference note for nodes](http://wiki.ros.org/ROS/Tutorials/UnderstandingNodes)
3. [Reference video for nodes](https://youtu.be/jWtkzDbez9M)

## ROS Topic

### Reference Links.
**1. [[Ros imported things to note]]**
2. [Reference notes for topic](http://wiki.ros.org/ROS/Tutorials/UnderstandingTopics)
3. [Reference video for topic](https://youtu.be/GAJ3c5XmJSA)
 
