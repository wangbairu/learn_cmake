cmake_minimum_required(VERSION 3.27 FATAL_ERROR)

project(TEST VERSION 1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

configure_file(test_config.h.in test_config.h)

add_executable(test test.cxx)

target_include_directories(test PUBLIC
                           "${PROJECT_BINARY_DIR}"
                           )