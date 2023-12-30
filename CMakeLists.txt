cmake_minimum_required(VERSION 3.27)
project(oldwest)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake_modules)

set(SDL2_PATH "C:/Users/games/Documentos/lib/SDL2-devel-2.28.5-mingw/SDL2-2.28.5/x86_64-w64-mingw32")

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIR})

add_executable(oldwest main.cpp)

target_link_libraries(${PROJECT_NAME} ${SDL2_LIBRARY} -lopengl32)