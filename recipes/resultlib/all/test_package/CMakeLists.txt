cmake_minimum_required(VERSION 3.5)
project(test_package LANGUAGES C)

find_package(resultlib REQUIRED CONFIG)

add_executable(${PROJECT_NAME} test_package.c)

target_link_libraries(${PROJECT_NAME} resultlib::resultlib)
