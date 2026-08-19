cmake_minimum_required(VERSION 3.20)

project(HNE
    VERSION 0.1.0
    LANGUAGES C CXX
)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(glfw3 CONFIG REQUIRED)
find_package(glad CONFIG REQUIRED)

add_executable(HNE
    src/main.cpp
)

target_link_libraries(HNE PRIVATE
    glfw
    glad::glad
    opengl32
)