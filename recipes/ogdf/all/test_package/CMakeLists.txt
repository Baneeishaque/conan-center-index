cmake_minimum_required(VERSION 3.15)
project(test_package CXX)
set(CMAKE_CXX_STANDARD 11)

find_package(ogdf REQUIRED CONFIG)
add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE ogdf::ogdf)
