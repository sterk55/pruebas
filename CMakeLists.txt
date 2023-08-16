cmake_minimum_required(VERSION 3.25)
project(prueba)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fopenmp")

# Incluye el módulo CPM
include(cmake/CPM.cmake)

# https://github.com/fmtlib/fmt.git
CPMAddPackage("gh:fmtlib/fmt#10.0.0")

find_package(MPI REQUIRED)
message(STATUS "******Run: ${MPIEXEC}")

add_executable(prueba main.cpp)
target_link_libraries(prueba fmt::fmt MPI::MPI_CXX)