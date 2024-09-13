cmake_minimum_required(VERSION 3.10)

set(PROJECT_NAME cmake_test)
project(${PROJECT_NAME})

set(path "${CMAKE_SOURCE_DIR}/test_cmake/")

include_directories(${path})

add_library(cmake_test_lib "${path}/test.cpp" "${path}/test.h")

add_executable(cmake_test_exe "${path}/main.cpp")

target_link_libraries(cmake_test_exe cmake_test_lib)

message(STATUS "Done")
