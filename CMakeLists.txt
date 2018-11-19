cmake_minimum_required(VERSION 3.1)
project(game.libretro.pokemini)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(POKEMINI_LIB NAMES pokemini_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(POKEMINI_CUSTOM_BINARY ${POKEMINI_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} POKEMINI "")

include(CPack)
