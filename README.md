# TIFA Lemele Frame Localisation
FOR EXTENSIVE DOCUMENTATION, SEE [THIS FILE](Documentation%20Azure%20Kinect.docx).

The goal of this project is to detect, localise and determine the orientation of a window frame using a Microsoft Azure Kinect DK. Image processing is done using Halcon. This repository contains a number of files. A quick explanation on which file is which:

- [KinectCloud based colored point cloud grabber.hdev](KinectCloud%20based%20colored%20point%20cloud%20grabber.hdev): use KinectCloud and CloudCompare to grab and convert point clouds
- [Azure Kinect Filtering.hdev](Azure%20Kinect%20Filtering.hdev): first iteration of the filtering script
- [Filters Demo simplified.hdev](Filters%20Demo%20simplified.hdev): a more advanced and simplified version of Azure Kinect Filtering
- [Filters Demo simplified SHOWEVERYSTEP.hdev](Filters%20Demo%20simplified%20SHOWEVERYSTEP.hdev): the same as the original, but it will visualise the object_model_3d with every step of the process
- [Window Frame Filtering.hdev](Window%20Frame%20Filtering.hdev): combination of KinectCloud based colored point cloud grabber and Filters Demo simplified SHOWEVERYSTEP. this script does everything, from grabbing a point cloud, visualising every step and generating an output .txt file
- [Cobot/Demo TiFa 10-01-2024.urp](Cobot/Demo%20TiFa%2010-01-2024.urp): Cobot demo application used for the demo day

## Imports and versions
- Microsoft Windows 11 22H2
- [Halcon](https://www.mvtec.com/products/halcon/) - MVTec HDevelop 23.05 Progress

Since the Azure Kinect isn't directly compatible with Halcon, the following programs are used to capture and convert point clouds:
- [KinectCloud](https://github.com/widVE/KinectCloud) (capturing coloured point clouds)
- [CloudCompare](https://www.cloudcompare.org/) (converting captured .pts file to .ply)

## External devices
[Universal Robots UR10e Cobot](https://www.universal-robots.com/products/ur10-robot/)