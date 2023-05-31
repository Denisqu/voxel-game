# Voxel game engine

## Links:
1. [learning resources](./docs/resources.md)

## Things to do:

**ENGINE**

- [ ] Complete "https://learnopengl.com/Getting-started"
- [ ] Прочитать хорошую статью о path-traced rendering в 2д "https://lodev.org/cgtutor/raycasting.html"
- [ ] Разобраться как работает "https://www.shadertoy.com/view/7dK3D3", сделать копию

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

