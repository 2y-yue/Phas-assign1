PHAS0100Assignment1
------------------

[![Build Status](https://travis-ci.com/[USERNAME]/PHAS0100Assignment1.svg?branch=master)](https://travis-ci.com/[USERNAME]/PHAS0100Assignment1)
[![Build Status](https://ci.appveyor.com/api/projects/status/[APPVEYOR_ID]/branch/master)](https://ci.appveyor.com/project/[USERNAME]/PHAS0100Assignment1)


Purpose
-------

This project serves as a starting point for the PHAS0100 Assignment 1 Linear Regression coursework. It has a reasonable folder structure for [CMake](https://cmake.org/) based projects,
that use [CTest](https://cmake.org/) to run unit tests via [Catch](https://github.com/catchorg/Catch2). 

Further information on the specific project is left as an exercise for the student.


Credits
-------

This project is maintained by [Dr. Jim Dobson](https://www.ucl.ac.uk/physics-astronomy/people/dr-jim-dobson). It is based on [CMakeCatch2](https://github.com/UCL/CMakeCatch2.git) that was originally developed as a teaching aid for UCL's ["Research Computing with C++"](http://rits.github-pages.ucl.ac.uk/research-computing-with-cpp/)
course developed by [Dr. James Hetherington](http://www.ucl.ac.uk/research-it-services/people/james)
and [Dr. Matt Clarkson](https://iris.ucl.ac.uk/iris/browse/profile?upi=MJCLA42).


Build Instructions
------------------

Build and run instructions are left as an excercise for the student. Examples of how to build using cmake were given in lectures and in the other CMake example projects.

**Build Requirement** 
- A C++ compiler (gcc/g++ = 9.3.0)
- Ubuntu 20.04 
- CMake 3.16.3

**Build Code**

‘cd yourfilepath’\
'mkdir build'\
'cd build'\
'cmake ..'\
'make'

Project Instructions
--------------------
This project contained two different method("Normal Equation Method" and "Gradient Descent Method") to solve parameters for the linear equations($ y=\theta_0+ \theta_x+ noise$). There are two ways for getting data, either randomly generating data or reading a specific txt file.

**Arguement  Instructions** 

\<Options\>: \

    |arguement                  |Desciption                                            |Default Value|
    |---------------------------|------------------------------------------------------|-------------|
    |-h,--help                  ｜Show this help message.
    |-s,--datasize              ｜Specify the datasize for DataCreator.                ｜ \<Default Value\> int 100|\
    |-par1,--theta0             ｜Specify the value of theta 0 for DataCreator.        ｜ \<Default Value> double 1|\
    |-par2,--theta1             ｜Specify the value of theta 1 for DataCreator.        ｜ \<Default Value> double 2|\
    |-f,--filepath              ｜Specify the filepath for FileLoader. |\
    |-m,--method<Compulsory>    ｜Specify the method name for Solver.   -"NormalEquation"  or  "GradientDescent" |\
    |-i,--iterations            ｜Specify the maximium iterations for GradientDescent Solver.  ｜ \<Default Value> int 100; |\
    |-e,--eta                   ｜Specify the Learning rate value for GradientDescent Solver.  ｜ \<Default Value> double 0.01|; 

**Example Code**

'./lrgFitDataApp -m NormalEquation -f ../../Testing/Data/TestData1.txt'
