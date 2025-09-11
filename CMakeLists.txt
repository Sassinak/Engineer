cmake_minimum_required(VERSION 3.20)

# check BOARD variable
if(NOT BOARD)
    set(BOARD damiao_mc02)
    message("BOARD not defined, use default value: ${BOARD}")
else()
    message("Use BOARD: ${BOARD}")
endif()
    
# import zephyr library
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})       # 很重要


# define cmake project
project(RP_Engineer)

target_sources(app PRIVATE
    ./src/main.cpp
)
