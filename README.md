# Change Detection in Image Sequences

Object level change detection is the process of finding the change in objects in a given image sequence with respect to the reference images. In this paper, we have proposed a difference-based algorithm which can be used to classify the changes in the two different videos by converting them to each different set of image frames. Our main objective is to find diffrence between two video sequences of the same path but taken at diffrent time. 

This algorithm is mainly focuses on detecting the changes in the image sequence of a video that are captured by a drone. We capture two different sets of videos (assuming that the drone travels in same path) of which one is the reference video and the other video is the one in which the changes has to be determined. The proposed method uses the YOLO model for the object detection, a simple centroid tracker for object tracking. The output of the system is a video with bounding boxes drawn around new and missing objects.


## Requirements
Install python 3.7.6
https://www.python.org/downloads/release/python-376/

Install the following packages using pip or conda
- opencv-python 3.4.2.16
- scikit-image 0.16.2
- scipy 1.3.x
- numpy 1.18.1
- pillow 7.0.0

To install using pip use the command

*pip install package-name==x.x.x*

To install using conda use the command

*conda install package-name=x.x.x*

Clone the repository running the command in bash

*git clone https://github.com/nandanm98/Change_Detection_in_Image_Sequences.git*


## Running the program
![](/Screenshots/out1.png)
Windows users can run the *run.bat* file.

Linux users can run the program in the bash opened in the cloned directory using the command
*python main.py*

Give the path og the video in the output window
Give the required thresholds and other input parameters
Run 
All the output log will be saved with the output video
