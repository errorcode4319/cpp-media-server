cmake_minimum_required(VERSION 3.1)

project(cpp-media-server
        VERSION 0.1.0
        LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 17)

if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE "Debug")
endif()
message(STATUS "CMake for ${PROJECT_NAME} v${PROJECT_VERSION}\n")

include_directories(${PROJECT_SOURCE_DIR}/src)

file(GLOB_RECURSE SOURCES src/**/*.cpp)
file(GLOB_RECURSE HEADERS src/**/*.hpp)

add_executable(cpp-media-server ${SOURCES} ${HEADERS})