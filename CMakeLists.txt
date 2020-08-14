cmake_minimum_required(VERSION 3.18)
project(learnsdla)
set( CXX_STANDARD 17)
include("pmm.cmake")

pmm(
    
    VCPKG
    REVISION 2020.06
    REQUIRES sdl2 sdl2-image[libjpeg-turbo,tiff,libwebp] sdl2-ttf
)

find_package(sdl2 CONFIG REQUIRED)

find_package(sdl2-image CONFIG REQUIRED)

find_package(sdl2-ttf CONFIG REQUIRED)

add_executable(learnsdla main.cpp)

target_link_libraries(learnsdla PRIVATE SDL2::SDL2 SDL2::SDL2main SDL2::SDL2_image SDL2::SDL2_ttf)