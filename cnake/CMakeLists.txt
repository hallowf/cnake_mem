cmake_minimum_required(VERSION 2.8.12)
project(cnake)

find_package(pybind11 REQUIRED)

if( $ENV{BUILD_TARGET} STREQUAL "linux")
    pybind11_add_module(c_writter lin_source.cpp)
elseif( $ENV{BUILD_TARGET} STREQUAL "windows" )
    pybind11_add_module(c_writter win_source.cpp)
endif()
