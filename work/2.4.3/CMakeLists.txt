#声明cmake最低版本
cmake_minimum_required(VERSION 2.8)
#声明一个cmake工程
project(SLAM)
#添加一个程序
add_executable(slam slam.cpp)

add_library(hello SHARED libSLAM.cpp)

add_executable(useHello useHello.cpp)
target_link_libraries(useHello hello)


set( CMAKE_BUILD_TYPE "Debug")