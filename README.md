## Gen3 + Vision MoveIt Configuration Package

This is a custom MoveIt2 configuration package for the Kinova Gen3 Ultra lightweight robot, a 6DoF arm with vision module and without gripper.

### Prerequisites
- Install ROS2 following [these](https://docs.ros.org/en/iron/Installation.html) instructions (Tested with ROS2 Iron)
- Install MoveIt2 following [these](https://moveit.picknik.ai/main/doc/tutorials/getting_started/getting_started.html) instructions. I recommended to follow the instructions exactly as I am aware of some problems arising from using the binary install instead. \
This installation also includes the necessary Kinova Kortex API and packages.
- Creat your own colcon workspace ([instructions](https://docs.ros.org/en/iron/Tutorials/Beginner-Client-Libraries/Creating-A-Workspace/Creating-A-Workspace.html))
- Clone this package into your workspace/src directory
- Navigate to your workspace directory and run `colcon build`
- Finally, source your workspace `source ./install/setup.bash`

### Usage
- To launch the robot in simulation, use `ros2 launch gen3_6dof_vision_moveit_config robot.launch.py robot_ip:=yyy.yyy.yyy.yyy use_fake_hardware:=true`\
- To use the physical robot, use `ros2 launch gen3_6dof_vision_moveit_config robot.launch.py robot_ip:=192.168.1.10`