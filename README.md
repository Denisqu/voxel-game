# Voxel game engine

## Links:
1. [learning resources](./docs/resources.md)

## Things to do:

**ENGINE**

- [ ] Complete "https://learnopengl.com/Getting-started"
- [ ] Complete "https://learnopengl.com/Lighting/"
- [ ] Complete "https://learnopengl.com/Model-Loading/"
- [ ] Complete "https://learnopengl.com/Getting-started"
- [ ] Complete "https://learnopengl.com/Advanced-OpenGL/Depth-testing"
- [ ] Refactor code after tutorials
- [ ] Develop basic voxel terrain generator
- [ ] Develop new voxel renderer based on rendering voxels with ray-tracing (or pathtracing, etc...)

**CMAKE**

- [x] ~~Create .bat scripts for cmake~~
- [x] ~~Setup cmake with vcpkg~~
- [x] ~~Setup gitignore~~
- [ ] Add C++ 20 c++ version in cmake
- [x] ~~Add opengl and other libraries~~
- [ ] Setup gtests

**README**
- [x] ~~Write instructions for building a project~~

## How to build:
```
cmake -G "Visual Studio 17 2022" -DVCPKG_PATH="C:/Users/Denis/My Data/Работа/git projects/vcpkg/vcpkg" -B./build
```

### Dependencies:
```
vcpkg install glfw3:x64-windows
vcpkg install glad[gl-api-latest]:x64-windows
```

--------------------------------------------------------------

