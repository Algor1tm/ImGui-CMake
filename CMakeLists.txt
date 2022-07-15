# CMakeList.txt : CMake project for ImGui-CMake, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.16)

project ("ImGui")
set(CMAKE_CXX_STANDARD 17)

# Add source to this project's executable.
add_library (ImGui
    "imconfig.h"
    "imgui.cpp"
    "imgui.h"
    "imgui_demo.cpp"
    "imgui_draw.cpp"
    "imgui_internal.h"
    "imgui_tables.cpp"
    "imgui_widgets.cpp"
    "imstb_rectpack.h"
    "imstb_textedit.h"
    "imstb_truetype.h")

if ( CMAKE_COMPILER_IS_GNUCC )
    target_compile_options("ImGui" PRIVATE -Wall -Wextra)
endif()
if ( MSVC )
    target_compile_options("ImGui" PRIVATE /W3)
endif()


# TODO: Add tests and install targets if needed.
