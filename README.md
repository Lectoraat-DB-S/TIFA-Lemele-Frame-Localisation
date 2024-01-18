# TIFA Lemele Frame Localisation
FOR EXTENSIVE DOCUMENTATION, SEE [THIS FILE](Documentation%20Azure%20Kinect.docx).

The goal of this project is to detect, localise and determine the orientation of a window frame using a Microsoft Azure Kinect DK. Image processing is done using Halcon. This repository contains a number of files. A quick explanation on which file is which:

- KinectCloud based colored point cloud grabber.hdev: use KinectCloud and CloudCompare to grab and convert point clouds
- Azure Kinect Filtering.hdev: first iteration of the filtering script
- Filters Demo simplified.hdev: a more advanced and simplified version of Azure Kinect Filtering
- Filters Demo simplified SHOWEVERYSTEP.hdev: the same as the original, but it will visualise the object_model_3d with every step of the process
- Window Frame Filtering.hdev: combination of KinectCloud based colored point cloud grabber and Filters Demo simplified SHOWEVERYSTEP. this script does everything, from grabbing a point cloud, visualising every step and generating an output .txt file
- Cobot/Demo TiFa 10-01-2024.urp: cobot demo application used for the demo day

## Imports and versions
Microsoft Windows 11 22H2
Halcon - MVTec HDevelop 23.05 Progress
Since the Azure Kinect isn't directly compatible with Halcon, the following programs are used to capture and convert point clouds:
- KinectCloud (capturing coloured point clouds) https://github.com/widVE/KinectCloud
- CloudCompare (converting captured .pts file to .ply) https://www.cloudcompare.org/

## External devices
Universal Robots UR10e Cobot