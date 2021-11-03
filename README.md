# YOLOv5 Transfer Learning using COCO 2017 Image Dataset
In this notebook[coco_2017.ipynb], we shall train YOLOv5 model on coco dataset & use it to predict images in the test set. \ 
The coco 2017 dataset contains 118287 images[train], 5000 images[val] & images[test]. \
Note that only the train & val images have annotations. 

# Dataset
Download the datasets from this link: 
[https://cocodataset.org/#download](url)

For newbies, an easy way to download the data is to first locate the links here[boxed in red]: 
![alt text](https://github.com/kwquan/COCO_2017/blob/main/data_1.png)

Next, [for each link]right-click & copy link address:
![alt text](https://github.com/kwquan/COCO_2017/blob/main/data_2.png)

Open up command line, cd to desired directory & download using curl & the copied link:
![alt text](https://github.com/kwquan/COCO_2017/blob/main/data_3.png)

Unzip the files using this: \
![alt text](https://github.com/kwquan/COCO_2017/blob/main/data_4.png)

# File Structure
To enable YOLOv5 to train on custom data, we need to put the files in the following format:
![alt text](https://github.com/kwquan/COCO_2017/blob/main/files.png)

In our directory, we need to first create 2 folders[images & labels]. \
Within each folder, we then create 3 folders[train,val.test]. \
Since test images do not have labels, we shall leave that out for now. \
After downloading the images, kindly place them in their respective folders before proceeding to the next step. 

# Create Labels
For each image, we need to create a txt file that contains the bounding box information[seperated by 1 space]: \
category id, bounding box x coordinate, bounding box y coordinate, bounding box width, bounding box height 

A sample is provided below: 

![alt text](https://github.com/kwquan/COCO_2017/blob/main/sample_text.png)

Note that all box info values have to be scaled using image height/width. \
Using the code provided in the notebook, the txt files for each image can be created & stored under their respective folders in 'label'. 
