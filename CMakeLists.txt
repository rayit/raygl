cmake_minimum_required(VERSION 3.5.0)
project(project VERSION 0.1.0 LANGUAGES C CXX)

find_package(OpenGL REQUIRED)

add_executable(project 
        src/main.cpp
        src/glad.c
        src/glad.h)

include_directories(include)

target_link_libraries(project glfw OpenGL::GL)
