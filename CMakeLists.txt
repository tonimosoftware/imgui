cmake_minimum_required(VERSION 3.27)
set(CMAKE_CXX_STANDARD 20)

project(imgui)

add_library(
    ${PROJECT_NAME}
    STATIC

    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_tables.cpp
    imgui_widgets.cpp

    backends/imgui_impl_vulkan.cpp
    backends/imgui_impl_win32.cpp
)

target_include_directories(
    imgui
    PRIVATE
    .
    backends
)