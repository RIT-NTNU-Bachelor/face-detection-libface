cmake_minimum_required( VERSION 3.22 )

project( face_detection_with_lib_face )

find_package( OpenCV REQUIRED )

message(STATUS "OpenCV_LIBS = ${OpenCV_LIBS}")

include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable(Program src/main.cpp)
target_link_libraries(Program ${OpenCV_LIBS})