# MonoCamCalib4AD
*Note: an improved version is expected to come online, with references to a paper under review*

This repository mirrors the [Monocular Camera Calibration for Autonomous Driving — a comparative study](https://ieeexplore.ieee.org/document/9096104) paper, which summarizes the main camera models used for perspective cameras (narrow and wide-angle), and fisheye cameras, describing the various distortion parameters involved. It demonstrates the  calibration of a wide-angle camera setup and a fisheye lens setup, comparing the use of various distortion models. Furthermore, it describes the use of homography for perspective transformations between a camera view and a virtual camera view. The main goal of this demo is to provide, together with the cited document, an overview on monocular camera calibration and bids-eye view perspective transformation, serving as a starting point for researchers starting to work with monocular vision, paricularly for autonomous driving.
This repository provides all the algorithms used throughout the document, using a Jupyter notebook and OpenCV 4.1.1, so one can easily experiment and run then without any further installations.

**TO GET STARTED, you should open the [Calibration&BirdsEyeView](https://github.com/ipleiria-robotics/MonoCamCalib4AD/blob/master/Calibration&BirdsEyeView.ipynb) file and and go to ![Colab Icon](colab-badge.svg) shown on top.**
     
## Calibration algorithm
*A camera consists mainly of a planar optical sensor and a lens, together with the electronics needed to obtain thed igital image of the scene projected onto the optical sensor. Camera images exhibit distortion due to the lens characteristics and production defects. The most common distortion effects are the radial distortion, tangential distortion and the thin prism distortion, which affect the captured point coordinates, and can be rectified using calibration algorithms considering, for instance, the following distortion models:*
 * *Standard Model*
 * *Rational Model*
 * *Thin Prism Model*
 * *Tilted Model*
 * *Fisheye Model*
 
Below you can see some of the results that can be obtained through the application of the calibration results to remove the image distortion. 

### Wide-angle Lens Example
Distorted             |  Undistorted
:-------------------------:|:-------------------------:
<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/1.7mm_original.png">|<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/1.7mm_undistorted.png">

### Fisheye Lens Example
Distorted             |  Undistorted
:-------------------------:|:-------------------------:
<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/distorted_img.png">|<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/undistorted_img.png">

## Homography Results
*The homography can be used to relate the transformation between two different camera views, specified on a common reference frame. For autonomous driving, our reference plane is the ground plane, which can be fixed with respect to the vehicle. By placing a planar chessboard in front of the robot and in view of the (previously calibrated) camera, one can use the same techniques to estimate the camera pose with respect to the chessboard on the floor, that is, the extrinsic parameters (or the inverse, the chessboard pose with respect to the camera). That information can later be used to compute a birds-eye-view of the road, considering a virtual camera.*

### Birds-eye View Example
Distorted             |  Undistorted
:-------------------------:|:-------------------------:
<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/undistorted.png">|<img width="320" height="240" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/chessboard.png">

# Conclusions
*The results above show how important the calibration can be, with further details given in the paper. Computing the birds-eye-view can help improve the results for lane detection and tracking. By providing the Jupyter notebook together with the paper, we hope that others can more easily understand and apply these important concepts, which are ever more present on these camera systems used for autonomous driving.*
