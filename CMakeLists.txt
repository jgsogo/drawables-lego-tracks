cmake_minimum_required(VERSION 3.15)
project(drawables-lego-tracks
        LANGUAGES C CXX
        VERSION 0.1.0
        DESCRIPTION "Library of drawables with LEGO tracks")

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

set(CMAKE_CXX_STANDARD 20)

add_subdirectory(src)

option(BUILD_TESTS "Also build the tests" ON)
if (BUILD_TESTS)
    add_subdirectory(tests)
endif()
