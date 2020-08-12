cmake_minimum_required(VERSION 3.18)
project(learnsdla)
set( CXX_STANDARD 17)
include("pmm.cmake")

pmm(
    
    VCPKG
    REVISION 2020.06
    REQUIRES sdl2
)

find_package(sdl2 CONFIG REQUIRED)

add_executable(learnsdla main.cpp)

target_link_libraries(learnsdla PRIVATE SDL2::SDL2 SDL2::SDL2main)