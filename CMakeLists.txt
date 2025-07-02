cmake_minimum_required(VERSION 3.10)

# Project name and language
project(pepe C)

# Specify the C standard (optional)
set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED True)

file(GLOB SOURCES "./src/*.c")
file(GLOB INCLUDES "./include/*.h")

# Add executable from source files
add_executable(pepe ${SOURCES})

target_include_directories(pepe PRIVATE ./include)