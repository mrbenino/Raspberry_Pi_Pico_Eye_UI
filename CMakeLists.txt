cmake_minimum_required(VERSION 3.22)

include($ENV{PICO_SDK_PATH}/pico_sdk_init.cmake)
pico_sdk_init()

project(Raspberry_Pi_Pico_Eye_UI)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)
set(PICO_EXAMPLES_PATH ${PROJECT_SOURCE_DIR})

add_executable(Raspberry_Pi_Pico_Eye_UI main.cpp)

target_link_libraries(Raspberry_Pi_Pico_Eye_UI pico_stdlib)

# create map/bin/hex file etc.
pico_add_extra_outputs(Raspberry_Pi_Pico_Eye_UI)