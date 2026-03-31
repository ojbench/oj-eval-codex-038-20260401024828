cmake_minimum_required(VERSION 3.10)
project(problem_038_vectorpp LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Optimize for performance but keep reasonable defaults
if (NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

add_executable(code src/main.cpp)

target_compile_options(code PRIVATE -O2 -pipe -static-libstdc++ -static-libgcc)

