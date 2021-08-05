#https://hsf-training.github.io/hsf-training-cmake-webpage/aio/index.html

cmake_minimum_required(VERSION 3.11...3.21)

project(
        piHardware_cam
        LANGUAGES CXX C)

set(CMAKE_CXX_STANDARD 11)

add_executable(piHardware_cam main.cpp)

add_library(bcm2835 bcm2835-1.68/src/bcm2835.c bcm2835-1.68/src/bcm2835.h)

target_link_libraries(piHardware_cam PRIVATE bcm2835)