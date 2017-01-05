cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

set(LIBRARY_NAME mongoose)

set(CMAKE_CXX_FLAGS "-g -Wall")

set(SOURCE_FILES include/mongoose.h src/mongoose.c)

add_library(${LIBRARY_NAME} ${SOURCE_FILES})

target_include_directories(${LIBRARY_NAME} PUBLIC
   $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
   $<INSTALL_INTERFACE:include>
)
