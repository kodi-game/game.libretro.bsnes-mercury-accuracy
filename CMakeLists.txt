project(game.libretro.bsnes-mercury-accuracy)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(libretro-bsnes-mercury-accuracy REQUIRED)

set(DEBLIBS bsnes-mercury-accuracy)
set(BSNES_MERCURY_CUSTOM_BINARY ${BSNES_MERCURY_LIB}
                                ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX}
                                ${DEBLIBS})

build_addon(${PROJECT_NAME} BSNES_MERCURY ${DEBLIBS})
