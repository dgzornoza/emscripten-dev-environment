cmake_minimum_required(VERSION 3.21)
project(sample)
add_executable(sample src/main.cpp)

if (CMAKE_SYSTEM_NAME STREQUAL Emscripten)
    set(CMAKE_EXECUTABLE_SUFFIX .html)
    target_link_options(sample PUBLIC -sUSE_SDL=2)
endif()