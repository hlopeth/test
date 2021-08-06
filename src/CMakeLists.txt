cmake_minimum_required(VERSION 3.16)
set (CMAKE_CXX_STANDARD 11)

add_subdirectory(glfw)

project(Editor VERSION 0.1.0)

include_directories(include/)
include_directories(glfw/include)

add_executable(Editor main2.cpp glad.c)
target_link_libraries(Editor glfw)