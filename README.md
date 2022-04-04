<center>
    <h1><b>CMake</b></h1>
</center>

CMake is a tool to manage building of source code.
## Basic Top-Level CMakeLists.txt
The top-level CMakeLists.txt is the entry point of our project.There can be several CMakeLists.txt files in subdirectories (for example, libraries or other executables associated with the project).
Example:
```cmake
cmake_minimum_required(VERSION 3.22.2)
# set the project name
project(cmake_learn VERSION 1.0)
# Build 
add_executable(${PROJECT_NAME} main.cpp)
```
The first line is the version of CMake, which is required to process the file, the second is the project name and its versions.The next line specifies which binary to build and their related source files.
## Running CMake
### 1. Classic method
```bash
mkdir build
cd build
cmake ..
make
```

## 2. Mordern method
This method is cleaner and more cross-platform-friendly:
```bash
cmake -S . -B build
cmake --build build
```