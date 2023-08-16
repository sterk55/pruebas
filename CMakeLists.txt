cmake_minimum_required(VERSION 3.25)
project(prueba)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fopenmp")

add_executable(prueba main.cpp)
