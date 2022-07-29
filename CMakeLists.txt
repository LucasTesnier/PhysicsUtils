cmake_minimum_required(VERSION 3.17)
project(physicutils LANGUAGES CXX)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED true)

add_compile_options(
    "-Wall" "-Wextra" "-Werror" "-pedantic" "-Wpointer-arith" "-fpic"
)

option(TESTING OFF)
if (TESTING)
    enable_testing()
    add_compile_options("--coverage" "-fprofile-arcs" "-ftest-coverage")
    add_link_options("--coverage" "-fprofile-arcs" "-ftest-coverage")
    add_subdirectory(tests)
endif()

add_subdirectory(src)