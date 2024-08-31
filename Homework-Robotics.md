# Homework - Robotics

In a cube-stacking task, multiple cubes are in the front of a robot. The robot is tasked to stack these blocks together. The extents of the blocks are given.

For simplicity, we assume that the poses of the blocks and the robot are all known. we pick each cube from its top, perpendicular to the ground, so you can assume the end-effector pose for grasping each cube can be directly computed from the cube's pose.

<img src="stack_cubes.png" alt="stack_cubes" style="zoom:25%;" />

> The image is from [NVIDIA cuRobo Docs](https://curobo.org/advanced_examples/2_block_stacking_example.html).

Discuss how to implement a block stacking with robot motion planners following the guidelines:

1. [5 pts] Write a pseudo code for performing this task. Use functions like `motion_plan(...)` to represent the APIs you need (3 pts), and discuss what arguments should be provided and how to compute them (2 pts).
2. [2 pts] When grasping a cube, directly planning the robot to the grasping pose will likely make the end-effector colliding with the cube. Can you come up with any simple strategy to avoid this?
3. [2 pts] Open question: If the simplicity assumptions cannot be fulfilled, and the robot is equipped with a depth camera, discuss what essential modules and procedures for the robot to finish the task.
4. [Bonus 2pts] In the question above, assume each module can be implemented by a function like `acquire_robot_camera_rgbd_img(...)`, `rgbd_img_to_point_cloud(...)`, and `grasp_plan_from_object_point_-cloud(...)`, update your pseudo code, and explain the input and output for each function as well as how to compute them.
