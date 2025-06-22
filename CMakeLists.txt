cmake_minimum_required(VERSION "3.15.0")

project(VortexStore CXX)

if(PROJECT_SOURCE_DIR STREQUAL PROJECT_BINARY_DIR)
  message(FATAL_ERROR "In-source builds are not allowed")
endif()

add_subdirectory(src bin)
add_subdirectory(test)