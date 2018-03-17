cmake_minimum_required(VERSION 3.2)
project(demo2)

# OpenGL
find_package(OpenGL REQUIRED)
INCLUDE_DIRECTORIES(${OPENGL_INCLUDE_DIR})

# FreeGLUT
include_directories(../external/freeglut/include)

# main
file(GLOB SOURCE_FILES
    "*.h"
    "*.hpp"
    "*.c"
    "*.cpp"
)

add_executable(demo2 ${SOURCE_FILES})

target_link_libraries(demo2 freeglut_static)
