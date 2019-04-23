# Easy_hand_eye_calibration_kinova

Use the packages for hand-eye calibration of a 6-DOFs Kinova-jaco arm! The calibration is done between the end-effector frame of kinova arm and color_optical_frame of realsense camera.

## Prerequisite
- ROS kinetic

- Official packages of Kinova_jaco
  - kinova_bringup
  - j2n6s300_moveit_config

- Official package of realsense2

- Realsense camera mounted in hand.

- AR marker with size 5.4 * 5.4 (cm)

## Contents
- AR track

  Track the pose of the AR markers. See Readme in the package for details.

- Visp_hand2eye_calibration

  Low-level dependency of the package easy_handeye. Just keep it.
  
- Easy_handeye

  Core package for implementation of hand-eye calibration. See Readme in the package for details.
  
## User Instructions
  1. Make sure the prerequisites are ready. Build the packages with catkin tool.
  
  2. Launch warmup.launch in easy_handeye/easy_handeye/launch. Wait until all the files have already been launched.
  
  3. Launch calibrate.launch in the same folder. 
  
  4. Then start the calibration process. Place a AR marker on the table, and make it completely inside the field of view of camera by moving the arm manually. Change the position and orientation of end effector step by step and do calibration. Please refer to the instructions in Readme of easy_handeye package. (Please read carefully for the tricks! Such as how to move the arm for better calibration accuracy.)
  
  5. When calibration completes, manually write done the calibration parameters.
  
  6. You can also try to make it more convenient by enable moving the arm automatically and saved the parameters in a file. (Please refer to the instructions in Readme of easy_handeye package.) 


