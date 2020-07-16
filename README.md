# MonoCamCalib4AD
This repository mirrors the [Monocular Camera Calibration for Autonomous Driving — a comparative study](https://www.researchgate.net/publication/341500803_Monocular_Camera_Calibration_for_Autonomous_Driving_-_a_comparative_study) paper, that summarizes the main camera models used for perspective cameras (narrow and wide-angle), and fisheye cameras, describing the various distortion parameters involved. It provides results on the calibration of a wide-angle camera setup and a fisheye lens setup, comparing the use of various distortion models. Furthermore, it describes the use of homography for perspective transformations between a camera view and a virtual camera view. The main goal of this paper is to provide, in a single document, an overview on monocular camera calibration and bids-eye view perspective transformation, serving as a starting point for researchers starting to work with monocular vision.
Here, it is available all the algorithms used throughout the document, through a Jupyter notebooks using OpenCV 4.1.1, so one can easily experiment and run then without any further installations.

**GETTING START, you should open the [Calibration&BirdsEyeView](https://github.com/ipleiria-robotics/MonoCamCalib4AD/blob/master/Calibration&BirdsEyeView.ipynb) file and and go to 
![Alt text](https://colab.research.google.com/assets/colab-badge.svg) shown on top.**

## Calibration algorithm
*A camera consists mainly of a planar optical sensor and a lens, together with the electronics needed to obtain thedigital image of the scene projected onto the optical sensor. Camera images exhibit distortion due to the lens characteristics and production defects. The most common distortion effects are the radial distortion, tangential distortion and the thin prism distortion, which affect the captured point coordinates and can be rectified using this calibration algorithms approaching the following models:*
 * *Standard Model*
 * *Rational Model*
 * *Thin Prism Model*
 * *Tilted Model*
 * *Fisheye Model*
 

### Wide-angle Lens Example
Distorted             |  Undistorted
:-------------------------:|:-------------------------:
<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/1.7mm_original.png">|<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/1.7mm_undistorted.png">

### Fisheye Lens Example
Distorted             |  Undistorted
:-------------------------:|:-------------------------:
<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/distorted_img.png">|<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/undistorted_img.png">

## Homography Results
The homography relates the transformation between two world planes defined on a common reference frame. For autonomous driving, our reference plane is the ground plane. By placing a planar chessboard in front of the robot and in view of the (previously calibrated) camera, one can use the same techniques to estimate the camera pose with respect to the chessboard on the floor, that is, the extrinsic parameters (or the inverse, the chessboard pose with respect to the camera).

### Birds-eye View Example
Distorted             |  Undistorted
:-------------------------:|:-------------------------:
<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/undistorted.png">|<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/chessboard.png">

# Conclusions
The results presented show that it is important to fit the distortion model used for each specific combination of camera and lens, given that some lens and distortion models, although more complete, may be unsuitable for the setup at hand. Beware that this is a very low cost system, with low cost lenses, thus the imperfections that are seen in the borders of the image, which can not be corrected by these models.
