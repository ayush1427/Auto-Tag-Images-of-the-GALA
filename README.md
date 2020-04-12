# HackerEarth Prize Competition- Auto-Tag Images of the Gala

This is a competition that was hosted on HackerEarth and last submission date was April 7th, 2020.

## Description

### **Problem statement**

Galas are the biggest parties of the year. Hosting firms of these events are well aware that everyone from around the world has their eyes on these nights. It can be for inspiration or for critique. It takes months of meticulous planning and delegation to host these events.

One such firm has decided to take a data-driven approach for planning their gala nights going forward. Aesthetics and entertainment are the most crucial segments of these events. So, this firm has hired you to help them aggregate and classify all images. These images are published by attendees and the paparazzi on various social media channels and other sources. You are required to build an image auto-tagging model to classify these images into separate categories.
Data

The dataset consists of the following two columns:

    Column Name 	Description
    Image 	    Name of Image
    Class 	    Category of Image ['Food', 'Attire', 'Decorationandsignage', 'misc']

### **Data description**
The data folder consists of two images folders and two CSV files.

Folders

    train: Contains 5983 images for 4 classes ['Food', 'misc', 'Attire', 'Decorationandsignage']
    test: Contains 3219 images

CSV files

    train.csv: (5983 x 2)
    test.csv: (3219x1)

sample_submission

    Image,Class
    image0001.jpg,Food
    image0002.jpg,Attire
    image0003.jpg,Food
    image0004.jpg,misc
    image0005.jpg,Attire

### **Evaluation metric**

    score = 100 * f1_score ( actual_values, predicted_values, average = 'weighted' )

Note: To avoid any discrepancies in the scoring, ensure all the index column ('Image_File') values in the submitted file match the values in the provided **test.csv** file.

[Competition Link](https://www.hackerearth.com/challenges/competitive/hackerearth-deep-learning-challenge-auto-tag-images-gala/machine-learning/auto-tag-images-of-the-gala-9e47fb31/)

## My understanding of the competition

It is Classification problem with metric evaluation as f1_score. ResNet50 which is a Pre-trained classification architectures has been used as a base model. And upon it, a pretrained VGG19 model has been used that works fine on this dataset, with suitable data augmentations and regularizations. Hoping for a easy solution as this was my first attempt.

## My approach

1. Check the class distribution of imbalances 
2. Training Images Viualization 
3. Image Shape Variations to set the resize values
4. Creating Folders for Dataset
5. Normalization Parameter
6. performed augmentation on the dataset
7. Train the model with Adam optimizer. 
8. Saving best checkpoints based on best achieved validation score.
9. Prediction on the trained model.

## Files
1. [Ipynb notebook](https://github.com/ayush1427/ayush1427/blob/master/Auto-tag-galas-classification.ipynb)
2. [Dataset zipped](https://drive.google.com/open?id=1uHPc9sJ8jrKRLBYSo5p4QdAf_Y7cMqLu) 

## Contributions 
Any improvements to my technique would be greatly appreciated, including improvement, typos, etc ..
