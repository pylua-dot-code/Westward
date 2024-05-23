cmake_minimum_required(VERSION 3.10)
project(Westward-Game)

# Set path to SFML directory
set(SFML_DIR "Include/SFML/lib/cmake/SFML")

# Find SFML components
find_package(SFML 2.5 COMPONENTS graphics audio REQUIRED)

# Add include directories for SFML
include_directories(${SFML_INCLUDE_DIR})

# Add your source files
add_executable(Westward-Game src/main.cpp)

# Link SFML libraries
target_link_libraries(Westward-Game PRIVATE sfml-graphics sfml-audio sfml-window sfml-system)
