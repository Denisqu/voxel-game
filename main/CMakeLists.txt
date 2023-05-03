cmake_minimum_required(VERSION 3.25)
project(voxel_game)

set(VCPKG_PATH "C:/Program Files/vcpkg/vcpkg")
#set(CMAKE_CXX_STANDARD 20)

# cmake could not find packages from VCPKG with find_package,
# so I had to do this very
# straight forward (01.05.23)
include_directories(${VCPKG_PATH}/installed/x64-windows/include)
link_directories(${VCPKG_PATH}/installed/x64-windows/lib)

add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE glad.lib glfw3dll.lib)
