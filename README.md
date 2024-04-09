# Tiger Detection using ATRW Dataset with TensorFlow-GPU Backend

This readme provides a comprehensive guide on training your own custom tiger detection model using the ATRW dataset by CVWC (Computer Vision Winter School) with a TensorFlow-GPU backend on a Linux-based setup. The process involves several steps:

## Steps

### 1. Data Preprocessing

#### 1a. Download the ATRW dataset by CVWC
Download the [tiger detection dataset](https://cvwc2019.github.io/challenge.html), including both the image dataset and the annotation files.

#### 1b. Edit the discrepancy of filename tags in XML files
Correct any discrepancies in the name of XML files and the filename tags within them to prevent issues during the generation of TFRecords.

#### 1c. Split the dataset into train and test
Split the dataset into training and validation sets and organize them into appropriate directories.

### 2. Setting up the working environment

#### 2a. Create a tmux session and link TensorFlow Docker image
Set up a tmux session for managing tasks and link a TensorFlow Docker image, ensuring proper utilization of GPU resources.

#### 2b. Set up TensorFlow Directory
Download the TensorFlow object detection repository and set up the directory structure accordingly.

#### 2c. Download the Faster-RCNN-Inception-V2-COCO model
Download the pre-trained Faster-RCNN-Inception-V2-COCO model from TensorFlow's model zoo.

#### 2d. Download the tutorial's repository from GitHub
Download the repository containing necessary scripts and configurations for training the object detection model.

#### 2e. Compile Protobufs and run setup.py
Compile the Protobuf files and run setup.py to prepare the environment for training.

### 3. Generate Training Data

#### 3a. Generate CSV and TFRecords
Use XML files to create CSV files containing image data and generate TFRecords for training.

#### 3b. Create Label Map
Create a label map specifying class names and IDs for the objects to be detected.

#### 3c. Configure training
Configure the object detection training pipeline, specifying model parameters and file paths for training data.

#### 3d. Run the training
Initiate the training process using the configured pipeline, ensuring proper GPU utilization and monitoring training progress.

### 4. Saving and Inferring the model

#### 4a. Exporting the inference model
Export the trained model as a frozen inference graph (.pb file) for inference purposes.

#### 4b. Evaluating the model
Evaluate the trained model's performance using evaluation scripts and visualize results using TensorBoard.

### 5. Deploying it on Raspberry Pi

Refer to the [TensorFlow-Object-Detection-on-the-Raspberry-Pi](https://github.com/EdjeElectronics/TensorFlow-Object-Detection-on-the-Raspberry-Pi) tutorial for deploying the trained model on a Raspberry Pi.

## Results on Different Models

The trained model's performance can be evaluated and compared across different architectures, such as Faster-RCNN-Inception-V2, SSD-Inception-v2, and SSDLite-MobileNet.


This readme provides a detailed guide for training a custom tiger detection model using TensorFlow-GPU on a Linux-based setup, enabling you to deploy the model for real-world applications.
