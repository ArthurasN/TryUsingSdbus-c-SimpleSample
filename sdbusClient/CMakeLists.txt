cmake_minimum_required(VERSION 3.5)

project(sdbusClient LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


# First, find sdbus-c++
find_package(sdbus-c++ REQUIRED)

# Use the sdbus-c++ target in SDBusCpp namespace

add_executable(sdbusClient main.cpp)
target_link_libraries(sdbusClient PRIVATE SDBusCpp::sdbus-c++)
