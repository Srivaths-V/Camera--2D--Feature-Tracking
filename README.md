# Sensor Fusion Program - 2nd Project 2D Feature Tracking

<img src="images/keypoints.png" width="820" height="248" />

The idea of the camera section of Sensor fusion course is to build a collision detection system - that's the overall goal for the Final Project - 3D Object Tracking. As a preparation for this, I have built the 2D feature tracking part and tested various detector / descriptor combinations to see which ones perform best. This 2D feature tracking project consists of four parts:

* First, task was on loading images, setting up data structures and putting everything into a ring buffer to optimize memory load. 
* Then, integrated several keypoint detectors such as HARRIS, FAST, BRISK and SIFT and compare them with regard to number of keypoints and speed. 
* In the next part, I focussed on descriptor extraction and matching using brute force and also the FLANN approach. 
* In the last part, once the code framework is complete, I tested the various algorithms in different combinations and compared them with regard to some performance measures. 

With this project, the keypoint matching part will be set up and which will be used for 3D-Object Tracking project, where the focus is on integrating Lidar points and on object detection using deep-learning. 

## Dependencies for Running Locally
* cmake >= 2.8
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* OpenCV >= 4.1
  * This must be compiled from source using the `-D OPENCV_ENABLE_NONFREE=ON` cmake flag for testing the SIFT and SURF detectors.
  * The OpenCV 4.1.0 source code can be found [here](https://github.com/opencv/opencv/tree/4.1.0)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./2D_feature_tracking`.
