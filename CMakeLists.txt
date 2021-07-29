cmake_minimum_required(VERSION 3.10)
project(pcd_pic)

set(CMAKE_CXX_STANDARD 14)

#pcl
find_package( PCL REQUIRED)
include_directories( ${PCL_INCLUDE_DIRS} )
link_directories(${PCL_LIBRARY_DIRS})

#opencv
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )



add_executable(pcd_pic main.cpp originalVibe.cpp)
target_link_libraries( pcd_pic ${OpenCV_LIBS} )