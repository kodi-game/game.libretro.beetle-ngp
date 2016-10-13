cmake_minimum_required(VERSION 3.1)
project(game.libretro.beetle-ngp)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-beetle-ngp REQUIRED)

set(DEPLIBS beetle-ngp)
set(BEETLE_NGP_CUSTOM_BINARY ${BEETLE_NGP_LIB}
                             ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BEETLE_NGP DEPLIBS)
