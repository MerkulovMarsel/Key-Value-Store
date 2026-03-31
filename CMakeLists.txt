cmake_minimum_required(VERSION 3.10)

project(GigaMap VERSION 1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

#include(FetchContent)
#FetchContent_Declare()
#FetchContent_MakeAvailable()


add_library(config INTERFACE)
target_include_directories(config INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

enable_testing()

add_subdirectory(src)
add_subdirectory(test)


