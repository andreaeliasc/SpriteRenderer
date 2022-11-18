cmake_minimum_required(VERSION 3.22)

project(Pong VERSION 1.0)
set(CMAKE_CXX_STANDARD 23)
add_executable(Pong src/main.cpp src/Game/game.cpp src/Game/game.h)

add_subdirectory(src/Math)
target_include_directories(
    Pong PUBLIC src/Math
)

target_link_directories(
    Pong PRIVATE src/Math
)

target_link_libraries(
    Pong
    math
    SDL2
    SDL2_image

)

