cmake_minimum_required(VERSION 4.3)

# set the project name
project(cmake VERSION 0.1)

# whole src dir
add_subdirectory(src)

# config file with #VERSIONS variables
configure_file(cmon_config.h.in cmon_config.h)

# add the executable
add_executable(cmon src/main.c)

install(TARGETS cmon DESTINATION bin)
