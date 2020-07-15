# MonoCamCalib4AD
The algorithms used throughout the NAME and URL paper, are available through a Jupyter notebooks here, so one can easily experiment and run then without any further installations.
To start, you must open the [Calibration&BirdsEyeView](https://github.com/ipleiria-robotics/MonoCamCalib4AD/blob/master/Calibration&BirdsEyeView.ipynb) file and and go to 
![Alt text](https://colab.research.google.com/assets/colab-badge.svg) shown on top.

The paper mentioned above, summarizes the main camera models used for perspective cameras (narrow and wide-angle), and fisheye cameras, describing the various distortion parameters involved. It provides results on the calibration of a wide-angle camera setup and a fisheye lens setup, comparing the use of various distortion models. Furthermore, it describes the use of homography for perspective transformations between a camera view and a virtual camera view. The main goal of this paper is to provide, in a single document, an overview on monocular camera calibration and bids-eye view perspective transformation, serving as a starting point for researchers starting to work with monocular vision.

## Calibration Results

### Wide-angle Lens Example
Distorted             |  Undistorted
:-------------------------:|:-------------------------:
<img align="left" width="640" height="480" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/1.7mm_original.png">|<img align="left" width="640" height="480" src="https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/1.7mm_undistorted.png">

### Fisheye Lens Example
Distorted             |  Undistorted
:-------------------------:|:-------------------------:
![alt text](https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/distorted_img.png)|![alt text](https://github.com/PedroMartins95/Calibration-BirdsEyeView4FisheyeLens/blob/master/undistorted_img.png)

## Homography Results
