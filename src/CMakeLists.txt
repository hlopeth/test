cmake_minimum_required(VERSION 3.16)
set (CMAKE_CXX_STANDARD 11)

add_subdirectory(libs/glfw)
add_subdirectory(libs/glew)

project(Editor VERSION 0.1.0)

include_directories(include/)
include_directories(libs/glfw/include)
include_directories(libs/glew/include)

add_executable(Editor main.cpp)
target_link_libraries(Editor ${OPENGL_LIBRARIES} glfw libglew_static)