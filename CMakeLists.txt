cmake_minimum_required( VERSION 3.22 )

project( face_detection_with_lib_face )

find_package( OpenCV REQUIRED )

message(STATUS "OpenCV_LIBS = ${OpenCV_LIBS}")

# Recurively add all files in src
# Not recommended but works. 
file(GLOB_RECURSE SRC_FILES src/*.cpp)
add_executable(Program ${SRC_FILES})


include_directories( ${OpenCV_INCLUDE_DIRS} )


target_link_libraries(Program ${OpenCV_LIBS})
target_include_directories(Program PUBLIC ./include)