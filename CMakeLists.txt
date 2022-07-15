# CMakeList.txt : CMake project for ImGui-CMake, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

project ("ImGui-CMake")

# Add source to this project's executable.
add_executable (ImGui-CMake "ImGui-CMake.cpp" "ImGui-CMake.h")

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET ImGui-CMake PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed.
