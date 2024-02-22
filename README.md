# Face Detection with libfacedetection library

This is a experimental repository for testing the library called libfacedetection.

About the library:

> This is an open source library for CNN-based face detection in images. The CNN model has been converted to static variables in C source files. The source code does not depend on any other libraries. What you need is just a C++ compiler. You can compile the source code under Windows, Linux, ARM and any platform with a C++ compiler.


The library can be found on Github here: 
https://github.com/ShiqiYu/libfacedetection 


## How to run?

This repository is using CMake. You can use the CMake plugin for vscode or use the command line.

1. Make a build dir and cd into it: 
```terminal
mkdir build
cd build
```
2. Run the cmake command:
```terminal
cmake ../
```
3. Run the make command
```terminal
make
```
4. Run the executable created
```terminal
./Program
```


## Features

This repository implement the example that was given. It has:

- Face detection confidence level
- Green box around each face. Up to 12 faces in one frame
- Circle on 5 landmarks 


## Result 

![Screenshot from 2024-02-22 09-52-00](https://github.com/RIT-NTNU-Bachelor/face-detection-libface/assets/66110094/43c02234-bff7-42b8-b853-f673920f83bf)

