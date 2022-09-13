# Setup project
cmake_minimum_required(VERSION 3.10 FATAL_ERROR)
project(psflib)

# add sources and headers
file(GLOB sources ${PROJECT_SOURCE_DIR}/*.c)
file(GLOB headers ${PROJECT_SOURCE_DIR}/*.h)

# build library
add_library(psflib STATIC ${sources} ${headers})
set_property(TARGET psflib PROPERTY POSITION_INDEPENDENT_CODE ON)
