GaussianProcessMotionPlanner
===================================================
This library is an implementation of GPMP2 (Gaussian Process Motion Planner 2) algorithm described in [Motion Planning as Probabilistic Inference using Gaussian Processes and Factor Graphs](http://www.cc.gatech.edu/~bboots3/files/GPMP2.pdf) (RSS 2016). The core library is developed in C++ language, and an optional Matlab toolbox is provided. Examples are provided in Matlab scripts. A ROS interface is also available within [PIPER](https://github.com/gtrll/piper).


Prerequisites
------

- CMake >= 2.6 (Ubuntu: `sudo apt-get install cmake`), compilation configuration tool.
- [Boost](http://www.boost.org/) >= 1.50 (Ubuntu: `sudo apt-get install libboost-all-dev`), portable C++ source libraries.
- [GTSAM](https://github.com/borglab/gtsam) >= 4.0 alpha, a C++ library that implement smoothing and mapping (SAM) framework in robotics and vision.
Here we use factor graph implementations and inference/optimization tools provided by GTSAM.

Compilation & Installation
------

In the library folder execute:

```
$ mkdir build
$ cd build
$ cmake ..
$ make check  # optional, run unit tests
$ make install
```

Matlab Toolbox
-----

An optional Matlab toolbox is provided to use our library in Matlab. To enable Matlab toolbox during compilation:

```
$ cmake -DGPMP2_BUILD_MATLAB_TOOLBOX:OPTION=ON -DGTSAM_TOOLBOX_INSTALL_PATH:PATH=/path/install/toolbox ..
$ make install
```

After you install the Matlab toolbox, don't forget to add `/path/install/toolbox` to your Matlab path.

Tested Compatibility
-----

The gpmp2 library is designed to be cross-platform. It has been tested on Ubuntu Linux and Windows for now.

- Ubuntu: GCC 4.8 - 4.9, 5.3 - 5.4
- Windows: Visual C++ 2015 (Matlab toolbox not tested)
- Boost: 1.50 - 1.61


Questions & Bug reporting
-----

Please use Github issue tracker to report bugs. For other questions please contact [Sourangshu Ghosh](mailto:sourangshug123@gmail.com)

License
-----

GPMP2 is released under the MIT license, reproduced in the file LICENSE in this directory.
