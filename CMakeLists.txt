cmake_minimum_required(VERSION 3.21)

project(Warzombies)

set_property(GLOBAL PROPERTY USE_FOLDERS TRUE)
set(CMAKE_C_STANDARD 17)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(srcfiles
    src/main.c
)

add_subdirectory(external/raylib)
add_executable(Warzombies ${srcfiles})

target_link_libraries(Warzombies raylib)