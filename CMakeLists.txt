cmake_minimum_required(VERSION 4.3)

# set the project name
project(cmon VERSION 0.1)

# hardcoded for my system - overwrite with env
SET (CMAKE_C_COMPILER			"clang")

SET (CMAKE_C_FLAGS_INIT			"-Wall -std=c23")
SET (CMAKE_C_FLAGS_DEBUG_INIT		"-g")
SET (CMAKE_C_FLAGS_MINSIZEREL_INIT	"-Os -DNDEBUG")
SET (CMAKE_C_FLAGS_RELEASE_INIT		"-O3 -DNDEBUG")
SET (CMAKE_C_FLAGS_RELWITHDEBINFO_INIT	"-O2 -g")

#SET (CMAKE_CXX_FLAGS_INIT		"-Wall -std=c++17")
#SET (CMAKE_CXX_FLAGS_DEBUG_INIT	"-g")
#SET (CMAKE_CXX_FLAGS_MINSIZEREL_INIT	"-Os -DNDEBUG")
#SET (CMAKE_CXX_FLAGS_RELEASE_INIT	"-O3 -DNDEBUG")
#SET (CMAKE_CXX_FLAGS_RELWITHDEBINFO_INIT	"-O2 -g")

# whole src dir
add_subdirectory(src)

# add the executable
add_executable(cmon src/main.c)

install(TARGETS cmon DESTINATION bin)
