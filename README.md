
# Astro RaspiCam: C++ API for using Raspberry Camera for Astrophotography (with OpenCV 2)

A modified C++ RaspiCam API to support long exposure for Astrophotography.


This library allows to use the Raspberry Pi Camera under BSD License.

The project is started by the AVA research group (rafael Muñoz Salinas; rmsalinas@uco.es). Please note that is NOT the OFFICIAL repository of RaspiCam, these can be found [here](http://www.uco.es/investiga/grupos/ava/node/40).

This repository is used in the [Kerberos.io](https://github.com/kerberos-io) project.

## Features

 - Supports long exposure (6s for RpiCam V1 ,10s for RpiCam V2)
 - Supports ISO from 100 to 800
 - Supports setting camera mode, image size and more..

## Requirements

 -OpenCV 2

#### Install opencv on RPi:
```
$ sudo apt install libopencv-dev

```

## Compiling and Installing

Clone the repository to your raspberry. Then, uncompressed the file and compile:


	cd Astro-RaspiCam
	mkdir build
	cd build
	cmake ..

At this point you'll see something like

	-- CREATE OPENCV MODULE=1
	-- CMAKE_INSTALL_PREFIX=/usr/local
	-- REQUIRED_LIBRARIES=/opt/vc/lib/libmmal_core.so;/opt/vc/lib/libmmal_util.so;/opt/vc/lib/libmmal.so
	-- Change a value with: cmake -D<Variable>=<Value>
	--
	-- Configuring done
	-- Generating done
	-- Build files have been written to: /home/pi/raspicam/trunk/build

If OpenCV development files are installed in your system, then you see following output; otherwise this option will be 0 and the opencv module of the library will not be compiled.

	-- CREATE OPENCV MODULE=1


Finally compile, install and update the ldconfig:

	make
	sudo make install
	sudo ldconfig


### Example
