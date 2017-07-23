---
layout: post
title:  'How to install opencv3 with Python2 inside a virtualenv'
date: 2017-07-23
categories: OpenCV Install Python2 virtualenv ubuntu
---

# Introduction
Here I'm going to try to give a "simple" guide to create a virtualenv containing opencv3
with video enabled.

# First download a bunch of library

* First make sure that you are up to date with your repositories:
     `sudo apt-get update`
* Download the build tools
     `sudo apt-get install build-essential cmake git pkg-config`
* Install some video libraries:
     `sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libgtk2.0-dev`
* (Not mandatory) You can install some libraries that should optimize OpenCV (unfortunately it looks like magic to me):
     `sudo apt-get install libatlas-base-dev gfortran`
* Ensure that you have python 2 installed:
     `python --version`
This should yield:
     `Python 2.7.13 #or any other like Python 2.7.x`

# Now let's configure the virtualenv

* Ensure that you have virtualenv helpers installed (plenty of resources on the net like [this one](http://roundhere.net/journal/virtualenv-ubuntu-12-10/))
* Create a Python2 virtualenv (I will name it very originally "opencv3"):
     `mkvirtualenv opencv3 --python=/usr/bin/python2.7`
* Switch to it if it was not done by default, make sure that your PS1 looks like that in your shell, particularly the name of the virtualenv should appear:
     `(opencv3) [rest of the PS1]``
Mine for instance is: `(opencv3) ┌─[ado@parrot]─[~]`
* Install the python build tools:
     `sudo apt-get install python-dev`
* Install numpy:
    `pip install numpy`

# Now let's compile and install opencv3

* Clone the [git repository](https://github.com/Itseez/opencv.git):
     `git clone https://github.com/Itseez/opencv.git`
* Go into the directory:
     `cd opencv`
* Small point, perhaps not valid today, but last time I had an issue with the compilation and I had to use the 3.2.0 branch of opencv (it might be fixed or not, but the below branch works at least of today):
     `git checkout 3.2.0`
* Create a build directory and switch to it:
     `mkdir build && cd build`
* Prepare the build:
     `cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..`
* Check that in the report there is a line like:
     `FFMPEG: YES`
* Still in the build directory, start the compilation:
     `make -j2 #the 2 means that the build will use 2 jobs in parallel, you can increase it depending on your system, as a rule of thumb you should use -jX, X being the number of cores you have`
* Go drink a few coffees (you deserve it)
* If no errors appeared, install the compiled program:
     `sudo make install`
* Add the new dynamic libraries installed:
     `sudo ldconfig`

# The final touch

* Now link the cv2 library to your virtualenv, normally the following should be ok if you followed a standard install of the components (path of python2 site packages, and creation of the "opencv3" virtualenv):
    `ln -s /usr/local/lib/python2.7/site-packages/cv2.so ~/.virtualenvs/opencv3/lib/python2.7/site-packages/cv2.so`
* Now try the below from a python shell, and while having the opencv3 virtualenv active:

     {% highlight python %}
     import cv2
     cv2.__version__ #should yield 3.2.0
     video_capture = cv2.VideoCapture(0)
     ret, frame = video_capture.read()
     print ret  # yields True
     {% endhighlight %}

If it works congratulations, you have a working virtualenv with opencv3 and video compatible.
