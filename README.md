# Installation

## Dependency

## Step1:  The first step is to update and upgrade any existing pakages

    $ sudo apt-get update
    $ sudo apt-get upgrade
    
## Step2: We then need to install some developer tools, including CMake, which helps us configure the OpenCV build process:

    $ sudo apt-get install build-essential cmake pkg-config
    
## Step3: Next, we need to install some image I/O packages that allow us to load various image file formats from disk. Examples of such file formats include JPEG, PNG, TIFF, etc.:

    $ sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev
    
## Step4: Just as we need image I/O packages, we also need video I/O packages. These libraries allow us to read various video file formats from disk as well as work directly with video streams:

    $ sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
    $ sudo apt-get install libxvidcore-dev libx264-dev
    
## Step5: The OpenCV library comes with a sub-module named highgui  which is used to display images to our screen and build basic GUIs. In order to compile the highgui  module, we need to install the GTK development library:

    $ sudo apt-get install libgtk2.0-dev

## Step6: Many operations inside of OpenCV (namely matrix operations) can be optimized further by installing a few extra dependencies:

    $ sudo apt-get install libatlas-base-dev gfortran

## Step7: Lastly, let’s install both the Python 2.7 and Python 3 header files so we can compile OpenCV with Python bindings:

    $ sudo apt-get install python2.7-dev python3-dev

## Step8: Install pip pakages

    $ sudo apt-get install python3-pip

## Step9: To get python 2 version

    $ sudo apt-get install python-pip

## Step10: Installing numpy and matplotlib your raspberry pi

    $ pip3 install numpy 

## Step11: Now Install Opencv

    git clone https://github.com/opencv/opencv.git

## Step12: setup our build using CMake:

    $ cd opencv
    $ mkdir build
    $ cd build
    $ cmake -DCMAKE_BUILD_TYPE=RELEASE –DCMAKE_INSTALL_PREFIX=/usr/local -DENABLE_PRECOMPILED_HEADERS=OFF -DWITH_FFMPEG=OFF ..

## Step13: Finally, We are now ready to compile opencv

    $ make -j4
    $ sudo make install
    $ sudo ldconfig

## Step14: Installing picamera

	$ pip3 install “picamera[array]”
