cmake_minimum_required(VERSION 3.10)
project(lab5-7)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)

add_executable(client ${SOURCE_DIR}/client_program.cpp)
add_executable(server ${SOURCE_DIR}/server_program.cpp)
include_directories(${INCLUDE_DIR})

find_package(cppzmq REQUIRED)
target_link_libraries(client cppzmq)
target_link_libraries(server cppzmq)