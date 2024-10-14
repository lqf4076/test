# 指定运行该CMakeLists所需要的最低CMake版本
cmake_minimum_required(VERSION 3.28) 

set(CMAKE_C_COMPILER "D:/LQF/Program/Dev-Cpp/MinGW64/bin/gcc.exe")
set(CMAKE_CXX_COMPILER "D:/LQF/Program/Dev-Cpp/MinGW64/bin/c++.exe")
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# 指定工程名字为cmake-tutorial，使用CXX、C、ASM三种语言
project(HelloWorld)

add_library(
    a
    src/a.cpp
)

add_executable(
    main   
    src/main.cpp
)
target_link_libraries(main a)
target_include_directories(main PRIVATE include)