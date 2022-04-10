cmake_minimum_required(VERSION 3.22.2)
# set the project name and version number
project(cmake_learn VERSION 1.0)
# Add the adder library to the build(build the library)
add_subdirectory(Adder)
# Build main
add_executable(${PROJECT_NAME} main.cpp)
#include Adder directory to target
target_include_directories(${PROJECT_NAME} PUBLIC Adder)
#link the library to our executable
target_link_libraries(${PROJECT_NAME} PUBLIC adder)