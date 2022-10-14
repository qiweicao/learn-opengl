cmake_minimum_required(VERSION 3.0.0)
project(learn-opengl VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# set(CMAKE_INSTALL_PREFIX "${PROJECT_SOURCE_DIR}")

option(GLFW_BUILD_DOCS OFF)
option(GLFW_BUILD_EXAMPLES OFF)
option(GLFW_BUILD_TESTS OFF)
add_subdirectory(external/glfw)

add_subdirectory(external/glad)

set(MAIN_INCLUDE
  ${PROJECT_SOURCE_DIR}/external/glad/include/
  ${PROJECT_SOURCE_DIR}/external/glfw/include/
)
set(MAIN_LIBRARY
  glfw
  glad
)

add_subdirectory(src)
