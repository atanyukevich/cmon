cmake_minimum_required(VERSION 4.3)

# set the project name
project(cmon VERSION 0.1)

# whole src dir
add_subdirectory(src)

# add the executable
add_executable(cmon src/main.c)

install(TARGETS cmon DESTINATION bin)
