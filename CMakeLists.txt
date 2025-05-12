cmake_minimum_required(VERSION 3.21)

project(tweak_png VERSION 1.4.7 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

option(ENABLE_UNICODE "Enable Unicode support" ON)

add_subdirectory(src)
