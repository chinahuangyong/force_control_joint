cmake_minimum_required(VERSION 3.19)
project(force_control_sim)

set(CMAKE_CXX_STANDARD 14)

include_directories("include/"
    "sample/"
    )

link_directories("lib/")

add_executable(force_control_sim sample/simulate.cc
    sample/uitools.c)

target_link_libraries(force_control_sim
    mujoco
    glfw
    pthread)