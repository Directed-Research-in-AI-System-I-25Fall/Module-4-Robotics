# Practice Assignment - Robotics

This tutorial guides you through the basics of *physics simulation* and *motion planning* for robotics applications. You will use various tools and frameworks to understand the principles of robot motion planning.

## Task 1: Setup Environment and Introduction to Robotics Research (6 pts)

To begin, you must prepare your environment for conducting robotics research. This lab can be completed using any combination of physics simulation and motion planning frameworks.

**Recommended Simulators:**

- **PyBullet** (Highly recommended; lightweight and easy to use)
- **MuJoCo**
- **Isaac Sim** (Requires RTX GPU)
- **SAPIEN**
- **CoppeliaSim**
- **Gazebo**

*Recommended Motion Planning Frameworks:**

- **[MPlib](https://github.com/haosulab/MPlib)** (Highly recommended; lightweight and easy to use)
- **cuRobo** (Best utilized with Isaac Sim and with GPU)
- **MoveIt/MoveIt 2** (Requires ROS/ROS 2 respectively)

Begin by setting up your chosen tools. Refer to the "get started" guides or example codes provided by each tool. For additional resources and helpful code snippets, visit [Simulately](https://simulately.wiki/).

Of note, the core of the motion planning libraries lies in accurately computing the kinematics. This should be independent with the simulator, i.e., the kinematics APIs of the motion planner can be used individually, without any simulator.

### Setup and Explore the Simulator (3pts)

1. [1 pt] Install your selected simulator. Report on the simulator chosen and describe any notable observations encountered during exploration.
2. [1 pt] Load a robot model, preferably the Franka Panda, into the simulator. Initialize the simulator so the robot appears in its default pose. Report the screenshot.
3. [1 pt] Use the APIs provided to directly get the joint limits, current joint positions, and current end-effector pose of the robot. Report the APIs you use and the results.

### Setup and Explore the Motion Planner (3pts)

1. [1 pt] Install your chosen motion planning framework. Report on the motion planner chosen and describe any notable observations encountered during exploration.
2. [2 pts] Configure the motion planner for your robot, ensuring it includes APIs for forward and inverse kinematics, as well as motion planning.

## Task 2: Explore Forward Kinematics (4 pts)

This task involves visualizing the robot's workspace.

1. Start the motion planner.
2. [2 pts] Sample in the robot's *configuration space* and compute the forward kinematics with the API provided by the motion planner for each sample to get the end-effector's pose (1 pt). Apply the joint positions to the robot in the simulator (1 pt). Report the screenshot of the simulation and attach the corresponding code.
3. [2 pts] Uniformly sample at least 1000 configurations in the configuration space, compute their end-effector poses, and visualize them in a 3D plot. `matplotlib` or `plotly` are recommended for visualization. Include the generated 3D plot (better saved as a vector graphic) in your report.

## Task 3: Explore Inverse Kinematics (Bonus, 1pts)

This advanced task focuses on inverse kinematics and collision avoidance.

1. Start both the simulator and the motion planner.
2. Randomly generate an end-effector pose within the robot's workspace and compute the joint configurations using inverse kinematics. Verify the accuracy of the inverse kinematics by computing forward kinematics on the solved joint positions and comparing it with the end-effector pose.

**Deliverable:** Provide a comprehensive report on the implementation and attach the code. Include screenshots of the final robot pose in the simulator.
