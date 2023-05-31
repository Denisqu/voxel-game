cmake_minimum_required(VERSION 3.25)
project(voxel_game)

#set(VCPKG_PATH "C:/Program Files/vcpkg/vcpkg")
#set(CMAKE_CXX_STANDARD 20)

#set(VCPKG_PATH C:/Users/Denis/My Data/Работа/git projects/vcpkg/vcpkg)
set(CMAKE_TOOLCHAIN_FILE ${VCPKG_PATH}/scripts/buildsystems/vcpkg.cmake)
set(INCLUDE_DIR ${VCPKG_PATH}/installed/x64-windows/include)
set(LIB_DIR ${VCPKG_PATH}/installed/x64-windows/lib)



# cmake could not find packages from VCPKG with find_package,
# so I had to do this very
# straight forward (01.05.23)
include_directories(${INCLUDE_DIR})
link_directories(${LIB_DIR})

add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE glad.lib glfw3.lib)
#add_library(${PROJECT_NAME} glfw3.dll)

get_target_property(OUT voxel_game LINK_LIBRARIES)
message(STATUS ${OUT})
message(${INCLUDE_DIR})
message(${LIB_DIR})