cmake_minimum_required(VERSION 3.5)

project(AutoUnitTests LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

enable_testing()

find_package(Qt5 COMPONENTS Core Test REQUIRED)

include_directories(include)

add_subdirectory( src build/src )
add_subdirectory( test build/test )
