cmake_minimum_required(VERSION 3.1)
project(game.libretro.bsnes-mercury-accuracy)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-bsnes-mercury-accuracy REQUIRED)

set(BSNES-MERCURY-ACCURACY_CUSTOM_BINARY ${BSNES-MERCURY-ACCURACY_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BSNES-MERCURY-ACCURACY "")
