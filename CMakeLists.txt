cmake_minimum_required(VERSION 3.4)
project(capture)

set(CMAKE_CXX_FLAGS "-std=c++11 -O2 ${SSE_FLAGS} -g -march=native")
set(CMAKE_BUILD_TYPE Release)

find_package(OpenCV 3 REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(capture capture.cpp)
target_link_libraries(capture ${OpenCV_LIBS})
