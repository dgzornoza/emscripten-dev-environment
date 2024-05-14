cmake_minimum_required(VERSION 3.21)

project(sample)

add_executable(${PROJECT_NAME}  
    src/main.cpp
)

message(CMAKE_SYSTEM_NAME => ${CMAKE_SYSTEM_NAME})

if (CMAKE_SYSTEM_NAME STREQUAL Emscripten)
    set(CMAKE_EXECUTABLE_SUFFIX .html)
    target_link_options(${PROJECT_NAME} PUBLIC -sUSE_SDL=2)
endif()