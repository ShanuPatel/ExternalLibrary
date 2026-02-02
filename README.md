# ExternalLibrary

A lightweight OpenGL external dependency setup that makes using OpenGL with CMake simple and beginner-friendly.
This project helps you quickly integrate common libraries and focus on learning and building, not fighting build systems.

---

## Usage
1. git submodule add https://github.com/ShanuPatel/ExternalLibrary.git ExternalLibrary
2. git submodule update --init --recursive

## Linking
Example for linking a package in CMake:

```cmake
target_link_libraries(${LIB_NAME} PUBLIC Packages)
```

---

## List of Libraries

- binary – (custom/local folder)  
- [glad](https://github.com/Dav1dde/glad)  
- [glfw](https://github.com/glfw/glfw)  
- [glm](https://github.com/g-truc/glm)  
- [MikkTSpace](https://github.com/mmikk/MikkTSpace)  
- [spdlog](https://github.com/gabime/spdlog)   
- [stb](https://github.com/nothings/stb)

---
