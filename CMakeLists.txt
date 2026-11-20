cmake_minimum_required(VERSION 3.10)

project(rlImGui LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_library(
  rlImGui
  STATIC
  rlImGui.cpp
)

target_include_directories(
  rlImGui
  PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}
)

target_link_libraries(rlImGui PUBLIC raylib imgui)

target_compile_definitions(
  rlImGui
  PUBLIC
  IMGUI_DISABLE_OBSOLETE_FUNCTIONS
  IMGUI_DISABLE_OBSOLETE_KEYIO
)
