cmake_minimum_required(VERSION 3.12)

# Set your project name here once
set(PROJECT_NAME blink)  # <--- change this 
set(PICO_SDK_PATH "/home/marnie/Documents/pico/pico-sdk") #<--- dir of pico-sdk

include(pico_sdk_import.cmake)

project(${PROJECT_NAME} C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

pico_sdk_init()

add_executable(${PROJECT_NAME}
    ${PROJECT_SOURCE_DIR}/${PROJECT_NAME}.c
)

target_link_libraries(${PROJECT_NAME} pico_stdlib)
pico_add_extra_outputs(${PROJECT_NAME})
