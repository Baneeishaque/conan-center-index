cmake_minimum_required(VERSION 3.15)
project(test_package LANGUAGES CXX)

find_package(cuda-api-wrappers REQUIRED CONFIG)

add_executable(${PROJECT_NAME} test_package.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE cuda-api-wrappers::runtime-and-driver)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_11)
target_compile_definitions(${PROJECT_NAME} PRIVATE
    CUDA_API_WRAPPERS_VERSION=\"${cuda-api-wrappers_VERSION_STRING}\")
