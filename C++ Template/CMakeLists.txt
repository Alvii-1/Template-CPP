# REMEMBER TO CHANGE <project> TO THE NAME OF THE NEW PROJECT IN THIS FILE

# --- | Setting minimum version
cmake_minimum_required(VERSION 3.20)

# --- | Project name (Change name for each project)
project(project LANGUAGES CXX)

# --- | Set C++ Standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# --- | Output exe directly in build/
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR})

# --- | Collect all .cpp files in src/
file(GLOB_RECURSE SOURCES "src/*.cpp")

# --- | Add the executable and its source (make sure you change the name here too)
add_executable(project ${SOURCES})

# --- | Include directories
target_include_directories(project PRIVATE include)
