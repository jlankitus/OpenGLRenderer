cmake_minimum_required(VERSION 3.10)
project(OpenGLRenderer)

set(CMAKE_CXX_STANDARD 11)

include_directories(${CMAKE_SOURCE_DIR}/include)
link_directories(${CMAKE_SOURCE_DIR}/lib)

find_package(OpenGL REQUIRED)

add_library(glad src/glad.c)
add_executable(MyOpenGLProject src/main.cpp)
target_link_libraries(MyOpenGLProject glad ${OPENGL_LIBRARIES} glfw3)
