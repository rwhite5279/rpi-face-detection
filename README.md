README.md
==========

*Face Detection on the Raspberry Pi* is a simple interactive demonstration of computer-based image recognition. It was originally developed in early 2024 for presentation at the [Southern California Linux Expo](https://socallinuxexpo.org) *The Next Generation* event in Pasadena, California.

Organization
============

This repository includes:

* this README.md file
* `bin/` - contains the `face_detection.py` program
* `docs/` - contains references, including an OpenDocument text (ODT) file that can be used in presenting the demonstration, and an inventory of items to bring for sharing the demo
* `img/` - contains some photos/screenshots of the demo

Setup
=====

This particular version of the demonstration was run on a Raspberry Pi 4B running Raspbian with a USB mouse, USB keyboard, and USB webcam attached. The demonstration will run on other POSIX platforms (macOS, Linux on Windows), perhaps with some modifications for webcam drivers as needed.

Software installation
---------------------

From the Terminal in the home directory:

1.  
```
sudo apt update && sudo apt upgrade -y   # Update the Raspberry Pi
```
2.
```
python -m venv ~/venv                    # create a virtual environment
```

3.
```
source ~/venv/bin/activate      # start up the virtual environment
```
Optional step: modify `.bashrc` to include this same line so that the virtual environment is launched every time a Terminal window is opened.

4.    
```
sudo apt install python3-pip             # install pip3
```

5.    
```
pip3 install opencv-python       # download and install opencv module
```

Running the demonstration
-------------------------

1. Put the `face_detection.py` file on the Desktop of the Raspberry Pi
2. Open a Terminal and run the command
```
python ~/Desktop/face_detection.py
```
3. The environment may allow the window to be resized. If possible, expand the window so that demo viewers are able to better see the face recognition analysis.
4. Ask viewers to tilt their head to one side, or to obscure part of their face with hair or a mask. Does the face recognition still work?
5. Does the program work on faces in a darkened room? Does it work on faces with darker complexions?
6. Are there any features in the camera's view that the algorithm mistakenly identifies as faces? Why might that be?
7. Use the 30x Zoom feature in the window to display the Red-Green-Blue values of each pixel. Note that algorithms don't "know" what a face looks like. They see patterns of numbers, and things that are "faces" generally have a certain pattern of numbers that an algorithm can identify.

Licenses
=======

* Handout - CC-by-4.0
* Software - MIT


References
==========

* [*Computer Vision with Raspberry Pi](https://www.oreilly.com/content/raspberry-pi-cookbook-computer-vision/), Monk, S. 2016. O'Reilly. Retrieved 2025-03-11.
