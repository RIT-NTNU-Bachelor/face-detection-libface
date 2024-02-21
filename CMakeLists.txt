cmake_minimum_required( VERSION 3.10 )

project(face_detection_with_lib_face VERSION 0.0.1)

find_package( OpenCV REQUIRED )

message(STATUS "OpenCV_LIBS = ${OpenCV_LIBS}")

# Recurively add all files in src
# Not recommended but works. 
file(GLOB_RECURSE SRC_FILES src/*.cpp)
add_executable(Program ${SRC_FILES})


# Include the directory where the header files are
# include_directories(./include)
include_directories( ${OpenCV_INCLUDE_DIRS} )


target_link_libraries(Program ${OpenCV_LIBS})
target_include_directories(Program PUBLIC include)