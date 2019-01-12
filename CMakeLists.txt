cmake_minimum_required(VERSION 3.5)

project(clox C)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS}")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS_RELEASE} -g")

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin/")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin/")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin/")

file(GLOB_RECURSE srcs "${CMAKE_SOURCE_DIR}/clox/*.c")
file(GLOB_RECURSE hdrs "${CMAKE_SOURCE_DIR}/clox/*.h")

add_executable("${PROJECT_NAME}" ${srcs} ${hdrs})
