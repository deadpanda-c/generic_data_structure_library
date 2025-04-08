cmake_minimum_required(VERSION 3.22)
project(generic_data_structures_library)

set(CMAKE_CXX_STANDARD 20)

file(GLOB_RECURSE SOURCES src/*.cpp)
include_directories(include)

add_library(generic_data_structures_library SHARED ${SOURCES})

set(MAIN_FILE main.cpp)
add_executable(generic_data_structures_library_test ${SOURCES} ${MAIN_FILE})
