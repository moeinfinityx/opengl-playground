cmake_minimum_required(VERSION 3.2)

project(OpenGLLab)

set(CMAKE_CXX_STANDARD 11)

add_subdirectory(external/glfw)
add_subdirectory(external/glm)

add_subdirectory(external/freeglut)

add_subdirectory(demo1)
add_subdirectory(demo2)
