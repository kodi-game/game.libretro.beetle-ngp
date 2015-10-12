project(game.libretro.beetle-ngp)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(libretro-beetle-ngp REQUIRED)

set(DEPLIBS beetle-ngp)
set(BEETLE_NGP_CUSTOM_BINARY ${BEETLE_NGP_LIB}
                             ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX} beetle-ngp)

build_addon(${PROJECT_NAME} BEETLE_NGP DEPLIBS)
