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

## Inputs

**Reference video path:** Enter the path of the reference video or use browse button to select the file using UI.

**New video path:** Enter the path of the new video or use browse button to select the file using UI.

**Rotation:** Set a rotation when loading the video frames(90, 180, 270)

**Computation backend:** Backend is the API used to interact with the hardare.

**Target device:** It is the device on which the computation is to be done. Refers to device such as CPU or GPU. It is different for each manufacturer. Example OpenCL for AMD GPUs and CUDA for NVIDIA GPUs.

**CONF_THRESHOLD:** Confidence threshold for yolo

**NMS_THRESHOLD** Non maximum suppression threshold. For a better understanding of thresholds check [this](https://www.pyimagesearch.com/2018/11/12/yolo-object-detection-with-opencv/) article.

**max_diaappearing:** Maximum number of frames an object must be missing to stop tracking the object.

**Save output video** Selecting this chekcbox saves the ouptut video in the same folder as the new video

**Save log** Selecting this chekcbox saves the log file in the same folder as the new video. The log files contains the detections and tracking information of the objects, how they are matched and the object IDs of missing and new objects.

After setting all the inputs click on the run button to start the change detection process. To abort the process click on the abort button. Click on the exit button to exit the application.
