cmake_minimum_required(VERSION 3.2)
project(OpenGLTest)

# OpenGL
find_package(OpenGL REQUIRED)
INCLUDE_DIRECTORIES(${OPENGL_INCLUDE_DIR})

# GLAD
include_directories(../external/glad/include)
add_library(glad ../external/glad/src/glad.c)

# GLFW
include_directories(../external/glfw/include)

# stb
include_directories(../external/stb)

# main
file(GLOB SOURCE_FILES
    "*.h"
    "*.hpp"
    "*.c"
    "*.cpp"
)

# set(SOURCE_FILES main.cpp)

add_executable(OpenGLTest ${SOURCE_FILES})

target_link_libraries(OpenGLTest glfw ${GLFW_LIBRARIES})
target_link_libraries(OpenGLTest glad)
target_link_libraries(OpenGLTest ${OPENGL_LIBRARIES})
target_link_libraries(OpenGLTest ${GLEW_LIBRARIES})
