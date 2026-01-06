cmake_minimum_required(VERSION 3.11.0)              # Minimum CMake Version Required

project(                                            # Our Project Function Have three parameters, Project Name, Code Version and Languages.
    CppProjectTemplate 
    VERSION 1.0.0 
    LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)                          # Here we are rewriting existing CMake variables for config.
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)                       # These are features that are not on the standard but they are on the compiler.

set(LIBRARY_NAME "Library")                         # We want to create a variable to store the Library name at all levels.
set(EXECUTABLE_NAME "Executable")

option(COMPILE_EXECUTABLE "Whether to Compile Executable" OFF)
# To turn on this option on build time use the following cli:
# cmake .. -DCOMPILE_EXECUTABLE=ON

add_subdirectory(src)

if(COMPILE_EXECUTABLE)
    add_subdirectory(app)
else()
    message("W/O EXE Compile Link")
endif()

# The Idea is to have one CMakeList.txt file per folder and then if they are nested to have add_subdirectory() per each.