cmake_minimum_required(VERSION 3.24)

project(standalone 
    VERSION 1.0
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# set( 
#     headers
#     ${CMAKE_CURRENT_SOURCE_DIR}/include/demo.h
# )

set( 
    sources
    ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp
)

# important need to add this sentence to include the directory
# include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

# add_library(${PROJECT_NAME} ${headers} ${sources})

add_executable(${PROJECT_NAME} ${sources})

target_link_libraries(
    ${PROJECT_NAME}
    Demo
)

target_include_directories(${PROJECT_NAME} PUBLIC
    ${CMAKE_SOURCE_DIR}/include
)


