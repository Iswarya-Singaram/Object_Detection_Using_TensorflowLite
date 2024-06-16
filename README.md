# Object Detection Using TensorflowLite
Welcome to our Object Detection project, built using TensorFlow Lite and Raspberry Pi! This project leverages the power of machine learning to identify objects in real-time through a web camera. Designed to be lightweight and efficient, it's a perfect demonstration of edge AI capabilities, making it ideal for various applications such as home automation, security, and educational purposes.This guide provides step-by-step instructions for how to set up TensorFlow Lite on the Raspberry Pi and use it to run object detection models
<p align=center>
<img src="https://github.com/Iswarya-Singaram/Object_Detection_Using_TensorflowLite/assets/145309713/1c5b9b39-831e-4db2-aa8f-e0ced233a0c6" width="500" height="300">
</p>

## Features
<ul>
<li>Real-Time Object Detection: Identify and classify objects in real-time using a live feed from a web camera.</li></br>
<li>Edge Computing: Efficiently runs on Raspberry Pi, showcasing the potential of edge AI devices.</li></br>
<li>TensorFlow Lite: Utilizes TensorFlow Lite for optimized performance on low-power devices.</li></br>
<li>Easy Setup: Simple installation and configuration process to get the model up and running quickly.</li></br>
</ul>
<p align=center>
<img src="https://github.com/Iswarya-Singaram/Object_Detection_Using_TensorflowLite/assets/145309713/523a6fe4-77b5-4511-b9c7-f1f961fc3e91" width="500" height="300">
</p>

## How it works
<ul>
<li>Capture: The Raspberry Pi's connected web camera captures images in real-time.</li>
<li>Process: The captured images are processed using a pre-trained TensorFlow Lite object detection model.</li>
<li>Identify: The model identifies the objects present in the images and outputs their names.</li>
</ul>
<p align=center>
<img src="https://github.com/Iswarya-Singaram/Object_Detection_Using_TensorflowLite/assets/145309713/388ab8fa-658e-48ad-8340-a8045cc43135" width="500" height="300">
</p>

 ## Requirements
   <ol>
<li>Raspberry Pi 4 or 5 (preferably with 2GB RAM or more)</li>
<li>Web camera compatible with Raspberry Pi</li>
<li>TensorFlow Lite</li>
<li>Python 3</li>
 </ol>

 ## Getting Started
 The Getting Started part consists of the following subparts 
 <ol>
   <li>Setting up the raspberry pi</li>
   <li>Download the github repository and create an environment</li>
   <li>Installing all the necessary packages</li>
   <li>Setting up the object detection model</li>
   <li>Running the model</li>
 </ol>

 ## Setting Up the Raspberry Pi
 ### Step-1:Update Your Raspberry Pi
 Open the teminal in your raspberry pi and update it using the following command
 ~~~
sudo apt-get update
sudo apt-get dist-upgrade
~~~
 The upgrade process should only take a minute or two, depending on when it was last updated.
 ### Step-2:Set Up the Configuration
For Raspberry Pi 4 and 5:
No additional configuration is needed, as the camera is enabled by default.

For Lower Versions of Raspberry Pi:
<ol>
<li>Click the Pi icon in the top left corner of the screen.</li>
<li>Select Preferences -> Raspberry Pi Configuration.</li>
<li>Go to the Interfaces tab.</li>
<li>Verify that Camera is set to Enabled. If it is not, enable it now.</li>
<li>Reboot the Raspberry Pi to apply the changes.</li>
</ol>
<p align="center">
  <img src="https://github.com/Iswarya-Singaram/Object_Detection_Using_TensorflowLite/assets/145309713/7dc9ce06-914d-4be7-9e5f-30a3b0448817">
</p>

## Download the github repository and create an environment
### Step1: Download the github repository
Next, clone the github repository by using the following command
~~~
git clone https://github.com/EdjeElectronics/TensorFlow-Lite-Object-Detection-on-Android-and-Raspberry-Pi.git
~~~
This downloads everything into a folder called TensorFlow-Lite-Object-Detection-on-Android-and-Raspberry-Pi.Since, the folder name is too long, we can rename it to tflite1 by using the following command. Then use cd to change the directory to tflite1
~~~
mv TensorFlow-Lite-Object-Detection-on-Android-and-Raspberry-Pi tflite1
cd tflite1
~~~
### Step 2:Create an environment
 Next up is to create a virtual environment called "tflite1-env".
 Install virtualenv by using
 ~~~
sudo pip3 install virtualenv
~~~
Then, create the "tflite1-env" virtual environment by issuing:
~~~
python3 -m venv tflite1-env
~~~
This will create a folder called tflite1-env inside the tflite1 directory. The tflite1-env folder will hold all the package libraries for this environment. Next, activate the environment by issuing:
~~~
source tflite1-env/bin/activate
~~~
Note:To reactivate the tflite1-env virtual environment every time you open a new terminal window, you should navigate to the /home/pi/tflite1 directory and issue the command source tflite1-env/bin/activate. When the virtual environment is active, you will see (tflite1-env) appear at the beginning of your command prompt.
## Installing all the necessary packages
Next, we'll install TensorFlow and OpenCV along with their required dependencies. While OpenCV is not essential for running TensorFlow Lite, the object detection scripts in this repository utilize it to capture images and visualize detection results.
~~~
pip install tensorflow==2.12
~~~
You can install any tensorflow version of your choice
<p align="center">
  <img src="https://github.com/Iswarya-Singaram/Object_Detection_Using_TensorflowLite/assets/145309713/70074049-dd87-4b18-8100-26eee172b4cd">
</p>
If you come across an error like "Failed to build wheels" as shown in the screenshot above, follow these steps in the terminal...
Install h5py by cloning the git

~~~
git clone https://github.com/h5py/h5py.git
~~~
And change the directory into h5py
~~~
cd h5py
pip install -r requirements.txt
pip install wheel
pip install cython numpy
pip install pkgconfig
sudo apt-get install libhdf5-dev
python setup.py build
python setup.py install
cd ..
pip -c "import h5py"
pip install tensorflow==2.12
~~~
Now run the Object detection model using the following command

~~~
python3 TFLite_detection_webcam.py --modeldir=Sample_TFLite_model
~~~








 



 

 
 
