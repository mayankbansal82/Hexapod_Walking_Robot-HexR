# Hexapod_Walking_Robot-HexR

In this project, a physical hexapod walking robot was developed for my Legged Robotics course. The robot parts were 3D printed and assembled and then the appropriate leg trajectories were calculated to move the leg of the robot. A tripod gait is adopted in this project for the walking of the robot.


### Tools used
- 3D Printer (Ultimaker) with PLA material
- Arduino Uno
- PCA9685 16 channel servo controller
- SG90 servo motors
- ROS serial

### Methodology

- The CAD model of the hexapod robot developed in [this project](https://www.instructables.com/Simple-NodeMCU-18-DOF-Hexapod/) was selected and the .stl files were downloaded. The parts were 3D printed in an Ultimaker and assembled using Arduino Uno, servo controller and SG90 servo motors.

- Since there were only 16 channels on the servo controller and the robot is of 18 DOF, the remaining two servos were provided the PWM signal using Arduino itself.

- Arduino was setup as a subscriber which takes joint angles from the publisher set up in the main machine. The publisher calculates the joint angles using IK from the end-effector spatial point generated from the trajectory planning.

- The subscriber moves the servos according to the joint angles received.

### Result

![Alt Text](https://github.com/mayankbansal82/Hexapod_Walking_Robot-HexR/blob/main/Images/Hexapod.jpeg)

The robot performing the tripod gait motion can be seen in the below GIF.

![Alt Text](https://github.com/mayankbansal82/Hexapod_Walking_Robot-HexR/blob/main/Images/output.gif)


