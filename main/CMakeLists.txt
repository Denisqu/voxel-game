# https://docs.conan.io/2/tutorial/consuming_packages/build_simple_cmake_project.html
# https://gist.github.com/Trass3r/74e323ce43230b5e4840fab50d93a41d

# рабочий вариант
# PS C:\git repos\voxel-game\main\build> cmake .. -G "Visual Studio 17 2022" -DCMAKE_TOOLCHAIN_FILE:filepath=./conan_toolchain.cmake -B./

set(CMAKE_PREFIX_PATH "./build")
cmake_minimum_required(VERSION 3.15)
project(voxel_game)

find_package(glfw3 3.3 REQUIRED)

add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} glfw)