cmake_minimum_required(VERSION 3.26)
project(game_api)

set(CMAKE_CXX_STANDARD 14)

find_package(Crow)

include_directories(src)

add_executable(game_api
        main.cpp
)

target_include_directories(game_api PRIVATE Crow)
target_link_libraries(game_api PUBLIC Crow::Crow)
