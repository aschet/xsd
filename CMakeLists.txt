cmake_minimum_required(VERSION 3.20)
project(xsd LANGUAGES CXX)

find_package(XercesC REQUIRED)

add_subdirectory(xsd/xsd)
