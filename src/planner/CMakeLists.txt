
cmake_minimum_required(VERSION 3.5.1)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CLIENT_ROOT_FOLDER}/bin)

include_directories(${CLIENT_ROOT_FOLDER}/include/lib)
include_directories(${CLIENT_ROOT_FOLDER}/include)
link_directories(${CLIENT_ROOT_FOLDER}/lib)

add_library(planner-lib common.cpp)
# add_executable(planner planner.cpp)
add_library(planner planner.cpp)

target_link_libraries(planner planner-lib router common)
target_include_directories(planner PUBLIC .)