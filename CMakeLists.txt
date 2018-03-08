cmake_minimum_required(VERSION 3.1)
project(game.libretro.pokemini)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-pokemini REQUIRED)

set(POKEMINI_CUSTOM_BINARY ${POKEMINI_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} POKEMINI "")

include(CPack)
