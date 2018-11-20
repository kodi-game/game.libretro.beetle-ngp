cmake_minimum_required(VERSION 3.1)
project(game.libretro.beetle-ngp)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(BEETLE-NGP_LIB NAMES mednafen_ngp_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(BEETLE-NGP_CUSTOM_BINARY ${BEETLE-NGP_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BEETLE-NGP "")

include(CPack)
