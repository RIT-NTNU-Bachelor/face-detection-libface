cmake_minimum_required( VERSION 3.22 )

project( face_detection_with_lib_face )

find_package( OpenCV REQUIRED )

message(STATUS "OpenCV_LIBS = ${OpenCV_LIBS}")

include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable( detect-image detect-image.cpp )


target_link_libraries( detect-image ${OpenCV_LIBS} )
target_link_libraries( detect-image /libfacedetection/build/install/lib/libfacedetection.so )
target_link_libraries( detect-image /opencv/build/lib/libopencv_highgui.so )
target_link_libraries( detect-image /opencv/build/lib/libopencv_imgproc.so )
target_link_libraries( detect-image /opencv/build/lib/libopencv_core.so )
target_link_libraries( detect-image /opencv/build/lib/libopencv_imgcodecs.so )
target_link_libraries( detect-camera ${OpenCV_LIBS} )
target_link_libraries( detect-camera /libfacedetection/build/install/lib/libfacedetection.so )
target_link_libraries( detect-camera /opencv/build/lib/libopencv_highgui.so )
target_link_libraries( detect-camera /opencv/build/lib/libopencv_video.so )
target_link_libraries( detect-camera /opencv/build/lib/libopencv_imgproc.so )
target_link_libraries( detect-camera /opencv/build/lib/libopencv_core.so )
target_link_libraries( detect-camera /opencv/build/lib/libopencv_videoio.so )