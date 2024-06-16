# Object Detection Using TensorflowLite
Welcome to our Object Detection project, built using TensorFlow Lite and Raspberry Pi! This project leverages the power of machine learning to identify objects in real-time through a web camera. Designed to be lightweight and efficient, it's a perfect demonstration of edge AI capabilities, making it ideal for various applications such as home automation, security, and educational purposes.This guide provides step-by-step instructions for how to set up TensorFlow Lite on the Raspberry Pi and use it to run object detection models
## Features
<ul>
<li>Real-Time Object Detection: Identify and classify objects in real-time using a live feed from a web camera.</li></br>
<li>Edge Computing: Efficiently runs on Raspberry Pi, showcasing the potential of edge AI devices.</li></br>
<li>TensorFlow Lite: Utilizes TensorFlow Lite for optimized performance on low-power devices.</li></br>
<li>Easy Setup: Simple installation and configuration process to get the model up and running quickly.</li></br>
</ul>

## How it works
<ul>
<li>Capture: The Raspberry Pi's connected web camera captures images in real-time.</li>
<li>Process: The captured images are processed using a pre-trained TensorFlow Lite object detection model.</li>
<li>Identify: The model identifies the objects present in the images and outputs their names.</li>
</ul>

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
![raspberry-pi-configuration-camera](https://github.com/Iswarya-Singaram/Object_Detection_Using_TensorflowLite/assets/145309713/7dc9ce06-914d-4be7-9e5f-30a3b0448817)


 

 
 
