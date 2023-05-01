# https://docs.conan.io/2/tutorial/consuming_packages/build_simple_cmake_project.html
# https://gist.github.com/Trass3r/74e323ce43230b5e4840fab50d93a41d

# build with: cmake .. -G "Visual Studio 17 2022" "-DCMAKE_TOOLCHAIN_FILE=C:/Program Files/vcpkg/vcpkg/scripts/buildsystems/vcpkg.cmake" -B./
cmake_minimum_required(VERSION 3.25)
project(voxel_game)

#set(CMAKE_PREFIX_PATH "./build")
set(VCPKG_PATH "C:/Program Files/vcpkg/vcpkg")

#set(CMAKE_CXX_STANDARD 20)

#find_package(glfw3 CONFIG REQUIRED)
#find_package(glad CONFIG REQUIRED)

# cmake could not find packages from VCPKG with find_package,
# so I had to do this very
# straight forward (01.05.23)
include_directories(${VCPKG_PATH}/installed/x64-windows/include)
link_directories(${VCPKG_PATH}/installed/x64-windows/lib)

add_executable(${PROJECT_NAME} src/main.cpp)

target_link_libraries(${PROJECT_NAME} PRIVATE glad.lib glfw3dll.lib)
#target_link_libraries(${PROJECT_NAME} PRIVATE glfw3)
#target_link_libraries(${PROJECT_NAME} glfw glad::glad)
#target_link_libraries(main PRIVATE glfw)

